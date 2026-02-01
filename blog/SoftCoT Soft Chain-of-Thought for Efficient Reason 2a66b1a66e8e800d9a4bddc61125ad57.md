---
layout: default
title: "SoftCoT: Soft Chain-of-Thought for Efficient Reasoning"
date: 2024-06-15
category: Research
tags: ["llm", "cot", "reasoning"]
permalink: /blog/softcot/
---

<style>
  .post-container {
    max-width: 900px;
    margin: 0 auto;
    padding: 20px;
  }

  .post-header {
    margin-bottom: 40px;
    padding-bottom: 20px;
    border-bottom: 2px solid #eee;
  }

  .post-title {
    font-size: 2.5em;
    margin-bottom: 15px;
    color: #333;
  }

  .post-meta {
    display: flex;
    gap: 20px;
    color: #888;
    font-size: 0.95em;
    flex-wrap: wrap;
  }

  .post-category {
    background: #EC707D;
    color: white;
    padding: 4px 12px;
    border-radius: 15px;
    font-size: 0.9em;
  }

  .post-tags {
    display: flex;
    gap: 10px;
    margin-top: 10px;
  }

  .tag {
    background: #f0f0f0;
    padding: 3px 10px;
    border-radius: 12px;
    font-size: 0.85em;
    color: #666;
  }

  .post-content {
    line-height: 1.8;
    color: #444;
  }

  .post-content h2 {
    margin-top: 40px;
    margin-bottom: 20px;
    color: #333;
    font-size: 1.8em;
    border-bottom: 2px solid #f0f0f0;
    padding-bottom: 10px;
  }

  .post-content h3 {
    margin-top: 30px;
    margin-bottom: 15px;
    color: #444;
    font-size: 1.4em;
  }

  .post-content p {
    margin-bottom: 20px;
  }

  .post-content strong {
    color: #EC707D;
    font-weight: 600;
  }

  .post-content ul, .post-content ol {
    margin-left: 30px;
    margin-bottom: 20px;
  }

  .post-content li {
    margin-bottom: 10px;
  }

  .post-content img {
    max-width: 100%;
    height: auto;
    margin: 20px 0;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  }

  .source-link {
    background: #f8f9fa;
    padding: 15px;
    border-left: 4px solid #EC707D;
    margin: 20px 0;
    border-radius: 5px;
  }

  .source-link a {
    color: #EC707D;
    text-decoration: none;
    font-weight: 500;
  }

  .source-link a:hover {
    text-decoration: underline;
  }

  .back-link {
    display: inline-block;
    margin-top: 40px;
    color: #EC707D;
    text-decoration: none;
    font-weight: 500;
  }

  .back-link:hover {
    text-decoration: underline;
  }
</style>

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
    </div>

    # SoftCoT: Soft Chain-of-Thought for Efficient Reasoning with LLMs
