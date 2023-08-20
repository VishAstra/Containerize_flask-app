### Flask Docker Application This repository contains a simple Flask application with Dockerfile to containerize it.

### **Instructions** **

*Prerequisites* 

- *Docker installed on your machine*
- *Docker Hub account (for image registry)*

Building Image 

1. Clone this repository

Copy code

```bash
git clone https://github.com/VishAstra/flask-hello-app.git 
```

2. Navigate to the repository directory

Copy code

```bash
cd flask-hello-app 
```

3. Build the Docker image from the Dockerfile

Copy code

```bash
docker build -t my-flask-app . 
```

4. Once built, verify the image is created

Copy code

```bash
docker images 
```

You should see the my-flask-app image listed.

1. Running Container To run the Flask app container:

Copy code

```bash
docker run -p 8080:8080 my-flask-app The app will be available at [http://localhost:8080](http://localhost:8080/)
```

Pushing Image to Docker Hub To share the image on Docker Hub:

6.Log into Docker CLI

Copy code

```bash
docker login 
```

7. Tag image with Docker Hub username

Copy code

```bash
docker tag my-flask-app /my-flask-app 
```

8. Push image

Copy code

```bash
docker push /my-flask-app
```

 The image is now available publicly on Docker Hub.

***Deploying to Cloud Use Docker Hub integration in your cloud platform (AWS ECS, GCP Run etc) to deploy the containerized Flask app. This allows running the application at scale.***
