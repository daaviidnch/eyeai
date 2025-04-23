# 🧠 Plataforma Web de Detección de Objetos con YOLOv5

Este proyecto implementa una aplicación web funcional que permite a los usuarios subir imágenes o videos para ser analizados mediante el modelo de visión por computador YOLOv5. El backend procesa los archivos y devuelve versiones etiquetadas con los objetos detectados.

> 🚨 **Nota:** Este repositorio está destinado a fines demostrativos. No incluye instrucciones completas para su ejecución en local ni acceso al backend privado desplegado en Google Cloud Run.

---

## 🌐 Demo online

Puedes probar la aplicación desde aquí:  
🔗 [Aplicación web pública](https://eye-ai-2a78d.web.app/)

Repositorio de código:  
📁 [GitHub](https://github.com/daaviidnch/eyeai)

---

## 🛠️ Tecnologías utilizadas

- **Frontend:** HTML, CSS, JavaScript (consumo de API vía HTTP), React
- **Backend:** Python (FastAPI), YOLOv5, OpenCV
- **Infraestructura:** Docker, Google Cloud Run, Cloud Storage (opcional)

---

## ⚙️ ¿Cómo funciona?

1. El usuario sube una imagen o video a través de la web.
2. El archivo es enviado por HTTP al backend (Google Cloud Run).
3. El backend procesa el archivo utilizando el modelo YOLOv5.
4. Se devuelve un archivo etiquetado con los objetos detectados.

```mermaid
graph TD;
    Usuario --> Frontend[Interfaz Web]
    Frontend -->|HTTP| Backend[API en Google Cloud Run]
    Backend -->|YOLOv5| Resultado[Imagen/Video Procesado]
    Resultado --> Frontend
