# Curso de Tailwind CSS

Herramientas
 - NPM es el sistema de gestión de paquetes por defecto para Node.js
 - Autoprefixer es una libreria que nos ayuda poder agregar a nuestro codigo el ventorprefixer
 - PostCSS
 - Instalamos la extension "Tailwind CSS IntelliSense" en nuestro VScode
 - Instalamos un live server con "npm install live-server -g"  (-g una instalacón global) es un  
   servidor local, el cual tambien es una extension para VScode.

Instalación
===========
- Inicializamos el proyecto con -- "npm init -y" que nos genera el archivo de package.json
- Instalamos nuestras librerias -- "npm install tailwindcss autoprefixer postcss-cli"
Inicilizamos las librerias instaladas:
  - "npx tailwindcss init" que nos crea un archivo de nombre tailwind.config.js
  - creamos un archivo de nombre -- "touch postcss.config.js"

Editamos los siguientes archivos:
  - postcss.config.js con
      module.exports = {
        plugins: [
          require('tailwindcss'),
          require('autoprefixer'),
        ]
      }

  - Creamos un carpeta con su archivo -- css/tailwind.css el nombre del archivo puede ser cualquiera 
    y dentro del archivo agregamos lo siguiente:
      @tailwind base;
      @tailwind components;
      @tailwind utilities;
    que es un directiva que agrega el codigo base de tailwind que hace que todo funcione, tailwind.css es nuestro archivo css origen
  - Creamos una carpeta con su archivo -- public/index.html 

    inicializamos el archivo con:
      html:5 se agrega estructura html

  - Creamos nuestro archivo css destino con un comando npm, editamos el archivo packge.json parte de 
    scripts :
      "scripts": {
        "build": "postcss css/tailwind.css -o public/css/style.css"
      },
    nos vamos a la terminal y lo ejecutamos con "npm run build" nos genera el archivo public/css/style.css el cual debe tener contenido.

