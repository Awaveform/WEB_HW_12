# WEB_HW_12

docker run --name contacts-postgres -p 5432:5432 -e POSTGRES_PASSWORD=567234 -d postgres

pip install alembic SQLAlchemy
alembic init migrations
pip install psycopg2-binary

alembic.ini:
    sqlalchemy.url = postgresql+psycopg2://postgres:567234@localhost:5432/postgres
env.py:
    from src.database.db import Base
    target_metadata = Base.metadata

alembic revision --autogenerate -m "initial"
alembic upgrade head

poetry add python-jose["cryptography"]
poetry add passlib["bcrypt"]
poetry add python-multipart

poetry add python-jose

create user:
{
  "username": "usertest",
  "email": "test@api.com",
  "password": "123456"
}

add contact:
{
    "first_name": "Bob",
    "last_name": "Vessa",
    "email": "abc@test.com",
    "phone_number": "988714674612",
    "birthday": null,
    "additional_data": null,
    "id": 1
}

