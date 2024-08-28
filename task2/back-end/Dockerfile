# Use the latest version of Ubuntu as the base image
FROM ubuntu:latest

# Update the APT package list and upgrade all installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED if you encounter an error
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask using pip3
RUN pip3 install Flask

# Set the working directory to /app
WORKDIR /app

# Copy the api.py file into the Docker image
COPY api.py /app

# Expose port 5252 for the Flask app
EXPOSE 5252

# Command to run the Flask app
CMD ["python3", "api.py"]
