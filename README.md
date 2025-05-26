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

##############################################################################################
API Endpoints
1) Add Flashcard : POST /flashcard/
{
  "student_id": "stu001",
  "question": "What is photosynthesis?",
  "answer": "A process used by plants to convert light into energy"
}
Response:{
  "message": "Flashcard added successfully",
  "subject": "Biology"
}
Get Flashcards
2)GET /get-subject?student_id=stu001&limit=3
Response:[
    {
        "student_id": "stu001",
        "question": "What is an acid-base reaction?",
        "answer": "A chemical reaction that occurs between an acid and a base",
        "subject": "Chemistry"
    },
    {
        "student_id": "stu001",
        "question": "What is photosynthesis?",
        "answer": "Photosynthesis is the process through which plants make food using sunlight.",
        "subject": "Biology"
    },
    {
        "student_id": "stu001",
        "question": "What is Newton's Second Law?",
        "answer": "Force equals mass times acceleration",
        "subject": "Physics"
    },
    {
        "student_id": "stu001",
        "question": "What is the Pythagorean theorem?",
        "answer": "a² + b² = c²",
        "subject": "General"
    }
]
