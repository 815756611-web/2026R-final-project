# 路线 B：PIP 的贝叶斯层级混合聚类 K 评估

本报告用于比较 K=2 到 K=6 之间不同终端 cluster 数的可行性。模型是贝叶斯层级 ROI 混合聚类：ROI 是终端分析单位，每个 ROI 内保留被试级观测，cluster 参数通过 NIW-Gaussian 层级混合模型进行 MCMC 抽样。

## overall_recommended_K

- 推荐 K：2
- 推荐依据：overall_score=0.9779；不是只看 BIC，而是综合模型表现、归属稳定性、共聚类结构和解释性。
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
| 2 | 2 | 2 | 0 | 3 | 58 | 20701.22 | 20912.38 | 21029.54 | 20957.05 | 1.0000 | 1.0000 | 1 | 1 | 1 | 0.9779 | TRUE |
| 3 | 2 | 2 | 1 | 3 | 58 | 20735.31 | 21055.69 | 21030.78 | 20973.54 | 0.9990 | 1.0000 | 1 | 1 | 1 | 0.8399 | FALSE |
| 4 | 2 | 2 | 2 | 3 | 58 | 20775.27 | 21204.87 | 21030.89 | 20975.88 | 0.9877 | 0.9508 | 1 | 1 | 1 | 0.7272 | FALSE |
| 5 | 2 | 1 | 3 | 3 | 58 | 20804.10 | 21342.92 | 21040.27 | 20972.71 | 0.9805 | 0.9508 | 1 | 1 | 1 | 0.6976 | FALSE |
| 6 | 2 | 1 | 4 | 3 | 58 | 20825.62 | 21473.66 | 21041.71 | 20978.80 | 0.9747 | 0.9508 | 1 | 1 | 1 | 0.5446 | FALSE |

## 输出文件

- `mcmc_model_comparison_PIP.csv`：完整 K 评估表。
- `mcmc_overall_recommended_K_PIP.csv`：自动推荐 K 的单行结果。
- `mcmc_coclustering_KXX_PIP.csv`：每个 K 的 ROI 后验共聚类矩阵。
- `mcmc_coclustering_PIP.csv`：推荐 K 对应的共聚类矩阵。
- `mcmc_fit_PIP.rds`：保存每个 K 的 MCMC 后验对象，包括 z_draws。
