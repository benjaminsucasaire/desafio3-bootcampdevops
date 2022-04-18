# Desafio Devops

El proyecto contiene una aplicación básica con Node, Ngnix y MySQL.

Con cada actualización de la página, se registrará un nuevo registro en la base de datos y se mostrará en la lista, en la misma página.

El proyecto contiene algunas falencias y errores, analizar e implementar las correcciones correspondientes.

Si no entiendes algún concepto o parte del problema, ¡no hay de qué preocuparse! Queremos que aceptes el desafío hasta donde sepas.

### ¿Lo que debe hacerse? ### 

 - ajustes que hacen que todas las aplicaciones se levanten y se comuniquen
 - un README que contiene información sobre el problema a lo largo del proyecto para identificar y corregir errores

Comprométase en el camino para que podamos entender su forma de pensar!! :)

### Problemas encontrados ### 

crear el network en el docker-compose
networks:
node-network:
driver: bridge


detallar puerto en db para ver la creación desde mi pc
ports:
- "3306:3306"

se agregó en entrypoint
docker-entrypoint.sh

generar el archivo .env en la carpeta nginx
cp .env.example .env



ejecutar la creación de los Dockerfile
docker-compose build

desplegar los contenedores
docker-compose  up -d



se agregó en el Dockerfile de node

RUN npm install
CMD ["node", "index.js"]

se agregó en el Dockerfile de nginx
COPY nginx.conf /etc/nginx/conf.d
