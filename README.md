# Concept Art to 3D Scene Pipeline

A three-stage generative AI pipeline converting 2D concept art into navigable, editable 3D scenes.

## Stages
1. **Multi-view synthesis** - Zero123++ generates multiple views from a single image
2. **3D reconstruction** - nerfstudio/gsplat builds a Gaussian Splat from synthesised views
3. **Generative editing** - GaussianEditor and Instruct-NeRF2NeRF enable text-driven scene editing

## Requirements

## Structure
```text
concept-to-3d/
├── inputs/                # source concept art images
├── outputs/
│   ├── multiview/         # Zero123++ synthesised views
│   ├── splat/             # nerfstudio training output
│   └── edited/            # GaussianEditor / IN2N outputs
├── stage1_multiview/      # Zero123++ scripts
├── stage2_reconstruction/ # nerfstudio config + launch scripts
├── stage3_editing/
│   ├── gaussianeditor/
│   └── in2n/
├── evaluation/            # PSNR/SSIM/LPIPS scripts, comparison notebooks
├── notebooks/             # exploratory Jupyter notebooks
├── logs/                  # prompt logs, run configs
└── paper/                 # written report
```