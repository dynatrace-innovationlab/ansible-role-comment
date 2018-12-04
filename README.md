# Ansible Role: Dynatrace Comment

This role will send a comment to a Dynatrace problem ticket.

## Download

The role is available via:

- Ansible Galaxy
- GitHub

## Configuration

Please find below a list of variables that have to be configured:

| Name            | Default | Description
|-----------------|---------|------------
| tenant_url      |         | URL of your Dynatrace tenant
| api_token       |         | API Token from your Dynatrace tenant
| problem_id      |         | Problem ID of the Dynatrace problem ticket you want to comment on
| comment         |         | actual comment text
| user            | Ansible | user the comment is sent from (String or email address)
| context         | Ansible | context the comment was sent from


## Usage (Example):

```yaml
---
- hosts: localhost
  vars:
    tenant_url: 'https://XXXXXX.live.dynatrace.com'
    api_token: 'XXXXX'

  tasks:
  - include_role:
      name: dynatrace_problem_comment
    vars:
      problem_id: 'XXXX'
      comment: 'Hello from Ansible'
      user: 'your@email.com'
      context: 'Ansible'

```
