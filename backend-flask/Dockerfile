FROM python:3.10-slim-buster

WORKDIR /backend-flask

# Copy requirements.txt from local host to container
COPY requirements.txt requirements.txt

# Install python libraries using pip
RUN pip3 install -r requirements.txt

# Copy everything from working directory /backend-flask to container
COPY . .

# Set environment variable inside variable
ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]