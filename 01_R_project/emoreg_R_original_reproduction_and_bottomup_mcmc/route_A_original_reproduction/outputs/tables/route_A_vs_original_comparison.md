# Route A comparison with published system maps

Generated from current Route A outputs. BF method: `jzs_exact`; BF threshold on 2*log(BF): `4.6`; cluster minimum: `15` voxels.

Original-paper threshold reset used here:

- JZS Bayes factor with medium Cauchy scale r = sqrt(2)/2.
- Evidence for the alternative: BF > 10, equivalent to 2*log(BF) about 4.6.
- Evidence for the null: BF < 1/10, equivalent to signed 2*log(BF) below -4.6.
- Consensus maps follow the original product-map step: smooth both binary maps with FWHM 3 voxels, multiply them, then threshold product > 0.01.

Consensus map versus published maps:

| system | route_voxels | original_voxels | intersection_voxels | original_coverage | route_extra_fraction | route_to_original_ratio | dice | jaccard |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| common_appraisal | 18489 | 13044 | 13032 | 0.999 | 0.295 | 1.417 | 0.827 | 0.704 |
| reappraisal_only |  4052 |  2441 |  2386 | 0.977 | 0.411 | 1.660 | 0.735 | 0.581 |
| non_modifiable_emotion | 31835 | 17046 | 16930 | 0.993 | 0.468 | 1.868 | 0.693 | 0.530 |
| modifiable_emotion | 13087 |  8908 |  8897 | 0.999 | 0.320 | 1.469 | 0.809 | 0.679 |

Single-dataset after-cluster maps versus published maps:

| system | tag | route_voxels | original_voxels | original_coverage | route_extra_fraction | dice | jaccard |
| --- | --- | --- | --- | --- | --- | --- | --- |
| common_appraisal | AHAB | 24848 | 13044 | 0.826 | 0.567 | 0.568 | 0.397 |
| common_appraisal | PIP |  5640 | 13044 | 0.382 | 0.117 | 0.533 | 0.364 |
| reappraisal_only | AHAB |  3110 |  2441 | 0.352 | 0.724 | 0.309 | 0.183 |
| reappraisal_only | PIP |  2464 |  2441 | 0.319 | 0.684 | 0.318 | 0.189 |
| non_modifiable_emotion | AHAB | 18829 | 17046 | 0.367 | 0.668 | 0.349 | 0.211 |
| non_modifiable_emotion | PIP | 13290 | 17046 | 0.340 | 0.564 | 0.382 | 0.236 |
| modifiable_emotion | AHAB | 14662 |  8908 | 0.737 | 0.553 | 0.557 | 0.386 |
| modifiable_emotion | PIP |  5775 |  8908 | 0.458 | 0.293 | 0.556 | 0.385 |

Route A voxel summary:

| dataset | system | n_subjects | bf_method | bf_threshold_2log | voxels_before_cluster | voxels_after_cluster | cluster_min_voxels |
| --- | --- | --- | --- | --- | --- | --- | --- |
| AHAB | common_appraisal | 182 | jzs_exact | 4.6 | 24927 | 24848 | 15 |
| AHAB | reappraisal_only | 182 | jzs_exact | 4.6 |  3391 |  3110 | 15 |
| AHAB | non_modifiable_emotion | 182 | jzs_exact | 4.6 | 19051 | 18829 | 15 |
| AHAB | modifiable_emotion | 182 | jzs_exact | 4.6 | 14796 | 14662 | 15 |
| PIP | common_appraisal | 176 | jzs_exact | 4.6 |  5738 |  5640 | 15 |
| PIP | reappraisal_only | 176 | jzs_exact | 4.6 |  2707 |  2464 | 15 |
| PIP | non_modifiable_emotion | 176 | jzs_exact | 4.6 | 13566 | 13290 | 15 |
| PIP | modifiable_emotion | 176 | jzs_exact | 4.6 |  5865 |  5775 | 15 |

Interpretation:

- The consensus maps still cover nearly all published-map voxels, so the issue is not missing the original regions.
- The outward expansion mainly comes from the consensus product-map step: smoothing plus a low product threshold expands borders beyond the hard binary intersection.
- The detailed numeric table is `route_A_vs_original_system_maps_detailed.csv`.
