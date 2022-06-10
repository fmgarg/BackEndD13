# Desafío "SERVIDOR CON BALANCE DE CARGAS". 

Este proyecto se encuentra realizado utilizando JS, NodeJS, express, express-handlebars, express-session, passport-local, sockets.io y bootstrap, entre otras.

Utilizando el modulo cluster se intenta balancear la carga del server creando tantos workers como CPUs tenga el servidor donde se ejecuta node.


## Consideraciones generales

El proyecto corresponde al desafío de la clase 28 del curso de Back End en Coderhouse.

El nombre del usuario en los saludos NO esta hardcodeado sino que se obtiene a traves de socket desde una variable pusheada con req.session.user.

Los usuarios son almacenados en la base de datos ecommerce en Mongo Atlas, lo mismo las sesiones.

Las contraseñas se encryptan con la biblioteca bcrypt.

#### `Acerca de mi`

Mi nombre es Francisco González, tengo 42 años y en la actualidad me encuentro estudiando en Coder para ser desarrollador Full Stack. 

Me pueden contactar a través de mi email: [fmgarg@gmail.com](mailto:fmgarg@gmail.com) y/o por whatsapp: +549 11 5412 2848.