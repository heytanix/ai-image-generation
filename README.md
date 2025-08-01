# AI Image Generation with Stable Diffusion

## Introduction
This project provides a comprehensive guide to generating high-quality images from text descriptions using the **Stable Diffusion v1.5** model. The included Jupyter Notebook (`ai-image-generation.ipynb`) walks through the entire pipeline, from setting up the environment and loading the pre-trained model to generating and saving custom images. This serves as a practical demonstration of state-of-the-art text-to-image synthesis.

## 🫡 You can help me by Donating
[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/heytanix)

### Model & Technology Overview:
* **Model**: `runwayml/stable-diffusion-v1-5`
* **Architecture**: Latent Diffusion Model
* **Core Libraries**: Hugging Face `diffusers`, `transformers`, `accelerate`
* **Framework**: PyTorch

**Objective**:
The primary goal of this project is to create a clear and reusable workflow for leveraging a powerful, pre-trained diffusion model on a local machine with GPU acceleration. It aims to make advanced AI image generation accessible to developers and enthusiasts.

## Technologies Used
The implementation relies on a stack of modern deep learning and AI libraries:
1.  **Stable Diffusion**: The core text-to-image generation model.
2.  **Hugging Face `diffusers`**: A high-level library for working with diffusion models, providing the `StableDiffusionPipeline`.
3.  **PyTorch**: The underlying deep learning framework for tensor computations and GPU management.
4.  **CUDA**: For accelerating the model inference on NVIDIA GPUs.
5.  **Pillow**: A Python library for image manipulation and saving.

## Project Workflow
### Step 1: Environment Setup
* All required Python packages are listed in `requirements.txt`.
* The first step in the notebook installs these dependencies using `pip`.

### Step 2: Hardware Configuration
* The notebook verifies that a CUDA-enabled GPU is available to ensure fast processing times.
* It configures PyTorch to use the GPU and sets the data type to `torch.float16` for optimized performance and lower memory consumption.

### Step 3: Model Loading
* The pre-trained `runwayml/stable-diffusion-v1-5` model is downloaded from the Hugging Face Hub.
* The entire `StableDiffusionPipeline` is loaded and moved onto the GPU for inference.

### Step 4: Image Generation
* A user-defined text `prompt` is created to describe the desired image.
* Inference parameters, such as `num_inference_steps`, are set to control the trade-off between image quality and generation speed.
* The pipeline processes the prompt to generate the image.

### Step 5: Display and Save Output
* The final generated image is displayed directly in the notebook.
* A script is provided to save the image to a local `output_images` directory with a unique, timestamped filename.

### Conclusion
This project successfully demonstrates an end-to-end pipeline for local AI image generation. By leveraging the Hugging Face `diffusers` library, it becomes straightforward to download and run powerful models like Stable Diffusion. The notebook serves as both a learning tool and a practical script for creative image synthesis, highlighting the accessibility of modern AI tools for developers.

## Acknowledgments
* [Hugging Face](https://huggingface.co/) (for the `diffusers` library and model hosting)
* [RunwayML](https://runwayml.com/) and [Stability AI](https://stability.ai/) (for their pioneering work on the Stable Diffusion model)
* [PyTorch Team](https://pytorch.org/)
