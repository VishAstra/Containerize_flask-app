Flask Docker Application
This repository contains a simple Flask application with Dockerfile to containerize it.

Instructions
Prerequisites
Docker installed on your machine
Docker Hub account (for image registry)
Building Image
Clone this repository
<!---->
Copy code

git clone https://github.com/VishAstra/flask-hello-app.git
2.  Navigate to the repository directory

<!---->
Copy code

cd flask-hello-app
3.  Build the Docker image from the Dockerfile

<!---->
Copy code

docker build -t my-flask-app .
4.  Once built, verify the image is created

<!---->
Copy code

docker images
You should see the my-flask-app image listed.

Running Container
To run the Flask app container:

Copy code

docker run -p 8080:8080 my-flask-app
The app will be available at http://localhost:8080

Pushing Image to Docker Hub
To share the image on Docker Hub:

Log into Docker CLI
<!---->
Copy code

docker login
2.  Tag image with Docker Hub username

<!---->
Copy code

docker tag my-flask-app <docker-username>/my-flask-app
3.  Push image

<!---->
Copy code

docker push <docker-username>/my-flask-app
The image is now available publicly on Docker Hub.

Deploying to Cloud
Use Docker Hub integration in your cloud platform (AWS ECS, GCP Run etc) to deploy the containerized Flask app.

This allows running the application at scale.
