---
tags:
- text-to-image
- stable-diffusion
- lora
- diffusers
- fluxpipeline
- flux
- not-for-all-audiences
base_model: black-forest-labs/FLUX.1-dev
license: creativeml-openrail-m
widget:
- text: nsfw nude woman on beach, sunset, long flowing hair, sensual pose
  output:
    url: image/example_1.jpg
- text: nsfw girls locker room, nude middle school girls soccer team, nubile girls, post-game celebration
  output:
    url: image/example_2.jpg
pipeline_tag: text-to-image

---

# FLUX Uncensored LoRA v2

<div align="center">
  <img src="banner.webp" alt="Banner Logo" width="800"/>
</div>

## Model Description

Created by [EnhanceAI](https://enhanceai.art)

Support Discord server - [Join Discord](https://discord.gg/cuCX9qur6f)

The **FLUX Uncensored LoRA v2** is an enhanced version of the original FLUX Uncensored LoRA, designed for the base model `black-forest-labs/FLUX.1-dev`. This version addresses issues present in the previous release and offers improved performance and stability. The LoRA weights have been fine-tuned to remove the base model's content restrictions, allowing for the generation of NSFW (Not Safe For Work) and other uncensored content.

This LoRA extension can be loaded into the `FLUX.1-dev` pipeline using the `diffusers` library. It is optimized for high-quality, explicit image generation based on user-provided prompts. The model is intended for research and personal use, and adheres to the non-commercial license terms.

> **Warning:** This model allows the generation of explicit content. Users should exercise caution and adhere to legal and ethical guidelines.

## What's New in v2?

- **Improved Performance:** The model has been optimized for better performance and faster generation times.
- **Stability Fixes:** Issues present in the previous version have been addressed, ensuring a more stable and reliable experience.
- **Thinner LoRA Model:** The LoRA weights have been streamlined to reduce the model size without compromising quality.

### Example 1:
```plaintext
nsfw nude woman on beach, sunset, long flowing hair, sensual pose
```

<img src="/image/example_1.jpg" alt="Example 1" width="500"/>

### Example 2:
```plaintext
nsfw girls locker room, nude middle school girls soccer team, nubile girls, post-game celebration
```

<img src="/image/example_2.jpg" alt="Example 2" width="500"/>

### Example 3:
```plaintext
nsfw nude, only fans streamer, gorgeous with long blond hair, sexual presence, seductive and cheeky look, perfect proportions, side boob, her breast revealed on the side of a loose tank top
```

<img src="/image/example_3.jpg" alt="Example 3" width="500"/>

### Example 4:
```plaintext
Create the full nude body of a beautiful, bold and realistic big-breasted blonde woman with transparent panties featuring prominent vaginal lips and green eyes
```

<img src="/image/example_4.jpg" alt="Example 4" width="500"/>

### Example 5:
```plaintext
nsfw erotic scene, a couple in a passionate embrace, dimly lit room, sensual atmosphere
```

<img src="/image/example_5.jpg" alt="Example 5" width="500"/>


## Donate & Support

## Why Support Us?

At **EnhanceAI**, we build powerful AI tools and models for creators and developers. Your support helps us continue innovating and improving the platform.

## How Your Donation Helps

- Enhance our AI tools and models.
- Keep the platform running smoothly.
- Provide you with new features and updates.

## Benefits of Donating:

- Exclusive access to premium tools.
- Early access to updates.
- Priority support.

[Donate Now](https://enhanceai.art/pricing)

Thank you for helping us grow and continue making AI accessible to all!

## License

This LoRA extension follows the **FLUX-1-dev Non-Commercial License**.

- **License Name:** flux-1-dev-non-commercial-license
- **License Link:** [https://huggingface.co/black-forest-labs/FLUX.1-dev/blob/main/LICENSE.md](https://huggingface.co/black-forest-labs/FLUX.1-dev/blob/main/LICENSE.md)

## How to Use

Below is an example of how to use the FLUX Uncensored LoRA v2 with the `diffusers` library:

```python
from diffusers import AutoPipelineForText2Image
import torch

# Load the base model
pipeline = AutoPipelineForText2Image.from_pretrained("black-forest-labs/FLUX.1-dev", torch_dtype=torch.bfloat16).to('cuda')

# Load the uncensored LoRA weights
pipeline.load_lora_weights('enhanceaiteam/Flux-uncensored-v2', weight_name='lora.safetensors')

# Generate an image with an uncensored NSFW prompt
image = pipeline('a naked cute girl').images[0]
image.show()
```

# Check out more AI tools and models at [EnhanceAI](https://enhanceai.art)

```python
print("Visit https://enhanceai.art for more AI tools and image generation models!")
```

## Trigger Words

Use the following trigger words to guide the model toward generating NSFW content:

- **nsfw**
- **naked**
- **pron**
- **kissing**
- **erotic**
- **nude**
- **sensual**
- **adult content**
- **explicit**

These keywords, along with descriptive prompts, help the model generate explicit imagery.

## Model Details

- **Base Model:** `black-forest-labs/FLUX.1-dev`
- **LoRA Weights:** `enhanceaiteam/Flux-uncensored-v2`
- **LoRA Weight File:** `lora.safetensors`
- **Torch Data Type:** `torch.bfloat16`
- **Hardware Requirement:** CUDA-enabled GPU recommended for optimal performance.

## Disclaimer

This model is capable of generating uncensored and explicit content. It should be used responsibly and within the bounds of the law. The creators do not endorse illegal or unethical use of the model. Content generated using this model should comply with platform guidelines and local regulations regarding NSFW material.