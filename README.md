<h1 align="center">Laravel Commands</h1>

<p align="center">
  <a href="https://laravel.com" target="_blank">
    <img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="280" alt="Laravel Logo">
  </a>
</p>

En Laravel 12, los comandos de Artisan se agrupan por funcionalidades. Acá te dejo un listado general (no exhaustivo pero bastante completo) de los comandos más comunes. Podés correr `php artisan list` para ver todos los disponibles en tu proyecto, ya que algunos dependen de los *packages* instalados.

## 🤖 **Comandos**

---

### 🔧 **Migrations y Seeds**

```bash
php artisan migrate
php artisan migrate:rollback
php artisan migrate:reset
php artisan migrate:refresh
php artisan migrate:fresh
php artisan migrate:fresh --seed
php artisan db:seed
php artisan db:seed --class=NombreSeeder
php artisan schema:dump
```

---

### 🎨 **Make (Generadores de clases)**

```bash
php artisan make:model Nombre
php artisan make:model Nombre -m     # con migration
php artisan make:model Nombre -mc    # con migration + controller
php artisan make:migration create_users_table
php artisan make:controller NombreController
php artisan make:controller NombreController --resource
php artisan make:seeder NombreSeeder
php artisan make:factory NombreFactory
php artisan make:request StoreNombreRequest
php artisan make:middleware NombreMiddleware
php artisan make:command NombreCommand
php artisan make:event NombreEvent
php artisan make:listener NombreListener
php artisan make:job NombreJob
php artisan make:notification NombreNotification
php artisan make:policy NombrePolicy
php artisan make:rule NombreRule
php artisan make:observer NombreObserver
php artisan make:mail NombreMail
php artisan make:resource NombreResource
```

---

### 🚀 **Serve / Cache / Configuración**

```bash
php artisan serve
php artisan config:cache
php artisan config:clear
php artisan route:cache
php artisan route:clear
php artisan view:cache
php artisan view:clear
php artisan optimize
php artisan optimize:clear
php artisan clear-compiled
```

---

### 🛠️ **Routes, Controllers y Requests**

```bash
php artisan route:list
php artisan route:clear
php artisan route:cache
php artisan make:controller Api/TestController
php artisan make:request StoreTestRequest
```

---

### 🧪 **Testing**

```bash
php artisan test
php artisan test --filter=NombreTest
```

---

### 🔐 **Autenticación / Usuarios (si usás Laravel Breeze o Jetstream, por ejemplo)**

```bash
php artisan make:auth          # si estás en Laravel 6-7 (obsoleto en 12)
php artisan breeze:install
php artisan jetstream:install livewire
php artisan jetstream:install inertia
```

---

### 📦 **Queues / Jobs**

```bash
php artisan queue:work
php artisan queue:listen
php artisan queue:restart
php artisan queue:failed
php artisan queue:retry
php artisan queue:flush
```

---

### 🧰 **Storage / Filesystem**

```bash
php artisan storage:link
```

---

### 🧩 **Otros útiles**

```bash
php artisan tinker
php artisan schedule:run
php artisan down         # modo mantenimiento
php artisan up           # salir de mantenimiento
php artisan env          # muestra el entorno actual
php artisan about        # muestra info del sistema
```

## 🚩 **Commands with Flags**

### ⚙️ **Modelos (`make:model`)**

```bash
php artisan make:model NombreModelo                   # Crea un modelo básico.
php artisan make:model NombreModelo -m                # Crea modelo y su migration.
php artisan make:model NombreModelo -c                # Crea modelo y un controlador básico.
php artisan make:model NombreModelo -r -c             # Crea modelo y un controlador resource (CRUD).
php artisan make:model NombreModelo -f                # Crea modelo y factory.
php artisan make:model NombreModelo -s                # Crea modelo y seeder.
php artisan make:model NombreModelo --all             # Crea modelo, migration, factory, seeder, controlador resource todo junto.
```

### 📄 **Requests (make:request)**

```bash
php artisan make:request NombreRequest                 # Crea una clase para validar datos de requests HTTP.
```

### 📁 **Controladores (make:controller)**

```bash
php artisan make:controller NombreController                            # Crea un controlador básico sin métodos.
php artisan make:controller NombreController --resource                 # Crea controlador con métodos CRUD: index, create, store, show, edit, update, destroy.
php artisan make:controller NombreController --api                      # Crea controlador con métodos API (sin create ni edit).
php artisan make:controller NombreController --invokable                # Crea controlador con un único método __invoke().
php artisan make:controller NombreController --resource --model=Modelo  # Controlador CRUD vinculado a un modelo.
```

### 📦 **Recursos API (make:resource)**

```bash
php artisan make:resource NombreResource                # Crea un recurso para transformar un modelo.
php artisan make:resource NombreResource --collection   # Crea un recurso para transformar una colección.
```
