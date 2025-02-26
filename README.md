# **Plataforma de Blogs - Despliegue Automatizado**  

Este proyecto es una plataforma de blogs diseñada para ser escalable, eficiente y fácil de usar. Utiliza tecnologías modernas para garantizar una experiencia fluida tanto para desarrolladores como para usuarios finales. Su arquitectura está optimizada para despliegues automatizados en entornos basados en Docker y AWS.  

## **Características Clave**  

### Plataforma de Blogs:  
- Gestión de publicaciones y comentarios.  
- Soporte para categorías y etiquetas.  
- Diseño modular para facilitar la extensión y personalización.  

### Automatización del Despliegue:  
- Configuración de CI/CD con GitHub Actions.  
- Despliegue automatizado en instancias AWS EC2.  
- Docker Compose para orquestación de contenedores.  

### Contenerización:  
- Configuración Dockerizada para garantizar portabilidad.  
- Scripts para construir, desplegar y reiniciar servicios.  

## **Tecnologías Utilizadas**  

- **Backend:** Spring Boot (Java)  
- **Contenerización:** Docker y Docker Compose  
- **Despliegue:** AWS EC2 con GitHub Actions  
- **Control de Versiones:** Git  
- **Automatización:** Workflows YAML para CI/CD  

## **Cómo Funciona el Despliegue Automatizado**  

Este proyecto incluye un archivo de workflow (`deploy.yml`) que gestiona el despliegue automático cada vez que se realizan cambios en la rama `main`:  

1. **Verificación del Repositorio:** Se asegura de que el servidor ya contenga el repositorio Git.  
2. **Clonación y Actualización:** Si falta el repositorio, lo clona; si existe, obtiene y aplica los últimos cambios.  
3. **Reinicio de Servicios:** Detiene los servicios actuales, reconstruye los contenedores y reinicia todo el entorno con Docker Compose.
