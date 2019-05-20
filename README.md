# enterprise-example
A project to have enterprise level code and tools as reference. The cloud proviers used are Google Cloud Platform and Amazon Web Services.

# Pipeline
Bigger corporations seem to be more eager to:
- run their CI/CD jobs with Jenkins (configured by a Jenkinsfile) and custom Groovy files
- have projects be scanned by SonarQube
- publish their artifacts to Nexus
- deploy their applications using the cloud providers deploy services
  - AWS: CodePipeline
  - GCP: Deployment Manager

# Infrastructure
Bigger corporations are making a move to the cloud
- they use templates to manage their infrastructure
  - AWS: Cloudformation YAML files
  - GCP: Deployment Manager YAML files
  - Custom: popular are Ansible and Terraform
- run their applications inside a container
  - Docker (configured by a Dockerfile)

# Application
Bigger corporations
- tend to use Java Spring for their server-side code
- tend to use a popular framework like React, Angular or Vue for their client-side code
- are building more and more microservices with NodeJs
- are even going serverless with functions/lambdas
