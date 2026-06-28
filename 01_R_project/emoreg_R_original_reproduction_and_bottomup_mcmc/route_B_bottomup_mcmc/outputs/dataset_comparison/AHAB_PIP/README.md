# 路线 B：AHAB 与 PIP 的共识图比较与跨样本稳定性检验

用途：比较两个数据库是否支持相似的 ROI 聚类结构。这里使用路线 B 的模型评价与聚类匹配方法，不使用路线 A 的 product map。

方法：

- AHAB 和 PIP 分别用路线 B 的 ROI-MCMC 混合模型拟合。
- 每个数据库内部先按 overall_recommended_K 选择 K；如果旧结果没有该列，则回退到最低近似 BIC。模型表同时保留 AIC、BIC、WAIC 和 PSIS-LOO/LOOIC。
- 在共同 ROI 上比较两个数据库的最大后验 cluster 归属，计算 ARI 和 NMI。
- 对两个数据库的 cluster 两两计算空间 Dice/Jaccard，再按 Dice 从高到低做一对一匹配。
- 只对匹配上的 cluster 生成二值共识图：某个 ROI 必须同时属于 AHAB 的该 cluster 和 PIP 的匹配 cluster，才会进入对应共识图。

当前模型选择：

- AHAB：选中 K=2；BIC=19734.27；AIC=19522.14；WAIC=20029.59；LOOIC=19862.08
- PIP：选中 K=2；BIC=20912.38；AIC=20701.22；WAIC=21029.54；LOOIC=20957.05

当前一致性结果：

- 共同 ROI 数：61
- ARI：0.6253；NMI：0.418
- 平均最大后验概率：AHAB=1；PIP=1
- 匹配 cluster 数：2

匹配 cluster 与共识图：

- match 1：AHAB cluster 2 vs PIP cluster 1；Dice=0.9254；Jaccard=0.8612；共识体素=30796
- match 2：AHAB cluster 1 vs PIP cluster 2；Dice=0.6860；Jaccard=0.5221；共识体素= 5423

主要文件：

- `selected_model_evaluation.csv`：每个数据库选中 K 和模型支撑指标。
- `cluster_assignment_agreement.csv`：共同 ROI 上的 ARI/NMI 和后验置信度。
- `cluster_pair_spatial_similarity.csv`：所有 cluster 两两空间相似性。
- `matched_cluster_consensus.csv`：一对一匹配结果和二值共识图路径。
- `nifti/`：二值模型共识图，其中 `labels_AHAB_PIP.nii.gz` 是把匹配结果合并成标签图。
