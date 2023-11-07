# Use the latest Ubuntu base image as the starting point.
FROM ubuntu:latest

# Update the package list to get the latest information about available packages.
RUN apt-get update

# Upgrade all installed packages to their latest versions.
RUN apt-get upgrade -y

# Install Python 3 and pip (Python package manager) for dependencies.
RUN apt-get install -y python3 python3-pip

# Use pip to install the Flask web framework.
RUN pip install Flask

# Use pip to install Flask-CORS, a Flask extension for handling Cross-Origin Resource Sharing (CORS).
RUN pip install flask-cors

# Set the working directory inside the container to /app.
WORKDIR /app

# Copy the local file api.py to the /app directory in the container.
COPY ./api.py /app/api.py

# Expose port 5252 to allow incoming network connections to the container on this port.
EXPOSE 5252

# Define the command to run when the container starts. In this case, it runs the Python script api.py.
CMD python3 api.py
