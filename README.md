# CreateYourRecipe.com: Recipe Web App 

A recipe web app built with **Python, Flask and SQLAlchemy**. Users can browse and search recipes, filter by cuisine, create their own recipes with ingredients and step-by-step instructions, and leave comments.

Built by a team of four at BCIT, with automated tests that run on every push through **GitHub Actions**.

## Features

- **Browse and search** recipes by name, with filters such as cuisine type
- **Create recipes** with a title, cuisine, cook time, difficulty, ingredients and instructions. Ingredient and instruction fields can be added dynamically on the form.
- **Recipe pages** showing ingredients, instructions and comments
- **Comments**: add and delete comments on a recipe
- **Delete recipes**, with a confirmation message after actions
- **Ingredient page** for adding ingredients

## Tech stack

| Area | Tools |
|---|---|
| Backend | Python, Flask |
| Database | SQLite with Flask-SQLAlchemy |
| Frontend | Jinja2 HTML templates, CSS, JavaScript |
| Testing | pytest (unit and functional tests) |
| CI | GitHub Actions runs pytest on every push |
| Deployment | Gunicorn (`wsgi.py`) |

## Data model

| Table | Purpose |
|---|---|
| `Recipe` | Title, instructions, cuisine, cook time, difficulty |
| `Ingredient` | Ingredient name and measurement |
| `Reqs` | Links recipes to ingredients, with quantity |
| `Comments` | Comments on a recipe |

## Project structure

```
app.py            Flask app and routes
models.py         SQLAlchemy models
db.py             Database setup
searchRecipe.py   Search and filter logic
utils.py          Helper functions
manage.py         Create, reset and seed the database
wsgi.py           Entry point for Gunicorn
templates/        HTML pages (home, list, recipe, create, ingredient)
static/           CSS, JavaScript, images
tests/            Unit and functional tests
data/             SQLite database
```

## Run it

Requires Python 3.10 or newer.

```bash
pip install -r requirements.txt
python app.py
```

Then open **http://localhost:5555**.

To reset or seed the database with sample recipes:

```bash
python manage.py
```

## Run the tests

```bash
pytest
```

## My contribution (Muhammad Baig Mirza)

- Built the **recipe creation** feature: the create page and route, with dynamic fields for adding ingredients and instructions
- Added **delete recipe** and success messages when a recipe is created
- Worked on the **database models** and setup
- Added the **search bar** on the home page
- Updated the **recipe, list, home and ingredient page layouts** and styling
- Named and titled the site (CreateYourRecipe.com)

## Team

[@HsuSteven](https://github.com/HsuSteven), [@heytoki](https://github.com/heytoki), [@Strive-Vexil](https://github.com/Strive-Vexil) and [@MuhammadBai](https://github.com/MuhammadBai)
