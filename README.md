<p align="center"><img src="assets/header.svg" alt="Shen Yuan — LLM post-training and evidence-grounded AI systems" width="100%" /></p>

# 沈愿 · Shen Yuan

**大模型后训练 / 强化学习对齐 / Agentic RAG**

上海交通大学 · 统计建模与卫生经济学硕士在读（2025–2028）  
武汉理工大学 · 大数据管理与应用（2021–2025）

我关注语言模型如何在真实约束下做出可靠决策：用监督数据建立行为基线，用偏好与奖励调整策略，再用可追溯评测检查效果与代价。统计建模与数据策略经历让我重视实验设计、失败归因和证据边界。

[GitHub](https://github.com/Shenyyyuan) · [学术邮箱](mailto:shenyuan001@sjtu.edu.cn)

## Selected Work

### 01 / [DeepResearch · 可验证工具 Agent 与后训练](https://github.com/Shenyyyuan/DeepResearch)

研究多跳问答中的证据选择、工具终止和奖励设计。构建可重放 Search→Reader→Verifier 环境，保留 SFT 失败案例；补充显式 DPO/PPO、GAE、策略版本隔离与 CPU 验证。

**值得展开的技术问题**：引用正确为何仍会答错？SFT loss 很低为何不能停止？如何避免用错误 reward 放大已有行为缺陷？

[方法与实验](https://github.com/Shenyyyuan/DeepResearch#2-方法) · [训练实现](https://github.com/Shenyyyuan/DeepResearch/tree/main/src/alignment) · [验证记录](https://github.com/Shenyyyuan/DeepResearch/tree/main/reports)

### 02 / [MedicalGPT · 医疗问答偏好与安全评测](https://github.com/Shenyyyuan/MedicalGPT)

基于开源 MedicalGPT 开展领域后训练实验。围绕医疗数据稀缺、候选偏好质量与评审偏差，补充分组清洗、安全标注契约、DPO 入口以及配对统计评测。

**值得展开的技术问题**：如何避免“总是拒答”获得更安全的假象？AAR、RM 偏好准确率与 win rate 有什么区别？怎样识别自动 judge 的长度偏差？

[贡献边界](https://github.com/Shenyyyuan/MedicalGPT/blob/main/docs/CONTRIBUTIONS.md) · [评测协议](https://github.com/Shenyyyuan/MedicalGPT/blob/main/docs/EVALUATION_PROTOCOL.md) · [新增实现](https://github.com/Shenyyyuan/MedicalGPT/tree/main/src/medical_alignment)

### 03 / [RAG Workflow · 中文知识库与检索实验](https://github.com/Shenyyyuan/rag-workflow)

实现文档入库、父子块检索、FAISS+BM25+RRF、CrossEncoder 与多阶段 Agent 工作流。新增 HyDE、纠错检索和反思式生成入口，并用逐题报告比较质量与时延。

**已公开的实验范围**：18 篇自编短文、24 个问题的 CPU 诊断实验；各方法的收益与成本均保留，正式学术知识库评测仍待扩展。

[系统与决策](https://github.com/Shenyyyuan/rag-workflow#4-技术决策) · [逐题实验](https://github.com/Shenyyyuan/rag-workflow/blob/main/reports/retrieval_bge.json) · [高级 RAG](https://github.com/Shenyyyuan/rag-workflow/tree/main/src/advanced_rag)

## How I Approach Engineering

- **先定义测量对象**：协议成功、任务成功、证据可靠与推理正确分别验收。
- **记录取舍**：同时展示质量、token、时延和失败案例。
- **保持可复现**：冻结数据、prompt 与模型版本，保留逐题结果和回归测试。
- **区分证据状态**：已验证实现、历史记录和待运行假设分开陈述。

## Technical Focus

| 方向 | 实践内容 |
|---|---|
| Post-training | PyTorch、Transformers、PEFT/LoRA、SFT、DPO、PPO、Reward Modeling |
| Retrieval & Agents | FAISS、BM25、RRF、BGE、CrossEncoder、LangGraph、证据与工具协议 |
| Experimentation | Python、SQL、统计建模、A/B 实验、配对比较与置信区间 |

此前在上海哈啰普惠科技有限公司从事数据策略与商业分析实习（2025.05–2025.09），参与实验评估、用户分层与归因分析。

<sub>项目页分别说明上游来源、个人扩展与实验状态。欢迎围绕方法、失败案例和工程取舍交流。</sub>
