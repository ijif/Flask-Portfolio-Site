# Flask on Heroku 



* Running Python 3.6 🐍
* Access to a Postgres Database 📘
* Static Files management with [WhiteNoise](http://whitenoise.evans.io/en/stable/) 🔌


## Summary of steps to deploy your app
_(Assuming you've already created an account with Heroku)_

##### 1. Clone the repo
```bash
$ git clone *Cloned Repo && cd *Nme of repo
```

##### 2. Login to Heroku
```bash
$ heroku login
```

##### 3. Create your Heroku apps
```bash
$ heroku create
```

##### 4. Set the Python Path
```bash
$ heroku config:set PYTHONPATH=flask_heroku_example
```

##### 5. Add Postgres Add-on to your Heroku app
(Use Heroku's site to add Postgres. It's free)

##### 6. Initialize the Database
```bash
$ # Create the initial schema
$ heroku pg:psql < schema.sql
$ # Load some initial testing data
$ heroku pg:psql < initial_data.sql
```

##### 7. Deploy & Profit
```bash
$ git push heroku master
```

## Running the app locally
_(You need to have installed Postgres locally to run the app. For a simpler sqlite alternative, please check the aforementioned tutorial)_

```bash
# Create the virtualenv
$ mkvirtualenv flask-heroku-example
# Install dependencies
$ pip install -r requirements.txt
# Run the app
$ python flask_heroku_example/main.py
# Now point your browser to localhost:5000
```
