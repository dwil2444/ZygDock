#**ZygDock**

:whale: Demonstrates how to initialize a simple docker image. :whale:

The Dockerfile in the directory contains the four layers of the image.

python:3.6.1-alpine serves as the base layer of the image since it has the version
of python required to run 'app.py'.

1. **Clone the repository**, then navigate to the directory using terminal.

2. Run the following command to **build the docker image:**

```
$ docker image build -t 'image-name-here' .
```

3. Run the following command in a different terminal to **ensure that the image does
show up in your image list:**

```
 $ docker image ls
```
The base image from the docker file : python:3.6.1-alpine should appear in the list of images.

4. To **run the docker image**, run the following command from the terminal:
```$ docker run -p 3000:3000 -d 'image-name-here'
```
The flask application will default to port 5000 of your application unless otherwise specified. The -p flag maps a port running inside the container to your host. In this case, you’re mapping the Python app running on port 3000 inside the container to port 3000 on your host.
[You can specify the Flask port by specifying the port number in the app.py file ```app.run(host='0.0.0.0', port = 3000)```]

5. Navigate to http://localhost:XXXX [where XXXX represents a port number] in a browser. The message :
  "Zygium says hello beautiful world" will be displayed.

6. To view a list of running containers, run the following command:
  ```docker container ls
  ```

7. Stop the docker container with the following command:
  ```docker stop 'xxxx'
  ```
  [where xxxx represents the first four digits of the container id]

8. You can remove all docker images with the following command:
```docker rmi -f $(docker images -a -q)
```
