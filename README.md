# Appointat

LLM Algorithm Engineer at Ant Group (阿福). I work on memory systems for LLM agents, self-evolving experiment loops, and LLM × graph computing. Before that: core maintainer at [CAMEL-AI](https://github.com/camel-ai/camel), GraphRAG maintainer at [DB-GPT](https://github.com/eosphoros-ai/DB-GPT).

## What I think

**On memory**

- Memory is not storage. It is external state a decision can use — the measure is whether the channel from history to the current decision works, not how much history is kept. → [几万字都讲不明白的 Memory 架构与思考](https://mp.weixin.qq.com/s/bl77_Mb85C4AKe8h4__V6Q)
- Time is a first-class dimension. Bi-temporal, time-sliced recall turns "when was this true" into a hard constraint on retrieval and aggregation, not a metadata field. → same article
- Parametric vs. non-parametric memory is a question of where the write cost lands: compiled into weights at training time, or paid at commit and retrieve/inject time. The ceiling of the latter is interface bandwidth, retrieval-aggregation error and policy learning. → [参数化 Memory 漫谈](https://mp.weixin.qq.com/s/ZTg1bEd2Vx2h7TakM7060w)
- Forgetting is something to design, not a bug. Optical compression (DeepSeek-OCR) hints at memory tiers where old context is re-rendered smaller and decays gracefully. → [用 8500 字解析 DeepSeek OCR 与记忆系统](https://mp.weixin.qq.com/s/ki5Tq-kTnzadfTbiqEItOg)

**On agents**

- Fast and slow thinking as two models: a Thinker that plans and a cheaper Actor that executes tool calls — built in 2024, before "thinking" models existed. → [Chat2Graph · Reasoner](https://github.com/TuGraph-family/chat2graph/blob/master/doc/en-us/principle/reasoner.md)
- One active, many passive: a single Leader decomposes work into a sub-job DAG for many Experts, with recursion and error re-injection instead of a flat group chat. → [Chat2Graph · Leader](https://github.com/TuGraph-family/chat2graph/blob/master/doc/en-us/principle/leader.md)
- "Less structure": agent workflows should be searched and optimised — MCTS over declarative configs, context engineered per layer — not hand-written as SOPs. → [Chat2Graph · Workflow generation](https://github.com/TuGraph-family/chat2graph/blob/master/doc/en-us/principle/workflow_generator.md), the [OSPP 2025 project](https://summer.ospp.ac.cn/2025/org/prodetail/257280066) I mentored
- Research is itself an agent loop: falsifiable hypotheses → experiments → judge + verifier → attribution. Failed experiments are memory too — replay for the next hypothesis.

## Open source

| Project | Role |
| --- | --- |
| [Chat2Graph](https://github.com/TuGraph-family/chat2graph) — graph-native agentic system | Lead contributor (#1 by commits and lines); OSPP 2025 mentor |
| [Apache GeaFlow (incubating)](https://github.com/apache/geaflow) — streaming graph engine | Contributor — [CASTS](https://github.com/apache/geaflow/pull/737), an LLM reasoning operator |
| [DB-GPT](https://github.com/eosphoros-ai/DB-GPT) — agentic AI data assistant | GraphRAG module maintainer, 2024 |
| [CAMEL-AI](https://github.com/camel-ai/camel) — multi-agent framework | Core maintainer, 2023–2024; led the [Mixture-of-Agents design](https://github.com/camel-ai/multi-agent-streamlit-ui/blob/feature/multi-agent/design_docs/concept_of_multi_agent_system.md) |
| [LeAgent](https://github.com/Appointat/LeAgent) | Author — an early (2023) RAG chatbot that cites its sources inline |

## Blog

- [几万字都讲不明白的 Memory 架构与思考](https://mp.weixin.qq.com/s/bl77_Mb85C4AKe8h4__V6Q) — memory as ledger → views → policy, and time as a hard constraint. Also on [AntData](https://mp.weixin.qq.com/s/iwhtcselOV6ui8PBbUPvEA) and [OceanBase](https://mp.weixin.qq.com/s/b_0KOiRzzrEb4hul-T7MKQ).
- [参数化 Memory 漫谈](https://mp.weixin.qq.com/s/ZTg1bEd2Vx2h7TakM7060w) — parametric vs. non-parametric memory (on 阿里技术).
- [用 8500 字解析 DeepSeek OCR 与记忆系统](https://mp.weixin.qq.com/s/ki5Tq-kTnzadfTbiqEItOg) — optical compression as a memory tier (on OceanBase).
- Chat2Graph design docs: [overview](https://github.com/TuGraph-family/chat2graph/blob/master/doc/en-us/principle/overview.md) · [memory — DIKW layers](https://github.com/TuGraph-family/chat2graph/blob/master/doc/en-us/principle/memory.md) · [reasoner](https://github.com/TuGraph-family/chat2graph/blob/master/doc/en-us/principle/reasoner.md) · [workflow generation](https://github.com/TuGraph-family/chat2graph/blob/master/doc/en-us/principle/workflow_generator.md)

## Background

- Alliance Sorbonne Université — engineering degree in computer systems, 2025
- Shanghai University — B.Eng. in information engineering, 2024
- Software engineering intern, Synopsys, 2023

## Awards

- Ant Group AI X-STAR, 2026
- Ant Group Open Source Pioneer Award, 2024
- [MCM/ICM 2022](https://www.contest.comap.com/undergraduate/contests/mcm/contests/2022/results) Outstanding Winner (top 0.16%)
- Qian Weichang Presidential Scholarship — Shanghai University's highest undergraduate honour
- National Scholarship (国家奖学金)
- Outstanding Graduate of Shanghai, 2024

📫 appointat@gmail.com
