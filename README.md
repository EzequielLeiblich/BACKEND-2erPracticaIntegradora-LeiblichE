# 2da Práctica de integración sobre proyecto final

## LEIBLICH Ezequiel Gaston

## Comisión 43345 - Programación Backend

Este repositorio contiene la práctica de integración sobre el proyecto de ecommerce en el cual se han configurado los siguientes elementos:

## Modelo de Usuario

Se ha creado un nuevo modelo llamado "User", que cuenta con los siguientes campos:

> first_name: String
> 
> last_name: String
> 
> email: String (único)
> 
> age: Number
> 
> password: String (Hash)
> 
> cart: ID con referencia a Carts
> 
> role: String (default: 'user')
> 

## Passport Strategies
Se han desarrollado las estrategias necesarias de Passport para que funcionen correctamente con el nuevo modelo de usuarios. Esto permite gestionar la autenticación de usuarios de manera segura y eficiente.

## Sistema de Login
El sistema de login del usuario ha sido modificado para ofrecer dos opciones de autenticación: mediante sesiones o mediante JSON Web Tokens (JWT), según tu elección.

## JWT Authentication
La autenticación con JWT, se ha desarrollado una estrategia llamada "current" que permite extraer la cookie que contiene el token para obtener el usuario asociado a dicho token. En el token válido, se devolverá el usuario asociado al mismo; de lo contrario, se devolverá un error de Passport. Se ha utilizado un extractor de cookie para facilitar este proceso.

## Ruta /api/sessions/
Se ha agregado la ruta /current al router de sesiones (sessions) para proporcionar una manera de obtener el usuario actualmente autenticado. Esta ruta utilizará el modelo de sesión que estés utilizando (sesiones tradicionales o JWT) para devolver en la respuesta el usuario actual.

¡Gracias por revisar este proyecto de integración en el ecommerce! Si tienes alguna pregunta o comentario, no dudes en hacerlo.
