---
layout: default
title: "Chain of Agents: Large Language Models Collaborating on Long-Context Tasks"
date: 2024-06-15
category: Research
tags: ["llm"]  <!-- 新增：为 CoA 添加 llm 标签 -->
permalink: /blog/chain-of-agents/
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
    <h1 class="post-title">Chain of Agents: Large Language Models Collaborating on Long-Context Tasks</h1>
    <div class="post-meta">
      <span>📅 June 15, 2024</span>
      <span class="post-category">Research</span>
      <span>⏱️ 15 min read</span>
    </div>
    <div class="post-tags">
      <span class="tag">CoA</span>
      <span class="tag">LLM</span>
      <span class="tag">Multi-Agent</span>
    </div>
  </div>

  <div class="post-content">
    <div class="source-link">
      📄 <strong>论文来源:</strong> <a href="https://arxiv.org/abs/2406.02818" target="_blank">Chain of Agents: Large Language Models Collaborating on Long-Context Tasks</a>
    </div>

    <h2>核心问题</h2>
    <p>LLM在处理长上下文时遇到困难</p>
    
    <p>目前的主流解决方法：</p>
    <ul>
      <li>输入缩减（RAG），可能漏掉关键信息</li>
      <li>窗口扩展，难以精准聚焦</li>
    </ul>
    
    <p>本文的动机：<strong>需要一种新的方法，既能覆盖全部信息，又能保持高焦点</strong></p>

    <h2>Chain of Agents（CoA)</h2>
    
    <img src="https://pic1.zhimg.com/v2-e32a5872f8906506880ab554bd4151c2_1440w.jpg" alt="CoA架构图">
    
    <h3>工作代理：</h3>
    <ul>
      <li>分块：将冗长的源文档切割成多个片段chunk i</li>
      <li>链式处理：每个worker负责自己的chunk，以及上一个worker传来的摘要CU+用户问题，一起生成新的摘要传给下一个worker</li>
    </ul>
    
    <p>整个过程中，关键信息通过CU的的传递被不断聚合，每个worker都能承上启下，而且由于每个worker只处理一个短上下文，所以它能始终保持专注</p>
    
    <h3>管理代理：</h3>
    <p>根据最后一个Woker传来的CUI，对照Query生成最终的答案</p>
    
    <h3>优势：</h3>
    <ul>
      <li>无需训练，不需要微调模型</li>
      <li>高可解释性，可以回溯检查每一个CU，看推理链是在哪一步断掉的</li>
      <li>成本效益，时间复杂度从O(n²)->O(nk)</li>
    </ul>

    <h2>CoA与其他长上下文处理方法的对比</h2>
    
    <img src="https://pic2.zhimg.com/v2-f3aa563a7f9fb75794758a669c1758bf_1440w.jpg" alt="方法对比">

    <h2>实验：九个长上下文数据集的统计信息</h2>
    
    <img src="https://pic2.zhimg.com/v2-6919793366ea6c6add964377f97b160d_1440w.jpg" alt="数据集统计">
    
    <p>LLM窗口：8k</p>
    
    <p>query-based–是否基于查询，基于查询的（问答，摘要），否则就是通用的。</p>
    
    <p>可以处理通用的 不需要特定查询的任务，表示CoA框架不仅能处理RAG擅长的查询任务，也能处理RAG无法处理的通用长文本任务</p>

    <h2>Experiment Setup</h2>

    <h3>数据集</h3>

    <h4>问答部分</h4>
    <ul>
      <li><strong>HotpotQA</strong>: 基于维基百科的多跳（multi-hop）问答数据集。它要求模型跨越多个段落进行推理才能找到答案</li>
      <li><strong>MuSiQue</strong>: 多跳问答数据集。它被认为比 HotpotQA 难得多，因为一个样本里可能包含更多"跳"、无解的问题以及更难的干扰内容</li>
      <li><strong>NarrativeQA</strong>: 在<strong>整本书或电影剧本</strong>上进行问答的数据集。其答案可能是抽象的、摘录的、"是/否"或无解的</li>
      <li><strong>Qasper</strong>: 在 NLP（自然语言处理）论文上进行问答的数据集。它的问题答案同样包含摘录、抽象、"是/否"和无解等类型</li>
      <li><strong>QUALITY</strong>: 基于故事和文章的数据集，每个样本都带有选择题。模型需要从选项中选出正确答案</li>
    </ul>

    <h4>摘要部分</h4>
    <ul>
      <li><strong>QMSum</strong>: <strong>基于查询</strong>的摘要数据集。它由来自学术、工业产品等多个领域的会议记录组成</li>
      <li><strong>GovReport</strong>: <strong>通用</strong>摘要数据集（即没有特定查询）。它包含美国政府问责局（GAO）发布的冗长报告</li>
      <li><strong>BookSum</strong>: 用于长篇叙事（如小说、戏剧、故事）摘要的数据集。论文中使用的是 BookSum 的"书籍级别"（book-level）的分区来进行实验</li>
    </ul>

    <h4>代码补全</h4>
    <ul>
      <li><strong>RepoBench-P</strong>: 这是一个从 GitHub 代码仓库收集的数据集。任务是给定一个很长的代码库（long code base），模型需要生成下一行代码</li>
    </ul>

    <h3>评估指标</h3>
    <ul>
      <li><strong>Summarization (摘要任务):</strong> 使用 ROUGE 的几何平均值</li>
      <li><strong>Code Completion (代码补全):</strong> 使用"代码相似度得分"</li>
      <li><strong>QUALITY (问答数据集):</strong> 使用"完全匹配"(exact match)</li>
      <li><strong>其余的问答任务:</strong> 使用 F1 分数</li>
    </ul>

    <h3>LLMs</h3>
    <ul>
      <li><strong>PaLM 2:</strong> 这是一个 decoder-only 的模型系列，实验中使用了 text-bison@001 和 text-unicorn@001 这两个版本。它们的上下文窗口<strong>限制为 8k</strong></li>
      <li><strong>Gemini 1.0:</strong> 实验中使用的是 gemini-ultra，其输入限制为 <strong>32k</strong> tokens</li>
      <li><strong>Claude 3:</strong> 它包含三个能力递增的模型：claude-3-haiku, claude-3-sonnet, 和 claude-3-opus，这些模型能够处理 <strong>200k</strong> tokens 的上下文窗口，为长上下文任务提供了一个非常强的基线（Baseline）</li>
    </ul>

    <h3>Baseline</h3>
    <p>CoA要打败的对手。</p>
    
    <ul>
      <li><strong>Vanilla (即 Full-Context):</strong> 这是"<strong>窗口扩展</strong>"方法的代表。它<strong>直接</strong>将所有 token 喂给 LLM，直到把 LLM 的上下文窗口塞满。这意味着如果使用 Claude 3，它就会利用全部 <strong>200k</strong> 的窗口</li>
      <li><strong>Retrieval-Augmented Generation (RAG):</strong> 这是"<strong>输入缩减</strong>"方法的代表。它使用了一个最先进的（state-of-the-art）检索器。具体做法：首先将源文本切分成 300 个词的"块"(chunks)，然后用检索器对这些块进行"重排序"，最后，只把<strong>排名最高的 Top-n 个块</strong>喂给 LLM，直到把 LLM 的上下文窗口塞满</li>
      <li><strong>其他多代理方法 (Other Multi-agent approaches):</strong> 为了证明 CoA 不仅仅是"多代理"就行，而是"链式"结构特别好，作者还额外构建了两种可能的多代理方法作为对比。【Multi-Agent Voting & Multi-Agent Hierarchical Structure】</li>
    </ul>

    <h2>实验结果</h2>
    
    <img src="https://picx.zhimg.com/v2-1a55e520a8a5dddf709a74009c055d51_1440w.jpg" alt="实验结果1">
    
    <p>本文提出的 Chain-of-Agents (CoA) 框架，在所有测试的数据集上，都显著优于（significantly outperforms）现有的两种主流方法——Vanilla（全文输入）和 RAG（检索增强）。</p>
    
    <img src="https://picx.zhimg.com/v2-8bfc97c1ddbbbd3b266eae304bd786ef_1440w.jpg" alt="实验结果2">
    
    <p>"窗口扩展"方法的<strong>根本缺陷</strong>：即使窗口再大，模型也会"迷失在中间"，无法有效聚焦和利用信息。</p>
    
    <p><em>注：为什么BookSum通用摘要不和RAG进行比较，是因为这个问题它没有查询，RAG不适用于这类非查询的摘要任务。</em></p>

    <h2>分析</h2>

    <h3>CoA在RAG检索不到"gold answer"时表现效果显著好</h3>
    <p><strong>方法：</strong>在Narrative QA数据集上根据RAG检索到黄金答案所在片段，来给样本进行分类</p>
    
    <p><strong>结果：</strong>RAG 的表现高度依赖其"检索/重排序"的质量。当黄金答案片段排在前面时（如 "0-2"，RAG得分高），RAG 表现好。当 RAG <strong>检索失败</strong>时（图中的 "Fail (15%)" 点），RAG 的 F1 分数非常低（约 0.08）。但在<strong>同样</strong>的样本上，CoA 的分数（约 0.18）<strong>远高于 RAG</strong>。</p>
    
    <img src="https://pic3.zhimg.com/v2-b3af5f236a9637361628d345efd4396a_1440w.jpg" alt="RAG对比">

    <h3>输入越长，CoA优势越大</h3>
    <p><strong>方法：</strong>在 BookSum 数据集上，使用 Claude 3 模型，对比 Full-200k（200k 窗口）和 CoA-8k（8k 协作）。</p>
    
    <p><strong>结果：</strong>CoA在所有长度上都优于Full-200k，而且随着输入长度的增加，优势更加明显</p>
    
    <img src="https://pic4.zhimg.com/v2-8c21810f9ab0a4f08369054261e57e5b_1440w.jpg" alt="长度对比">

    <h3>CoA缓解了"Lost in Middle"</h3>
    <p><strong>方法：</strong>复现了"迷失在中间"的实验，将黄金答案放在长上下文的不同位置（X 轴），观察模型 F1 分数（Y 轴）的变化。</p>
    
    <p><strong>结果：</strong>Full模型严重出现"迷失在中间"问题，而CoA表现出较强韧性</p>
    
    <img src="https://pic2.zhimg.com/v2-90cb7145778fdb1f999bc04f59e6bc83_1440w.jpg" alt="Lost in Middle">

    <h3>CoA的协作实现了复杂推理</h3>
    <p>通过一个多跳推理的案例，直观展示CoA的工作流程</p>
    
    <img src="https://pic4.zhimg.com/v2-a19cf9e3d797034e091ec09588670a01_1440w.jpg" alt="案例分析">

    <h2>Ablation Study 消融研究</h2>
    <p>验证CoA框架中各个组件的必要性</p>
    
    <ul>
      <li>实验1，去掉manager agent，让最后一个work agent直接生成答案</li>
      <li>实验2，改变agent的阅读顺序，例如从后往前读</li>
    </ul>
    
    <img src="https://pic3.zhimg.com/v2-289ad158afdc97dee5d6f81e2ce36cfe_1440w.jpg" alt="消融研究">

    <h2>如何从多路径中找到答案</h2>
    <p>上一部分的对比中发现虽然自然顺序的平均分最高，但从右到左或随机顺序有时候能得到更好的答案</p>
    
    <p>因此提出问题：如果能同时运行多条路径，性能是否能进一步提升？</p>
    
    <p>探索两种方法：</p>
    <ul>
      <li><strong>w/ vote:</strong> 运行多个路径，进行投票得到结果</li>
      <li><strong>w/ judge:</strong> 运行多个路径，得到最终的通讯单元CU，使用一个额外的LLM作为裁判，来判断哪一个CU更可靠</li>
    </ul>
    
    <img src="https://pic3.zhimg.com/v2-a07684ec31f9f93b54c1dcc033a285e6_1440w.jpg" alt="多路径">
    
    <p>与table 7对比，我们发现<strong>几乎所有的多路径方法都能进一步提高了性能（未来的研究方向）</strong></p>

    <h2>结论</h2>
    <ul>
      <li>CoA 是一个无需训练 (training free)、任务/长度通用 (task/length agnostic)、可解释 (interpretable) 且成本效益高 (cost-effective) 的框架。</li>
      <li>实验结果：CoA 的性能大幅超越了 RAG（检索增强）和 Long Context LLMs（长上下文模型，即暴力扩大窗口的方法）。</li>
      <li>原因分析：CoA 通过整合"信息聚合"和"上下文推理"，成功缓解了"迷失在中间" (lost-in-the-middle) 的问题，并且在输入样本越长时表现得越好。</li>
    </ul>

    <h2>局限性 (Limitations)</h2>
    <ol>
      <li><strong>通信效率：</strong> LLM 之间的通信效率有待提高。目前的 LLM 都是为了与"人类规范"对齐而训练的，这对于 LLM 之间的"内部通信"来说并非最优。未来可以通过微调 (finetuning) 或上下文学习 (in-context learning) 来改善。</li>
      <li><strong>通信形式：</strong> CoA 目前只采用了"链式"通信，没有探索其他更复杂的通信方式，比如"辩论" (debating)或"复杂讨论" (complex discussions)。</li>
      <li><strong>成本与延迟：</strong> 运行 CoA 的成本和延迟可以进一步降低。例如，通过"<strong>模型路由" (model routing)技术</strong>，在某些步骤中用更小、更高效的模型来替换昂贵的大模型。</li>
    </ol>

    <a href="/blog/" class="back-link">← Back to Blog</a>
  </div>
</div>
