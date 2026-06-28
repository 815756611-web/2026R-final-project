# 路线 A：四系统整理输出

这里按原文四个系统整理路线 A 的输出。基础结果仍保留在 `outputs/nifti` 和 `outputs/tables`。

整理规则：

- 系统顺序：`reappraisal_only` -> `common_appraisal` -> `non_modifiable_emotion` -> `modifiable_emotion`。
- 同一个体素如果已经被前一个系统接收，后面的系统不会再重复生成 ROI。
- 只有非空 NIfTI 才会复制或写入；空白图不会放入系统文件夹。
- ROI 来自系统图的三维连通簇，默认至少保留 15 个体素。

四个系统文件夹：

- `reapp`：重评专属系统 (`reappraisal_only`)
- `common`：共同评价系统 (`common_appraisal`)
- `nonmod`：不可调节情绪系统 (`non_modifiable_emotion`)
- `mod`：可调节情绪系统 (`modifiable_emotion`)
