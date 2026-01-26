# PyShop - E-Commerce Product Catalog

A modern, full-stack Django web application showcasing an e-commerce product catalog with promotional offer management. Built to demonstrate software engineering best practices in Python web development.

## 🎯 Project Overview

PyShop is a lightweight yet feature-rich e-commerce platform that provides:
- **Product Management**: Browse and display products with pricing and inventory tracking
- **Offer System**: Create and manage promotional discount codes
- **Admin Dashboard**: Full CRUD operations via Django's intuitive admin interface
- **Responsive UI**: Bootstrap-powered responsive design for all device sizes

## 🛠 Tech Stack

| Layer | Technology |
|-------|-----------|
| **Backend** | Django 5.0.6 |
| **Database** | SQLite3 |
| **Frontend** | HTML5, Bootstrap 5.0.2 |
| **Language** | Python 3.x |
| **ORM** | Django ORM |

## ✨ Key Features

### Products Module
- **Product Model**: Store product information including name, price, stock quantity, and product images
- **Inventory Management**: Track real-time stock levels
- **Price Management**: Flexible pricing system with floating-point precision

### Offers Module
- **Discount Codes**: Create promotional codes with customizable discount percentages
- **Offer Descriptions**: Detailed offer information for marketing purposes
- **Admin Integration**: Manage offers directly through the Django admin panel

### Admin Interface
- Custom admin configuration for products and offers
- List display columns optimized for quick viewing (name, price, stock for products; code, discount for offers)
- Full CRUD operations through Django's built-in admin

## 📁 Project Structure

```
pyshop/
├── manage.py                 # Django management CLI
├── db.sqlite3               # SQLite database
├── README.md                # Project documentation
│
├── pyshop/                  # Main project configuration
│   ├── settings.py          # Django settings and configuration
│   ├── urls.py              # Project-level URL routing
│   ├── asgi.py              # ASGI configuration for deployment
│   └── wsgi.py              # WSGI configuration for deployment
│
├── products/                # Products application (Django app)
│   ├── models.py            # Product and Offer models
│   ├── views.py             # View handlers and business logic
│   ├── urls.py              # App-level URL routing
│   ├── admin.py             # Admin interface configuration
│   ├── apps.py              # App configuration
│   ├── tests.py             # Unit tests
│   ├── migrations/          # Database migration files
│   └── templates/           # HTML templates for products app
│       └── index.html       # Product listing page
│
└── templates/               # Project-level templates
    └── base.html            # Base template with Bootstrap setup
```

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd pyshop
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install django
   ```

4. **Run migrations**
   ```bash
   python manage.py migrate
   ```

5. **Create a superuser (admin account)**
   ```bash
   python manage.py createsuperuser
   ```

6. **Start the development server**
   ```bash
   python manage.py runserver
   ```

7. **Access the application**
   - Application: `http://localhost:8000/products/`
   - Admin Panel: `http://localhost:8000/admin/`

## 📋 API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/products/` | GET | Display all products |
| `/products/new/` | GET | New product placeholder (extensible) |
| `/admin/` | GET/POST | Admin dashboard |

## 🗄 Database Schema

### Products Table
```
id (PK) | name | price | stock | image_url
```

### Offers Table
```
id (PK) | code | description | discount
```

## 💡 Architecture Highlights

- **Separation of Concerns**: Clear separation between models, views, and templates
- **Django Best Practices**: Follows Django conventions for app structure and configuration
- **Scalability**: Modular app design allows easy addition of new features
- **Admin-Driven Development**: Leverages Django admin for rapid development
- **Database Migrations**: Version-controlled database schema through migrations

## 🔮 Future Enhancements

- [ ] User authentication and shopping cart functionality
- [ ] Product search and filtering capabilities
- [ ] Advanced offer management with expiration dates
- [ ] Order processing and payment integration
- [ ] Product reviews and ratings system
- [ ] Email notifications for promotions
- [ ] REST API using Django REST Framework
- [ ] Unit and integration test coverage
- [ ] Docker containerization for deployment
- [ ] CI/CD pipeline integration

## 📝 Development Notes

### Running Tests
```bash
python manage.py test
```

### Creating New Migrations
```bash
python manage.py makemigrations
```

### Accessing Django Shell
```bash
python manage.py shell
```

## 🔐 Security Considerations

- **DEBUG Mode**: Currently enabled for development. Disable in production.
- **SECRET_KEY**: Should be stored as environment variable in production
- **ALLOWED_HOSTS**: Configure appropriately for deployment
- **CSRF Protection**: Enabled by default

## 📚 Learning Resources

- [Django Official Documentation](https://docs.djangoproject.com/)
- [Django Best Practices](https://docs.djangoproject.com/en/5.0/topics/http/)
- [Bootstrap Documentation](https://getbootstrap.com/docs/5.0/)

## 📄 License

This project is provided as-is for educational and portfolio purposes.

---
