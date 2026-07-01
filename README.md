# amz-price-tracker

# Rastreador de Precios de Amazon 🛒📈

Un sistema automatizado diseñado para monitorear las fluctuaciones de precios de productos específicos en Amazon y enviar alertas en tiempo real. Este proyecto demuestra la implementación de herramientas de automatización self-hosted y entornos de contenedores para resolver problemas reales de seguimiento de datos.

## 🛠️ Tecnologías y Arquitectura

*   **Core de Automatización:** n8n (Herramienta de automatización de flujos de trabajo).
*   **Entorno y Despliegue:** Docker y Docker Compose (Alojado de forma local/servidor propio).
*   **Extracción de Datos:** Web Scraping / Peticiones HTTP.
*   **Notificaciones:** API de Bot de Telegram.

## 🚀 Características Principales

*   **Programación Automatizada:** Revisa periódicamente la página del producto sin intervención manual.
*   **Análisis de Datos:** Extrae métricas de precio y disponibilidad directamente de la fuente.
*   **Alertas Instantáneas:** Envía una notificación inmediatamente cuando se detecta una baja o cambio de precio.
*   **Infraestructura en Contenedores:** Fácilmente desplegable y aislado utilizando Docker.

## 📁 Estructura del Repositorio

*   `Workflow AMZ Tracker.json`: La exportación completa del flujo de n8n. Puedes importar este archivo directamente en tu propia instancia de n8n.
*   `docker-compose.yml`: (Opcional) El archivo de configuración utilizado para levantar el entorno de n8n.
*   `README.md`: Documentación del proyecto.

## 🔍 QA e Insights Técnicos (Fase Actual de Optimización)

Como parte de las prácticas de mejora continua y control de calidad (QA), el proyecto se encuentra actualmente en mantenimiento para corregir los siguientes casos borde:
*   **Consistencia en el Web Scraping:** El flujo ocasionalmente captura elementos alternativos en lugar del precio real actual debido a cambios dinámicos en la estructura del frontend (DOM) de Amazon.
*   **Solución Planificada:** Implementar selectores CSS/XPaths de respaldo (fallbacks) y añadir pasos de validación de datos para asegurar que solo los datos numéricos limpios del precio activen el sistema de notificaciones.
