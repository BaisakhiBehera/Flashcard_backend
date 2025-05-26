#  Smart Flashcard Backend API

This is a Django REST Framework (DRF) project for a Smart Flashcard System. Users can add flashcards with questions and answers. The system automatically infers the subject based on keywords. Later, users can fetch flashcards grouped across different subjects.

---

## 🚀 Features

- Add flashcards with automatic subject classification (rule-based).
- Fetch a mix of flashcards from different subjects.
- API supports multiple students (`student_id`).
- Built with Django, DRF, and MySQL.

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/BaisakhiBehera/Flashcard_backend.git
cd Flashcard_backend

2. Create Virtual Environment

python -m venv venv
source venv/bin/activate    # macOS/Linux
venv\Scripts\activate

3. Install Dependencies
pip install -r requirements.txt

⚙️ Database Setup (MySQL)
1.Create a MySQL database (e.g., flashcard_db).

2.In settings.py, update:DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'flashcard_db',
        'USER': 'your_mysql_username',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
3. Apply migrations


🏃 Running the Server : python manage.py runserver
