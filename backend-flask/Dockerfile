FROM python:3.10-slim-buster

#indside container
#make a new folder inside container

WORKDIR /backend-flask

#outside container -> inside contianer
#this files contians all the libraries needed to run the app

COPY requirements.txt requirements.txt

#run the python libraries
RUN pip3 install -r requirements.txt

#copy everything from  backend-flask to backend-flask (container)

COPY . .

#set env variables
#inside container,and will remain set when the container is running

ENV FLASK_ENV=development


EXPOSE ${PORT}

#CMD (command)
#
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]