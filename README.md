# Ansible Role: Dynatrace Comment

This role allows to send comments to Dynatrace.

### Usage (Example):

```yaml
- hosts: localhost
  vars:
    tenant_url: 'https://XXXXXX.live.dynatrace.com'
    api_token: 'XXXXX'


  tasks:
  - include_role:
      name: dynatrace_comment
    vars: 
      problem_id: ''
      comment: 'Hello from Ansible'

```
