

# Instalación y Configuración Inicial

## Preparación Inicial
1. Instalar docker -> https://docs.docker.com/get-docker/
2. Instalar docker-compose -> https://docs.docker.com/compose/install/

## Instalación de Odoo con docker
1. Descargar el repositorio
~~~
git clone https://github.com/difusionvisual/odoo-docker-template.git
~~~
2. Ingresar a la carpeta 
~~~
cd odoo-docker-template
~~~
3. Crear archivo .env y docker-compose.yaml
~~~
cp copy.env .env
cp copy.docker-compose.yaml docker-compose.yaml
~~~
4. Editar parámetros de .env
~~~
Ejemplo:
ODOO_VERSION=15
WEB_HOST=odoo_15
WEB_PORT=15069
~~~
5. Opcional: Editar docker-compose.yaml, esto siempre y cuando se requiera añadir nuevos servicios o modificar parámetros.
6. Ejecutar docker-compose
7. Si se desea añadir una ruta a un directorio local especifico, usar el siguiente formato en el archivo docker-compose.yaml 
 `- /Ruta/carpeta/local/en/mi/pc:/mnt/extra-addons-customize`
~~~
docker-compose up -d
~~~