# Introduction

This is a starter tutorial on how to use podman to generate a container image and then run the container. 

## Application components
This application primarily consists of 2 parts - hello world web app file and a dockerfile. This start-up project will demonstrate how to setup podman on your localhost, build a container image and then run the container in detached mode. 

## Application structure
```
  |── docs                      # Contains edited nginx configuration file that will be copied to the image
  |    ├── img                  # Contains all images referenced in mkdocs
  |    ├── *.md                 # Other mkdocs .md files
  ├── mkdocs.yml                # YAML for for mkdocs
  ├── .gitattributes
  |
  ├── Dockerfile                # Dockerfile for the web-app
  ├── helloworld.py             # Simple hello world python program using Flask API
  ├── README.md                 # Standard README.md file
```
