# 路线 A：AHAB 与 PIP 的共识图比较与跨样本稳定性检验

用途：比较两个数据库在原文四个理论系统上的空间共识。这里使用的是路线 A 的原文复现逻辑，不是路线 B 的 MCMC 聚类。

方法：

- 对每个系统分别读取 `AHAB` 和 `PIP` 的 `*_after_cluster_*.nii.gz` 二值系统图。
- 先对两个二值图做三维平滑，`consensus_smooth_fwhm_vox = 3`。
- 逐体素相乘得到 product map：两个数据库都支持的位置乘积更高。
- 使用阈值 `consensus_product_threshold = 0.01` 二值化，得到 AHAB/PIP 共识图。
- 共识图文件写入 `route_A_original_reproduction/outputs/nifti`，文件名为 `*_consensus_AHAB_PIP.nii.gz`。

当前共识图体素数：

| system | display_name | tag1 | tag2 | consensus_voxels | output_nifti |
| --- | --- | --- | --- | --- | --- |
| common_appraisal | Common Appraisal | AHAB | PIP | 18489 | C:/Users/81575/Desktop/vscode_box/emoreg_project_annotation_copy_2026-06-26/01_R_project/emoreg_R_original_reproduction_and_bottomup_mcmc/route_A_original_reproduction/outputs/nifti/common_appraisal_consensus_AHAB_PIP.nii.gz |
| reappraisal_only | Reappraisal Only | AHAB | PIP |  4052 | C:/Users/81575/Desktop/vscode_box/emoreg_project_annotation_copy_2026-06-26/01_R_project/emoreg_R_original_reproduction_and_bottomup_mcmc/route_A_original_reproduction/outputs/nifti/reappraisal_only_consensus_AHAB_PIP.nii.gz |
| non_modifiable_emotion | Non-modifiable Emotion | AHAB | PIP | 31835 | C:/Users/81575/Desktop/vscode_box/emoreg_project_annotation_copy_2026-06-26/01_R_project/emoreg_R_original_reproduction_and_bottomup_mcmc/route_A_original_reproduction/outputs/nifti/non_modifiable_emotion_consensus_AHAB_PIP.nii.gz |
| modifiable_emotion | Modifiable Emotion | AHAB | PIP | 13087 | C:/Users/81575/Desktop/vscode_box/emoreg_project_annotation_copy_2026-06-26/01_R_project/emoreg_R_original_reproduction_and_bottomup_mcmc/route_A_original_reproduction/outputs/nifti/modifiable_emotion_consensus_AHAB_PIP.nii.gz |

跨样本稳定性检验：

- 样本 1：AHAB；样本 2：PIP。
- 每个系统的共识图只保留两个样本在平滑 product map 后共同支持的位置，因此可作为 AHAB/PIP 跨样本稳定区域。
- 下表的 Dice/Jaccard 用于检查本次跨样本共识区域与下载到的原文系统图是否空间一致。

与下载的原文系统图的空间重叠：

| system | original_map | dice | jaccard | intersection_voxels | a_voxels | b_voxels |
| --- | --- | --- | --- | --- | --- | --- |
| common_appraisal | Common Appraisal.nii | 0.8266 | 0.7044 | 13032 | 18489 | 13044 |
| reappraisal_only | Reappraisal Only.nii | 0.7349 | 0.5810 |  2386 |  4052 |  2441 |
| non_modifiable_emotion | Non-modifiable Emotion.nii | 0.6927 | 0.5299 | 16930 | 31835 | 17046 |
| modifiable_emotion | Modifiable Emotion.nii | 0.8090 | 0.6793 |  8897 | 13087 |  8908 |

如何理解：Dice/Jaccard 越高，说明本次 R 复现的 AHAB/PIP 共识图与下载到的原文系统图空间越接近。体素数差异通常来自 BF 近似实现、平滑阈值、cluster size 阈值、输入 beta 图版本和 NIfTI 网格/header 处理差异。
