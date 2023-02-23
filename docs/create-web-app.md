# Create Web App
Here we will create the web-app file that is written in python and uses Flask API. 

Create file `helloworld.py` and copy the following content in there : 

```
from flask import Flask, request
from flask_restful import Resource, Api

app = Flask(__name__)
api = Api(app)

class Greeting (Resource):
    def get(self):
        return 'Hello World!'

api.add_resource(Greeting, '/') # Route_1

if __name__ == '__main__':
    app.run('0.0.0.0','3333')
```