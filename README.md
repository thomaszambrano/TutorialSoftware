# DjangoTutorials - Online Store

A Django web application built as part of a software architecture course. It implements an online store with product listings, product detail pages, a contact page, and a product creation form connected to a SQLite database.

## Built With

- Python 3
- Django
- Bootstrap 5
- SQLite
- factory_boy (for database seeding)

## Features

- Home, About, and Contact pages
- Product listing page pulling data from the database
- Product detail page with comments section
- Product creation form with validation
- Django Admin panel to manage products and comments

## Project Structure

```
djangocourse/
├── helloworld_project/    # Django project settings and main URLs
├── pages/                 # Main app
│   ├── models.py          # Product and Comment models
│   ├── views.py           # All views
│   ├── urls.py            # App routes
│   ├── factories.py       # Faker factories for seeding
│   ├── admin.py           # Admin panel registration
│   ├── management/
│   │   └── commands/
│   │       └── seed_products.py  # DB seeder command
│   ├── static/pages/
│   │   └── app.css
│   └── templates/
│       ├── pages/         # Home, About, Contact, Base layout
│       └── products/      # Index, Show, Create, Created templates
└── manage.py
```

## Setup & Installation

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/DjangoTutorials.git
cd DjangoTutorials
```

**2. Create and activate a virtual environment**
```bash
python3 -m venv .venv
source .venv/bin/activate        # Mac/Linux
.venv\Scripts\activate           # Windows
```

**3. Install dependencies**
```bash
pip install django factory_boy
```

**4. Run migrations**
```bash
python manage.py makemigrations
python manage.py migrate
```

**5. Seed the database**
```bash
python manage.py seed_products
```

**6. Create an admin user (optional)**
```bash
python manage.py createsuperuser
```

**7. Run the server**
```bash
python manage.py runserver
```

Then open http://127.0.0.1:8000/ in your browser.

## Available Routes

| URL | Description |
|-----|-------------|
| `/` | Home page |
| `/about/` | About page |
| `/contact/` | Contact page |
| `/products/` | List of all products |
| `/products/<id>` | Product detail with comments |
| `/products/create` | Create a new product |
| `/admin/` | Django admin panel |

## Author

Developed by: Your Name  
Course: Software Architecture - EAFIT
