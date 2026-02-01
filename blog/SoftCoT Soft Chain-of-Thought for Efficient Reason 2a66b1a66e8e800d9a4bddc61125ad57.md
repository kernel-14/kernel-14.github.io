---
layout: default
title: "SoftCoT: Soft Chain-of-Thought for Efficient Reasoning"
date: 2024-06-15
category: Research
tags: ["llm", "cot", "reasoning"]
permalink: /blog/softcot/
---

<div class="post-container">
  <div class="post-header">
    <h1 class="post-title">SoftCoT: Soft Chain-of-Thought for Efficient Reasoning</h1>
    <div class="post-meta">
      <span>📅 June 15, 2024</span>
      <span class="post-category">Research</span>
      <span>⏱️ 12 min read</span>
    </div>
    <div class="post-tags">
      <span class="tag">SoftCoT</span>
      <span class="tag">LLM</span>
      <span class="tag">CoT</span>
    </div>
  </div>

  <div class="post-content">
        <div class="source-link">
      📄 <strong>论文来源:</strong> <a href="https://arxiv.org/abs/2502.12134" target="_blank">SoftCoT: Soft Chain-of-Thought for Efficient Reasoning with LLMs</a>
    <!-- 将你的正文内容放在这里；可以使用 Markdown（Jekyll 会渲染）或 HTML。 -->

    # SoftCoT: Soft Chain-of-Thought for Efficient Reasoning with LLMs
标签: CoT, LLM
论文链接：
[SoftCoT: Soft Chain-of-Thought for Efficient Reasoning with LLMs](https://arxiv.org/abs/2502.12134)
项目链接：
[https://github.com/xuyige/SoftCoT](https://github.com/xuyige/SoftCoT)
- CoT：通过产生中间推理步骤，使[LLM](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=LLM&zhida_source=entity)能解决复杂推理任务
## **核心问题**
如何在**提升推理能力**的同时，**避免[灾难性遗忘](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=%E7%81%BE%E9%9A%BE%E6%80%A7%E9%81%97%E5%BF%98&zhida_source=entity)**（catastrophic forgetting)

- 旧方法1：hard token decoding，模型必须像人一样逐字逐句地生成我们能读懂的，离散的推理步骤，这种方法把AI的“思考”限制在它那有限的、离散的词汇表里了 。
- 旧方法2：Continuous-Space Reasoning，[连续空间推理](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=%E8%BF%9E%E7%BB%AD%E7%A9%BA%E9%97%B4%E6%8E%A8%E7%90%86&zhida_source=entity)，不让ai说出具体的词，而是让他在内部用更灵活、更抽象的软思考（数学向量）来处理，但是这个方法有一个巨大的问题，它要求把整个AI大模型重新微调一遍，这么做的后果是”灾难性遗忘“，AI可能为了学习这个新的软思考技巧，把自己之前学会的其它所有知识和能力都忘掉了。
- 本文的新方法：SoftCoT，既能享受到软思考的好处（连续空间思考），又能完美避开灾难性遗忘（不需要改变LLM）。

## **Introduction（思考历程）**

## **CoT链式思考**

优点：能提高模型在复杂推理任务上的表现啊，让AI的思考表现变得可解释性

不足：1.错误传播，如果中间某一步出错了会导致整个推理链崩溃；2.效率低下，为了解决错误传播的问题，诞生了像”[自洽性](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=%E8%87%AA%E6%B4%BD%E6%80%A7&zhida_source=entity)“（self-consistency)或”思想树“（Tree-of-thought)这样的方法，它们的核心思想是让模型多想几次然后投票，但这样非常耗时，计算效率低

## **CCoT连续空间推理（软思考）**

为了提高效率，研究者开始探索跳过具体文本的步骤，CCoT尝试让模型在连续空间中进行推理，使用模型内部的隐状态作为软思考，不生成具体的词汇

优点：表达能力更强，用很短的连续表示就能超过很长的离散文本推理

不足：CCoT需要对整个LLM进行全模型微调（full-model fine-tuning），而当你试图在一个已经很强大的模型（eg LLaMA3.1-8B）上进行微调时，模型虽然学会了新任务，但会严重忘记它之前预训练好的能力，导致其推理能力甚至比微调前的零样本CoT还差

## **本文的解决方案：SoftCoT**

1.冻结主LLM，防止灾难性遗忘

2.引入助手模型：轻量级、固定的助手模型（assistant model）

3.生成“软思考”，助手模型针对每一个问题，生成软思考令牌，具体来说，它不生成词语，而是输出其最后一层状态

4.训练“投影模块”，助手模型和主LLM时两个不同的模型，他们表示的空间不相同，因此加入一个可训练的[projection module](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=projection+module&zhida_source=entity)

5.核心训练：在整个SoftCoT框架中，唯一需要训练的就是这个轻量级的投影模块。

## **方法论**

## **符号定义**

