
##### Run command general form:
`
$ docker-compose run app sh -c "<command>"
`

### **Steps**

#### Start a virtualenv on project root and install the dependencies (optional):
`$ python3.7 -m venv venv`  
`$ source venv/bin/activate`
`$ pip install -r requirements.txt`

#### Start django project
`
$ docker-compose run app sh -c "django-admin.py startproject <project name> ."
`

#### Set environment variables on container

- Put the env variables on vars.env file
SECRET_KEY=\<SECRET KEY> (no quotes)

- Run docker-compose up  
`
$ docker-compose up
`
- Alternatively, the image can be built first, and then the container can be run
with the env file passed:  
`
$ doc run -itd --env-file ./vars.env 80d
`

#### Start django app
`
$ docker-compose run app sh -c "python manage.py startapp <app name> ."
`