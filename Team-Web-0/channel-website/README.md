Team Website
===

This project is initialised using: `$ npm init --yes`

## Getting Started
Clone this repository
```
$ git clone git@github.com:rbergenl/enterprise-example.git [folder-name]
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
### Ensure code quality with IDE plugins.
- Install plugins/extensions for your IDE
    - Linting and code styling for javascript, html and css: `prettier`, `.editorconfig` and `eslint`.
    - Linting for CloudFormation templates: `cfn-lint`.
    - Preview Markdown files: `markdown-preview`.
### Get feedback after each committed change
- Setup `prettier` to enforce code styling (checked in the continuous integration pipeline)
- Setup a minimum pipeline which runs unit tests (Jest or Jasmine) on every git push in feature branches.
- Unit Tests coverage should be above 80%
- Do implement SonarQube as well for static code analysis, improving code quality and security.
- If on github, enable automatic security fixes (mostly creating pull request to bump versions of dependencies)
- Continuously ensure product quality by running a Lighthouse Audit (automated via npm). The factors PWA, accessibility and performance should be in green (>90)
### Keep a stable build
- Use the default `npm outdated`, `npm update` and `npm audit` commands to update the dependencies and prevent security issues (use ` --depth 9999` to perform the command on deeper dependency tree). Might first need to remove the current `rm -r ./node_modules package-lock.json`. Also use `npm ls <package>` to see the current state for that package.
### Use standards for consistency
- Use the shared styling variables (`team-shared-styling`)
- Implement a `dataLayer` to be consumed by analytics
## Automate deployment to production
- If deploying to AWS, use a cross-account deployment pipeline. Copy static files to a CDN or deploy a Stack update via CloudFormation.

## Contributing
- Read the [`CONTRIBUTING.md`]('./CONTRIBUTING.md') file for the guidelines
