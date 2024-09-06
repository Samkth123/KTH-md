
## Deploying on Railway

Point Railway to your deployment source and let the platform handle the rest.

### Flexible Deployment Sources
- **Code repositories**: With or without Dockerfiles. Railway will build an OCI compliant image based on what you provide
	- **OCI compliant image**
		- **The Open Container Initiative** is an open governance structure for the express purpose of creating open industry standards around container formats and runtimes. Established in June 2015 by Docker and other leaders in the container industry


### Development lifecycle

Software development extends far beyond code deployment. Railway's feature set is tailor-made, and continuously evolving, to provide the best developer experience we can imagine.

**Configuration Management:**
- **Variables and Secrets:**
	- Easily manage configuration values and sensitive data with variable management tools

**Environment and Workflow:**
- **Environment Management**
	- Create both **static and ephemeral environments** to create workflows that complement your processes
		- A **static environment** is a fixed, stable deployment setup where the configuration and infrastructure do not change frequently. Once set up, it remains consistent unless manually updated
		- An **ephemeral environment** is temporary and often dynamically created and destroyed as needed. It is usually used for specific tasks like testing or development, where a fresh environment is needed for each session
- ==Orchestration & Tooling==: Build Railway into any workflow using **CLI** or **API**

**Deployment Monitoring:**
- **Observability**:
	- Keep a pulse on your deployments with Railways built-in observability tools

## The Basics

### In a Nutshell

- **[Dashboard](https://docs.railway.app/overview/the-basics#dashboard--projects)** - Main entrypoint for all projects under your account.
- **[Project](https://docs.railway.app/overview/the-basics#project--project-canvas)** - A collection of services under the same network.
    - **[Project Settings](https://docs.railway.app/overview/the-basics#project-settings)** - Contains all project-level settings.
- **[Service](https://docs.railway.app/overview/the-basics#services)** - A target for a deployment source (e.g. Web Application).
    - **[Service Variables](https://docs.railway.app/overview/the-basics#service-variables)** - A collection of configurations and secrets.
    - **[Service Metrics](https://docs.railway.app/overview/the-basics#service-metrics)** - Rundown of metrics for a service.
    - **[Service Settings](https://docs.railway.app/overview/the-basics#service-settings)** - Contains all service-level settings.
- **[Deployment](https://docs.railway.app/overview/the-basics#deployments)** - Built and deliverable unit of a service.
- **[Volumes](https://docs.railway.app/overview/the-basics#volumes)** - Persistent storage solution for services.
    - **[Volume Metrics](https://docs.railway.app/overview/the-basics#volume-metrics)** - Rundown of metrics for volumes (e.g. disk usage over time).
    - **[Volume Settings](https://docs.railway.app/overview/the-basics#volume-settings)** - Contains all volume-level settings.

#### Dashboard
Dashboard is the main entrypoint to Railway where all projects are shown in the order they where last opened

Projects contain your services and environments

#### Project / Project Canvas

A project represents a capsule for compsing infrastructure in Railway. Think of a project as an application stack, a service group, or even a collection of service groups.

Services within a project are automatically joined to a private network scoped to that project
##### Project setting
Page that contain all the project level settings.
Common project settings are:
- **Transfer project** - transfer your project between workspaces
- **Environments** - Manage various setting regarding environments
- **Members** - Add or remove members to collaborate on your project
==- **Danger** - Remove individual services or delete the entire project==

#### Services

A Railway service is a deployment target for your deployment source. Deployment sourves can be **code repositories** or Docker images. ==Once you create a service and choosen a source, Railway will analyze the source, build a Docker image (if you source is a code repository) and deploy it to the service==

Out of the box, your service is deployed with a set of default configurations which can be overridden as needed

#### Service Variables

Service Variables provide a powerful way to manage configuration and secrets across services in Railway

You can configure variables scoped to services or to projects to be shared amongst all services

#### Service Metrics

==Service Metrics provide an essential overview of CPU, memory, and network usage for a given service==

#### Service Settings
This tab contains all the service level settings

- ==Source - Here you can configure the deployment source ,which can be either a GitHub repository== with a specific branch or an image with optional credentials
- ==Networking - Generate a Railway-provided domain== or add your custom one
- Custom Build Command - Here you can configure a custom build command if you need to overwrite the default, only applicable with Nixpacks based builds
- Custom Start Command - Here you can configure a custom start command if you need to overwrite the default.

## Advanced Usage

### Deploy Options

Deployments are created with some default options that can be overridden. Some of the options available are -

- Replicas: By default, your deployment will go out with a single instance. With replicas, you have the ability to scale up your deployment instances
- Deployment Region: ==Deployments are pushed to the 'us-west1' region unless a different region is specified==
- Scheduled Execution...
- App Sleep: Services are serverful and always-on. You can control this behavior, to spin down resources when they are not being used, by enabling App Sleep.


### Networking

#### Private Netoworking
Private networking is a feature within R