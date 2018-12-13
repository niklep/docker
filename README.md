# docker

This role installs and configures Docker

## Requirements

Debian

## Role Variables

| Name                      | Default / Mandatory | Description                                                                                                                                                                            |
|:--------------------------|:-------------------:|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `docker_daemon_config`    | `{}`                | Docker daemon configuration ([reference](https://docs.docker.com/engine/reference/commandline/dockerd/#daemon-configuration-file]) which is directly written to the configuration JSON |
| `docker_privileged_users` | `[]`                | List of users to be added to the docker group                                                                                                                                          |

## Example Playbook

```yml
- hosts: build
  roles:
    - role: docker
      docker_privileged_users:
        - jenkins
      docker_daemon_config:
        mtu: 1400
```

## License

This work is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

## Author Information

- [Janne Heß](https://github.com/dasJ)
