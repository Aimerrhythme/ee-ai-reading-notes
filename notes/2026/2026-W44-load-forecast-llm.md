# 2026-W44 · 大模型也能做负荷预测吗

> 标签：#负荷预测 #大模型 #零样本 ｜ 阅读时长：约 5 分钟

## 本周读了什么
- 负荷预测常缺本地长历史。Liao 等把 Amazon Chronos（把时间序列当成「语言」预训练的模型）直接做零样本/少样本负荷预报，在五个真实数据集上对比九个基线，多数时延上误差更低，且未针对这些负荷数据微调。
- 面向综合能源系统，有工作用「时间序列提示 + 多任务对齐」把多能负荷接到预训练 LLM，在澳洲户用光伏负荷上做零样本迁移，强调跨户可搬。
- Chronos-2 一类时序基础模型还能吃协变量；在 ISO New England、ENTSO-E 上对比专用深度学习：短时延微调后很强，零样本与长时延仍弱于任务专用模型——课堂上点一句「能直接用，但别指望完全免训练」即可。

## 课堂一句带过
> 「负荷缺历史时，可以先试把曲线当序列丢给预训练时序大模型做零样本，再决定要不要微调。」

## 链接
1. [Zero and Few Shot Load Forecasting with Large Language Models](https://arxiv.org/abs/2411.11350) — arXiv / 2024
2. [Zero-shot Load Forecasting for Integrated Energy Systems: A Large Language Model-based Framework with Multi-task Learning](https://arxiv.org/abs/2502.16896) — arXiv / 2025
3. [Assessing Covariate-Informed Grid Load Forecasting with a Time-Series Foundation Model](https://arxiv.org/abs/2609.06656) — arXiv / 2026

## 我的一点想法
专升本课堂只需对比「专用网络 vs 预训练时序模型」的数据门槛，不必展开微调细节。
