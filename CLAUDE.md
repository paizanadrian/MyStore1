# Weiboo — Django E-commerce UI Kit

## Proiect
- Django 5.1.3, Python, SQLite
- UI kit e-commerce — frontend complet, backend în construcție
- Fără aplicații Django separate (totul în pachetul `Weiboo/`)

## Structură views
- `Weiboo/homeViews.py` — pagini home (10 variante index, login, wishlist)
- `Weiboo/shopViews.py` — shop (cart, checkout, product details)
- `Weiboo/blogViews.py` — blog (news, contact)
- `Weiboo/pagesViews.py` — pagini statice (about, faq, error)
- `Weiboo/urls.py` — toate rutele URL

## Comenzi esențiale
```bash
# Pornire server
.venv/Scripts/python manage.py runserver

# Migrări (când adaugi modele)
.venv/Scripts/python manage.py makemigrations
.venv/Scripts/python manage.py migrate

# Shell Django
.venv/Scripts/python manage.py shell

# Verificare sintaxă Python
.venv/Scripts/python -m py_compile Weiboo/homeViews.py
```

## Convenții cod
- Snake_case pentru variabile și funcții
- Views sunt funcții simple (function-based views), nu class-based
- Fiecare view returnează `render(request, 'template.html', context)`
- Templates în `templates/`, static files în `static/`

## Reguli importante
- NU modifica `settings.py` fără să ceri confirmare
- SECRET_KEY este insecure (development only) — nu o expune în producție
- Când adaugi un URL nou, adaugă-l în `Weiboo/urls.py`
- Când creezi un view nou, pune-l în fișierul views corespunzător categoriei

## Status backend
- Autentificare: de implementat
- Modele: de creat
- API: de construit
- Logică business: de adăugat
