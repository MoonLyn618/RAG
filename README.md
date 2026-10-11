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




---


## 课后作业：材料场景的RAG问答


### 任务情境：储氢材料性能查询


选择文献中的一种储氢材料，回答：


> 该材料的储氢容量是多少？对应的测试温度、压力及实验条件是什么？请引用文献依据。


**主案例论文：** Maharana 等，2025，*Retrieval augmented generation for building datasets from scientific literature*，Journal of Physics: Materials 8，035006，DOI：[10.1088/2515-7639/ade1fa](https://doi.org/10.1088/2515-7639/ade1fa)。


- [本账号已 fork 的代码与数据：RAG-dataset-gen](https://github.com/MoonLyn618/RAG-dataset-gen)
- [作者原始项目](https://github.com/catastropiyush/RAG-dataset-gen)
- 项目中的 `selected_df.xls` 为文献摘要输入；`final_extracted_1611.xlsx` 为提取后的数据集；`RAG_new.ipynb` 和 `Prompting.ipynb` 可用于对照检索增强与直接提示方法。文件格式和读取方式以项目说明为准。


### 材料场景相关论文（5篇）


第1篇用于本次储氢材料作业；其余4篇用于了解RAG向其他材料问题的迁移。


| 材料场景 | 论文与出处 | 阅读重点／作业关联 | 论文链接 | 全文或配套资源 |
|---|---|---|---|---|
| 储氢材料数据提取（主案例） | Retrieval augmented generation for building datasets from scientific literature（Journal of Physics: Materials，2025） | 从文献摘要提取材料名称、储氢容量、温度、压力和实验条件；对照直接提示与RAG。 | [期刊论文](https://doi.org/10.1088/2515-7639/ade1fa) | [作者预印本](https://www.cambridge.org/engage/chemrxiv/article-details/67e277f06dde43c9081f4b38)；[已fork的代码与数据](https://github.com/MoonLyn618/RAG-dataset-gen) |
| 储氢材料发现（拓展） | “DIVE” into hydrogen storage materials discovery with AI agents（Chemical Science，2026） | 观察文献数据提取、材料候选生成与性能预测如何组成更完整的工作流。 | [论文与全文](https://pubs.rsc.org/en/content/articlehtml/2026/sc/d5sc09921h) | DOI：10.1039/D5SC09921H |
| 光催化材料 | Materials Dual-Source Knowledge Retrieval-Augmented Generation for Local Large Language Models in Photocatalysts（Journal of Chemical Information and Modeling，2025） | 将实验CSV数据与PDF文献共同用于检索，理解多来源证据组织和本地RAG。 | [期刊论文](https://doi.org/10.1021/acs.jcim.5c01941) | [开放全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC12728951/)；[作者演示资源](https://github.com/mipypf/mdsk-rag) |
| 石墨烯合成与回答评价 | Large language models in materials science: assessing RAG evaluation frameworks through graphene synthesis（RSC Advances，2026） | 理解材料问答如何评价：除检查答案数值外，还要核对检索依据、条件及专家判断。 | [论文与全文](https://pubs.rsc.org/en/content/articlelanding/2026/ra/d5ra09726f) | DOI：10.1039/D5RA09726F |
| 生物降解聚合物 | Retrieval Augmented Generation of Literature-derived Polymer Knowledge: The Example of a Biodegradable Polymer Expert System（arXiv预印本，2026） | 对照VectorRAG与GraphRAG，理解段落检索、材料实体关系和带引用的回答。 | [论文页面](https://arxiv.org/abs/2602.16650) | [PDF](https://arxiv.org/pdf/2602.16650) |


### 小组作业：复现RAG流程


| 环节 | 具体任务 | 保留的证据 |
|---|---|---|
| ① 知识准备 | 选取主案例项目中的相关摘要，进行切块并保留来源；提交3个片段，标出材料、性能和测试条件。 | 片段编号、原文、论文题名或DOI；摘要未报告的信息标记为“未报告”。 |
| ② 文本检索 | 围绕储氢容量及测试条件提出问题，选取Top-K相关片段并保留片段编号；核对材料名称、容量单位和温压条件。 | 检索问题、Top-K结果、选择理由；说明是否能覆盖所问信息。 |
| ③ 增强生成 | 构造“问题＋证据＋回答要求”的提示词；对照直接回答与带证据回答，核查数值、条件和引用。 | 完整提示词、两种回答及核查结果；证据不足时明确说明，不能补编数值。 |


可在网页问答工具中手动复现三个环节，并如实标注“人工选取片段”；使用代码实现时记录模型、检索方法及K值。两种方式都需要展示证据如何进入回答。


### 学习通提交


**1页流程图＋3个知识片段＋带引用的回答与对照。**


回答建议用表格列出：材料名称、储氢容量及单位、测试温度、测试压力、实验条件、证据片段编号、原文出处。不同温压条件下的数据分别呈现，不直接混用。


### 评价要点


- **找对：** 片段与材料及问题相关，保留适用条件。
- **给对：** 提示词包含证据、来源和回答要求。
- **答对：** 数值、单位和条件与原文一致，引用可追溯；缺失信息如实说明。

