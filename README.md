# Heroku Custom Blog

A passion project to basically make a much worse version of wordpress for Heroku.

Django for the backend with blob storage for media, sql db and eventually react front-end (django templates for now)


# Building

1. Use python to create a venv: `python3 -m venv ./heroku-blog-venv`
2. Activate venv: 
    - Windows: `.\heroku-blog-venv\Scripts\Activate.ps1`
    - NIX: `source ./heroku-blog-venv/bin/activate`
3. Install python reqs: `python -m pip install -r requirements.txt`
4. Run locally: `python maange.py runserver`

# Deployment

## To Heroku

1. Install [heroku cli](https://devcenter.heroku.com/articles/heroku-cli#install-the-heroku-cli)
2. heroku:auth login
3. Set DATABASE_URL, DEBUG and SECRET_KEY using heroku:config
4. Add heroku as a git remote: `heroku git:remote -a <app name>`
5. Once your changes are merged into main, you can push them with: `git push heroku main`