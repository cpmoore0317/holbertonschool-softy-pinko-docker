# Use the latest Ubuntu as the base image
FROM ubuntu:latest

# Update APT package lists and install Python 3, Python 3 pip, and Flask
RUN apt-get update -y
RUN apt-get install -y python3 python3-pip
RUN pip3 install flask

# Set the working directory in the container
WORKDIR /app

# Copy the Python script to the working directory in the container
COPY api.py /app/api.py

# Expose port 5252 for the Flask application
EXPOSE 5252

# Run the Flask application
CMD ["python3", "api.py"]
