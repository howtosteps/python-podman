# Create a DockerFile

We will now create a DockerFile that is used to build an OCI image. The image contains all the dependencies the Python application requires, including Python itself. Podman uses `DockerFile` just like standard docker.  

In the project directory, create a file named `DockerFile`
```
FROM python:3
ADD helloworld.py /
RUN pip install flask
RUN pip install flask_restful
EXPOSE 3333
CMD [ "python", "./helloworld.py"]
```
This tells Podman (***just like Docker***) to:

* Build an image starting with the Python 3 image
* Copy helloworld.py to image and set the working directory to /
* Install python dependencies - flask , flask_restful
* Expose application port 3333
* Run python command when image is started
