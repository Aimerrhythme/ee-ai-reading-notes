# 2026-W44 · Transformer 怎么看光伏出力

> 标签：#光伏预测 #Transformer ｜ 阅读时长：约 5 分钟

## 本周读了什么
- 光伏出力随云走，预报要同时用历史功率和向前看的气象。Zhang 等提出 Cross-Unet：Transformer 做多尺度时间编码与通道间注意力，再把历史发电和天气预报接起来。华北四站、澳洲一站，输入含数值预报、卫星辐照和 AI 气象，时效 4 小时到 7 天；多数配置优于文中基线。
- Gao 等的 PV-Client 把注意力打在功率与气象变量之间，而不是只沿时间轴；趋势另交线性层。三座实站上，均方误差优于文中次优基线。
- Wu 等用 iTransformer 读目标序列、LSTM 读协变量，交叉注意力融合后，在澳大利亚公开数据上分四季检验。

## 课堂一句带过
> 「光伏预报里，注意力可以打在辐照和功率之间，也可以把历史曲线和天气预报接在一起。」

## 链接
1. [Rethinking the use of deep learning methods for photovoltaic power forecasting](https://www.nature.com/articles/s41467-026-73817-3) — Nature Communications / 2026
2. [Cross-variable Linear Integrated ENhanced Transformer for Photovoltaic power forecasting](https://arxiv.org/abs/2406.03808) — arXiv / 2024
3. [Enhanced Photovoltaic Power Forecasting: An iTransformer and LSTM-Based Model Integrating Temporal and Covariate Interactions](https://arxiv.org/abs/2412.02302) — arXiv / 2025

## 我的一点想法
上课点到这两种接法即可。
