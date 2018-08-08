#**ZygDock**

Demonstrates how to initialize a simple docker image. :whale:

The Dockerfile in the directory contains the four layers of the image.

python:3.6.1-alpine serves as the base layer of the image since it has the version
of python required to run 'app.py'.

Clone the repository, then navigate to the directory using terminal.

Run the following command to build the docker image:

```
$ docker image build -t 'image-name-here' .
```

Run the following command in a different terminal to ensure that the image does
show up in your image list:

```
 $ docker image ls
```
The base image from the docker file : python:3.6.1-alpine should appear in the list of images :+1:
