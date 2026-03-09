# Potenciando Power BI con IA: Guía de Integración vía MCP ⚡

Optimiza tu flujo de trabajo en análisis de datos conectando Claude Desktop con tus modelos de Power BI. Esta integración utiliza el protocolo MCP para permitir que la IA interactúe directamente con tus archivos locales.

Con esta configuración, puedes auditar relaciones, generar DAX complejo y documentar modelos mediante lenguaje natural, eliminando tareas repetitivas.

---
### 💻 Requisitos Previos

* Para una implementación exitosa, asegúrate de contar con:

* Power BI Desktop (Activo y con un archivo .pbix cargado).

* Claude Desktop instalado.

* Visual Studio Code (Para la gestión del servidor MCP).

Nota: Esta solución es exclusiva para entornos locales en Power BI Desktop.

---
### 📈 ¿Qué es el Model Context Protocol (MCP)?

El MCP actúa como un puente de comunicación estandarizado entre modelos de lenguaje (LLM) y fuentes de datos externas.

Al configurar este "servidor" intermedio, Claude adquiere capacidades para:

Explorar la estructura: Leer tablas, columnas y medidas existentes.

Ejecutar consultas: Probar sentencias DAX en tiempo real.

Escritura técnica: Crear o sugerir mejoras en las medidas del modelo.

---
### 🚀 Proceso de Instalación

1. Despliegue del Servidor en VS Code
  La inteligencia del sistema reside en una extensión específica de Visual Studio Code:

  * Abre VS Code y dirígete al Marketplace de extensiones.

  * Instala: Power BI Modeling MCP Server.

2. Localización del Ejecutable
  Claude necesita la ruta física del servidor para iniciar la conexión:

  * Navega en tu explorador de archivos a: %USERPROFILE%\.vscode\extensions.

  * Ubica la carpeta que comience con analysis-services.powerbi-modeling-mcp.

  * Dentro de la subcarpeta server, busca el archivo powerbi-modeling-mcp.exe. y toma la ruta completa

  * Copia la ruta completa (Usa Shift + Click derecho -> Copiar como ruta).

---
### ⚙️ Configuración de Claude Desktop

Para que Claude reconozca el servidor, debemos editar su archivo de configuración JSON:

* En Claude Desktop, ve a Settings > Developer > Edit Config.

Añade el siguiente bloque, asegurándote de usar doble barra invertida (\\) para evitar errores de sintaxis:

<img width="558" height="178" alt="image" src="https://github.com/user-attachments/assets/c1332a5e-202b-4ef8-8cc9-50c45607ddbe" />

Reinicio Crítico: Cierra Claude por completo y vuelve a abrirlo para cargar la nueva configuración.

---
### ⚠️ Resolución de Problemas (Troubleshooting)

* Servidor no detectado: Verifica que la ruta en el JSON sea exacta y use \\.

* Error de conexión: Asegúrate de que el archivo .pbix esté abierto antes de consultar a Claude.

* Falla de lectura: Confirma que la extensión en VS Code esté actualizada y activa.

---
### 📫 Conéctate conmigo

* **LinkedIn:** https://www.linkedin.com/in/flabevy
* **Portafolio:** https://github.com/FlaBevilacqua

---
