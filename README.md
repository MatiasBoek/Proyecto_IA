# Generador de Mensajes (Gemini) y de Imágenes (Vertex AI)

Este proyecto demuestra la integración de dos potentes servicios de IA de Google:
- **Google Gemini:** para la generación de texto (mensajes de RR.HH. para ausencias).
- **Vertex AI:** para la generación de imágenes de bienvenida a partir de prompts.

## Requisitos Fundamentales

- Python 3.10+
- **Una cuenta de Google Cloud:** Se puede usar la capa gratuita, pero requiere vincular una tarjeta para la verificación inicial.
- **Un proyecto de Google Cloud:** con la API de Vertex AI habilitada.
- **Una clave de API de Google AI Studio:** para el uso de Gemini.

## 1. Configuración Obligatoria: Google Cloud y `.env`

Para que **ambas partes del proyecto funcionen**, es indispensable configurar el acceso a los servicios de Google. Usaremos un archivo `.env` para gestionar nuestras credenciales de forma segura. En el archivo .env.example se indican las APIs necesarias para el proyecto 

### Paso A: Preparar tu Entorno en Google Cloud

1.  **Crea un Proyecto:** Ve a la [Consola de Google Cloud](https://console.cloud.google.com/) y crea un nuevo proyecto. Anota el **ID del Proyecto** (ej: `mi-proyecto-ia-123456`).
2.  **Habilita la Facturación:** Asegúrate de que la facturación esté habilitada para tu proyecto. Es un requisito para usar las APIs, aunque no superes la capa gratuita.
3.  **Habilita la API de Vertex AI:** En tu proyecto, ve a la sección de APIs y servicios y [habilita la "Vertex AI API"](https://console.cloud.google.com/apis/library/aiplatform.googleapis.com).
4.  **Genera una API Key para Gemini:** Ve a [Google AI Studio](https://aistudio.google.com/app/apikey), crea un nuevo proyecto y genera una API key.

### Paso B: Configurar tu archivo `.env`

1.  Busca el archivo `.env.example` en este repositorio.
2.  Crea una copia de ese archivo y renómbrala a `.env`.
3.  Abre el nuevo archivo `.env` y rellénalo con los datos que obtuviste en el paso anterior. Debería verse así:

### En el archivo .env.example se indican las APIs necesarias para el proyecto 




