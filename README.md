# Desafío "SERVIDOR CON BALANCE DE CARGAS". 

Este proyecto se encuentra realizado utilizando JS, NodeJS, express, express-handlebars, express-session, passport-local, sockets.io y bootstrap, entre otras.

Utilizando el modulo cluster se intenta balancear la carga del server creando tantos workers como CPUs tenga el servidor donde se ejecuta node.


## Consideraciones generales

El proyecto corresponde al desafío de la clase 30 del curso de Back End en Coderhouse.

## Primera consigna. Ejecutar forkear el servidor o ejecutarlo en modo CLUSTER.

Se usó minimist. El comando para seleccionar el modo CLUSTER del server.js es: 
node server --puerto 8081 --modo CLUSTER
Si no se le pasa el parámetro inicia en puerto 8080 y modo FORK por default.

En localhost:PUERTO/info se accede a una vista con la informacion solicitada.

Con NODEMON el comando para iniciar en modo CLUSTER es: 
nodemon server --puerto 8081 --modo CLUSTER

Con FOREVER el comando para iniciar en modo CLUSTER es: 
forever server.js --puerto 8081 --modo CLUSTER
forever list MUESTRA LOS PROCESOS ACTIVOS
forever stopall DETIENE LOS PROCESOS ACTIVOS, TAMBIEN HAY QUE CERRAR LAS VENTANAS DE NODE

Desde la consola se verifican los procesos de node.exe activos con el comando:
tasklist /fi "imagename eq node.exe"

Con PM2 para iniciar en modo fork se ejecuta el siguiente comando:
pm2 start server.js --name="server" --watch
detenemos con:
pm2 stop all

Para iniciar en modo cluster usamos:
pm2 start server.js --name="server" --watch -i max
detenemos con:
pm2 stop all

Con NGINX
node server --puerto 8081 --modo CLUSTER
node server --puerto 8080
inicio ngins.exe
Puedo acceder a ambos servidores/ puertos desde localhost:80/info o /randoms

Luego levanto 4 server modo fork para servir a las peticiones:
pm2 start server.js --name="server8082" --watch -- fork 8082
pm2 start server.js --name="server8083" --watch -- fork 8083
pm2 start server.js --name="server8084" --watch -- fork 8084
pm2 start server.js --name="server8085" --watch -- fork 8085

Finalizo y vuelvo a levantar nginx.exe

Compruebo que puedo ingresar a las distintas rutas.








#### `Acerca de mi`

Mi nombre es Francisco González, tengo 42 años y en la actualidad me encuentro estudiando en Coder para ser desarrollador Full Stack. 

Me pueden contactar a través de mi email: [fmgarg@gmail.com](mailto:fmgarg@gmail.com) y/o por whatsapp: +549 11 5412 2848.