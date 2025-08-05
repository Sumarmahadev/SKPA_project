"# My Project" 

#  SKPA Internship API Project

This project implements REST APIs for two forms used in railway bogie maintenance:

1. **Bogie Checksheet**
2. **Wheel Specification**
Built using **Django**, **Django REST Framework**, **PostgreSQL**,and ** Api Tested by Postman**.


## Tech Stack used 

- **Backend**: Django 5.x, Django REST Framework
- **Database**: PostgreSQL
- **Tools**: Postman (for API testing)
- **Language**: Python 3.x

---
## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Sumarmahadev/SKPA_project.git
cd SKPA_project

### 2️⃣ **Create Virtual Environment & Install Dependencies**
```bash
python -m venv venv
venv\Scripts\activate      # Windows
# OR
source venv/bin/activate   # macOS/Linux

pip install -r requirements.txt

2)Configure PostgreSQL Database
Open SKPA_project/settings.py and update with your database details:

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': '<your_db_name>',
        'USER': '<your_db_user>',
        'PASSWORD': '<your_db_password>',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
 # user,port ,PASSWORD etc are added in main project 

4️) Apply Migrations
 #by this we get one Migrations inside our SKPA_APP it maintenance the database table releted things like it create database model wrire postgresql query ... we get these  after running  or executeing bellow command

python manage.py makemigrations
python manage.pt migrate


5)**Create Superuser
# by this we get the web besed user interface for admin .so by using this admin can do curd opertions, that's the main advantage of django
to create this we have to run the bellow command

python manage.py createsuperuser 






## API Reference

#### 1) Create a Bogie Checksheet

These two are first api end point to get and post 
| Method | Endpoint                            | Description                |
| ------ | ----------------------------------- | -------------------------- |
| POST   | `/api/forms/bogie-checksheet/`      | Create a new bogie record  |
| GET    | `/api/forms/bogie-checksheet/list/` | Retrieve all bogie records |


sample Post body:
{
  "formNumber": "BOGIE-2025-001",
  "submittedBy": "engineer_01",
  "submittedDate": "2025-07-30",
  "adjustingTube": "DAMAGED",
  "cylinderBody": "WORN OUT",
  "pistonTrunnion": "GOOD",
  "plungerSpring": "OK",
  "axleGuide": "CRACKED",
  "bogieFrameCondition": "REPAIRED",
  "bolster": "REPLACED",
  "bolsterSuspensionBracket": "GOOD"
}


## 2) Wheel Specification  
#This one is 2nd api end point 
| Method |Endpoint                                | Description
| POST   | `/api/forms/wheel-specifications/`      | Create a new wheel record  |
| GET    | `/api/forms/wheel-specifications/list/` | Retrieve all wheel records |


## sample post body

{
  "formNumber": "WHEEL-2025-001",
  "submittedBy": "technician_01",
  "submittedDate": "2025-08-01",
  "condemningDia": "95 mm",
  "lastShopIssueSize": "96 mm",
  "treadDiameterNew": "100 mm",
  "wheelGauge": "1676 mm"
}

## **Testing with Postman**
#Open Postman.
-----------------

Create a new request (POST or GET).
Enter the API URL (e.g., http://127.0.0.1:8000/api/forms/bogie-checksheet/).


#For POST requests:
-------------------
Go to Body → select raw → choose JSON.
Paste one of the sample request bodies above.
Click Send.
Expected responses:
201 Created → Data saved successfully
200 OK → Data retrieved successfully

##after this we check data on Postman by Get method,we can verfiy data admin and in database
## Demo

Insert gif or link to demo


## Authors
Name: Sumar chimacode
Role: Backend Developer (Internship Assignment)
Email:sumarchimacode@gmail.com

GitHub:-https://github.com/Sumarmahadev/SKPA_project

GitHub: Sumarmahadev


