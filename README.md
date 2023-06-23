Pasos para intalar proyecto ecommerce

PREREQUISITOS:
-Para manejo de BD - Apache Mysql
	https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/8.0.28/xampp-windows-x64-8.0.28-0-VS16-installer.exe/download
	*Descargar Xaamp

-Para navegar entre versiones de node - npm instalar del siguiente link:

	https://github.com/coreybutler/nvm-windows/releases
	*Descargar el instalador nvm-setup.exe e instalarlo
	*comprobar que este instalado abrir cmd y ejecutar: nvm -v
	*listamos las versiones diponibles de node con el comando: nvm list available
	*Instalamos la version 14.20.1 con el comando: nvm install 14.20.1
	*Para usar la version ya instalada usamos el comando: nvm use 14.20.1

DEPENDENCIAS:
node version 14.20.1
angular sirve a partir de la version 15

INSTALACION PROYECTO:
-Descargar el proyecto abrir con VScode la carpeta angular-ecommerce-app-master y ejecutar los comandos: 
	* cd backend   -  para navegar a la carpeta backend
	* npm install
	* cd..	- para volver a la raiz
	* cd client - para navegar a la carpeta client
	* npm install

-Crear Base de Datos en Mysql:
	*Nombre de BD: myapp
	*En la carpeta backend en la raiz encontrara el archivo sql_dump.sql abralo copie todo el codigo y
	copielo en el apartado de ejecuciones de SQL para crear las tablas en la BD myapp.

-CONFIGURACIONES PARA BD MYSQL
	*En la carpeta backend navegar a la carpeta database al archivo db.js cambiar el siguiente codigo:
	const connection = mysql.createConnection({
  	  host: 'localhost',
  	  user: 'root',
  	  password: '',
  	  database: 'myapp',
	});

-Inicializacion de Proyecto
	*Abra un terminal para backend
	  Ejecute el comando: node app.js
	*Abra un terminal para client
	  Ejecute el comando: ng serve


