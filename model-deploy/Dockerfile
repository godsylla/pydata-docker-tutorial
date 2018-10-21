# template for how to use docker to setup a flask app
# and serve up a python model
# an external app can make API calls to it an get the output
# easy way to deploy a model for wider consumption

# pull the image wh has flask on it
FROM tiangolo/uwsgi-nginx-flask:python3.6

# specifying work directory
WORKDIR /app/

COPY requirements.txt /app/
RUN pip install -r ./requirements.txt

# sets OS level variables
# the variable you want to set, and what you want to set it to
ENV ENVIRONMENT production

# then copy it into your main.py and __init__.py
COPY main.py __init__.py /app/
