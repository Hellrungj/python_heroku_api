# python_heroku_api

[![Python 3.8](https://img.shields.io/badge/python-3.8-blue.svg)](https://www.python.org/downloads/release/python-360/)
[![Docker](https://badgen.net/badge/icon/docker?icon=docker&label)](https://https://docker.com/)
![Django](https://img.shields.io/badge/-Django-%23092E20?style=flat&logo=django&logoColor=white)

A quickstart api using docker and django that can be deploy easily to Heroku

## Authors

- [@Hellrungj](https://www.github.com/Hellrungj)
  
## Deployment

To deploy this project see [Deploying with Docker on Heroku](https://devcenter.heroku.com/categories/deploying-with-docker) documentation. 
  
## Environment Variables

Docker Env
- `HOST`: '0.0.0.0'
- `PORT`: '8000'
- `DEBUG`: 0



## Run Django Server Development Locally

Clone the project

```bash
  git clone https://github.com/Hellrungj/python_heroku_api.git
```

Install Python 3

```bash
  apt install python3
```

Install pipenv

```bash
  pip install pipenv
```

Install dependencies

```bash
  pipenv install
```

Activate python virtual environment
```bash
  pipenv shell
```

Go to the project directory

```bash
  cd api/
```

Install dependencies
Start the server
```bash
  python manage.py runserver
```

## Run Docker Container Locally

Clone the project

```bash
  git clone https://github.com/Hellrungj/python_heroku_api.git
```

Install Docker

```bash
  Install the app from https://docs.docker.com/get-docker/
```

Build Image
```bash
docker build -t  django-heroku-app
```

Run the Container:
```bash
docker run -it -e "HOST:0.0.0.0" -e "PORT=8000" -e "DEBUG=0" -p 8000:8000 django-heroku-app
```