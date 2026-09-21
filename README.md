# Nuvora — Tienda de Ropa Online (actividad de clase)

Proyecto educativo de la asignatura **Media Técnica en Mantenimiento de Bases de Datos**,
Institución Educativa Fundadores. Docente: **William Álvarez**.

Tienda de ropa online conectada a **Firebase** (Firestore + Authentication + Hosting).

## Estructura

- `index.html` — vitrina pública: muestra los productos guardados en Firestore, con filtro por categoría.
- `admin.html` — panel de administrador: login con Firebase Authentication y formulario para agregar, editar y eliminar productos. Las imágenes se guardan como texto (base64) directamente en Firestore, así el proyecto funciona 100% en el plan gratuito **Spark** sin necesitar Firebase Storage.
- `firebase-config.js` — configuración de conexión al proyecto Firebase.
- `styles.css` — estilos de toda la tienda.
- `firestore.rules` — reglas de seguridad: cualquiera puede leer productos, solo un usuario autenticado puede escribir.

## Cómo correrlo localmente

```bash
firebase serve
```

## Cómo desplegarlo

```bash
firebase deploy
```

## Crear el usuario administrador

En Firebase Console → Authentication → Sign-in method, habilita **Correo electrónico/contraseña**,
y en la pestaña **Users** crea el usuario que usará el profesor o el estudiante para entrar a `admin.html`.
