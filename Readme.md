# Jenkins Pipeline for React based application using SonarQube, Argo CD, Helm and Kubernetes

![Pipeline-1](https://github.com/user-attachments/assets/9a399479-f00c-49b5-b980-0109fafc8c37)

Here are the step-by-step details to set up an end-to-end Jenkins pipeline for a Java application using SonarQube, Argo CD, Helm, and Kubernetes:

Prerequisites:

   -  React application code hosted on a Git repository
   -  Jenkins server
   -  Kubernetes cluster
   -  Helm package manager
   -  Argo CD

Steps:

    1. Install the necessary Jenkins plugins:
       1.1 Git plugin
       1.2 NPM and Yarn Wrapper and Steps
       1.3 NodeJS plugin
       1.4 Pipeline plugin
       1.5 Kubernetes Continuous Deploy plugin

    2. Create a new Jenkins pipeline:
       2.1 In Jenkins, create a new pipeline job and configure it with the Git repository URL for the React application.
       2.2 Add a Jenkinsfile to the Git repository to define the pipeline stages.
 
    3. Define the pipeline stages:
        Stage 1: Checkout the source code from Git.
        Stage 2: Build the React application using npm.
        Stage 3: Run unit tests using Jest.
        Stage 4: Run SonarQube analysis to check the code quality.
        Stage 5: Deploy the application to a test environment using Helm.
        Stage 6: Run user acceptance tests on the deployed application.
        Stage 7: Promote the application to a production environment using Argo CD.

    4. Configure Jenkins pipeline stages:
        Stage 1: Use the Git plugin to check out the source code from the Git repository.
        Stage 2: Use the Node Integration plugin to build the React application.
        Stage 3: Use the Jest plugins to run unit tests.
        Stage 4: Use the SonarQube plugin to analyze the code quality of the React application.
        Stage 5: Use the Kubernetes Continuous Deploy plugin to deploy the application to a test environment using Helm.
        Stage 6: Use Argo CD to promote the application to a production environment.

    5. Set up Argo CD:
        Install Argo CD on the Kubernetes cluster.
        Set up a Git repository for Argo CD to track the changes in the Helm charts and Kubernetes manifests.
        Create a Helm chart for the React application that includes the Kubernetes manifests and Helm values.
        Add the Helm chart to the Git repository that Argo CD is tracking.

    6. Configure Jenkins pipeline to integrate with Argo CD:
       6.1 Add the Argo CD API token to Jenkins credentials.
       6.2 Update the Jenkins pipeline to include the Argo CD deployment stage.

    7. Run the Jenkins pipeline:
       7.1 Trigger the Jenkins pipeline to start the CI/CD process for the React application.
       7.2 Monitor the pipeline stages and fix any issues that arise.

This end-to-end Jenkins pipeline will automate the entire CI/CD process for a React application, from code checkout to production deployment, using popular tools like SonarQube, Argo CD, Helm, and Kubernetes.
