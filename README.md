## cacti-client

[![Build Status](https://travis-ci.org/Oefenweb/ansible-cacti-client.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-cacti-client) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-cacti--client-blue.svg)](https://galaxy.ansible.com/list#/roles/5697)

Set up a machine (client) so it can be monitored by cacti (server).

#### Requirements

None

#### Variables

* `cacti_client_user`: [default: `cacti`]: The user that the cacti server will use to login
* `cacti_client_group`: [default: `cacti`]: The primary group of the cacti user
* `cacti_client_groups`: [default: `[]`]: The secondary groups of the cacti user

* `cacti_client_authorized_keys`: [default: `[]`]: Authorized key declarations
* `cacti_client_authorized_keys.{n}.src`: [required]: The local path of the key
* `cacti_client_authorized_keys.{n}.state`: [optional, default: `present`]: State

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - cacti-client
    vars:
      cacti_client_authorized_keys:
        - src: ../../../files/cacti-client/etc/cacti/id_rsa.pub
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-cacti-client/issues)!
