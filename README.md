# RAG：检索增强生成

本仓库整理RAG课程的相关论文，围绕三个环节展开：

**文本分块 → 文本检索 → 上下文增强**

## 论文阅读列表

| 环节 | 论文 | 阅读重点 | 论文页面 | PDF全文 |
|---|---|---|---|---|
| 文本分块 | Is Semantic Chunking Worth the Computational Cost?（NAACL Findings 2025） | 比较语义分块与固定长度分块，理解分块效果与计算成本。 | [论文页面](https://aclanthology.org/2025.findings-naacl.114/) | [PDF](https://aclanthology.org/2025.findings-naacl.114.pdf) |
| 文本分块 | Late Chunking: Contextual Chunk Embeddings Using Long-Context Embedding Models | 理解先编码、后分块的思路，以及如何保留片段的上下文信息。 | [论文页面](https://arxiv.org/abs/2409.04701) | [PDF](https://arxiv.org/pdf/2409.04701) |
| 文本检索 | Dense Passage Retrieval for Open-Domain Question Answering（EMNLP 2020） | 理解双编码器、问题与文本的向量表示，以及相关片段的检索。 | [论文页面](https://aclanthology.org/2020.emnlp-main.550/) | [PDF](https://aclanthology.org/2020.emnlp-main.550.pdf) |
| 上下文增强 | RECOMP: Improving Retrieval-Augmented LMs with Compression and Selective Augmentation | 理解如何压缩、筛选检索内容，再用于增强生成模型的输入。 | [论文页面](https://arxiv.org/abs/2310.04408) | [PDF](https://arxiv.org/pdf/2310.04408) |
| 上下文增强 | LongLLMLingua: Accelerating and Enhancing LLMs in Long Context Scenarios via Prompt Compression（ACL 2024） | 理解提示词压缩，以及如何保留长上下文中的关键信息。 | [论文页面](https://aclanthology.org/2024.acl-long.91/) | [PDF](https://aclanthology.org/2024.acl-long.91.pdf) |

## 结合课堂案例思考

以高血压指南问答为例：

- **文本分块：** 如何将指南切成可检索的知识片段，同时保留适用条件？
- **文本检索：** 如何根据患者的问题，找到相关的指南内容？
- **上下文增强：** 如何筛选和组织检索证据，让模型依据资料回答？

## 阅读任务

任选一篇论文，回答以下问题：

1. 论文解决了RAG中的什么问题？
2. 核心方法是什么？请结合论文中的一张图说明。
3. 如何将该方法用于课堂中的高血压指南问答案例？

本页面提供论文原始页面与全文链接，论文版权归原作者或相应权利人所有。
