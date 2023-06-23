## Pasos para instalar el proyecto eCommerce

### PREREQUISITOS:
- Para el manejo de la base de datos - Apache MySQL.
  Descargue XAMPP desde el siguiente enlace: [Descargar XAMPP](https://sourceforge.net/projects/xampp/files/XAMPP%20Windows/8.0.28/xampp-windows-x64-8.0.28-0-VS16-installer.exe/download).

- Para navegar entre versiones de Node.js, instale npm desde el siguiente enlace:
  Descargue el instalador nvm-setup.exe e instálelo desde: [Descargar nvm-setup.exe](https://github.com/coreybutler/nvm-windows/releases).
  Asegúrese de que esté instalado abriendo CMD y ejecutando el siguiente comando:

```
nvm -v
```
Liste las versiones disponibles de Node.js con el siguiente comando:
```
nvm list available
```
Instale la versión 14.20.1 con el siguiente comando:
```
nvm install 14.20.1
```
Para usar la versión ya instalada, ejecute el siguiente comando:
```
nvm use 14.20.1
```
### DEPENDENCIAS:
- Node.js versión 14.20.1.
- Angular a partir de la versión 15.

### INSTALACIÓN DEL PROYECTO:
1. Descargue el proyecto y ábralo con VScode.
2. Navegue hasta la carpeta `nombre-carpeta` y ejecute los siguientes comandos en una terminal:
 ```bash
 cd backend
 npm install
 cd ..
 cd client
 npm install
 ```
1. Cree la base de datos en MySQL:
- Nombre de la base de datos: myapp.
- En la carpeta backend en la raíz del proyecto, encontrará el archivo sql_dump.sql. Ábralo, copie todo el código y péguelo en el apartado de ejecuciones de SQL para crear las tablas en la base de datos myapp.
2. CONFIGURACIONES PARA BD MYSQL:
- Navegue hasta la carpeta backend y vaya a la carpeta database. Abra el archivo db.js y cambie el siguiente código:
```
const connection = mysql.createConnection({
  host: 'localhost',
  user: 'root',
  password: '',
  database: 'myapp',
});
```
3. INICIALIZACIÓN DEL PROYECTO:
- Abra una terminal para el backend y ejecute el siguiente comando:
```
node app.js
```
- Abra otra terminal para el cliente y ejecute el siguiente comando:
```
ng serve
```

