# Part 1: Docker file Creation, GitHub and Docker Hub Integration

## Identify a Sample Application.

-   Compile a python code using any compiler. I have used VS Code IDE to compile following code in ‘**app.py**’.

```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def welcome():
return 'Hello, World!'
```

-   Use ‘flask run’ command in VS Code terminal for execution of **‘app.py’** code:
-   Ensure you have already installed python and Flask. Check the installation with following commands

```
python - -version

flask - -version
# To install flask use command ‘pip install flask’ in VS code terminal
```

![](media/559c0d1cd01d7d264a717b845da24784.png)

-   Output on Screen is ‘Hello World!’ on IP 127.0.0.1:5000

    ![](media/5143b4f201319cb145a4e07d4dc99088.png)

## Dependencies

-   Flask

    For running same python and Linux would be required like **python:3.9.18-alpine3.18**)

## Creation of Docker file

-   Create a Dockerfile and requirements.txt files in VS code. Requirements.txt has the Flask version mentioned in it.
-   Install Docker Desktop and also create an account on <https://hub.docker.com>

![](media/926b10bc04e62590803251b003e37bb3.png)

![](media/3edccb3c7f25a4511bd72f8230148559.png)

-   Used CMD for Entry point
-   For port binding use:

docker container run -d -p 5000:5000 qasim56/qas_simple_flask_app:v1.0

![](media/f2f04cce9b613f05b3e494a372663c8e.png)

## Push code to Dockerhub

<https://hub.docker.com/repository/docker/qasim56/qas_simple_flask_app/general>

-   You can use command line or Docker Desktop for same

![](media/bb3fe4cbfe2e8993812b222d86811cf7.png)

## Create a GitHub Repository

-   Push code on Github repository: [**https://github.com/etechcrunch/Docker_repo.git**](https://github.com/etechcrunch/Docker_repo.git)
