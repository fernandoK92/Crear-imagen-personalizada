# Crear imagen personalizada
## 1. Título  
Crear imagen personalizada

## 2. Tiempo de duración  
15 minutos.  

## 3. Fundamentos  

Docker es una plataforma que permite empaquetar, distribuir y ejecutar aplicaciones dentro de contenedores. Un contenedor incluye todo lo necesario para que la aplicación funcione (dependencias, librerías, entorno), asegurando que se ejecute igual en cualquier máquina.

En esta práctica se trabajó con una aplicación React que debía ser contenida dentro de una imagen Docker usando Nginx para servir los archivos estáticos. Además, se utilizó un servicio backend simulado (MockAPI) para que el frontend pueda consumir datos correctamente.

Los conceptos fundamentales involucrados fueron:

Imagen Docker: plantilla inmutable con todo lo necesario para ejecutar la app.

Contenedor: instancia en ejecución de una imagen.

Dockerfile: archivo que define los pasos para construir una imagen.

Build y Run: docker build crea la imagen; docker run crea y ejecuta el contenedor.

Nginx: servidor web utilizado para servir la app React compilada.

Redirección de puertos: para acceder a la aplicación desde el navegador.

## 4. Conocimientos previos  

Para desarrollar la práctica se necesitaban conocer previamente:

Uso básico de la terminal (CMD/PowerShell).

Conceptos básicos de React: estructura del proyecto y comando npm run build.

Manejo fundamental de Docker:

docker build

docker run

docker ps, docker stop, docker rm

Estructura de un Dockerfile.

Conocimientos básicos de servidores web (Nginx).

Uso de Git para clonar repositorios.

## 5. Objetivos a alcanzar  

Objetivo general

Contenerizar una aplicación frontend en React creando una imagen Docker funcional y ejecutando el contenedor correspondiente.

Objetivos específicos

Clonar el repositorio del proyecto React.

Verificar el funcionamiento del frontend ejecutándolo localmente.

Crear y configurar correctamente un Dockerfile que construya el proyecto.

Crear un archivo nginx.conf para servir la aplicación con Nginx.

Construir la imagen Docker de la aplicación.

Ejecutar un contenedor a partir de la imagen creada.

Levantar el servicio backend simulado (mockAPI) para el correcto funcionamiento del frontend.

Validar que la aplicación es accesible a través de un puerto local.
  
## 6. Equipo necesario  

Docker Desktop instalado y funcionando.

Node.js y npm para ejecutar el proyecto React localmente.

Git para clonar repositorios.

Editor de texto (VS Code recomendado).

Navegador web (Chrome, Edge, etc.).

## 7. Material de apoyo  

Repositorio del frontend (React):
https://github.com/Daviddotcoms/suda-frontend-s6

Repositorio del backend simulado (MockAPI):
https://github.com/Daviddotcoms/mockAPI

Documentación básica usada:

Docker: https://docs.docker.com/

React: https://react.dev/

Nginx (configuración simple): https://nginx.org/

Comandos principales:

git clone

npm install, npm start, npm run build

docker build

docker run

docker ps, docker stop, docker rm
## 8. Procedimiento  

Clonación del repositorio del frontend

<img width="1857" height="830" alt="image" src="https://github.com/user-attachments/assets/23673293-d120-4f0c-a798-4081b5f0fede" />

una vez clonado , ingresamos a la carpeta donde su ubica el archivo del fronted 

<img width="1146" height="937" alt="image" src="https://github.com/user-attachments/assets/67e598f2-0534-4d69-891f-9608f51f5c90" />


en la parte de la ruta de la carpeta del fronted escribimos cmd para que nos abra directamente en el cmd


<img width="1146" height="937" alt="image" src="https://github.com/user-attachments/assets/abe4caf8-657a-4e3e-8337-b1989a0a1d50" />


una vez que se abra la terminal y con la ruta del frontend escribimos code . para que se nos en visual studio code

<img width="703" height="47" alt="image" src="https://github.com/user-attachments/assets/5bacdda5-f9df-4f7d-82e8-e1b9c171dda9" />


ingresamos a la terminal del proyecto y instalamos las dependecion con npm install .


