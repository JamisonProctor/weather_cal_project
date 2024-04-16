# Use the official Python image as the base image
FROM python:3.9

# Set environment variables for Python buffering and Django settings
ENV PYTHONUNBUFFERED 1
ENV DJANGO_SETTINGS_MODULE weather_cal.settings

# Create and set the working directory in the container
WORKDIR /django_app

# Install dependencies
COPY requirements.txt /django_app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy the Django project code into the container
COPY . /django_app/
