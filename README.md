Guía de instalación del proyecto Portal WEB

Esta guía proporciona los pasos necesarios para instalar y configurar correctamente el proyecto eCommerce.
Requisitos previos

Antes de comenzar con la instalación, asegúrese de tener los siguientes requisitos previos instalados:

    Apache MySQL para el manejo de la base de datos. Puede descargarlo desde el siguiente enlace: Descargar XAMPP.

    NVM (Node Version Manager) para la gestión de versiones de Node.js. Puede descargar el instalador desde el siguiente enlace: Descargar nvm-setup.exe. Asegúrese de ejecutar el instalador y seguir las instrucciones.

Dependencias

Asegúrese de tener las siguientes dependencias instaladas:

    Node.js versión 14.20.1
    Angular (se requiere la versión 15 o superior)

Instalación del proyecto

Siga los pasos a continuación para instalar el proyecto eCommerce:

    Descargue el proyecto y ábralo con VScode. Navegue hasta la carpeta "angular-ecommerce-app-master" y ejecute los siguientes comandos en una terminal:

bash

cd backend
npm install
cd ..
cd client
npm install

    Crear la base de datos en MySQL. Utilice las siguientes configuraciones:
        Nombre de la base de datos: myapp
        En la carpeta "backend" en la raíz del proyecto, encontrará el archivo "sql_dump.sql". Ábralo y copie todo el código. Luego, péguelo en la sección de ejecución de SQL en su cliente de MySQL para crear las tablas necesarias en la base de datos "myapp".

    Configuraciones para la base de datos MySQL:
        Navegue hasta la carpeta "backend" y abra el archivo "db.js" ubicado en la carpeta "database". Cambie el siguiente código:

    javascript

const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: '',
  database: 'myapp',
});

Inicialización del proyecto:

    Abra una terminal para el backend y ejecute el siguiente comando:

bash

node app.js

    Abra otra terminal para el cliente y ejecute el siguiente comando:

bash

    ng serve

Con estos pasos, habrá instalado y configurado correctamente el proyecto eCommerce. Ahora puede comenzar a trabajar en el desarrollo del proyecto.