![](https://pic2.zhimg.com/v2-6802eae8262d220b73e2c5a6569167cb_1440w.jpg)

input Q=[q1,q2,…,q_{|Q|}]

- -CoT–> (1) 推理步骤rationale steps R=[r1,r2,…,r*{|R|}]；(2) Q,R–>answer A=[a1,a2,..,a*{|A|}]

那么我们可以把生成过程表示为：

其中，Hard-CoT生成的R是离散的、人类可读的tokens，而我们的Soft-CoT关注的是R的连续表示。

## **SoftCoT框架**

![](https://pic1.zhimg.com/v2-c28e0d5bca1dfb6b311c4258f6a85df4_1440w.jpg)

CoT：将问题输入给LLM，然后一步一步推理得到答案

Cocount：将问题输入给LLM，然后先进行soft thinking,再将soft thoughts解码成中间推理步骤和答案,在这个过程中需要对大模型进行full-model fine-tuning

SoftCoT：冻结主LLM，先使用一个assistant model对问题进行软处理，然后把软处理的结果利用一个projection module投影到LLM能理解的空间中，主LLM利用原始的问题+额外加入的soft thoughts进行一步一步推理，得到最终的答案

## **实验设定**

## **数据集**

本文使用到的五个实验数据集的统计摘要：

![](https://pic4.zhimg.com/v2-bd6b8c62ab5b44406b75c601dc59ac6b_1440w.jpg)

## **Baselines**

1. zero-shot CoT，不经过任何训练的CoT
2. Zero-Shot CoT-Unk，零样本+Unk令牌，这些令牌的嵌入向量是可训练的（prompt tuning），这个对比是为了展示“模型之所以有效，是不是与助手无关，而只是由于在LLM中加入了一些可训练的参数（软提示）？”
3. Zero-Shot Assist，使用助手模型生成hard token，并且作为提示给LLM，用于说明softCoT比hardCoT好
4. Cocount框架
5. [LORA fine-Tuning](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=LORA+fine-Tuning&zhida_source=entity)，使用LORA（一种参数高效微调方法）对LLM进行微调，展示SoftCoT是否比标准、通用的参数微调方法更好

## **实验结果**

## **Comparison with Baselines**

![](https://pic1.zhimg.com/v2-a6b90e424fd77f7db6d2cbfb28e8bdb2_1440w.jpg)

1. 灾难性遗忘的存在，LoRA Fine-Tuning或Coconut这些方法反而使性能下降了，甚至不如Zero-Shot CoT
2. 简单的[UNK]令牌有微弱帮助（zero-shot CoT-Unk)，而且能降低结果的方差（使输出更稳定），说明在LLM中增加一点点计算容量或停顿令牌是有好处的
3. 使用助手是有效的，比CoT-Unk要更好

SoftCoT在五个数据集上一致超越了所有baselines

## **泛化到其它LLM**

![](https://pica.zhimg.com/v2-85adf8da61d804195bc852e49ef06886_1440w.jpg)

在[Qwen2.5-7B-Instruct](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=Qwen2.5-7B-Instruct&zhida_source=entity)上重复实验，发现SoftCoT仍然有效，而且在LLM原本较弱的领域（commonsense常识推理）上提升最明显，同时保留了LLM在原有强项（mathematical）上的能力，而且SoftCoT提升了零样本迁移的能力，对于没有训练数据的DU数据集也获得了性能提升

## **模型分析**

1. 软思考更高效简洁，只需要更少的thought tokens就可以达到最佳性能,说明softCoT比硬思考具有更强的信息密度和表征能力；SoftCoT可以缓解灾难性遗忘的问题（zero-shot assisit-CoT在tokens数量不足的时候，性能反而会低于基线）

![](https://pic4.zhimg.com/v2-64233c7b19ffe710944a65cf50af3477_1440w.jpg)

2. 助手模型的大小

发现：改变assit的规模不会显著影响最终任务的表现

![](https://picx.zhimg.com/v2-2b2ca756c95e7a6e3b07cfb830a77c93_1440w.jpg)

模型正交因素

![](https://pic2.zhimg.com/v2-035d9aecf3239dcab9ba3bab6ca5e8e5_1440w.jpg)

探讨SoftCoT与其它“增强技术”是否兼容，具体测试了“自洽性”（self-consistency）,也就是让模型生成多个推理路径，然后通过多数投票的方式来决定最终答案。

通过这个表格N=1和N=10的对比，发现SoftCoT 不是在做“自洽性”同样的事情。它是一个**独立的改进机制**，它**提升了“单一推理路径”的质量**，可以与其他技术（如自洽性）**叠加使用**以获得更好的效果 。

## **Conclusion**

SoftCoT：一种用于高效LLM推理的软链式思考提示方法

SoftCoT 框架的三个核心步骤 ：

1. 一个“助手模型”负责生成“软思考令牌” 。
2. 一个可训练的“投影模块”负责将这些“软思考”映射（翻译）到主LLM的表示空间中 。
3. 主LLM 应用这些“软思考”来进行最终的推理 。

SoftCoT的核心优势：

- 效率：为了提升效率，SoftCoT 在单次前向传播中就能生成所有的“软思考令牌”
- 规避灾难性遗忘：为了解决这个问题，SoftCoT 冻结了主LLM，并且只训练那个轻量级的“投影模块”

Limitations：

- SoftCoT不能完全替代推理路径：软思想表征主要是为了丰富探索的概率空间，而不是充当搜索机制本身。
- 可扩展性需要进一步的经验证据：这篇论文的实验是在 LLaMA-3.1-8B 和 Qwen2.5-7B 这两个模型上进行的，虽然它在这些约 70-80亿（7-8 billion）参数的模型上取得了成功，但这并不能自动保证它在更大的模型上也一样有效 。在同一个模型家族中，还存在着更大规模的LLM（例如几百亿甚至千亿参数的） 。因此，SoftCoT 是否能扩展（scale）到那些“超大规模LLM”（extremely large LLMs）上，目前还是一个“悬而未决的问题”（open question），这需要未来进行更“彻底的经验验证”
    <!-- ... existing content (原文正文，这里省略) ... -->
    <a href="/blog/" class="back-link">← Back to Blog</a>
  </div>
</div>