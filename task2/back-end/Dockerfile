# Use the official Ubuntu image from the Docker Hub
FROM ubuntu:latest

# Update the package list and install Python3 and pip3
RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y python3 python3-pip

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy the Python file to the /app directory
COPY api.py /app/api.py

# Command to run the Flask application
CMD ["python3", "api.py"]
