# Examen Android App

## Descripción

La aplicación **Examen Android App** permite a los usuarios registrarse, iniciar sesión y acceder a una pantalla principal que muestra un mensaje de bienvenida. Utiliza **Firebase** para la autenticación de usuarios y gestiona la navegación entre las actividades.

## Funcionalidades

1. **Registro de Usuario**: Los usuarios pueden crear una cuenta proporcionado su nombre, correo electrónico y contraseña.
2. **Inicio de Sesión**: Los usuarios pueden iniciar sesión con sus credenciales (correo electrónico y contraseña).
3. **Pantalla Principal**: Al iniciar sesión con éxito, los usuarios son redirigidos a la pantalla principal, donde verán un mensaje de bienvenida.
4. **Cerrar Sesión**: Los usuarios pueden cerrar sesión desde la pantalla principal y regresar a la pantalla de inicio de sesión.

## Estructura de la Aplicación

La aplicación tiene las siguientes actividades principales:

### 1. **LoginActivity**
- **Propósito**: Es la actividad donde los usuarios pueden iniciar sesión utilizando su correo electrónico y contraseña.
- **Comportamiento**:
  - Si el usuario ya tiene una cuenta, puede ingresar sus credenciales y presionar el botón "Ingresar".
  - Si la autenticación es exitosa, se redirige al usuario a la pantalla principal (MainActivity).
  - Si el inicio de sesión falla, se muestra un mensaje de error.

### 2. **RegistroActivity**
- **Propósito**: Es la actividad para que los nuevos usuarios se registren en la aplicación.
- **Comportamiento**:
  - El usuario debe ingresar su nombre completo, correo electrónico y contraseña.
  - Al completar los campos y presionar el botón "Registrarse", los datos se guardan en Firebase.
  - Si el registro es exitoso, el usuario es redirigido a la pantalla de inicio de sesión (LoginActivity).

### 3. **MainActivity**
- **Propósito**: Esta es la actividad principal que se muestra una vez que el usuario ha iniciado sesión.
- **Comportamiento**:
  - Muestra un mensaje de bienvenida con el correo electrónico del usuario autenticado.
  - Tiene un botón de "Salir" que cierra sesión y redirige al usuario a la pantalla de inicio de sesión (LoginActivity).

## Cómo Funciona

1. **Registro**:
   - El usuario abre la aplicación y se le presenta la pantalla de inicio de sesión (LoginActivity).
   - Si el usuario no tiene cuenta, presiona el enlace para ir a la pantalla de registro (RegistroActivity).
   - Después de completar el formulario de registro, se crea un nuevo usuario en Firebase y se redirige a la pantalla de inicio de sesión.

2. **Inicio de Sesión**:
   - El usuario ingresa su correo electrónico y contraseña en la pantalla de inicio de sesión.
   - Si las credenciales son correctas, Firebase valida el inicio de sesión y se redirige al usuario a la pantalla principal (MainActivity).
   - Si el inicio de sesión falla, se muestra un mensaje de error.

3. **Pantalla Principal**:
   - Una vez autenticado, el usuario es redirigido a MainActivity.
   - En esta pantalla, se muestra un mensaje de bienvenida con el correo electrónico del usuario.
   - El usuario puede presionar el botón "Salir" para cerrar sesión, lo que lo llevará de regreso a la pantalla de inicio de sesión.



