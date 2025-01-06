# Build Automation & CI/CD with Jenkins

## Technologies used:

- Jenkins, Docker, DigitalOcean, Linux, Git, Java, Maven, Groovy, GitLab

## Job 1: Install Jenkins on DigitalOcean
#### Job description:

- Create an Ubuntu server on DigitalOcean
- Set up and run Jenkins as Docker container
- Initialize Jenkins

## Job 2: Create a CI Pipeline with Jenkinsfile (Freestyle, Pipeline, Multibranch Pipeline)
#### Job description:

CI Pipeline for a Java Maven application to build and push to the
repository:
- Install Build Tools (Maven, Node) in Jenkins
- Make Docker available on Jenkins server
- Create Jenkins credentials for a git repository
- Create different Jenkins job types (Freestyle, Pipeline, Multibranch pipeline) for the Java Maven project with Jenkinsfile to:
  
    a. Connect to the application’s git repository  
    b. Build Jar  
    c. Build Docker Image  
    d. Push to private DockerHub repository

## Job 3: Create a Jenkins Shared Library
#### Job description:

Create a Jenkins Shared Library to extract common build
logic:
- Create separate Git repository for Jenkins Shared Library project
- Create functions in the JSL to use in the Jenkins pipeline
- Integrate and use the JSL in Jenkins Pipeline (globally and for a specific project in Jenkinsfile)

## Job 4: Configure Webhook to trigger CI Pipeline automatically on every change
#### Job description:

- Install GitLab Plugin in Jenkins
- Configure GitLab access token and connection to Jenkins in GitLab project settings
- Configure Jenkins to trigger the CI pipeline, whenever a change is pushed to GitLab

## Job 5: Dynamically Increment Application version in Jenkins Pipeline
#### Job description:

- Configure CI step: Increment patch version
- Configure CI step: Build Java application and clean old artifacts
- Configure CI step: Build Image with dynamic Docker Image Tag
- Configure CI step: Push Image to private DockerHub repository
- Configure CI step: Commit version update of Jenkins back to Git repository
- Configure Jenkins pipeline to not trigger automatically on CI build commit to avoid commit loop
