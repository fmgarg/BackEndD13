# Desafío "Usando el objeto PROCESS". 

Este proyecto se encuentra realizado utilizando JS, NodeJS, express, express-handlebars, express-session, passport-local, sockets.io y bootstrap, entre otras.

Al ingresar a la ruta localhost:8080/login te vas a encontrar con el formulario de login y la opción de registrarte.
Al ingresar se accede a la ruta '/home' donde se encuentran las vistas del socket de  productos y mensajes. 
Se puede ver el nombre del user en el margen superior de la pagina junto a un boton de logout. Desde ahí se pueden agregar productos y mensajes en el chat.

Si se agota la sesión la página se recarga (usando window.location.reload del lado del front) y vuelve al login.

Si el user hace un logout es redirigido a la ruta del login.

## Consideraciones generales

El proyecto corresponde al desafío de la clase 28 del curso de Back End en Coderhouse.

El nombre del usuario en los saludos NO esta hardcodeado sino que se obtiene a traves de socket desde una variable pusheada con req.session.user.

Los usuarios son almacenados en la base de datos ecommerce en Mongo Atlas, lo mismo las sesiones.

Las contraseñas se encryptan con la biblioteca bcrypt.

#### `Acerca de mi`

Mi nombre es Francisco González, tengo 42 años y en la actualidad me encuentro estudiando en Coder para ser desarrollador Full Stack. 

Me pueden contactar a través de mi email: [fmgarg@gmail.com](mailto:fmgarg@gmail.com) y/o por whatsapp: +549 11 5412 2848.