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
├── src                     
|   ├── components          # Javascript components
|   └── themes              # Sass files
├── test                    
│   ├── e2e                 # End-to-end tests
│   └── unit                # Unit tests
├── .editorconfig
├── Jenkinsfile
└── README.md

> Folders with an * are not source code but contains generated files

## Best Practices
- Install plugins for your IDE to support `.editorconfig` and `eslint`.
- Setup a minimum pipeline which runs unit tests on every git push in feature branches.
- Unit Tests coverage should be above 80%
- Use the shared styling variables (`team-shared-styling`) and shared react components (`team-shared-react`)
- Implement a `dataLayer` to be consumed by analytics

## Contributing
- Read the `CONTRIBUTING.md` file for the guidelines