<img width="1478" height="982" alt="image" src="https://github.com/user-attachments/assets/ebb97710-7428-44ea-890e-a2aed0b4c402" />

 npm run dev para desplegar 

<img width="771" height="312" alt="image" src="https://github.com/user-attachments/assets/aa26f6bd-f2e2-4177-b4da-8f0924ae0502" />

y se nos abrira en el navegador 

<img width="1912" height="1003" alt="image" src="https://github.com/user-attachments/assets/9a1c055b-130a-4bf3-b1fd-abdd760cdf21" />

Ojo para que nos carguen los datos del proyecto necesitamos un servicio backend simulado que lo tenemos que clonar tal cual como el frontend y aplicamos en la terminal del backend lo siguiente para que funcione 

<img width="1343" height="970" alt="image" src="https://github.com/user-attachments/assets/39ae698c-0190-4b19-bdfd-23f3175cca67" />

y listo nos cargara los datos en el frontend

Ahora vamos con la Creación del archivo Dockerfile y hacmos lo siguiente desde la terminal 

<img width="842" height="40" alt="image" src="https://github.com/user-attachments/assets/9b9db05a-00e3-4b7a-84f9-10e13af70f18" />

Para verificar que se creo el archivo dockerfile podemos verificarlo en visual studio code :

<img width="1471" height="925" alt="image" src="https://github.com/user-attachments/assets/e3f075bb-70f2-4b22-b5bb-4792c536effe" />

Dentro del archivo docker file ponemos agregamos el siguiente contenido

<img width="1472" height="897" alt="image" src="https://github.com/user-attachments/assets/fe2d16a2-0294-4758-a367-b1369f78b027" />

Ademas creamos el archivo nginx porque funciona como un servidor web de alto rendimiento, ideal para aplicaciones frontend en producción.


<img width="917" height="32" alt="image" src="https://github.com/user-attachments/assets/156103c9-31d0-4673-ac63-efa5579f4f0c" />


<img width="1481" height="960" alt="image" src="https://github.com/user-attachments/assets/3fa1ae5e-ff34-4fdf-a334-670a9a013a66" />


Construcción de la imagen Docker

<img width="742" height="673" alt="image" src="https://github.com/user-attachments/assets/2458845b-90f5-4af3-b348-d73e73457cac" />

Comando para verificar 

<img width="472" height="209" alt="image" src="https://github.com/user-attachments/assets/63a77bfd-3c96-4a61-b8e9-078026c06cd5" />


Ejecución del contenedor con la aplicación React

<img width="897" height="41" alt="image" src="https://github.com/user-attachments/assets/01d95b96-bb91-4137-87dc-fccf23dbe636" />

Se nos levantara en el http://localhost:3001/

<img width="1902" height="1017" alt="image" src="https://github.com/user-attachments/assets/e2ac4cb1-9e1c-47aa-b35e-1a5613c60e61" />


## 9. Resultados esperados:
La aplicación React debe estar contenida correctamente en una imagen Docker funcional.

El contenedor debe ejecutarse sin errores y ser accesible en un navegador (ej. http://localhost:8080).

Los archivos estáticos deben ser servidos correctamente por Nginx.

El frontend debe comunicarse correctamente con el backend simulado (MockAPI).

La aplicación debe funcionar igual que en desarrollo, siendo portátil y reproducible en cualquier máquina con Docker.
## 10. Bibliografías
Docker, Inc. (2025). Docker Documentation. Disponible en: https://docs.docker.com/

Documentación oficial de Docker, que explica la creación de imágenes, contenedores y el uso de Dockerfile.

React, Inc. (2025). React – A JavaScript library for building user interfaces. Disponible en: https://react.dev/

Sitio oficial de React, utilizado para entender la estructura de proyectos React y la compilación de aplicaciones para producción.

Nginx, Inc. (2025). Nginx Documentation. Disponible en: https://nginx.org/

Documentación oficial de Nginx, consultada para servir aplicaciones estáticas y configurar el servidor dentro de Docker.

DavidDotComs. (2025). Repositorio Suda Frontend S6. GitHub. Disponible en:
