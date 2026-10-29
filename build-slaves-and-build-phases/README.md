# Build Slaves and Build Phases in DevOps

A student project demonstrating Jenkins build agents (also called build slaves in older terminology) and a staged CI/CD pipeline.

## Project objectives

- Understand how a Jenkins controller assigns work to build agents.
- Organize a software workflow into pipeline stages.
- Demonstrate source checkout, build, testing, packaging, and a deployment placeholder.
- Review build results and console logs in Jenkins.

## Technologies

- Jenkins
- Jenkins Pipeline (`Jenkinsfile`)
- Git and GitHub
- Shell commands on a Linux-compatible Jenkins agent

## Pipeline stages

1. **Source Code Checkout** — checks out the configured source repository.
2. **Build Phase** — creates a sample application file.
3. **Testing Phase** — checks that the generated file exists and is not empty.
4. **Packaging Phase** — creates `application.tar.gz` and archives it in Jenkins.
5. **Deployment Phase** — demonstration placeholder; no real deployment is configured.

## Requirements

- A Jenkins controller
- A connected Jenkins agent with the label `build-slave`
- A Git repository configured as the Jenkins job's SCM
- A Linux-compatible agent with `sh` and `tar`

## Run in Jenkins

1. Push this repository to GitHub.
2. In Jenkins, create a Pipeline job.
3. Configure the job to use this GitHub repository.
4. Use **Pipeline script from SCM** and select **Git**.
5. Set the Script Path to `Jenkinsfile`.
6. Ensure an online agent has the label `build-slave`.
7. Run **Build Now** and inspect **Console Output** and the stage view.

## Notes

- The deployment stage only prints a message. It does not deploy to a server or cloud service.
- The pipeline uses `checkout scm`, so it is intended to run as a Pipeline job configured from source control.
- The accompanying report is in `docs/P9-DevOps.pdf`.
