# CircleCI Pipeline

## Pipeline is configured in config.yml and it contains 3 main components:

- orbs and it responsible for including the services are used
- Jobs and it contains two main parts:
  - build and it's responsible for installing the dependeincies, linting and building the backend and frontend
  - Deploy the application after successful installation
- Workflow and it's responsible for configuring the workflow:
  - Build
  - Hold and wait for manual approval
  - Deploy

Pipeline starts automatically after git push the the connected repo
