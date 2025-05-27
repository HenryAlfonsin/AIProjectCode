# AIProductCode
# Text-to-Image + Caption Generator with BLIP Fine-Tuning

This Hugging Face Space takes a **text prompt** as input and generates:
- A **realistic image** using `stabilityai/sd-turbo` (Stable Diffusion Turbo)
- A **descriptive caption** of that image using `Salesforce/blip-image-captioning-base` (BLIP)

It also includes an **optional fine-tuning interface** that allows you to upload your own dataset to improve the captioning model (BLIP) on custom images and descriptions.


## Features:

**Text Prompt → Image** (via `sd-turbo`)
**Image → Caption** (via BLIP model)
**Optional fine-tuning** of the captioning model using a user-uploaded CSV
Fast generation using GPU-optimized models
Built with `diffusers`, `transformers`, and `gradio`


## How to Use:

1. **Enter a text prompt** (e.g., _"A cat astronaut in space"_).
2. Click **"Generate Image + Caption"**.
3. View the generated image and its auto-generated caption.


## Optional: Fine-tune the Captioning Model:

You can improve the captioning quality on your own dataset:

1. Prepare a `.csv` file with the following columns:
2. Upload the CSV using the upload box.
3. Click **"Fine-tune BLIP"**.
4. The captioning model will be updated using your examples (small-scale training).

> Fine-tuning is optimized for lightweight customization and may take a few minutes. Ideal for small datasets only.


## Models Used

- **Stable Diffusion Turbo** (`stabilityai/sd-turbo`)  
Fast, high-quality text-to-image generation.

- **BLIP Captioning Base** (`Salesforce/blip-image-captioning-base`)  
Vision-language model trained for image captioning.


## Dependencies

This app uses:
```txt
diffusers
transformers
torch
gradio
datasets
Pillow
