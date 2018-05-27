# ZygDock
Demonstrates how to initialize a simple docker image.


Clone the repository, then navigate to the directory using terminal.

Run the command $ python3 app.py. The terminal will log the following message:

Debug mode: off
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)

 Open your browser and visit localhost:5000.
 The following message will be posted in the browser:

 "Zygium says Hello Beautiful World"

 Run the following command in a different terminal to ensure that the image does
 show up in your image list:

 $ docker image ls

The Dockerfile in the directory contains the four layers of the image.

python:3.6.1-alpine serves as the base layer of the image since it has the version
of python required to run 'app.py'.
