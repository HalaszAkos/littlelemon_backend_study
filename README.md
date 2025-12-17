# LittleLemon Backend Study

Django REST Framework project for restaurant management with Menu and Table Booking APIs.

## Features

- **Menu API**: CRUD operations for restaurant menu items
- **Booking API**: Table reservation management with ViewSet
- **User Authentication**: Registration, login, and logout using Djoser
- **Token Authentication**: API authentication with token-based system
- **Browsable API**: Interactive API interface for testing

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/HalaszAkos/littlelemon_backend_study.git
cd littlelemon_backend_study
```

### 2. Create virtual environment
```bash
python -m venv venv
```

### 3. Activate virtual environment

**Windows:**
```bash
venv\Scripts\activate
```

**Mac/Linux:**
```bash
source venv/bin/activate
```

### 4. Install dependencies
```bash
pip install -r requirements.txt
```

### 5. Run migrations
```bash
python manage.py migrate
```

### 6. Create superuser (optional)
```bash
python manage.py createsuperuser
```

### 7. Run development server
```bash
python manage.py runserver
```

## API Endpoints

### Menu API
- `GET/POST /restaurant/menu/` - List all menu items or create new
- `GET/PUT/DELETE /restaurant/menu/<id>` - Retrieve, update or delete menu item

### Booking API
- `GET/POST /restaurant/booking/tables/` - List all bookings or create new
- `GET/PUT/DELETE /restaurant/booking/tables/<id>/` - Retrieve, update or delete booking

### Authentication API
- `POST /auth/users/` - Register new user
- `GET /auth/users/` - List all users
- `POST /auth/token/login/` - Login and get token
- `POST /auth/token/logout/` - Logout and delete token

### Admin
- `/admin/` - Django admin interface

## Testing with Browsable API

Visit `http://127.0.0.1:8000/restaurant/menu/` or any other endpoint in your browser to use Django REST Framework's interactive API interface.

## Database

By default, the project uses SQLite. To use MySQL, uncomment the MySQL configuration in `settings.py` and install mysqlclient:

```bash
pip install mysqlclient
```

## Technologies

- Django 5.2+
- Django REST Framework 3.16+
- Djoser 2.3+ (Authentication)
- SQLite (default) / MySQL (optional)

## License

This is a study project for learning Django REST Framework.
