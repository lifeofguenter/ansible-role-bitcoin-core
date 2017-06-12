[![Build Status](https://travis-ci.org/lifeofguenter/ansible-role-bitcoin-core.svg?branch=master)](https://travis-ci.org/lifeofguenter/ansible-role-bitcoin-core)

# Ansible Role: Bitcoin Core

An Ansible role that compiles and installs bitcoind, bitcoin-cli and bitcoin-tx (e.g. headless) on Debian like systems.

## Requirements

none

## Role Variables

- `bitcoin_version: 0.14.1`

- `bitcoin_user: bitcoin`

## Dependencies

none

## Example Playbook

```
- hosts: miner
  roles:
    - { role: lifeofguenter.bitcoin-core }
```

## License

[MIT](LICENSE)
