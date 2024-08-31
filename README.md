# Modelo de IA gratuito, privado y 100% local

### WebLLM: Inferencia de Modelos de Lenguaje en el Navegador

WebLLM es un motor de inferencia de modelos de lenguaje de alto rendimiento que ejecuta la inferencia directamente en los navegadores web con aceleración por hardware. Todo se ejecuta dentro del navegador sin necesidad de soporte de servidor y está acelerado con WebGPU.

WebLLM es completamente compatible con la API de OpenAI. Es decir, puedes usar la misma API de OpenAI en cualquier modelo de código abierto localmente, con funcionalidades que incluyen modo JSON, llamadas a funciones, transmisión en tiempo real, etc.

Podemos aprovechar muchas oportunidades divertidas para construir asistentes de IA para todos y habilitar la privacidad mientras disfrutamos de la aceleración por GPU.

Puedes usar WebLLM como un paquete base de npm y construir tu propia aplicación web sobre él siguiendo la documentación y comenzando con la guía Get Started. Este proyecto es un proyecto compañero de MLC LLM, que permite el despliegue universal de modelos de lenguaje de gran tamaño en diversos entornos de hardware.

### Lista de Modelos Soportados

Consulta la lista completa de modelos disponibles en MLC Models. WebLLM soporta un subconjunto de estos modelos disponibles y la lista se puede acceder en prebuiltAppConfig.model_list.

Aquí están las principales familias de modelos actualmente soportados:

Llama: Llama 3, Llama 2, Hermes-2-Pro-Llama-3
Phi: Phi 3, Phi 2, Phi 1.5
Gemma: Gemma-2B
Mistral: Mistral-7B-v0.3, Hermes-2-Pro-Mistral-7B, NeuralHermes-2.5-Mistral-7B, OpenHermes-2.5-Mistral-7B
Qwen (通义千问): Qwen2 0.5B, 1.5B, 7B

#

> [!Note]
> Particularmente he elegido el modelo Llama 3.8, que pesa 5.17 GB. Por lo tanto, es necesario esperar a que se descargue completamente este paquete antes de utilizar la aplicación. Asegúrate de tener suficiente espacio en tu dispositivo y una buena conexión a Internet para facilitar esta descarga.

#

### Aceleración por GPU en el Navegador

Este modelo se ejecuta a través de tu GPU para mejorar el rendimiento. Para asegurarte de que esto funcione correctamente, debes verificar si tu navegador soporta WebGPU y si está habilitado. WebGPU es una API web moderna diseñada para ofrecer acceso a las capacidades avanzadas de las GPUs.

- Cómo Verificar Soporte de GPU en tu Navegador:

1. Google Chrome:

Escribe en la barra de direcciones

```plaintext
chrome://gpu
```

Revisa la sección sobre WebGPU para ver si está habilitado.

2. Mozilla Firefox:

Escribe en la barra de direcciones y presiona Enter.

```plaintext
about:config
```

Busca _dom.webgpu.enabled_ y asegúrate de que esté configurado en true.

3. Microsoft Edge:

Similar a Google Chrome, escribe en la barra de direcciones y presiona Enter.

```plaintext
edge://gpu
```

Revisa la sección sobre WebGPU.
Si WebGPU no está habilitado, consulta la documentación de tu navegador sobre cómo activarlo. La compatibilidad y el rendimiento pueden variar según el navegador y el hardware de tu dispositivo, así que asegúrate de utilizar una versión actualizada del navegador.

También en la consola de desarrollo del navegador pueden ejecutar el siguiente script:

```javascript
navigator.gpu.requestAdapter();
```
