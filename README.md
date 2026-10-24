# 🚀 CI/CD Project: Java Maven Application Deployment on Apache Tomcat Server

## 📌 Project Overview

This project demonstrates the implementation of a **Continuous Integration and Continuous Deployment (CI/CD) pipeline for a Java Maven web application, deployed on an Apache Tomcat server using Docker and Jenkins**.

The pipeline automates the application build and packaging process with Maven, creates a Docker image containing the application, publishes the image to Docker Hub, and deploys the containerized application on Apache Tomcat.

The main objective of this project is to understand and implement an automated CI/CD workflow for building, containerizing, and deploying a Java web application.

## 🎯 Project Objectives

- Automate the Java Maven application build using Jenkins.
- Package the web application into a WAR file using Maven.
- Containerize the application using Docker.
- Use Apache Tomcat as the web application server.
- Push the Docker image to Docker Hub.
- Automate application deployment through a Jenkins pipeline.
- Configure email notifications for pipeline build results.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Java / JSP | Web application development |
| Apache Maven | Application build and WAR packaging |
| Jenkins | CI/CD pipeline automation |
| Docker | Application containerization |
| Apache Tomcat 9 | Java web application server |
| Git & GitHub | Source code management |
| Docker Hub | Docker image storage |
| Shell Scripting | DevOps automation |

## 🏗️ CI/CD Architecture

```text
Developer
   |
   v
GitHub Repository
   |
   v
Jenkins CI/CD Pipeline
   |
   v
Maven Build
   |
   v
WAR File Generation
   |
   v
Docker Image Creation
   |
   v
Push Image to Docker Hub
   |
   v
Deploy Docker Container
   |
   v
Apache Tomcat Server
   |
   v
Java Maven Web Application
```

## 🔄 CI/CD Pipeline Stages

**1. Source Code Management**  
The Java Maven application and Jenkins pipeline configuration are maintained in GitHub.

**2. Build and Package**  
Jenkins runs Maven commands to compile and package the application into a WAR file.

```bash
mvn clean package
```

**3. Docker Image Creation**  
Docker builds an image using Apache Tomcat 9 as the base image and copies the generated WAR file into Tomcat's web application directory.

**4. Docker Hub Integration**  
The pipeline authenticates with Docker Hub using Jenkins credentials and pushes the Docker image to the configured repository.

**5. Application Deployment**  
Jenkins deploys the Docker container, running the Java Maven web application on the Apache Tomcat server.

**6. Email Notification**  
The pipeline is configured to send email notifications containing the build result and Jenkins build URL.

## 📂 Project Structure

```text
CI-CD-PROJECTS/
├── README.md
└── Project 1/
    ├── Dockerfile
    ├── Jenkinsfile
    ├── Jenkinsfile-backup
    ├── pom.xml
    ├── maven.md
    ├── scripts/
    └── src/
        └── main/
            └── webapp/
                ├── index.jsp
                ├── demo.jsp
                └── WEB-INF/
                    └── web.xml
```

## 🚀 Run the Application Locally

### Prerequisites

- Java JDK
- Apache Maven
- Docker
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/Bikkythecoder/CI-CD-PROJECTS.git
cd CI-CD-PROJECTS
```

### 2. Build the Java Maven Application

```bash
cd "Project 1"
mvn clean package
```

### 3. Build the Docker Image

```bash
docker build -t javamavenapp:latest .
```

### 4. Deploy on Apache Tomcat Using Docker

```bash
docker run -d \
  --name javamavenapp_container \
  -p 9000:8080 \
  javamavenapp:latest
```

### 5. Access the Application

Open your browser and navigate to:

`http://localhost:9000`

## 💡 Key Learning Outcomes

- Understanding CI/CD principles and pipeline stages.
- Automating Java Maven application builds with Jenkins.
- Packaging Java web applications as WAR artifacts.
- Deploying Java web applications on Apache Tomcat.
- Building and managing Docker images and containers.
- Integrating GitHub, Jenkins, Maven, and Docker Hub.
- Automating application deployment and build notifications.

## 👨‍💻 Author

**Bikky Roy**

GitHub: [Bikkythecoder](https://github.com/Bikkythecoder)

---

⭐ This project demonstrates a practical DevOps workflow for **CI/CD automation of a Java Maven application deployed on an Apache Tomcat server using Jenkins and Docker**.