标签: CoT, LLM
论文链接：
[SoftCoT: Soft Chain-of-Thought for Efficient Reasoning with LLMs](https://arxiv.org/abs/2502.12134)
项目链接：
[https://github.com/xuyige/SoftCoT](https://github.com/xuyige/SoftCoT)
- CoT：通过产生中间推理步骤，使[LLM](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=LLM&zhida_source=entity)能解决复杂推理任务

<h2>核心问题</h2>
<p>如何在**提升推理能力**的同时，**避免[灾难性遗忘](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=%E7%81%BE%E9%9A%BE%E6%80%A7%E9%81%97%E5%BF%98&zhida_source=entity)**（catastrophic forgetting）</p>
<ul>
<li>旧方法1：hard token decoding，模型必须像人一样逐字逐句地生成我们能读懂的，离散的推理步骤，这种方法把AI的“思考”限制在它那有限的、离散的词汇表里了 。</li>
<li>旧方法2：Continuous-Space Reasoning，[连续空间推理](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=%E8%BF%9E%E7%BB%AD%E7%A9%BA%E9%97%B4%E6%8E%A8%E7%90%86&zhida_source=entity)，不让ai说出具体的词，而是让他在内部用更灵活、更抽象的软思考（数学向量）来处理，但是这个方法有一个巨大的问题，它要求把整个AI大模型重新微调一遍，这么做的后果是”灾难性遗忘“，AI可能为了学习这个新的软思考技巧，把自己之前学会的其它所有知识和能力都忘掉了。</li>
<li>本文的新方法：SoftCoT，既能享受到软思考的好处（连续空间思考），又能完美避开灾难性遗忘（不需要改变LLM）。</li>
</ul>

<h2> Introduction（思考历程）</h2>

<h3>CoT 链式思考</h3>
<p><strong>优点：</strong> 提高复杂推理表现，具有可解释性。<br>
<strong>不足：</strong>
1.错误传播，如果中间某一步出错了会导致整个推理链崩溃；
2.效率低下，为了解决错误传播的问题，诞生了像”[自洽性](https://zhida.zhihu.com/search?content_id=266142001&content_type=Article&match_order=1&q=%E8%87%AA%E6%B4%BD%E6%80%A7&zhida_source=entity)“（self-consistency）或”思想树“（Tree-of-thought）这样的方法，它们的核心思想是让模型多想几次然后投票，但这样非常耗时，计算效率低</p>


<h3>CCoT 连续空间推理（软思考）</h3>
<p>为了提高效率，研究者开始探索跳过具体文本的步骤，CCoT尝试让模型在连续空间中进行推理，使用模型内部的隐状态作为软思考，不生成具体的词汇</p>
<p><strong>优点：</strong> 信息密度高，表达能力强。<br>
<strong>不足：CCoT需要对整个LLM进行全模型微调（full-model fine-tuning），而当你试图在一个已经很强大的模型（eg LLaMA3.1-8B）上进行微调时，模型虽然学会了新任务，但会严重忘记它之前预训练好的能力，导致其推理能力甚至比微调前的零样本CoT还差</strong>


<h2> 本文的解决方案：SoftCoT</h2>
<img src="[https://pic1.zhimg.com/v2-c28e0d5bca1dfb6b311c4258f6a85df4_1440w.jpg](https://pic1.zhimg.com/v2-c28e0d5bca1dfb6b311c4258f6a85df4_1440w.jpg)" alt="SoftCoT框架对比图">
<ol>
  <li><strong>冻结主 LLM：</strong> 保持原始能力不丢失，防止灾难性遗忘。</li>
  <li><strong>引入助手模型：</strong> 使用轻量级模型生成中间隐状态（Hidden States）。</li>
  <li><strong>生成“软思考”</strong>，助手模型针对每一个问题，生成软思考令牌，具体来说，它不生成词语，而是输出其最后一层状态</li>
  <li><strong>训练投影模块：</strong> 助手模型和主LLM时两个不同的模型，他们表示的空间不相同，因此加入一个可训练的[projection module],唯一需要学习的部分，负责将助手的向量空间映射到主模型的理解范围。</li>
</ol>

<h2>方法论</h2>
<h3>符号定义</h3>
<p>设输入问题为 $Q = [q_1, q_2, \dots, q_{|Q|}]$。传统的 Hard-CoT 生成离散的 $R$。而 Soft-CoT 则处理 $R$ 的连续表征。</p>
<img src="[https://pic2.zhimg.com/v2-6802eae8262d220b73e2c5a6569167cb_1440w.jpg](https://pic2.zhimg.com/v2-6802eae8262d220b73e2c5a6569167cb_1440w.jpg)" alt="符号定义公式">

<h3>对比逻辑</h3>
<ul>
  <li><strong>CoT:</strong> 问题 $\rightarrow$ 离散步骤 $\rightarrow$ 答案。</li>
  <li><strong>Coconut:</strong> 全模型微调，实现软思考解码。</li>
  <li><strong>SoftCoT:</strong> 冻结 LLM + 助手模型生成软思考 $\rightarrow$ 投影 $\rightarrow$ 主模型推理。</li>
</ul>

<h2>实验设定</h2>
<h3>数据集</h3>
<p>实验涵盖了 GSM8K（数学）、StrategyQA（推理）、CommonsenseQA（常识）等五个关键数据集。</p>
<img src="[https://pic4.zhimg.com/v2-bd6b8c62ab5b44406b75c601dc59ac6b_1440w.jpg](https://pic4.zhimg.com/v2-bd6b8c62ab5b44406b75c601dc59ac6b_1440w.jpg)" alt="数据集统计">

<h3>Baselines</h3>
<ul>
  <li><strong>Zero-shot CoT:</strong> 基准性能。</li>
  <li><strong>CoT-Unk:</strong> 仅加入可训练的占位符（Prompt Tuning）。</li>
  <li><strong>Zero-Shot Assist:</strong> 助手生成文本作为 Prompt。</li>
  <li><strong>LoRA Fine-Tuning:</strong> 标准的参数高效微调。</li>
</ul>

<h2>实验结果</h2>
<h3>性能表现</h3>
<img src="[https://pic1.zhimg.com/v2-a6b90e424fd77f7db6d2cbfb28e8bdb2_1440w.jpg](https://pic1.zhimg.com/v2-a6b90e424fd77f7db6d2cbfb28e8bdb2_1440w.jpg)" alt="主实验结果图">
<ul>
  <li><strong>SoftCoT 一致超越所有 Baseline：</strong> 特别是在 LoRA 和 Coconut 出现性能下滑的情况下，SoftCoT 保持了增长。</li>
  <li><strong>证明有效性：</strong> 加入软思考比单纯加入 [UNK] 令牌或硬提示（Hard tokens）效果更好。</li>
</ul>

<h3>跨模型泛化</h3>
<img src="[https://pica.zhimg.com/v2-85adf8da61d804195bc852e49ef06886_1440w.jpg](https://pica.zhimg.com/v2-85adf8da61d804195bc852e49ef06886_1440w.jpg)" alt="泛化实验">
<p>在 Qwen2.5-7B 上同样有效，特别是在常识推理领域提升显著。</p>

<h2>模型分析</h2>
<ul>
  <li><strong>信息密度：</strong> SoftCoT 仅需极少量的 Thought tokens 即可达到峰值性能，远比离散文本高效。</li>
  <li><strong>兼容性：</strong> 与 Self-consistency（自洽性）完美兼容，N=10 时性能进一步叠加提升。</li>
</ul>
<img src="[https://pic2.zhimg.com/v2-035d9aecf3239dcab9ba3bab6ca5e8e5_1440w.jpg](https://pic2.zhimg.com/v2-035d9aecf3239dcab9ba3bab6ca5e8e5_1440w.jpg)" alt="自洽性对比">

<h2>结论</h2>
<p><strong>SoftCoT</strong> 是一种高效且防遗忘的推理增强框架。它通过<strong>单次前向传播</strong>生成软思考，解决了计算效率问题，并通过<strong>冻结主模型</strong>解决了稳定性问题。</p>

<h2>局限性</h2>
<ul>
  <li><strong>角色定位：</strong> 软思考主要优化搜索概率空间，尚不能完全替代逻辑严密的显示推理路径。</li>
  <li><strong>扩展性挑战：</strong> 虽在 7B-8B 模型上成功，但在千亿级超大规模模型上的表现仍需进一步验证。</li>
</ul>

<a href="/blog/" class="back-link">← Back to Blog</a>
    <a href="/blog/" class="back-link">← Back to Blog</a>
  </div>
</div>