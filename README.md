#############################################  Flask Application   ################################################
# update apt-get
sudo apt-get update
# install python3
sudo apt-get install -y python3
# install pip3
sudo apt-get install python3-pip
# install Flask
sudo pip3 install Flask   
# This is a simple Flask application that has two routes.
# The first route is the default route that returns a welcome message.
# The second route is /howareyou that returns a message.
# To run this application, run the following command:
python app.py 
# Then open a browser and go to http://localhost:5000/ to see the welcome message.
# To see the message from the /howareyou route, go to http://localhost:5000/howareyou.
# FLASK_APP=./opt/app.py flask run --host=0.0.0.0 --port=5000 to run the application in a Docker container.
############################################## Dockerfile   ##########################################################

##############################################  Docker Build   ##########################################################
docker build -t flaskapp .
##############################################  Docker Run   ##########################################################
docker run -p 5000:5000 flaskapp
