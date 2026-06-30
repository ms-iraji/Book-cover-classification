# Project Resources

## Source Code
The  source code of this research is available in this GitHub repository.
## Dataset
Dataset images are available upon request from the corresponding author iraji.ms@pnu.ac.ir.
<!--
The dataset used in this study can be downloaded from the following link:
https://drive.google.com/file/d/1PE0ElmRo-xN8C1q-f6O7e1RfmBefiGff/view?usp=sharing
-->
## Check points
The Check point models used in this study can be downloaded from the following link:
https://drive.google.com/file/d/1XEWbcIQJHtIbD1utO8S9_t-Rd6Lr6akp/view?usp=sharing
## Reproduction Guide

| Manuscript Item | Notebook Section | Output File |
|---|---|---|
| Table 4 - Image Model | train_vision() | checkpoints/vision_best_ema.pt |
| Table 4 - Text Model | train_text() | checkpoints/text_best_ema.pt |
| Table 4 - DIF Model | train_fusion() | checkpoints/fusion_best_ema.pt |
| Per-class metrics | compute_metrics() | results/*/best_per_class.csv |
| Accuracy/Loss curves | plot_curve() | results/*/curve_acc.*, curve_loss.* |
| Confusion matrices | plot_confusion() | results/*/cm_train.*, cm_test.* |
| t-SNE plots | run_tsne_and_plot() | results/*/tsne_train.*, tsne_test.* |

## Environment
See `requirements.txt`. Exact versions recorded from the execution environment:
torch 2.11.0+cu128, torchvision 0.26.0+cu128, transformers 5.12.0, easyocr 1.7.2

## Random Seeds
- Data split seed: 200
- Training seed: 42

## OCR Configuration
- Engine: EasyOCR v1.7.2
- Languages: ['en', 'fa']
- Cache included in `ocr_cache/`
