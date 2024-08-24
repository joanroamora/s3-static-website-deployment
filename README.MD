# 🇨🇴 S3 Static Website Deployment 👋

## Descripción
Este proyecto configura un bucket en Amazon S3 para servir una página web estática con acceso público. Utiliza GitHub Actions para automatizar el despliegue del contenido HTML.

## Requisitos
- Una cuenta de AWS con permisos para crear y configurar un bucket S3.
- Una cuenta de GitHub con permisos para crear repositorios y configurar GitHub Actions.
- Git instalado en tu máquina local.

## Configuración del Proyecto

### 1. Clonar el repositorio
Clona este repositorio en tu máquina local:
bash
git clone https://github.com/tu-usuario/s3-static-website-deployment.git


### 2. Configurar Amazon S3
Inicia sesión en tu cuenta de AWS.
Ve al servicio de S3 y crea un nuevo bucket.
Asegúrate de que el nombre del bucket sea único a nivel global.
Habilita el alojamiento de sitios web estáticos en la configuración del bucket.
Sube el archivo index.html al bucket.
### 3. Configurar GitHub Secrets
Ve a la página del repositorio en GitHub.
Entra a la sección de "Settings" y luego a "Secrets and variables" > "Actions".
Añade los siguientes secretos:
AWS_ACCESS_KEY_ID: Tu clave de acceso de AWS.
AWS_SECRET_ACCESS_KEY: Tu clave secreta de AWS.
AWS_BUCKET_NAME: El nombre del bucket que creaste en S3.
AWS_REGION: La región donde se encuentra tu bucket (ejemplo: us-east-1).
### 4. Configurar GitHub Actions
El repositorio ya incluye un archivo de workflow en .github/workflows/deploy.yml que se encargará de desplegar el sitio web en Amazon S3 cada vez que realices un push a la rama main.

### 5. Desplegar el Sitio Web
Haz un commit y push de los cambios al repositorio. Esto disparará el workflow de GitHub Actions y desplegará la página web en S3.

git add .
git commit -m "Initial commit"
git push origin main

## Acceso al Sitio Web
Una vez que el proceso de despliegue haya finalizado, puedes acceder a tu página web desde la URL pública de tu bucket S3.

## Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para obtener más información.

## End