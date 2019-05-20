# enterprise-example
A project to have enterprise level code and tools as reference. The cloud proviers used are Google Cloud Platform and Amazon Web Services.

## Pipeline
Bigger corporations seem to be more eager to:
- run their CI/CD jobs with Jenkins (configured by a Jenkinsfile) and custom Groovy files
- have projects be scanned by SonarQube
- publish their artifacts to Nexus
- deploy their applications using the cloud providers deploy services
  - AWS: CodePipeline
  - GCP: Deployment Manager

## Infrastructure
Bigger corporations are making a move to the cloud
- they use templates to manage their infrastructure
  - AWS: Cloudformation YAML files
  - GCP: Deployment Manager YAML files
  - Custom: popular are Ansible and Terraform
- run their applications inside a container
  - Docker (configured by a Dockerfile)
- collect all loggin and monitoring data into a Splunk dashboard

## Application
Bigger corporations
- tend to use Java Spring for their server-side code
- tend to use a popular framework like React, Angular or Vue for their client-side code
- are building more and more microservices with NodeJs
- are even going serverless with functions/lambdas

# Teams
Bigger corporations tend to have:
- Centralised teams which set standards and share their code:
  - A team which set styling standards and creates a styleguide
  - A team which creates shared code for pipelines to be used by individual teams
  - A team which creates shared components, either for Angular or React apps
- A team responsible for a backend microservice or app, mostly a Java application or NodeJs
- A team responsible for a web application or widget, written with either Angular or React (initialised via CLI)
- A team responsible for the website and building and running their own frontend
