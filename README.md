# Laravel Livewire Application

A modern web application built with **Laravel 13.15**, **Livewire 4.3**, and **Filament 5.6**. This project includes a complete admin panel, interactive components, and a responsive design with Tailwind CSS.

## 🚀 What Has Been Set Up

Your project is freshly installed with all core frameworks ready to use:

- ✅ **Laravel 13.15** - PHP web framework
- ✅ **Livewire 4.3** - Full-stack reactive components (like React but in PHP)
- ✅ **Filament 5.6** - Admin panel and form builder
- ✅ **Tailwind CSS 4** - Utility-first CSS framework
- ✅ **Vite** - Lightning-fast frontend build tool
- ✅ **MySQL Database** - With default User migrations

## 📋 Technology Stack

| Component | Version | Purpose |
|-----------|---------|---------|
| PHP | 8.3+ | Server-side language |
| Laravel | 13.15 | Web framework |
| Livewire | 4.3 | Reactive components without JavaScript |
| Filament | 5.6 | Admin panel & UI components |
| Tailwind CSS | 4 | CSS styling |
| Vite | 8 | Frontend build tool |
| MySQL | - | Database |
| NPM | - | Frontend dependencies |

## 📁 Project Structure

```
livewireapp/
├── app/
│   ├── Http/
│   │   └── Controllers/          # API & web controllers
│   ├── Models/
│   │   └── User.php              # User model
│   └── Providers/
│       └── AppServiceProvider.php # Service configuration
├── config/
│   ├── app.php                   # Application config
│   ├── database.php              # Database config
│   └── ...                       # Other configs
├── database/
│   ├── migrations/               # Database migrations
│   ├── seeders/                  # Database seeders
│   └── factories/                # Model factories for testing
├── resources/
│   ├── views/                    # Blade templates
│   ├── css/                      # Stylesheets
│   └── js/                       # JavaScript files
├── routes/
│   ├── web.php                   # Web routes
│   └── console.php               # Console commands
├── storage/                      # Files, logs, cache
├── tests/                        # PHPUnit tests
├── public/                       # Public assets
├── bootstrap/                    # Framework bootstrap
└── vendor/                       # Composer packages
```

## ⚙️ Installation & Setup

### Step 1: Install Dependencies

```bash
composer install
npm install
```

### Step 2: Setup Environment File

```bash
# Copy example env file
cp .env.example .env

# Generate application key
php artisan key:generate
```

### Step 3: Database Setup

1. **Create Database**: Open your MySQL client and run:
   ```sql
   CREATE DATABASE laravelapp;
   ```

2. **Update .env file** (if needed):
   ```
   DB_DATABASE=laravelapp
   DB_USERNAME=root
   DB_PASSWORD=your_password
   ```

3. **Run Migrations**:
   ```bash
   php artisan migrate
   ```

### Step 4: Build Frontend

```bash
npm run build
```

## 🎯 Running the Application

### Development Mode (Recommended)

Run everything together with one command:

```bash
composer run dev
```

This will start:
- 🔵 **Laravel Server** (http://localhost:8000)
- 🔄 **Queue Listener** (background jobs)
- 📊 **Log Viewer** (real-time logs)
- ⚡ **Vite Dev Server** (hot reload for CSS/JS)

### Manual Development

If you prefer to run services separately:

```bash
# Terminal 1 - Laravel Server
php artisan serve

# Terminal 2 - Frontend build (watches for changes)
npm run dev

# Terminal 3 (Optional) - Queue listener
php artisan queue:listen

# Terminal 4 (Optional) - Real-time logs
php artisan pail
```

### Production Build

```bash
npm run build
```

## 📝 Common Commands

### Artisan Commands (Laravel)

```bash
# Create a new controller
php artisan make:controller YourControllerName

# Create a new model
php artisan make:model YourModelName -m

# Create a new migration
php artisan make:migration create_table_name

# Create a Livewire component
php artisan livewire:create YourComponentName

# Create a Filament resource (admin panel)
php artisan make:filament-resource YourResourceName

# Run database migrations
php artisan migrate

# Reset database (fresh start)
php artisan migrate:fresh --seed

# Tinker (interactive PHP shell)
php artisan tinker

# Run tests
npm run test
```

### NPM Commands (Frontend)

```bash
# Development build (with hot reload)
npm run dev

# Production build
npm run build
```

## 🔐 Key Features

### Livewire Components
- Create interactive UI without writing JavaScript
- Real-time validation and updates
- Easy event handling

**Example:** Create a search component, form, or real-time counter - all with PHP!

### Filament Admin Panel
- Beautiful admin interface (at `/admin`)
- Create/Read/Update/Delete (CRUD) for models
- User authentication included
- Customizable forms and tables

### Database
- **Users table** - Already created
- **Cache table** - For caching
- **Jobs table** - For background jobs

## 🚀 Next Steps to Build Your Project

1. **Create Models** - Define your data structure:
   ```bash
   php artisan make:model Product -m
   ```

2. **Create Migrations** - Build your database tables:
   ```bash
   php artisan make:migration create_products_table
   ```

3. **Create Controllers** - Handle business logic:
   ```bash
   php artisan make:controller ProductController
   ```

4. **Create Livewire Components** - Build interactive UI:
   ```bash
   php artisan livewire:create product-search
   ```

5. **Create Filament Resources** - Add admin panel features:
   ```bash
   php artisan make:filament-resource Product
   ```

6. **Build Routes** - Add endpoints in `routes/web.php`

7. **Create Views** - Build your templates in `resources/views/`

## 📚 Documentation Links

- [Laravel Documentation](https://laravel.com/docs)
- [Livewire Documentation](https://livewire.laravel.com/docs)
- [Filament Documentation](https://filamentphp.com/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 🛠️ Troubleshooting

### Server won't start?
```bash
# Clear cache and config
php artisan cache:clear
php artisan config:clear
php artisan optimize

# Then start again
php artisan serve
```

### Database connection error?
- Check `.env` file for correct database credentials
- Ensure MySQL is running
- Run `php artisan migrate`

### Frontend not updating?
```bash
# Stop npm dev and restart
npm run dev
```

## 📖 Git Commits History

Your project has been set up with these commits:
1. ✅ Freshly installed Laravel 13.15.0
2. ✅ Installed Livewire v4.3

You're now ready to start building your features!

## 🎓 Quick Tutorial Example

Here's how to create your first feature (e.g., Todo app):

```bash
# 1. Create model
php artisan make:model Todo -m

# 2. Edit migration (database/migrations/...)
# Add: $table->string('title'); $table->boolean('completed')->default(false);

# 3. Create Livewire component
php artisan livewire:create todo-list

# 4. Add route in routes/web.php
# Route::get('/todos', \App\Livewire\TodoList::class);

# 5. Run migration
php artisan migrate

# Done! Your feature is ready to use
```

## 📞 Need Help?

- Check the documentation links above
- Use `php artisan tinker` to test code interactively
- Check logs in `storage/logs/`
- Run tests: `php artisan test`

---

**Happy Coding! 🎉**

This project is ready for development. Start building your features using the commands above!
