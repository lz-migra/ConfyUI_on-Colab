<div align="center">
  <h1>🎨 ComfyUI on Colab (English Version) <a href="https://colab.research.google.com/github/lz-migra/ConfyUI_on-Colab/blob/main/Locates/EN/ConfyUI_on_Colab_EN.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab" height="40" style="vertical-align: middle;"></a></h1>
</div>

This is an optimized implementation of **ComfyUI** for Google Colab, designed to provide a seamless experience. It features flexible storage configuration, automatic installation of advanced models, and multiple connectivity options.

## 🚀 Key Features

* **Dual Storage Management**: Option to run locally on Colab or mount **Google Drive** to persist models and outputs at `/content/drive/MyDrive/AI/ComfyUI`.
* **Smart Model Installation**: Built-in support for popular models such as Stable Diffusion 1.5, Protovision XL, and the Juggernaut series (v8, X, XL Hyper).
* **Advanced Multimodal Support**: Ability to install **Qwen VL**, a powerful model capable of understanding and editing images through complex instructions.
* **Connection Flexibility**: Choice between **Cloudflare** or **Localtunnel** tunnels to access the web interface securely.

## 🛠️ Technical Specifications

### Hardware Requirements

* **GPU**: A **T4 GPU** or higher is recommended. The notebook includes an automatic check that will halt execution if no GPU is detected, unless `CPU_ONLY` mode is explicitly enabled.
* **RAM**: For heavy models like Qwen VL, free Colab instances may encounter memory limitations.

### Core Dependencies

* **Base**: PyTorch with CUDA support (cu121/cu118).
* **Optimization**: `xformers` for efficient video memory (VRAM) management.
* **Downloads**: Uses `aria2` for ultra-fast model downloads from Civitai and Hugging Face.

## 📖 Configuration Guide

1.  **Mount Drive (Optional)**: Select `MOUNT` (MONTAR) in `DRIVE_MODE` to ensure your data is saved after the session ends.
2.  **Civitai Token**: To download models from Civitai, make sure to add your `CIVITAI_API_TOKEN` in the Google Colab *Secrets* (key icon 🔑).
3.  **Custom Models**: You can provide a JSON list to download specific models into custom folders.
    * *Useful Tool*: [JSON Generator for Models](https://script.google.com/macros/s/AKfycbzmfmxfFRKvlnwlDuHNwOhWqEzYd90f1YKaQxSuFQ3o8HyQW_oHZZgPo9j4vUQlJ7ZI/exec).

## 💡 Helpful Tips

* **Low VRAM Mode**: If you experience unexpected crashes, enable `USE_LOWVRAM` to optimize GPU resource allocation.
* **Updates**: By enabling `UPDATE_COMFY`, the system will perform an automatic `git pull` to ensure you have the latest features from the official repository.
* **Access**: Once started, look for the `🔗 ACCESS URL` message in the logs. If using Localtunnel, the system will also provide the necessary password/IP for access.

---

*Developed to facilitate access to generative AI tools for the global community.*

