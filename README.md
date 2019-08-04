# A Tiny Django API with Tastypie

- To install and run the project:

1. `git clone https://github.com/isnotafunction/tastypie-notes.git`

2. create a virtual environment and install dependencies `pip install -r requirements.txt`

3. apply migrations `python manage.py migrate`

4. populate the db with at least one note directly from the console:

```
python manage.py shell

>>> from api.models import Note
>>> note = Note(title="Awesome title", body="🤞")
>>> note.save()
>>> Note.objects.all()
...
```

5. `pyton manage.py runserver`

The server will run on port 8000 and you can now make requests against `http://localhost:8000/api/note`

6. GET `http://localhost:8000/api/note/1`
   POST `http://localhost:8000/api/note/`

Resources:

- [Create a Django API in Under 20 Minutes](https://codeburst.io/create-a-django-api-in-under-20-minutes-2a082a60f6f3) article
- [Tastypie docs](https://django-tastypie.readthedocs.io/en/latest/)
