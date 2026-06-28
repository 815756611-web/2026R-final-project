# K=5 / Cluster 1：common-appraisal-like

分入原因：该 cluster 由贝叶斯高斯混合模型在当前 K 值下估计得到，ROI 按最大后验概率归入此类。

命名依据：根据 cluster 内 ROI 的四个特征均值、Bayes factor 近似值和方向进行规则化命名。

- ROI 数量：58
- 平均最大后验概率：0.9995
- 情绪生成均值：0.0867
- 重评效应均值：0.0398
- 情绪生成 2logBF：68.453
- 重评效应 2logBF：18.1302

支撑数据：

- `cluster_mask.nii.gz`：该 cluster 的脑图。
- `cluster_roi_table.csv`：该 cluster 内 ROI、来源系统、后验概率和 ROI 组水平统计。
- `cluster_subject_effects.csv`：该 cluster 在每个被试上的平均特征值。
- `cluster_profile.csv`：该 cluster 的汇总画像和命名标签。
