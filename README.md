Proyecto Final Ecommerce
## Roles:
* "ADMIN"
* "CLIENTE"

## Descripcion:
EL usuario con rol "ADMIN" esta creado en base de datos con las siguientes credenciales:
* usuario: "administrador@gmail.com"
* password: "123456789"

Se hizo desploy HEROKU url: https://app-carrito-ecommerce.herokuapp.com/

Para realizar pruebas locales se puede importar este archivo en Postman 'Api-Proyecto-Final'

Endpoints

## Rol ADMIN:

Recurso: /api/info
Descripción: Informacion solicitada, credenciales para verificar el envio de email con Ethereal Email.
Método: GET

Recurso: /api/productos/:id?
Descripción: Obtener producto/s.
Método: GET


Recurso: /api/productos/
Descripción: Crear producto/s
Método: POST

Recurso: /api/productos/:id
Descripción: Actualizar producto.
Método: PUT

Recurso: /api/productos/:id
Descripción: Eliminar producto.
Método: DELETE

## Rol CLIENTE:

Recurso: /api/users
Descripción: Crear usuario - con rol "CLIENTE" se notificara con envio de email su respuesta y confirmacion de registro.
Método: POST

Recurso: /api/auth/login
Descripción: Login para tener session y acceso POST-"/api/auth/login" con su correspondiente usuario y password
Método: POST

Recurso: /api/auth/logout
Descripción: Permite salir session.
Método: GET

Recurso: /api/users/:id
Descripción: Actualizar usuario.
Método: PUT

Recurso: /api/users
Descripción: Obtener informacion de usuario
Método: GET

Recurso: /api/productos/:id?
Descripción: Obtener producto/s.
Método: GET

Recurso: /api/productos/categoria/:categoria
Descripción: Obtener categoria.
Método: GET

Recurso: /api/carrito
Descripción: Crear carrito
Método: POST

Recurso: /api/carrito/:id
Descripción: Eliminar carrito
Método: DELETE

Recurso: /api/carrito/:id_carrito/productos
Descripción: listar todos los productos del carrito
Método: GET

Recurso: /api/carrito/:id/productos
Descripción: Agregar producto/s
Método: POST

Recurso: /api/carrito/:id/productos/:id_prod
Descripción: Eliminar producto del carrito
Método: DELETE

## Ordenes
Luego de tener carrito con productos viene crear la orden POST-"/api/orden" donde atomaticamente enviar un email con el detalle de la compra y se borra el carrito.
Obtener ordenes segun el usuario GET-"/api/orden"

## Mensajes:
Crear mensajes POST-"/api/chats" segun el usuario en session se guarda el tipo de mensaje si es "sistema" (ADMIN) o "usuario" (CLIENTE).
Para obtener los mensajes segun el usuario es GET-"/api/chats/:email_usuario"