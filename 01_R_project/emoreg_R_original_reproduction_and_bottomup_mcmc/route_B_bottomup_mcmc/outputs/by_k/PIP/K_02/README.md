# 路线 B：K=2 聚类整理

这里是当前 K 值下的完整聚类整理结果。

K 值可行性支撑：

- mean_loglik：-10321.61
- requested_K：2
- occupied_K：2
- effective_K：2
- empty_cluster_count：0
- BIC 近似值：20912.38
- delta_BIC：0；越接近 0 表示相对支持越强。
- overall_score：0.9779
- 归属稳定性得分：1
- 共聚类结构得分：1
- 可解释性得分：0.8528
- 是否为 overall_recommended_K：TRUE
- mean_membership_entropy：0；越低表示分类越清晰。
- kept_draws：2000
- 是否为当前 tag 下最低 BIC：TRUE
- 请求的 K 值：2
- 实际非空 cluster 数：2
- 空 cluster 数：0

说明：K 是模型允许的潜在成分数，不等于最终一定会出现的非空脑区类别数。README 只展开至少分到 1 个 ROI 的非空 cluster；未被任何 ROI 作为最大后验类别的成分会记录在 `empty_clusters.csv`，不会生成空白 cluster 文件夹。

聚类摘要：

| cluster | route_b_label | n_rois | mean_max_posterior | emotion_generation_mean | reappraisal_effect_mean | emotion_generation_two_log_bf | reappraisal_effect_two_log_bf |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 1 | common-appraisal-like | 58 | 1 | 0.0867 |  0.0398 |  68.453 | 18.1302 |
| 2 | emotion-generation-stable-mixed | 3 | 1 | 0.2145 | -0.0284 | 100.000 |  3.3948 |

主要文件：

- `model_support.csv`：当前 K 的模型支撑指标。
- `posterior_roi_assignment.csv`：ROI 的后验聚类概率。
- `cluster_profile.csv`：各 cluster 的效应画像。
- `cluster_subject_effects.csv`：各 cluster 的被试级平均特征。
- `cluster_labels_K*.nii.gz`：当前 K 的整体彩色标签图。
- `cluster_*` 文件夹：每个非空 cluster 的脑图和数据。
