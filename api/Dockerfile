# Pull base image
FROM python:3.9
# Set environment varibles
# Prevents Python from writing pyc files to disc
ENV PYTHONDONTWRITEBYTECODE 1
# Prevents Python from buffering stdout and stderr
ENV PYTHONUNBUFFERED 1
# Set work directory
RUN mkdir /code
WORKDIR /code
# Install dependencies
RUN pip install pipenv
COPY Pipfile Pipfile.lock /code/
RUN pipenv install --system
# Copy project
COPY . /code/