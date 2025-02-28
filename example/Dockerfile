# use the latest ubuntu image as the base image
FROM ubuntu:latest

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
ADD . /app
# Install python3 and pip3
RUN apt-get update && apt-get install -y python3 python3-pip

CMD [ "python3", "app.py" ]