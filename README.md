TRABAJO PRACTICO: Hello-Stages (Node, Git y Docker)

Proyecto Hello-Stages implementado con control de versiones en Git y estructurado para entornos de desarrollo, prueba y producción mediante Docker.

Para poder ejecutar, probar y desplegar este proyecto, asegúrate de tener instaladas las siguientes herramientas en tu sistema:

Node.js (versión 24 o superior): Necesario para ejecutar el proyecto en el entorno local y correr los scripts de npm.

Git: Indispensable para el control de versiones y la gestión de ramas del repositorio.

Docker y Docker Compose: Requeridos para construir y levantar las imágenes y contenedores en sus diferentes perfiles (desarrollo, prueba y producción).

Instrucciones de Ejecución

1. Entorno Local (Node.js)
Desarrollo: Ejecutá npm run dev para iniciar el servidor local con recarga automática. Podés verificarlo en el navegador en http://localhost:3000.
Pruebas: Ejecutá npm test para correr la suite de tests del proyecto.

2. Perfiles de Docker y Docker Compose
El proyecto cuenta con tres perfiles independientes configurados mediante Docker Compose para cada etapa:
docker compose --profile dev up --build
(Para detenerlo: docker compose --profile dev down)

Perfil de Test (test):
Construye y ejecuta las pruebas automatizadas dentro de un contenedor aislado:
docker compose --profile test up --build

Perfil de Producción (prod):
Levanta la versión optimizada y limpia de la aplicación, ejecutándose con un usuario seguro y sin dependencias innecesarias:
docker compose --profile prod up --build
(Para detenerlo: docker compose --profile prod down)
