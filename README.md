# Ansible Role: Bitcoin Core

[![CircleCI](https://circleci.com/gh/lifeofguenter/ansible-role-bitcoin-core.svg?style=svg)](https://circleci.com/gh/lifeofguenter/ansible-role-bitcoin-core)

An Ansible role that compiles and installs bitcoind, bitcoin-cli and bitcoin-tx (e.g. headless) on Debian like systems.

## Requirements

none

## Role Variables

- `bitcoin_version: 25.0`

- `bitcoin_user: bitcoin`

- `bitcoin_home: "/home/{{ bitcoin_user }}"`

- `bitcoin_conf_datadir: "{{ bitcoin_home }}"`

- `bitcoin_conf_pid: /run/bitcoind/bitcoind.pid`

See https://en.bitcoin.it/wiki/Running_Bitcoin#Bitcoin.conf_Configuration_File for more options (prefix them with `bitcoin_conf_`)

## Dependencies

none

## Example Playbook

```
- hosts: miner
  roles:
    - { role: lifeofguenter.bitcoin_core }
```

## Munin Plugin

For this the munin-plugin to work, add the following override:

`/etc/systemd/system/munin-node.service.d/override.conf`

```ini
[Service]
ProtectHome = read-only
```

## Thank you

- Cédric Félizard ([infertux](https://github.com/infertux)) for [munin-bitcoin](https://github.com/infertux/munin-bitcoin)

## License

[MIT](LICENSE)
