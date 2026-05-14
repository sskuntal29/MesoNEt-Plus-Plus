# MesoNEt-

## MesoNet++

MesoNet++ is an enhanced, lightweight shallow CNN for deepfake detection designed for stronger real-world robustness.

### Core Improvements
- Squeeze-and-Excitation channel attention blocks after each encoder stage
- JPEG compression checks during training
- Label smoothing loss for calibrated fake-image confidence
- Expanded final convolutional layer
- Deeper classification heads
- AdamW optimizer with OneCycleLR scheduling

### Evaluation Setup
- Large-scale benchmark of 140,000 images
- Real images: FFHQ faces
- Fake images: StyleGAN2-generated faces

### Reported Results
- Clean accuracy: **93.6%**
- AUC: **0.984**
- JPEG robustness at quality 50:
  - Meso-4 accuracy drop: **4.7** percentage points
  - MesoNet++ accuracy drop: **1.4** percentage points
  - Compression-related performance-loss reduction: **~70%**
- Parameter increase over baseline: **~14%**

These results indicate that targeted, principled updates to shallow CNNs can significantly improve robustness under real-world perturbations without sacrificing lightweight efficiency.
