# 2026-W45 · 卷积网络怎么认输电线路故障

> 标签：#故障诊断 #卷积神经网络 #输电线路 ｜ 阅读时长：约 5 分钟

## 本周读了什么
- 配电网故障定位常受 PMU 布点成本限制。Khattak 等先用 SVM 做「前向选择 + 邻域微调」挑少量 PMU，再把故障前后电压电流对称分量差分序列喂给 1D CNN：在改版 IEEE-34/123 上，故障类型准确率约 99%+，故障线路定位约 94%–96%。
- Turanlı 等把残差式 1D CNN 分别训在配电公司实测、公开集与 Simulink 合成数据上，三相电压电流作输入，跨三类数据都能分出常见短路类型——课堂上可强调「仿真训、现场验」的闭环。
- Biswas 等用 1D CNN 只做特征抽取、决策树做分类，并配 SHAP 解释各相电压电流贡献；四种线路场景下检测/分类准确率都很高，且参数量与推理时延明显小于端到端 CNN/LSTM，适合讲「能用、还能说清为什么」。

## 课堂一句带过
> 「三相电压电流曲线丢进一维卷积，就能先判有没有故障、再分是哪种短路；测点不够时，先挑最有用的 PMU 再训网络。」

## 链接
1. [Selection of Optimal Number and Location of PMUs for CNN Based Fault Location and Identification](https://arxiv.org/abs/2509.02192) — arXiv / 2025
2. [Classification of Faults in Power System Transmission Lines Using Deep Learning Methods with Real, Synthetic, and Public Datasets](https://www.mdpi.com/2076-3417/14/20/9590) — Appl. Sci. / 2024
3. [Hybrid CNN-decision tree framework for efficient transmission line fault detection and classification: an XAI-based approach](https://www.nature.com/articles/s41598-026-45514-0) — Sci. Rep. / 2026

## 我的一点想法
专升本继电保护课只需对比「纯黑盒 CNN vs CNN+可解释分类器」，不必展开 PMU 选址算法细节。
