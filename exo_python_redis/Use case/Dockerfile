# base image
FROM python:3.8-alpine3.19

#Copy just the requirement.txt first to leverage Docker
#Install all dependences for python app
COPY ./requirements.txt /app/requirements.txt

WORKDIR /app

#install dependences in requirements.txt
RUN pip install -r requirements.txt 

#Copy all content to work directory /app
COPY . /app

#Specify the port number the container should expose
EXPOSE 5000

#run the application
CMD [ "python", "/app/main.py"]
