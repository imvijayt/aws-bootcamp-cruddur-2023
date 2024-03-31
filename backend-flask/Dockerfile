FROM python:3.10-slim-buster

#inside container
#make a new folder inside container
WORKDIR /backend-flask

#outside to insidercontainer
COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

# . means everything in the current directory
# . first period /backend-flask (outside container)
# . second period /backend-flask (inside container)
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}

# python -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]