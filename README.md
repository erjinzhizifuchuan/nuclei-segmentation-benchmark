# Nuclear Segmentation Benchmark and Model Selection

This repository provides the original dataset references, model references and an interactive decision-support tool for task-aware nuclear segmentation model selection.

## Interactive model-selection tool

The interactive recommendation interface is available here:

[Open the interactive decision-support tool](https://your-username.github.io/nuclei-segmentation-benchmark/decision_matrix_selector.html)

Replace the URL above with the final public URL of the HTML interface. If the HTML file is stored directly in the repository, it can also be linked using:

```markdown
[Open the interactive decision-support tool](docs/decision_matrix_selector.html)
```

## Benchmark datasets

| Dataset | Original publication |
|---|---|
| MoNuSeg | [A Multi-organ Nucleus Segmentation Challenge](https://pmc.ncbi.nlm.nih.gov/articles/PMC10439521/) |
| PanNuke | [PanNuke: An Open Pan-Cancer Histology Dataset for Nuclei Instance Segmentation and Classification](https://doi.org/10.1007/978-3-030-23937-4_2) |
| BBBC038 | [Nucleus segmentation across imaging experiments: the 2018 Data Science Bowl](https://pmc.ncbi.nlm.nih.gov/articles/PMC6919559/) |
| TissueNet | [Whole-cell segmentation of tissue images with human-level performance](https://doi.org/10.1038/s41587-021-01094-0) |
| CellBinDB | [CellBinDB: A large-scale multimodal annotated dataset for cell segmentation](https://doi.org/10.1093/gigascience/giaf069) |

The in-house skin H&E image set was used for validation. Because of institutional and ethical restrictions, the raw images are not publicly redistributed.

## Segmentation methods

The benchmark included 15 segmentation methods represented by 16 model configurations. CellposeSAM was evaluated in two configurations: dataset-trained CellposeSAM and direct inference using pretrained weights.

### Semantic segmentation

| Method | Original publication |
|---|---|
| FCN-8s | [Fully Convolutional Networks for Semantic Segmentation](https://openaccess.thecvf.com/content_cvpr_2015/html/Long_Fully_Convolutional_Networks_for_Semantic_Segmentation_CVPR_2015_paper.html) |
| U-Net | [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597) |
| Attention U-Net | [Attention U-Net: Learning Where to Look for the Pancreas](https://arxiv.org/abs/1804.03999) |
| TransUNet | [TransUNet: Rethinking the U-Net Architecture](https://doi.org/10.1016/j.media.2024.103280) |
| Swin-Unet | [Swin-Unet: Unet-like Pure Transformer for Medical Image Segmentation](https://arxiv.org/abs/2105.05537) |

### Instance-oriented segmentation

| Method | Original publication |
|---|---|
| Cellpose | [Cellpose: A Generalist Algorithm for Cellular Segmentation](https://doi.org/10.1038/s41592-020-01018-x) |
| StarDist | [Cell Detection with Star-convex Polygons](https://doi.org/10.1007/978-3-030-00934-2_30) |
| Mask R-CNN | [Mask R-CNN](https://openaccess.thecvf.com/content_ICCV_2017/html/He_Mask_R-CNN_ICCV_2017_paper.html) |
| HoVer-Net | [HoVer-Net: Simultaneous Segmentation and Classification of Nuclei](https://doi.org/10.1016/j.media.2019.101563) |
| CellViT | [CellViT: Vision Transformers for Precise Cell Segmentation and Classification](https://doi.org/10.1016/j.media.2024.103143) |
| CellposeSAM | [Cellpose-SAM: Superhuman Generalization for Cellular Segmentation](https://doi.org/10.1101/2025.04.28.651001) |

### Foundation models

| Method | Original publication |
|---|---|
| SAM | [Segment Anything](https://openaccess.thecvf.com/content/ICCV2023/html/Kirillov_Segment_Anything_ICCV_2023_paper.html) |
| MedSAM | [Segment Anything in Medical Images](https://doi.org/10.1038/s41467-024-44824-z) |
| HQ-SAM | [Segment Anything in High Quality](https://proceedings.neurips.cc/paper_files/paper/2023/hash/5f828e38160f31935cfe9f67503ad17c-Abstract-Conference.html) |
| EfficientSAM | [EfficientSAM: Leveraged Masked Image Pretraining for Efficient Segment Anything](https://openaccess.thecvf.com/content/CVPR2024/html/Xiong_EfficientSAM_Leveraged_Masked_Image_Pretraining_for_Efficient_Segment_Anything_CVPR_2024_paper.html) |

## Configuration note

CellposeSAM was evaluated using two configurations:

- Dataset-trained CellposeSAM
- Pretrained direct-inference CellposeSAM_eval

These two configurations correspond to one method but two evaluation settings.
