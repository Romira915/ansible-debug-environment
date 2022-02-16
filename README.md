# ansible-debug-environment

Development environment for debugging and verifying ansible.

## Usage

1. start up

```shell
docker-compose up --build
```

2. connect

```shell
docker exec -it ansible bash
```

3. exec ansible

```shell
ansible-playbook -i inventry.ini playbook.yml
```