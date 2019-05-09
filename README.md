# Ansible Role for Metricly Linux Agent Deployment
## Summary
This is an Ansible role for deploying Metricly's Linux agent.  This role is idempotent and can be used to enforce the agent's configuration state.  Currently, the Red Hat and Debian Linux flavors are supported.
For detailed information on the Linux Agent, please refer to the [online documentation](https://docs.metricly.com/integrations/agents/linux-agent/).

## Prerequisites
- Ansible 2.7.10+ ([install](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html))
- Python (on servers where Ansible will install the agent)

## Setup
##### Basic Instructions
1. Clone the repository
2. Choose whether to use the Simple Collector or Base Collector  ([relevant docs](https://docs.metricly.com/integrations/agents/linux-agent/linux-collectors/))
3. Locate your Metricly API key.  It can be found in the Metricly console at *Integrations > Linux* embedded in a bash command.
3. Configure `metricly-agent/vars/main.yml` to include your collector choice and API key.
4. Include the role in your playbook and run your playbook

##### Configuration Options
**Simple Collector:**
In `metricly-agent/vars/main.yml`, uncomment `#use_simple_collector: True`

**Base Collector:**
No configuration changes required.
If desired, statsd paramaters can be customized in  `metricly-agent/vars/main.yml`
