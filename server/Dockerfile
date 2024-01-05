FROM python:3.8.18

# Set the working directory to /home
WORKDIR /home

# copy files in conatiner
COPY ./ /home 

RUN apt-get update

# set as environment variable
env DEBUG="True"
env CELERY_BROKER_URL="redis://rediscontainer:6379"
env CELERY_RESULT_BACKEND="redis://rediscontainer:6379/0"
env DJANGO_DB="postgresql"
env POSTGRES_HOST="newpostgres"
env POSTGRES_NAME="db"
env POSTGRES_USER="postgres"
env POSTGRES_PASSWORD="postgres"
env POSTGRES_PORT="5432"


# Install system dependencies
RUN pip install --upgrade pip

# Install Python dependencies
RUN pip3 install -r requirements.txt

# install gunicorn
RUN pip3 install gunicorn

# expose port
EXPOSE 8000

# execute file and run command
RUN chmod +x /home/backend/server-entrypoint.sh 
CMD ["./backend/server-entrypoint.sh"]
