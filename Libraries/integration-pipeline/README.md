Team Pipeline
---

# Getting Started
- Initial Master configuration: jenkins.config.json
- Docker: build
- Flows: feature, develop and master
- Maven: build, test
- NPM: install, test, build, publish
- Scans: fortify (security of ...), nexus (security of dependencies), owasp (security of ...), sonar (code quality), twistlock (security of docker image), restassured (testing of api)

# Folder Structure

  .
  ├── infra                   # CloudFormation templates to create an infrastructure stack on AWS
  ├── references              # Contains example files to be used as a jump start for teams
  └── var                     # Groovy files with commands for each step in a pipeline

> Folders with an * are not source code but contains generated files

# Infrastructure


# Contributing
- Read the `CONTRIBUTING.md` file for the guidelines.
