# Image Generation with Stable Diffusion


### Objective

The objective of this project is to generate images from text prompts using a pre-trained generative AI model.

## Model Used

**Stable Diffusion v1.5**

Stable Diffusion is a pre-trained text-to-image diffusion model that generates images based on natural language prompts.

## Technologies Used

- Python
- PyTorch
- Hugging Face Diffusers
- Stable Diffusion v1.5
- CLIP Text Encoder
- Transformer
- U-Net
- Cross-Attention
- VAE (Variational Autoencoder)
- Diffusion Scheduler
- Google Colab

## Working

The user provides a text prompt such as:

> Astronaut in a jungle, cold color palette, muted colors, detailed, 8k

The prompt is processed by the text encoder and converted into numerical representations. Stable Diffusion then starts with random noise and progressively removes the noise while using the text information to guide the generation. Finally, the VAE decoder converts the generated latent representation into an image.

## Architecture

```text
Text Prompt
     ↓
Tokenization
     ↓
CLIP Text Encoder
     ↓
Text Embeddings
     ↓
Cross-Attention
     ↓
U-Net + Random Noise
     ↓
Iterative Denoising
     ↓
Clean Latent Representation
     ↓
VAE Decoder
     ↓
Generated Image
