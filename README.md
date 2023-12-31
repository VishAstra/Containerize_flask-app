### Flask Docker Application 
###This repository contains a simple Flask application with Dockerfile to containerize it.

### **Instructions** **

*Prerequisites* 

- Docker installed on your machine(scroll down to see the instruction to install docker 
- *Docker Hub account (for image registry)*

Building Image 

1. Clone this repository



```bash
git clone https://github.com/VishAstra/flask-hello-app.git 
```

2. Navigate to the repository directory



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



```bash
docker run -p 8080:8080 my-flask-app The app will be available at [http://localhost:8080]
```

Pushing Image to Docker Hub To share the image on Docker Hub:

6.Log into Docker CLI



```bash
docker login 
```

7. Tag image with Docker Hub username



```bash
docker tag my-flask-app /my-flask-app 
```

8. Push image



```bash
docker push /my-flask-app
```

 The image is now available publicly on Docker Hub.

***Deploying to Cloud Use Docker Hub integration in your cloud platform (AWS ECS, GCP Run etc) to deploy the containerized Flask app. This allows running the application at scale.***


🔚--------------------------------------------------------------------------------------------------------------------------------------------------------------
Here are the steps to install Docker on some common operating systems, including Amazon Linux on AWS EC2:

**Ubuntu/Debian**

```
sudo apt update
sudo apt install docker.io

```

**CentOS/RHEL/Amazon Linux**

```
sudo yum update
sudo yum install docker

```

**Fedora**

```
sudo dnf update
sudo dnf install docker-ce

```

**MacOS**

Download and install Docker Desktop from docker.com

**Windows 10/11**

Download and install Docker Desktop from docker.com

**AWS EC2 Amazon Linux**

```
sudo yum update -y
sudo yum install docker -y
sudo service docker start

```

**Verify Installation**

Check Docker version:

```
docker --version

```

Run a test container:


```
docker run hello-world

```
