#Use an official Python runtime as a parent image
FROM python:3.8.18

# Set environment variables

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set the working directory in the container
WORKDIR /apps

# Copy the requirements file into the container at /apps
COPY requirements.txt /apps

# Install any needed packages specified in requirements.txt

RUN pip install --upgrade pip && \
    pip install -r requirements.txt

# Copy the current directory contents into the container at /apps
COPY . /apps

# Collect static files
CMD ["sh", "docker.sh"]
EXPOSE 8000

