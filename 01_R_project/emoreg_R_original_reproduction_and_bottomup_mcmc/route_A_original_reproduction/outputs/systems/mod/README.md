# 可调节情绪系统

系统代码：`modifiable_emotion`

分入原则：情绪生成有 BF 支持，且重评方向表现为下降调节；用于定位可被重评改变的情绪反应区域。

包含内容：

- `original_logic.csv`：原文对应的 BF/t 判定逻辑。
- `system_voxel_summary.csv`：该系统在不同 tag 下的体素数量和簇控制摘要。
- `maps`：非空系统图和互斥系统图。
- `roi`：非重叠 ROI 连通簇和对应说明。

本文件夹中的 ROI 已经过互斥整理，避免同一 ROI 同时出现在多个系统中。
