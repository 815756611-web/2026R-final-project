# 路线 B：AHAB 的贝叶斯层级混合聚类 K 评估

本报告用于比较 K=2 到 K=6 之间不同终端 cluster 数的可行性。模型是贝叶斯层级 ROI 混合聚类：ROI 是终端分析单位，每个 ROI 内保留被试级观测，cluster 参数通过 NIW-Gaussian 层级混合模型进行 MCMC 抽样。

## overall_recommended_K

- 推荐 K：2
- 推荐依据：overall_score=0.9287；不是只看 BIC，而是综合模型表现、归属稳定性、共聚类结构和解释性。
- 推荐 K 下的实际非空终端 cluster 数：2

## 评分逻辑

- model_performance_score：由 BIC、AIC、WAIC、LOOIC 的相对排名合成，越高越好。
- assignment_stability_score：由平均最大后验概率、稳定 ROI 比例和低分类熵合成，越高越好。
- coclustering_score：由 MCMC 后验共聚类矩阵的清晰度和高置信成对关系比例合成，越高越好。
- interpretability_score：由可解释 cluster 比例、非空 cluster 比例、cluster 大小均衡性和效应强度合成，越高越好。
- overall_score：0.40*模型表现 + 0.25*归属稳定性 + 0.20*共聚类结构 + 0.15*解释性。

## K 比较表

| requested_K | occupied_K | effective_K | empty_cluster_count | minimum_cluster_size | maximum_cluster_size | aic_approx | bic_approx | waic | looic | mean_max_posterior | stable_080_fraction | coclustering_sharpness | confident_pair_fraction | interpretable_cluster_fraction | overall_score | overall_recommended_K |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 2 | 2 | 2 | 0 | 3 | 58 | 19522.14 | 19734.27 | 20029.59 | 19862.08 | 1.0000 | 1.0000 | 1 | 1 | 1 | 0.9287 | TRUE |
| 3 | 2 | 2 | 1 | 3 | 58 | 19554.27 | 19876.12 | 20027.82 | 19860.82 | 1.0000 | 1.0000 | 1 | 1 | 1 | 0.9162 | FALSE |
| 4 | 2 | 1 | 2 | 3 | 58 | 19595.00 | 20026.57 | 20040.50 | 19890.30 | 0.9830 | 0.9508 | 1 | 1 | 1 | 0.6772 | FALSE |
| 5 | 2 | 2 | 3 | 3 | 58 | 19620.33 | 20161.63 | 20049.86 | 19877.40 | 0.9888 | 1.0000 | 1 | 1 | 1 | 0.6285 | FALSE |
| 6 | 2 | 2 | 4 | 3 | 58 | 19645.89 | 20296.91 | 20030.76 | 19868.79 | 0.9986 | 1.0000 | 1 | 1 | 1 | 0.6531 | FALSE |

## 输出文件

- `mcmc_model_comparison_AHAB.csv`：完整 K 评估表。
- `mcmc_overall_recommended_K_AHAB.csv`：自动推荐 K 的单行结果。
- `mcmc_coclustering_KXX_AHAB.csv`：每个 K 的 ROI 后验共聚类矩阵。
- `mcmc_coclustering_AHAB.csv`：推荐 K 对应的共聚类矩阵。
- `mcmc_fit_AHAB.rds`：保存每个 K 的 MCMC 后验对象，包括 z_draws。
