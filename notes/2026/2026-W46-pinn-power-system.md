# 2026-W46 · 把摆动方程写进损失函数：PINN 在电力系统

> 标签：#物理信息神经网络 #暂态稳定 #状态估计 ｜ 阅读时长：约 5 分钟

## 本周读了什么
- 起点是 Misyris 等 2020 年的框架：把单机无穷大系统的摆动方程残差加进训练损失，用自动微分求导，少量数据即可还原功角与频率，计算比传统数值积分快约 87 倍，还能反推惯量、阻尼。
- ES-PINN 按「故障前—故障中—切除后」分段表示轨迹并严格衔接，得到可微的稳定边界，用来估计临界切除时间（CCT）；在 IEEE 9/14/30 节点系统上优于普通神经代理模型。
- 本周新预印本把摆动方程作为硬/软约束放进图神经算子：只看少数发电机母线的 PMU，一次前向推断出全部机组功角与转速，训练不需要状态标签；小系统上调好的卡尔曼平滑仍有优势。

## 课堂一句带过
> 「PINN 就是让神经网络一边拟合数据、一边满足摆动方程——数据少也不容易跑出违反物理的结果。」

## 链接
1. [Physics-Informed Neural Networks for Power Systems](https://arxiv.org/abs/1911.03737) — arXiv / 2019（IEEE PES GM 2020）
2. [Event-Structured Physics-Informed Neural Networks for Differentiable Critical Clearing Boundaries](https://arxiv.org/abs/2607.27681) — arXiv / 2026
3. [Dynamic State Estimation from Sparse PMUs via Physics-Informed Graph Neural Operators](https://arxiv.org/abs/2611.10468) — arXiv / 2026

## 我的一点想法
电力系统分析讲暂态稳定时，用单机无穷大系统对比「数值积分 vs PINN」即可，不必展开图算子。
