[![CI](https://github.com/StoneSoupKitchen/ansible-role-chrony/actions/workflows/ci.yml/badge.svg)](https://github.com/StoneSoupKitchen/ansible-role-chrony/actions/workflows/ci.yml)

# Ansible role: chrony

An Ansible role for configuring chrony.

## Requirements

Supported operating systems:
* Debian 10 (Buster)
* Debian 11 (Bullseye)

## Role Variables

The following table lists all variables that can be overridden
and their default values.

| Name                     | Default Value | Description                      |
| ------------------------ | ------------- | -------------------------------- |
| `chrony_package` | chrony | Name of the chrony package. Use `name=ver` format to pin. |
| `chrony_package_state` | present | Installation state for the chrony package. |

## Examples

```yaml
- hosts: all
  roles:
    - stonesoupkitchen.chrony
```

## Development

A Makefile is included for easier development with `pipenv`.
After cloning this repository,
use the following commands to set up an environment.

    pipenv install --dev

To lint your changes with ansible-lint:

    make lint

To run tests with molecule:

    make test

## License

See [LICENSE](./LICENSE).

