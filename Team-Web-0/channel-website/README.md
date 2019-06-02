Team Website
===

This project is initialised using: `$ npm init --yes`

## Getting Started
Clone this repository
```
$ git clone git@github.com:rbergenl/enterprise-example.git folder-name
```
Install node modules
```
$ npm install
```
Start project
```
$ npm start
```

## Folder Structure

    .
    ├── dist*                   # Dist folder to be published
    ├── infra                   # CloudFormation templates to create an infrastructure stack on AWS
    ├── server                  # Serves a page template with server side rendering
    ├── src                     
    |   ├── components          # Javascript components
    |   └── themes              # Sass files
    ├── test                    
    │   ├── e2e                 # End-to-end tests
    │   └── unit                # Unit tests
    ├── .editorconfig           # Configuration for code editors
    ├── .travis.yml             # Configuration for the Jenkins executor
    ├── jenkins.yml             # Configuration as Code for the Jenkins Runner
    ├── Jenkinsfile             # Configuration for the integration pipeline
    ├── README.md
    └── webpack.config.js       # Configuration for the Webpack source bundler

> Folders with an * are not source code but contains generated files

## Best Practices
### Get instant feedback during development
- Install plugins for your IDE to support `.editorconfig`,  `eslint` for javascript and ` cfn-lint` for cloudformation templates and `prettier` (or beautifier for html and javascript).
- Install `npm install npm-check --save-dev` and add script `"upgrade-interactive": "npm-check --update"` to interactively update the dependencies (to prevent security issues)
### Get feedback after each committed change
- Setup a minimum pipeline which runs unit tests on every git push in feature branches.
- Unit Tests coverage should be above 80%
- Do implement SonarQube as well for static code analysis, improving code quality and security.
### Keep a stable build
### Deliver an optimised product
- Run a Lighthouse Audit and make sure all factors are in green (add PWA and performance best practices)
### Use standards for consistency
- Use the shared styling variables (`team-shared-styling`)
- Implement a `dataLayer` to be consumed by analytics

## Contributing
- Read the [`CONTRIBUTING.md`]('./CONTRIBUTING.md') file for the guidelines
