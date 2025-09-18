<div align="center">

# ComfyUI [with HunyuanImage2.1 support]
**The most powerful and modular visual AI engine and application.**

**This repository is a fork of [ComfyUI](https://github.com/comfyanonymous/ComfyUI), which properly implements [HunyuanImage2.1](https://github.com/Tencent-Hunyuan/HunyuanImage-2.1).**


[![Website][website-shield]][website-url]
[![Dynamic JSON Badge][discord-shield]][discord-url]
[![Twitter][twitter-shield]][twitter-url]
[![Matrix][matrix-shield]][matrix-url]
<br>
[![][github-release-shield]][github-release-link]
[![][github-release-date-shield]][github-release-link]
[![][github-downloads-shield]][github-downloads-link]
[![][github-downloads-latest-shield]][github-downloads-link]

[matrix-shield]: https://img.shields.io/badge/Matrix-000000?style=flat&logo=matrix&logoColor=white
[matrix-url]: https://app.element.io/#/room/%23comfyui_space%3Amatrix.org
[website-shield]: https://img.shields.io/badge/ComfyOrg-4285F4?style=flat
[website-url]: https://www.comfy.org/
<!-- Workaround to display total user from https://github.com/badges/shields/issues/4500#issuecomment-2060079995 -->
[discord-shield]: https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Finvites%2Fcomfyorg%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&logo=discord&logoColor=white&label=Discord&color=green&suffix=%20total
[discord-url]: https://www.comfy.org/discord
[twitter-shield]: https://img.shields.io/twitter/follow/ComfyUI
[twitter-url]: https://x.com/ComfyUI

[github-release-shield]: https://img.shields.io/github/v/release/comfyanonymous/ComfyUI?style=flat&sort=semver
[github-release-link]: https://github.com/comfyanonymous/ComfyUI/releases
[github-release-date-shield]: https://img.shields.io/github/release-date/comfyanonymous/ComfyUI?style=flat
[github-downloads-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/total?style=flat
[github-downloads-latest-shield]: https://img.shields.io/github/downloads/comfyanonymous/ComfyUI/latest/total?style=flat&label=downloads%40latest
[github-downloads-link]: https://github.com/comfyanonymous/ComfyUI/releases

</div>

ComfyUI lets you design and execute advanced stable diffusion pipelines using a graph/nodes/flowchart based interface. Available on Windows, Linux, and macOS.

## Get Started with HunyuanImage2.1

Install ComfyUI following [this link](https://github.com/comfyanonymous/ComfyUI).

### Basic Workflow

Download the following models and place them in the appropriate ComfyUI directories:

#### Text Encoders
Download and put in your ComfyUI/models/text_encoders directory:
- [byt5_small_glyphxl_fp16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/text_encoders/byt5_small_glyphxl_fp16.safetensors)
- [qwen_2.5_vl_7b.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/text_encoders/qwen_2.5_vl_7b.safetensors)

#### VAE Models
Download and put in your ComfyUI/models/vae directory:
- [hunyuan_image_2.1_vae_fp16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/vae/hunyuan_image_2.1_vae_fp16.safetensors)
- **Optional (for refiner):** [hunyuan_image_refiner_vae_fp16.safetensors](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/blob/main/split_files/vae/hunyuan_image_refiner_vae_fp16.safetensors)

#### Diffusion Models
Download and put in your ComfyUI/models/diffusion_models directory:
- [diffusion models](https://huggingface.co/Comfy-Org/HunyuanImage_2.1_ComfyUI/tree/main/split_files/diffusion_models)

#### Workflow
You can then load up or drag the following workflow in ComfyUI:

* Non-distill model workflow (50-100 steps inference):
[hunyuan_image_2.1_workflow.json](./HunyuanImage-2.1.json)

* Distill model workflow (faster speed with 8-step inference but slightly lower quality):
[hunyuan_image_2.1_distill_workflow.json](./HunyuanImage-2.1-distill.json)
