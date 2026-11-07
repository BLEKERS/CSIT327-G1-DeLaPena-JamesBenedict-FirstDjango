# CampusConnect

A small Django project for a school community: users can sign up, log in, view a
dashboard and edit their own profile.

## 

## Project structure

```
campusconnect/        project settings and root URLs
accounts/             CustomUser model, forms, sign-up/login/profile views, tests
dashboard/            dashboard and admin panel views
templates/
  base.html           shared layout (Bootstrap CDN, navbar, message alerts)
  partials/form\_fields.html
  registration/       login.html, signup.html
  accounts/profile.html
  dashboard/          home.html, admin\_panel.html
  403.html
```

## Run it locally

Requires Python 3.12+.

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\\Scripts\\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser # optional
python manage.py runserver
```

Open http://127.0.0.1:8000/ - you are sent to the login page. Use **Sign up** to
create an account, then **My profile** in the navbar to edit it. An internet
connection is needed to load Bootstrap from the CDN.

To make a user an administrator (to see the admin panel), change their role in the
Django admin at `/admin/` (requires a superuser).

## 

