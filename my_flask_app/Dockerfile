# start by pulling the python image
FROM python:3.8-alpine

# copy the requirements file into the image
COPY ./requirements.txt /app/requirements.txt

# switch working directory
WORKDIR /app

# install the dependencies and packages in the requirements file
RUN pip install -r requirements.txt

# copy every content from the local file to the image
COPY . /app

# configure the container to run in an executed manner
ENTRYPOINT ["python"]

CMD ["app.py"]

#docker image build -t flask_docker .
#docker run -it -p 5000:5000 flask_docker
#docker run -it -p 5000:5000 marmunc/flask_app:v0.1