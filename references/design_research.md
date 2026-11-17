# 开发调研与取舍

调研日期为 2026-11-17。查阅范围限下列文件，仓库未本地运行，运行效果未验证。

## 官方规范

项目级 .agents/skills/ 由 Codex 扫描，SKILL.md 用 name/description 标识，可带支持目录和 UI 元数据。本实现使用本地官方 skill-creator 初始化与验证，方法放 references，业务资料集中 memory。[OpenAI Build skills](https://learn.chatgpt.com/docs/build-skills)

## Personal Assistant

已读 README、AGENT.md 和 agents/bootstrap.md。采用核心提示词、可切换角色、结构化 Markdown 档案与引导访谈。借鉴逐步建档、先读后局部写入、日期及历史记录。其整库读取、多问题访谈和健康关系采集超出本技能范围，本实现采用按需读取、单问题与商业相关信息。[README](https://github.com/ehsansasanian/assistant/blob/main/README.md) [核心提示词](https://github.com/ehsansasanian/assistant/blob/main/AGENT.md) [访谈流程](https://github.com/ehsansasanian/assistant/blob/main/agents/bootstrap.md)

## Hypersignal

已读 README 与 API main.py。聚合 RSS 机会信号，React 用 localStorage 保存来源与布局，FastAPI 代理抓取缓存，入口装配 HTTP 客户端、缓存与 feeds 路由。借鉴来源可追溯思想，信息流只用于机会线索，客户需求仍需验证。本实现采用本地研究文件工作流。[README](https://github.com/elite-barbs/hypersignal/blob/main/README.md) [API 入口](https://github.com/elite-barbs/hypersignal/blob/main/apps/api/src/hypersignal_api/main.py)

## Corellis

已读 README 架构和治理说明。使用 OpenClaw、Docker、Slack 及分层团队记忆协调目标与任务。借鉴索引导航、决定可追溯概念，个人场景采用本地文件。README 运营数据为项目方陈述，未独立核实。[Corellis README](https://github.com/CorellisOrg/Corellis/blob/main/README.md)

## 调研限制

Resume Review Agent 仓库页面可打开，README 原始路径 404，核心资料不足，未据此设计。[仓库](https://github.com/ajuzxx/langfuse-resume-review-agent)

YC 选题页面没有可读取正文，未提取方法。[YC How To Pick A Startup Idea](https://www.ycombinator.com/library/Ri-how-to-pick-a-startup-idea)

MIT、McGill 和 YC 访谈材料的方法与适用范围分别记录于 career_assessment.md 和 customer_discovery.md。状态机、评分刻度、E1～E4 和记忆协议是按需求建立的实现约定。

## 2026-11-17 联网优化

复核现有流程后，集中补充决策缺口，详细规则仍保存在各自的 references 和模板中。

| 查阅资料 | 观察与采用方式 |
| --- | --- |
| Strategyzer Test Card | 明确假设、实验、指标和阈值。增加实验 ID、单个主要假设与阈值变更记录 |
| Strategyzer Learning Card | 区分现场观察、解释和行动。增加“证据不足”和结论适用范围，限制单次实验结论的外推 |
| SBA Plan your business | 区分固定与变动成本，使用简单盈亏平衡模型。补充工时容量、回款与个人机会成本核对 |
| NN/g Interview Questions | 近期具体事件、中性澄清和拆分复合问题。补充单问题访谈示例 |
| Anthropic Context Engineering | 按需检索与结构化笔记。完善恢复摘要、正文核对和旧版索引兼容 |

Test Card 和 Learning Card 的原作者方法可用于实验设计与复盘。假设类别、阶段进入条件、硬约束检查和归档批次是本技能据实际缺口形成的实现选择。[Test Card](https://www.strategyzer.com/library/validate-your-ideas-with-the-test-card) [Learning Card](https://www.strategyzer.com/library/capture-customer-insights-and-actions-with-the-learning-card)

SBA 的简单盈亏平衡公式用于同一周期的产品或服务估算。工时上限和个人现金流检查为本技能补充，具体税费与规则需按用户所在地研究。[SBA Plan your business](https://www.sba.gov/counseling/plan-your-business/)

NN/g 的问题设计建议用于个人和客户访谈。当前示例为自行编写。[NN/g Interview Questions](https://www.nngroup.com/articles/interview-questions-mistakes/)

Anthropic 的资料说明按需读取与外部笔记如何支撑长任务。由此采用简短恢复摘要和路径索引，具体兼容与归档规则由本技能定义。[Effective context engineering](https://www.anthropic.com/research/effective-context-engineering-for-ai-agents)

资料原文已查阅，访问日期均为 2026-11-17。以上优化效果仍需通过技能实际使用持续检验。
