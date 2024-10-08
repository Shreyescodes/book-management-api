# Django Book Management API

A simple RESTful API built with Django REST Framework for managing a book collection. This project demonstrates basic CRUD operations and REST API concepts.

## Features

- Full CRUD functionality for books
- RESTful API endpoints
- JSON data format
- Built with Django REST Framework

## Prerequisites

- Python 3.8+
- Django 4.0+
- Django REST Framework

## Installation

1. Clone the repository
```bash
git clone https://github.com/Shreyescodes/django-book-api.git
cd django-book-api
```

2. Create and activate virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install django djangorestframework
```

4. Run migrations
```bash
python manage.py makemigrations
python manage.py migrate
```

5. Start the development server
```bash
python manage.py runserver
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/books/` | List all books |
| POST | `/api/books/` | Create a new book |
| GET | `/api/books/{id}/` | Retrieve a book |
| PUT | `/api/books/{id}/` | Update a book |
| DELETE | `/api/books/{id}/` | Delete a book |

## Usage Example

Creating a new book:
```bash
curl -X POST http://localhost:8000/api/books/ \
    -H "Content-Type: application/json" \
    -d '{
        "title": "Django for Beginners",
        "author": "John Doe",
        "description": "A comprehensive guide to Django",
        "price": "29.99"
    }'
```

## Project Structure
```
bookstore/
├── books/
│   ├── models.py      # Book model
│   ├── serializers.py # Book serializer
│   └── views.py       # BookViewSet
├── bookstore/
│   ├── settings.py    # Project settings
│   └── urls.py        # URL configurations
└── manage.py
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
