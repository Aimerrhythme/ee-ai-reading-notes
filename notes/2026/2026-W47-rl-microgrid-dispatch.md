# 2026-W47 · 给调度智能体装上"安全护栏"：强化学习做微电网调度

> 标签：#强化学习 #微电网 #能量管理 ｜ 阅读时长：约 5 分钟

## 本周读了什么
- 微电网调度难在风光与负荷不确定、约束多；强化学习（RL）把它当作"观测—动作—奖励"的序贯决策，训练后在线决策快。
- 偏远微电网案例：用"屏蔽控制单元"按约束分层把关，动作越界即被修正；协调风机、柴油机和电池，燃油降约 24%，电池老化不增加，约束全部满足。
- RL + MPC 组合：RL 负责机组启停等离散决策，把 MPC 的混合整数规划简化成线性规划，在线计算明显提速。
- 工业微电网新案例：把炼钢工序知识嵌入安全 PPO 调度工序负荷，工序零损失，电费比规则调度降 49.2%、比滚动 MILP 降 25.9%。

## 课堂一句带过
> 「强化学习调度像培养一个值班员：在仿真里反复试错学策略，上岗前再给它装上不许越限的护栏。」

## 链接
1. [Shielded Controller Units for RL with Operational Constraints Applied to Remote Microgrids](https://arxiv.org/abs/2512.01046) — arXiv / 2025
2. [Integrating Reinforcement Learning and Model Predictive Control with Applications to Microgrids](https://arxiv.org/abs/2409.11267) — arXiv / 2024
3. [Process-Knowledge-Embedded Safe DRL for Real-Time Dispatch of Process Loads in Industrial Microgrids](https://arxiv.org/abs/2608.03149) — arXiv / 2026

## 我的一点想法
讲微电网经济调度时，先用规则或 MILP 做基线，再说 RL 的优势和"安全约束"这个最大门槛。
