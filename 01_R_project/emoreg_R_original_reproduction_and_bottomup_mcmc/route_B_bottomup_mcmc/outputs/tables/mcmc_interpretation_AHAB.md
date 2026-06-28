# 路线 B：贝叶斯 MCMC 聚类结果说明

Tag：AHAB

分析单位：原文 ROI 连通簇；所有 ROI 作为同一个观察池进入模型。

## 1. K 值

本次选择 K=2；依据是 overall_recommended_K，综合模型表现、归属稳定性、共聚类结构和可解释性（overall_score=0.9287）。

## 2. Cluster 画像

- Cluster 1：modifiable-emotion-like；ROI 数= 3；平均最大后验归属概率=1.00；Emotion generation 均值=0.4449；Reappraisal effect 均值=-0.0864。
- Cluster 2：common-appraisal-like；ROI 数=58；平均最大后验归属概率=1.00；Emotion generation 均值=0.1535；Reappraisal effect 均值=0.0545。

## 3. 观察池说明

路线 B 不按原文四类系统分别建模，也不把系统标签作为分组变量。

本次共有 61 个原文 ROI 进入同一个模型。保留了 4 个来源标签作为追溯信息，但没有按来源标签分组建模或分系统解释。

## 4. 分类不确定性

查看 `mcmc_cluster_uncertainty_*.csv` 和 `mcmc_posterior_*.csv`。`max_posterior >= 0.80` 可视为相对稳定，低于 0.60 应解释为 mixed/uncertain unit。

## 5. 行为验证

- Cluster 2：重评效应与 reappraisal success 的相关 r=0.062；情绪生成与 emotion reactivity 的相关 r=-0.130。
- Cluster 1：重评效应与 reappraisal success 的相关 r=-0.046；情绪生成与 emotion reactivity 的相关 r=-0.138。

## 6. 文件读取关系

- 输入：`roi_subject_features_*.csv` 与 `roi_table_*.csv`
- 后验分类：`mcmc_posterior_*.csv`
- Cluster 画像：`mcmc_cluster_profile_*.csv`
- ROI 观察池元数据：`mcmc_roi_pool_metadata_*.csv`
- 行为验证：`mcmc_cluster_behavior_correlations_*.csv`
