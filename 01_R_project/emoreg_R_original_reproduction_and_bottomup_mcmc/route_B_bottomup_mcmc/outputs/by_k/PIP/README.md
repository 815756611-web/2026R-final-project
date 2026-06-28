# 路线 B：PIP 的 K 值整理

本层用于比较不同 K 值下的聚类可行性。

判断依据：overall_recommended_K 不是只看 BIC，而是综合模型表现、ROI 归属稳定性、MCMC 后验共聚类结构和 cluster 可解释性。BIC、AIC、WAIC、LOOIC 仍保留为模型表现指标。

| k | requested_K | occupied_K | effective_K | empty_cluster_count | kept_draws | mean_loglik | aic_approx | bic_approx | waic | looic | delta_bic | mean_membership_entropy | mean_max_posterior | coclustering_sharpness | interpretable_cluster_fraction | overall_score | overall_recommended_K | is_lowest_bic |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 2 | 2 | 2 | 2 | 0 | 2000 | -10321.61 | 20701.22 | 20912.38 | 21029.54 | 20957.05 |   0.0000 | 0.0000 | 1.0000 | 1 | 1 | 0.9779 | TRUE | TRUE |
| 3 | 3 | 2 | 2 | 1 | 2000 | -10323.66 | 20735.31 | 21055.69 | 21030.78 | 20973.54 | 143.3190 | 0.0075 | 0.9990 | 1 | 1 | 0.8399 | FALSE | FALSE |
| 4 | 4 | 2 | 2 | 2 | 2000 | -10328.64 | 20775.27 | 21204.87 | 21030.89 | 20975.88 | 292.4945 | 0.0312 | 0.9877 | 1 | 1 | 0.7272 | FALSE | FALSE |
| 5 | 5 | 2 | 1 | 3 | 2000 | -10328.05 | 20804.10 | 21342.92 | 21040.27 | 20972.71 | 430.5411 | 0.0394 | 0.9805 | 1 | 1 | 0.6976 | FALSE | FALSE |
| 6 | 6 | 2 | 1 | 4 | 2000 | -10323.81 | 20825.62 | 21473.66 | 21041.71 | 20978.80 | 561.2865 | 0.0425 | 0.9747 | 1 | 1 | 0.5446 | FALSE | FALSE |

每个 `K_XX` 文件夹都包含该 K 下的 cluster 文件夹和支撑数据。
