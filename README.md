# django-blog

A simple blog made with Django

this is just a tutorial for myself

resources:

- Corey Shafer <https://www.youtube.com/playlist?list=PL-osiE80TeTtoQCKZ03TU5fNfx2UY6U4p>

## Project Structure

This project is organized into three main Django applications:

### blog/
Handles everything related to blog posts.  
It provides the homepage with recent articles, individual post pages, and an “About” page.  
Only authenticated users can create, update, or delete their own posts.  
Each post has its own author, date, and dedicated URL, with pagination for easier browsing.

### polls/
Contains a simple polling module with questions and choices.  
At the moment, it mainly serves as a basic test app to demonstrate how multiple Django apps can coexist.

### users/
Manages user registration, login, logout, and password reset.  
A user profile is created automatically at registration, and users can edit their information (name, email, profile picture) from the profile page.

### How it fits together
Each app has its own URLs and templates, while the project-level `urls.py` routes visitors to the right module.  
The root of the site redirects to the blog, and media files (such as profile pictures) are served during development.

## How to run

1. Make a virtual environment and switch to it
2. Install dependencies
3. Migrate database
4. runserver

```sh
python -m venv django_blog_env
source /path/to/your/venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```
