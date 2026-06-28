# 共同评价系统：ROI 连通簇

这里的 ROI 是从该系统非空图中提取的三维连通簇。

为了避免同一脑区重复出现，脚本已经按固定系统顺序做互斥分配；已经进入前面系统的体素不会再进入本系统。

| tag | map_type | roi_folder | n_voxels | centroid_i | centroid_j | centroid_k |
| --- | --- | --- | --- | --- | --- | --- |
| AHAB | after_cluster | r001_ac_ahab | 16872 | 46.74 | 69.22 | 52.47 |
| AHAB | after_cluster | r002_ac_ahab |  1903 | 62.17 | 28.53 | 51.93 |
| AHAB | after_cluster | r003_ac_ahab |   256 | 17.48 | 32.76 | 62.30 |
| AHAB | after_cluster | r004_ac_ahab |   527 | 42.61 | 28.32 | 55.28 |
| AHAB | after_cluster | r005_ac_ahab |   175 | 40.55 | 50.76 | 52.79 |
| AHAB | after_cluster | r006_ac_ahab |   307 | 14.93 | 29.73 | 49.99 |
| AHAB | after_cluster | r007_ac_ahab |    44 | 40.50 | 35.32 | 47.16 |
| AHAB | after_cluster | r008_ac_ahab |  1869 | 16.42 | 70.27 | 33.71 |
| AHAB | after_cluster | r009_ac_ahab |   689 | 32.58 | 60.20 | 38.85 |
| AHAB | after_cluster | r010_ac_ahab |   905 | 46.35 | 57.80 | 39.57 |
| AHAB | after_cluster | r011_ac_ahab |    21 | 31.86 | 51.57 | 38.76 |
| AHAB | after_cluster | r012_ac_ahab |    19 | 43.16 |  7.89 | 37.32 |
| AHAB | after_cluster | r013_ac_ahab |    35 | 41.03 | 42.00 | 36.66 |
| AHAB | after_cluster | r014_ac_ahab |    48 | 10.44 | 34.75 | 35.81 |
| AHAB | after_cluster | r015_ac_ahab |   208 | 39.99 | 45.12 | 25.58 |
| AHAB | after_cluster | r016_ac_ahab |   523 | 59.77 | 25.35 | 23.77 |
| AHAB | after_cluster | r017_ac_ahab |    20 | 50.60 | 80.20 | 26.50 |
| AHAB | after_cluster | r018_ac_ahab |   129 | 37.68 | 19.19 | 24.31 |
| AHAB | after_cluster | r019_ac_ahab |   146 | 20.51 | 25.77 | 22.82 |
| AHAB | after_cluster | r020_ac_ahab |   152 | 15.38 | 61.86 | 19.53 |
| AHAB_PIP | consensus | r001_con_ahab_pip | 12704 | 43.71 | 66.95 | 56.47 |
| AHAB_PIP | consensus | r002_con_ahab_pip |   465 | 18.53 | 30.13 | 62.28 |
| AHAB_PIP | consensus | r003_con_ahab_pip |  1118 | 58.84 | 27.49 | 59.58 |
| AHAB_PIP | consensus | r004_con_ahab_pip |   707 | 40.50 | 25.85 | 56.66 |
| AHAB_PIP | consensus | r005_con_ahab_pip |   334 | 15.51 | 29.22 | 48.06 |
| AHAB_PIP | consensus | r006_con_ahab_pip |   122 | 31.98 | 87.06 | 46.52 |
| AHAB_PIP | consensus | r007_con_ahab_pip |   272 | 57.04 | 83.11 | 41.91 |
| AHAB_PIP | consensus | r008_con_ahab_pip |   367 | 65.86 | 27.60 | 42.26 |
| AHAB_PIP | consensus | r009_con_ahab_pip |  1397 | 16.58 | 67.75 | 34.23 |
| AHAB_PIP | consensus | r010_con_ahab_pip |    30 | 10.83 | 33.07 | 36.10 |
| AHAB_PIP | consensus | r011_con_ahab_pip |   568 | 57.14 | 25.21 | 22.44 |
| AHAB_PIP | consensus | r012_con_ahab_pip |   146 | 35.21 | 20.22 | 23.46 |
| AHAB_PIP | consensus | r013_con_ahab_pip |    23 | 45.26 | 18.13 | 23.00 |
| PIP | after_cluster | r001_ac_pip |  2421 | 47.90 | 67.60 | 59.86 |
| PIP | after_cluster | r002_ac_pip |   924 | 18.44 | 65.21 | 58.19 |
| PIP | after_cluster | r003_ac_pip |   163 | 18.28 | 29.33 | 61.40 |
| PIP | after_cluster | r004_ac_pip |   312 | 59.66 | 27.84 | 59.67 |
| PIP | after_cluster | r005_ac_pip |   395 | 38.79 | 25.15 | 57.83 |
| PIP | after_cluster | r006_ac_pip |   261 | 14.44 | 28.43 | 43.13 |
| PIP | after_cluster | r007_ac_pip |    16 | 31.75 | 87.00 | 46.62 |
| PIP | after_cluster | r008_ac_pip |    64 | 56.34 | 82.22 | 41.25 |
| PIP | after_cluster | r009_ac_pip |    91 | 64.60 | 26.51 | 41.92 |
| PIP | after_cluster | r010_ac_pip |   294 | 16.13 | 67.45 | 34.58 |
| PIP | after_cluster | r011_ac_pip |   332 | 60.90 | 66.26 | 34.57 |
| PIP | after_cluster | r012_ac_pip |    89 | 48.27 |  8.31 | 32.44 |
| PIP | after_cluster | r013_ac_pip |    34 | 29.44 |  7.50 | 33.82 |
| PIP | after_cluster | r014_ac_pip |    42 | 45.10 | 51.98 | 30.60 |
| PIP | after_cluster | r015_ac_pip |   163 | 55.46 | 24.56 | 21.66 |
| PIP | after_cluster | r016_ac_pip |    39 | 35.46 | 20.13 | 23.00 |
