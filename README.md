# Ansible playground

## About
This repo is dedicated to Ansible HW

## Prerequisites
Let's assume have 3 servers with different operating systems:
- Alpine
- Debian
- NetBSD

And we are to create IaC with Ansible to easily deploy FreeLABorga application on all our machines

## Project structure
```
.
├── README.md
├── README.pdf
├── src
│   ├── host_vars - the secrets are stored here
│   ├── inventory.yaml - hosts connection description
│   └── playbook.yaml - application installation and run scripts
└── templates
    └── freelaborga.service.j2 - systemd template
```

## Run scripts
Before running the scripts be sure to prepare configs in host_vars:
- Create alpine.yaml, debian.yaml and net_bsd.yaml
- Fill the configs according to examples

When configs are ready - run the following command:
```shell
ansible-playbook -i src/inventory.yaml src/playbook.yaml
```

## Infrastructure completeness
- Alpine
  - [X] Ping
  - [ ] Dependencies installation
  - [ ] Project installation
  - [ ] Project run
- Debian
  - [X] Ping
  - [X] Dependencies installation
  - [X] Project installation
  - [X] Project run
- NetBSD
  - [X] Ping
  - [ ] Dependencies installation
  - [ ] Project installation
  - [ ] Project run
