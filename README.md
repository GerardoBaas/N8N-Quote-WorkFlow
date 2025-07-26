# n8n Workflows - Plantillas de Automatización

Este repositorio contiene dos *workflows* listos para importar en [n8n](https://n8n.io/) que permiten automatizar tareas de atención al cliente y generación de cotizaciones, usando herramientas de IA, envío por WhatsApp, y formularios de respuesta por correo.

> ⚠️ **Importante:** Este flujo está configurado con datos de ejemplo para una tienda ficticia llamada **TechByte Store**. Debes personalizarlo según tu negocio o caso de uso real antes de utilizarlo en producción.

---

## 📁 Workflows incluidos

### 💬 `Chatbot_Simple.json`
Chatbot vía WhatsApp con IA que:
- Recibe mensajes del cliente.
- Responde preguntas frecuentes sobre productos o precios.
- Solicita datos para cotización.
- Ejecuta automáticamente el flujo de cotización (`Quotation_Tool`).

### 📦 `Quotation_Tool.json`
Generador automatizado de cotizaciones con:
- Asistente IA para procesamiento de solicitudes.
- Validación de modificaciones por correo electrónico.
- Generación de PDF con los datos de cotización.
- Envío final vía WhatsApp al cliente.

---

## 📄 Requisitos

- Instancia activa de [n8n](https://n8n.io/)
- API de WhatsApp Business configurada
- API de Google Gemini o similar
- Cuenta en [APITemplate.io](https://apitemplate.io/) (para generar PDF)
- Credenciales de Gmail OAuth2 (para envíos y formularios)

---

## 📂 Inventario de productos

Los flujos utilizan como fuente de datos un archivo JSON de ejemplo alojado en Google Drive, que contiene información como:

```json
[
  {
    "Producto": "RAM 16GB",
    "Precio": 850
  },
  {
    "Producto": "Disco Duro 1TB",
    "Precio": 1200
  }
]
```

> 🔁 Este archivo **debe ser reemplazado o actualizado** con el inventario real de tu negocio. El enlace al archivo se configura en el nodo `HTTP Request` como una URL pública de descarga directa de Google Drive.

---

## 🔧 Personalización necesaria

Antes de usar estos flujos en tu entorno, asegúrate de:

- Reemplazar referencias a `"TechByte Store"` con el nombre de tu negocio.
- Cambiar correos electrónicos de ejemplo (e.g., `[correo eliminado]`).
- Modificar los textos del asistente virtual según el tono o estilo de tu marca.
- Actualizar el inventario de productos con tus propios datos y precios.
- Configurar las credenciales requeridas en tu instancia de n8n.

---

## 🚀 Uso

1. Clona este repositorio.
2. Importa los archivos JSON desde el editor de n8n.
3. Configura tus credenciales.
4. Ajusta los nodos según tus necesidades (emails, nombres, herramientas).
5. Prueba con datos ficticios antes de poner en marcha.

---

## 📜 Licencia

MIT — Puedes usar, modificar y distribuir libremente este proyecto.
