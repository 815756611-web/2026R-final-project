# 重评专属系统：ROI 连通簇

这里的 ROI 是从该系统非空图中提取的三维连通簇。

为了避免同一脑区重复出现，脚本已经按固定系统顺序做互斥分配；已经进入前面系统的体素不会再进入本系统。

| tag | map_type | roi_folder | n_voxels | centroid_i | centroid_j | centroid_k |
| --- | --- | --- | --- | --- | --- | --- |
| AHAB | after_cluster | r001_ac_ahab |  60 | 39.85 | 56.43 | 70.70 |
| AHAB | after_cluster | r002_ac_ahab | 539 | 66.98 | 31.88 | 54.82 |
| AHAB | after_cluster | r003_ac_ahab | 297 | 13.66 | 33.22 | 55.96 |
| AHAB | after_cluster | r004_ac_ahab | 497 | 54.28 | 76.47 | 45.93 |
| AHAB | after_cluster | r005_ac_ahab | 384 | 25.14 | 79.18 | 49.21 |
| AHAB | after_cluster | r006_ac_ahab |  51 | 39.20 | 75.10 | 42.88 |
| AHAB | after_cluster | r007_ac_ahab |  18 | 45.50 | 19.11 | 41.72 |
| AHAB | after_cluster | r008_ac_ahab |  18 | 41.94 | 43.94 | 38.67 |
| AHAB | after_cluster | r009_ac_ahab |  50 | 15.42 | 63.12 | 34.62 |
| AHAB | after_cluster | r010_ac_ahab | 411 | 68.27 | 44.34 | 28.68 |
| AHAB | after_cluster | r011_ac_ahab |  27 | 21.19 | 83.41 | 37.93 |
| AHAB | after_cluster | r012_ac_ahab | 116 | 11.91 | 38.16 | 34.89 |
| AHAB | after_cluster | r013_ac_ahab |  20 | 41.15 |  8.35 | 35.90 |
| AHAB | after_cluster | r014_ac_ahab |  59 | 67.59 | 62.15 | 30.07 |
| AHAB | after_cluster | r015_ac_ahab |  33 | 40.79 | 32.42 | 28.18 |
| AHAB | after_cluster | r016_ac_ahab |  37 | 44.97 |  7.38 | 27.49 |
| AHAB | after_cluster | r017_ac_ahab | 200 | 35.81 | 16.51 | 23.15 |
| AHAB | after_cluster | r018_ac_ahab |  45 |  8.18 | 48.82 | 25.98 |
| AHAB | after_cluster | r019_ac_ahab | 131 | 61.82 | 23.10 | 21.99 |
| AHAB | after_cluster | r020_ac_ahab |  23 | 26.35 | 25.26 | 23.13 |
| AHAB | after_cluster | r021_ac_ahab |  63 | 14.89 | 57.11 | 17.37 |
| AHAB | after_cluster | r022_ac_ahab |  31 | 30.06 | 22.32 | 19.68 |
| AHAB_PIP | consensus | r001_con_ahab_pip | 946 | 65.47 | 31.53 | 54.76 |
| AHAB_PIP | consensus | r002_con_ahab_pip | 761 | 13.99 | 31.17 | 55.76 |
| AHAB_PIP | consensus | r003_con_ahab_pip |  69 | 49.19 | 64.39 | 60.54 |
| AHAB_PIP | consensus | r004_con_ahab_pip | 407 | 55.48 | 74.39 | 52.22 |
| AHAB_PIP | consensus | r005_con_ahab_pip | 472 | 24.22 | 81.04 | 49.70 |
| AHAB_PIP | consensus | r006_con_ahab_pip |  59 | 15.19 | 37.27 | 36.69 |
| AHAB_PIP | consensus | r007_con_ahab_pip | 191 | 58.16 | 81.84 | 31.95 |
| AHAB_PIP | consensus | r008_con_ahab_pip |  62 | 68.92 | 31.44 | 35.19 |
| AHAB_PIP | consensus | r009_con_ahab_pip | 365 | 29.77 | 20.17 | 22.17 |
| AHAB_PIP | consensus | r010_con_ahab_pip | 300 | 55.39 | 19.56 | 21.11 |
| AHAB_PIP | consensus | r011_con_ahab_pip | 267 | 66.23 | 54.70 | 17.91 |
| AHAB_PIP | consensus | r012_con_ahab_pip | 132 | 13.95 | 56.71 | 17.24 |
| PIP | after_cluster | r001_ac_pip | 116 | 40.53 | 31.34 | 59.46 |
| PIP | after_cluster | r002_ac_pip | 270 | 55.41 | 67.07 | 58.49 |
| PIP | after_cluster | r003_ac_pip |  97 | 22.88 | 76.06 | 56.42 |
| PIP | after_cluster | r004_ac_pip | 429 | 12.61 | 31.12 | 49.94 |
| PIP | after_cluster | r005_ac_pip | 533 | 64.59 | 29.87 | 49.34 |
| PIP | after_cluster | r006_ac_pip |  24 | 28.12 | 84.92 | 53.29 |
| PIP | after_cluster | r007_ac_pip |  18 | 53.83 | 79.11 | 52.78 |
| PIP | after_cluster | r008_ac_pip |  49 | 25.14 | 85.71 | 46.29 |
| PIP | after_cluster | r009_ac_pip |  15 | 56.33 | 79.93 | 47.27 |
| PIP | after_cluster | r010_ac_pip |  20 | 56.95 | 84.90 | 35.60 |
| PIP | after_cluster | r011_ac_pip |  20 | 46.15 |  9.10 | 34.65 |
| PIP | after_cluster | r012_ac_pip | 218 | 63.52 | 74.68 | 29.72 |
| PIP | after_cluster | r013_ac_pip |  31 | 31.42 |  5.90 | 30.10 |
| PIP | after_cluster | r014_ac_pip |  16 | 18.00 | 81.06 | 29.50 |
| PIP | after_cluster | r015_ac_pip | 189 | 28.63 | 21.19 | 21.72 |
| PIP | after_cluster | r016_ac_pip | 134 | 65.25 | 53.75 | 16.63 |
| PIP | after_cluster | r017_ac_pip | 197 | 53.19 | 19.93 | 18.86 |
| PIP | after_cluster | r018_ac_pip |  44 | 14.23 | 56.41 | 17.41 |
| PIP | after_cluster | r019_ac_pip |  28 | 59.18 | 59.50 | 13.82 |
| PIP | after_cluster | r020_ac_pip |  16 | 57.94 | 29.25 | 12.38 |
