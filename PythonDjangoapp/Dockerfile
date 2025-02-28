# install ubuntu base image
FROM ubuntu:latest
# Set the working directory to /app
WORKDIR /app
# Copy the current directory contents into the container at /app
ADD . /app
# Install python3, pip3, venv and django
RUN apt-get update && apt-get install -y python3 python3-pip python3-venv

# use bash shell for running commands
#
SHELL ["/bin/bash", "-c"]

# Create a virtual environment and
RUN python3 -m venv venv && source venv/bin/activate && pip install --no-cache-dir -r requirements.txt

# Run the application
ENTRYPOINT [ "python3" ]
CMD [ "python3", "manage.py", "runserver", "0.0.0.0:8000" ]
