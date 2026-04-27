# 📦 Laboratorio #2 — CRUD Rápido con Laravel

> **Guía práctica** para la implementación de un CRUD completo en Laravel utilizando el generador automático de código `ibex/crud-generator`.

---

## 📋 Descripción del Laboratorio

En este laboratorio se desarrolló un sistema CRUD (Create, Read, Update, Delete) sobre una tabla de productos (`products`) utilizando el framework **Laravel**. El proceso incluyó:

1. **Creación del proyecto** Laravel desde cero en el entorno WAMP.
2. **Configuración de variables de entorno** (archivo `.env`) con las credenciales de la base de datos.
3. **Corrección de errores típicos** relacionados con la longitud de cadena en migraciones, configurando `Schema::defaultStringLength(191)` en el método `boot()` del `AppServiceProvider`.
4. **Generación del modelo `Product`** junto con su migración correspondiente, definiendo los campos: `id`, `description` (string), `price` (double 8,2), `stock` (integer) y `timestamps`.
5. **Ejecución de las migraciones** para crear las tablas en la base de datos.
6. **Instalación del paquete generador de CRUD** `ibex/crud-generator`, que permite generar automáticamente controladores, vistas, modelos, migraciones y rutas.
7. **Publicación de los archivos del proveedor** del paquete y **generación automática del CRUD** para la tabla `products`.
8. **Registro de rutas RESTful** usando `Route::resource('products', ProductController::class)`, que crea automáticamente todas las rutas CRUD (index, create, store, show, edit, update, destroy).
9. **Configuración del frontend** con Laravel UI y Bootstrap, resolviendo errores relacionados con Vite y los archivos SASS.
10. **Uso de `$fillable`** en el modelo para proteger contra vulnerabilidades de asignación masiva, especificando únicamente los campos permitidos: `description`, `price` y `stock`.

---

## ⚙️ Comandos Principales Ejecutados

### 1️⃣ `composer require ibex/crud-generator --dev`

Instala el paquete generador de CRUD como dependencia de desarrollo. Esta herramienta permite generar automáticamente **controladores, vistas, modelos, migraciones y rutas** a partir del nombre de una tabla existente en la base de datos, ahorrando tiempo considerable en la construcción del CRUD.

```bash
composer require ibex/crud-generator --dev
```

---

### 2️⃣ `php artisan vendor:publish --tag=crud`

Publica los archivos de configuración y recursos del paquete `ibex/crud-generator` dentro del proyecto. Esto copia plantillas, vistas y archivos de configuración desde la carpeta `vendor/` hacia las carpetas de la aplicación (`config/`, `resources/`, etc.), permitiendo personalizar el comportamiento del generador.

```bash
php artisan vendor:publish --tag=crud
```

---

### 3️⃣ `php artisan make:crud products`

Genera automáticamente todos los archivos necesarios para el CRUD de la tabla `products`: el controlador con todos los métodos (index, create, store, show, edit, update, destroy), las vistas Blade correspondientes y las rutas. El parámetro `products` hace referencia al nombre de la tabla en la base de datos.

```bash
php artisan make:crud products
```

---

## 📸 Capturas de Funcionamiento

### Registro de Usuario

> _Inserta aquí una captura de pantalla del formulario de registro de usuario._

```

```

---

### Sección de Products

> _Inserta aquí una captura de pantalla del listado de productos (ruta `/products`)._

```
[ Captura #2 — Vista Index de Products ]
```

---

### Agregando un Producto

> _Inserta aquí una captura de pantalla del formulario para agregar un nuevo producto._

```
[ Captura #3 — Formulario Create Product ]
```

---

<br><br>

---

*Johanns Garcés — Cédula: 8-1000-355*
