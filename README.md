# ansible-role-metricly-agent
An Ansible role to deploy the Metricly agent on a Linux server.

To execute this role, you must first enter your Metricly API key in vars/main.yml
Alternatively, you can include the API key on the command line as an extra variable, using:
```"--extra-vars=metricly_api_key=<your api key>"```
