sbog/tempo
============

Simple role to install tempo

#### Requirements

Ansible 2.4

#### Role Variables

If you use docker swarm, you should specify variables for the host on which
the container is supposed to be run, and also indicate the name of the swarm
manager through which the stack will be deployed in variable
`tempo_swarm_manager`
```yaml
tempo_swarm_manager: swarm-manager01
```

#### Dependencies

None

#### Example Playbook

```yaml
- name: Install and configure tempo
  hosts: tempo
  remote_user: root
  roles:
    - { role: tempo, tags: [ 'tempo' ] }
```

#### License

Apache 2.0

#### Author Information

Stan Bogatkin (https://sbog.org)
