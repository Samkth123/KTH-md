
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
    - Projects contain your services and environments
- **[Service](https://docs.railway.app/overview/the-basics#services)** - A target for a deployment source (e.g. Web Application).
    - **[Service Variables](https://docs.railway.app/overview/the-basics#service-variables)** - A collection of configurations and secrets.
    - **[Service Metrics](https://docs.railway.app/overview/the-basics#service-metrics)** - Rundown of metrics for a service.
    - **[Service Settings](https://docs.railway.app/overview/the-basics#service-settings)** - Contains all service-level settings.
- **[Deployment](https://docs.railway.app/overview/the-basics#deployments)** - Built and deliverable unit of a service.
- **[Volumes](https://docs.railway.app/overview/the-basics#volumes)** - Persistent storage solution for services.
    - **[Volume Metrics](https://docs.railway.app/overview/the-basics#volume-metrics)** - Rundown of metrics for volumes (e.g. disk usage over time).
    - **[Volume Settings](https://docs.railway.app/overview/the-basics#volume-settings)** - Contains all volume-level settings.

##