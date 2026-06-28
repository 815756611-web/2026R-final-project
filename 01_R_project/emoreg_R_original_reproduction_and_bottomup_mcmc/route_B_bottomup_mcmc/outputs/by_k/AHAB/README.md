# 路线 B：AHAB 的 K 值整理

本层用于比较不同 K 值下的聚类可行性。

判断依据：overall_recommended_K 不是只看 BIC，而是综合模型表现、ROI 归属稳定性、MCMC 后验共聚类结构和 cluster 可解释性。BIC、AIC、WAIC、LOOIC 仍保留为模型表现指标。

| k | requested_K | occupied_K | effective_K | empty_cluster_count | kept_draws | mean_loglik | aic_approx | bic_approx | waic | looic | delta_bic | mean_membership_entropy | mean_max_posterior | coclustering_sharpness | interpretable_cluster_fraction | overall_score | overall_recommended_K | is_lowest_bic |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 2 | 2 | 2 | 2 | 0 | 2000 | -9732.068 | 19522.14 | 19734.27 | 20029.59 | 19862.08 |   0.0000 | 0.0000 | 1.0000 | 1 | 1 | 0.9287 | TRUE | TRUE |
| 3 | 3 | 2 | 2 | 1 | 2000 | -9733.134 | 19554.27 | 19876.12 | 20027.82 | 19860.82 | 141.8544 | 0.0000 | 1.0000 | 1 | 1 | 0.9162 | FALSE | FALSE |
| 4 | 4 | 2 | 1 | 2 | 2000 | -9738.498 | 19595.00 | 20026.57 | 20040.50 | 19890.30 | 292.3052 | 0.0386 | 0.9830 | 1 | 1 | 0.6772 | FALSE | FALSE |
| 5 | 5 | 2 | 2 | 3 | 2000 | -9736.167 | 19620.33 | 20161.63 | 20049.86 | 19877.40 | 427.3663 | 0.0401 | 0.9888 | 1 | 1 | 0.6285 | FALSE | FALSE |
| 6 | 6 | 2 | 2 | 4 | 2000 | -9733.944 | 19645.89 | 20296.91 | 20030.76 | 19868.79 | 562.6442 | 0.0107 | 0.9986 | 1 | 1 | 0.6531 | FALSE | FALSE |

每个 `K_XX` 文件夹都包含该 K 下的 cluster 文件夹和支撑数据。
