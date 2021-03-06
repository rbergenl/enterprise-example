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
- collect all logging and monitoring data into a Splunk dashboard

## Application
Bigger corporations
- tend to use Java Spring for their server-side code
- tend to use a popular framework like React, Angular or Vue for their client-side code
- are building more and more microservices with NodeJs
- are even going serverless with functions/lambdas

## Marketing
Bigger corporations use lots of different marketing platforms
- A Tag Management System to manage all tool implementations (google tag manager, tealium)
- A Cookie Consent (custom script)
- Analytics (google analytics, facebook pixel)
- A/B Testing (optimizely, visualwebsiteoptimizer)
- Personalisation (blueconic, relay42)
- Retargeting (doubleclick)
- Feedback (usabilla)
- Chat ()

# Teams
Bigger corporations tend to have:
- Centralised teams which set standards, share their code and manage platforms:
  - A team responsible for styling standards, creating a styleguide and reusable code
  - A team responsible for pipeline standards and creating reusable code for to be used by individual teams
  - A team responsible for creating shared components, either for Angular, React or Vue apps
  - A team responsible for marketing, which includes analytics, personalisation, a/b testing, etc.
- A team responsible for a backend microservice or app, mostly a Java application or NodeJs
- A team responsible for a web application or widget, written with either Angular, React or Vue (initialised via CLI)
- A team responsible for the website which share the same header and footer with a portal team
- A team responsible for a portal for which a user should be authenticated

> Channels on the web contain widgets which call services.
> Channels and widgets are styled using definitions in the styleguide.
> Widgets are composed of components from a shared library.
> Platforms deliver content and marketing tools used in different channels.
> Application and widgets are integrated and deployed using shared building blocks for pipelines.

# Channels
The Channels are the interaction points with the customer. The channels are
split over the domain of the organisation via different subdomains and paths.
- Portal Application (jam-stack - nodejs)
- Website Application (java)
- Native Application (react-native)

# Widgets
Widgets are client side applications placed on pages in different channels to provide a UI for interaction with the customer and business services.
- UserRegistration (angular)
- UserLogin (react)
- UserPreferences (vue)

# Services
Services are independent API's which perform actions like storage, retrieval or mutations on data from business systems.
- RegisterUser
- AuthenticateUser (nodejs)
- Preferences (java)

# Platforms
Platforms are tools used by the Business to manage their content and digital marketing activities.
- Content (management of pages, video, images and search (and widgets?))
- Marketing (management of tags for analytics, a/b testing, etc.)

# Libraries
The Libraries are shared code, like UI components to be used by widgets, CI/CD building
blocks to be used by all source code repositories. And Styleguide definitions to be used
for channels, widgets and UI components.
- UI Components Library to be used by and build with the widgets
- CI/CD Building Blocks to be used by the channels, libraries, services,  and widget
- Styleguide definitions (markup and styling) to be used by the channels, libraries and widgets


# Team Web 0
Responsible for hosting a channel, the Website. The website is hosted as a container.
It uses widgets, these files are hosted in a CDN. Widgets might interact with a backend service.
The team as DevOps is responsible for building the channel, and also for maintaining the infrastructure.
