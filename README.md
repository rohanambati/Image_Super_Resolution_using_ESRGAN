# Image Super Resolution using ESRGAN

**Super-charge low-res images** with a lean ESRGAN. Fast on CPUs. Clear results.

## Project Overview

This notebook builds and trains a simplified ESRGAN model for single-image super-resolution.
It upscales low-resolution inputs into crisp high-resolution outputs. Perfect for low-power devices.

## Technology Stack

**Python 3.8+**
**PyTorch** for model definition and training
**Google Colab** notebook environment
**kagglehub** for dataset download
*NumPy*, *Pillow*, *Matplotlib* for data handling and visualization

## Workflow

1. Download DIV2K data via `kagglehub.dataset_download()` into `/content/data/`
2. Preprocess images

   * Generate low-res (LR) and high-res (HR) pairs
   * Extract patches for training
3. Define models

   * Generator with RRDB blocks
   * Discriminator (patch-based)
   * Perceptual loss using pretrained VGG19
4. Training loop

   * 100 epochs
   * 250 images for training, 50 for validation
   * Track loss, PSNR, SSIM
5. Visualize training

   * Plot loss vs. epoch
   * Plot PSNR vs. epoch

## Dataset

Use the **DIV2K** dataset for training and validation.
Place `DIV2K_train_HR` and `DIV2K_train_LR_bicubic` in `/content/data/` or run the download cell.

## Installation & Setup

1. Clone the repo:
   `git clone https://github.com/rohanambati/Image_Super_Resolution_using_ESRGAN.git`
2. Open the Colab notebook:
   `Image Super Resolutoin using ESRGAN.ipynb`
3. Install requirements:
   `pip install torch torchvision kagglehub numpy pillow matplotlib`
4. Authenticate Kagglehub and run the download cell
5. Run all cells in order

## Usage

* **Train from scratch**: run the training cells
* **Inference**: upload your own LR image in the Colab widget and click “Enhance”

I think this gives a clear guide to get started.
