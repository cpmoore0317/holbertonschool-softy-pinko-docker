# Use the latest Ubuntu as the base image
FROM ubuntu:latest

# Update APT package lists
RUN apt-get update

# Upgrade currently installed software and install 'apt-utils' to avoid warnings
RUN apt-get install -y apt-utils
RUN apt-get upgrade -y

# Create a simple "Hello, World!" script
RUN echo "echo 'Hello, World!'" > /root/hello.sh

# Make the script executable
RUN chmod +x /root/hello.sh

# Run the script when the container starts
CMD ["/bin/bash", "/root/hello.sh"]
