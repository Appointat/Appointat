# Appointat

蚂蚁集团 LLM 算法工程师。为阿福 app 做 LLM 记忆系统、RSI（自进化）的探索与实现，以及 LLM × 图计算。此前是 [CAMEL-AI](https://github.com/camel-ai/camel) 核心维护者、[DB-GPT](https://github.com/eosphoros-ai/DB-GPT) GraphRAG 模块维护者。

## 我的看法

**关于记忆**

- Memory 不是存储，而是可被决策利用的外部状态。衡量它的不是存了多少历史，而是历史到当前决策的通道通不通。→ [几万字都讲不明白的 Memory 架构与思考](https://mp.weixin.qq.com/s/bl77_Mb85C4AKe8h4__V6Q)
- 时间是一等维度。bi-temporal + time-sliced recall 把「何时为真」变成检索与聚合的硬约束，而不是一个元数据字段。→ 同上
- 参数化与非参数化记忆的分别，在于写入成本落在哪：训练时编进权重，还是在 commit 与 retrieve/inject 时付。后者的上限是接口带宽、检索聚合误差和 Policy 的学习。→ [参数化 Memory 漫谈](https://mp.weixin.qq.com/s/ZTg1bEd2Vx2h7TakM7060w)
- 遗忘是要设计的特性，不是 bug。光学压缩（DeepSeek-OCR）暗示了一种记忆分层：旧上下文渐进缩小重渲染，体面地衰减。→ [用 8500 字解析 DeepSeek OCR 与记忆系统](https://mp.weixin.qq.com/s/ki5Tq-kTnzadfTbiqEItOg)

**关于智能体**

- 快慢思考拆成两个模型：Thinker 负责规划，更便宜的 Actor 负责执行工具调用——2024 年做的，那时还没有 thinking 模型。→ [Chat2Graph · 推理机](https://github.com/TuGraph-family/chat2graph/blob/master/doc/zh-cn/principle/reasoner.md)
- 单主动多被动：一个 Leader 把任务拆成子任务 DAG 交给多个 Expert，支持递归拆解与错误回注，而不是扁平的群聊。→ [Chat2Graph · Leader](https://github.com/TuGraph-family/chat2graph/blob/master/doc/zh-cn/principle/leader.md)
- Less structure：工作流应该被搜索和优化出来——在声明式配置上跑 MCTS、逐层做上下文工程——而不是手写 SOP。→ [Chat2Graph · 工作流自动生成](https://github.com/TuGraph-family/chat2graph/blob/master/doc/zh-cn/principle/workflow_generator.md)，我带的 [OSPP 2025 项目](https://summer.ospp.ac.cn/2025/org/prodetail/257280066)
- 研究本身就是一个 agent loop：可证伪的假设 → 实验 → judge + verifier → 归因。失败的实验也是记忆，是下一轮假设的经验回放。

## 开源

| 项目 | 角色 |
| --- | --- |
| [Chat2Graph](https://github.com/TuGraph-family/chat2graph) — 图原生智能体系统 | 第一贡献者（commits 与代码行均第一）；OSPP 2025 导师 |
| [Apache GeaFlow (incubating)](https://github.com/apache/geaflow) — 流式图计算引擎 | 贡献者——[CASTS](https://github.com/apache/geaflow/pull/737)，一个 LLM 推理算子 |
| [DB-GPT](https://github.com/eosphoros-ai/DB-GPT) — Agentic AI 数据助手 | GraphRAG 模块维护者，2024 |
| [CAMEL-AI](https://github.com/camel-ai/camel) — 多智能体框架 | 核心维护者，2023–2024；主导 [Mixture-of-Agents 设计](https://github.com/camel-ai/multi-agent-streamlit-ui/blob/feature/multi-agent/design_docs/concept_of_multi_agent_system.md) |
| [LeAgent](https://github.com/Appointat/LeAgent) | 作者——2023 年的早期 RAG 聊天机器人，回答里带出处 |

## 博客

- [几万字都讲不明白的 Memory 架构与思考](https://mp.weixin.qq.com/s/bl77_Mb85C4AKe8h4__V6Q) —— 记忆 = ledger → views → policy，时间是硬约束。[AntData](https://mp.weixin.qq.com/s/iwhtcselOV6ui8PBbUPvEA)、[OceanBase](https://mp.weixin.qq.com/s/b_0KOiRzzrEb4hul-T7MKQ) 转载。
- [参数化 Memory 漫谈](https://mp.weixin.qq.com/s/ZTg1bEd2Vx2h7TakM7060w) —— 参数化 vs 非参数化记忆。阿里技术转载。
- [用 8500 字解析 DeepSeek OCR 与记忆系统](https://mp.weixin.qq.com/s/ki5Tq-kTnzadfTbiqEItOg) —— 光学压缩作为记忆分层。OceanBase 转载。
- Chat2Graph 设计文档：[概览](https://github.com/TuGraph-family/chat2graph/blob/master/doc/zh-cn/principle/overview.md) · [记忆系统（DIKW 分层）](https://github.com/TuGraph-family/chat2graph/blob/master/doc/zh-cn/principle/memory.md) · [推理机](https://github.com/TuGraph-family/chat2graph/blob/master/doc/zh-cn/principle/reasoner.md) · [工作流自动生成](https://github.com/TuGraph-family/chat2graph/blob/master/doc/zh-cn/principle/workflow_generator.md)

## 背景

- Synopsys 软件工程实习，2023

## 奖项

- 蚂蚁集团 AI X-STAR，2026
- 蚂蚁集团开源先锋奖，2024
- [美国大学生数学建模竞赛（MCM/ICM）2022](https://www.contest.comap.com/undergraduate/contests/mcm/contests/2022/results) 特等奖 Outstanding Winner（前 0.16%）
- 校长奖学金，2022
- 国家奖学金，2022
- 上海市优秀毕业生，2024

📫 appointat@gmail.com
