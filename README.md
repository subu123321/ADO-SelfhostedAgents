# ado-agent

This project can be used to setup a docker hosted Azure DevOps agent. It will
start an Ubuntu Linux self-hosted agent.

---

## Installation Steps:

+ Edit the values in agent.env for your Azure DevOps account.

    - Use your own token from ADO -> User settings -> Personal access tokens.
The public access token needs the following custom scopes accessible by
choosing "Show all scopes".
Scopes:
    * Agent Pools (Read & manage)
    * Deployment Groups (Read & manage)

+ Start the agent:
    - ```bash
         export COMPOSE_FILE=development.yml
         docker-compose build --pull
         docker-compose up -d
    ```
