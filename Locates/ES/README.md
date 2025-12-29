<div align="center">
  <h1>🎨 ConfyUI on Colab (Versión en Español) <a href="https://colab.research.google.com/github/lz-migra/ConfyUI_on-Colab/blob/main/Locates/ES/ConfyUI_on_Colab_ES.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab" height="40" style="vertical-align: middle;"></a></h1>
</div>

Esta es una implementación optimizada de **ComfyUI** para Google Colab, diseñada específicamente para usuarios de habla hispana. Permite una configuración flexible de almacenamiento, instalación automática de modelos avanzados y múltiples opciones de conectividad.

## 🚀 Características Principales

* **Gestión de Almacenamiento Dual**: Opción para ejecutar de forma local en Colab o montar **Google Drive** para persistir modelos y resultados en `/content/drive/MyDrive/AI/ComfyUI`.
* **Instalación Inteligente de Modelos**: Soporte integrado para modelos populares como Stable Diffusion 1.5, Protovision XL, y la serie Juggernaut (v8, X, XL Hyper).
* **Soporte Multimodal Avanzado**: Capacidad de instalar **Qwen VL**, un modelo capaz de entender y editar imágenes mediante instrucciones complejas.
* **Flexibilidad de Conexión**: Selección entre túneles de **Cloudflare** o **Localtunnel** para acceder a la interfaz web.

## 🛠️ Especificaciones Técnicas

### Requisitos de Hardware

* **GPU**: Se recomienda una **T4 GPU** o superior. El notebook incluye una verificación automática que detendrá la ejecución si no se detecta una GPU, a menos que se active explícitamente el modo `SOLO_CPU`.
* **RAM**: Para modelos pesados como Qwen VL, las máquinas gratuitas de Colab pueden presentar limitaciones de memoria.

### Dependencias Principales

* **Base**: PyTorch con soporte CUDA (cu121/cu118).
* **Optimización**: `xformers` para una gestión eficiente de la memoria de video.
* **Descargas**: Utiliza `aria2` para descargas ultra rápidas de modelos desde Civitai y Hugging Face.

## 📖 Guía de Configuración

1. **Montar Drive (Opcional)**: Selecciona `MONTAR` en `MODO_DRIVE` para no perder tus datos al cerrar la sesión.
2. **Civitai Token**: Para descargar modelos de Civitai, asegúrate de añadir tu `CIVITAI_API_TOKEN` en los *Secrets* (icon de llave 🔑) de Google Colab.
3. **Modelos Personalizados**: Puedes ingresar una lista en formato JSON para descargar modelos específicos en carpetas personalizadas.
* *Herramienta útil*: [Generador de JSON para modelos](https://script.google.com/macros/s/AKfycbzmfmxfFRKvlnwlDuHNwOhWqEzYd90f1YKaQxSuFQ3o8HyQW_oHZZgPo9j4vUQlJ7ZI/exec).



## 💡 Información de Utilidad

* **Modo Low VRAM**: Si experimentas cierres inesperados, activa `USAR_LOWVRAM` para optimizar el uso de los recursos de la GPU.
* **Actualizaciones**: Al activar `ACTUALIZAR_COMFY`, el sistema realizará un `git pull` automático para asegurar que tienes las últimas funciones del repositorio oficial.
* **Acceso**: Una vez iniciado, busca en los logs el mensaje `🔗 URL DE ACCESO`. Si usas Localtunnel, el sistema también te proporcionará la contraseña/IP necesaria para el acceso.

---

*Desarrollado para facilitar el acceso a herramientas de IA generativa en la comunidad hispana.*
