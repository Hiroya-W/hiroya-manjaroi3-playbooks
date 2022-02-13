# hiroya-manjaroi3-playbooks

This is Ansible playbook meant to provision a personal machine running Manjaro Linux.
It is intended to run locally on a fresh Manjaro Linux.

- Target Distro: Manjaro Linux
- WM: i3-gaps

See also [Hiroya-W/dotfiles](https://github.com/Hiroya-W/dotfiles).

## Install dependencies

Install Ansible in the Python virtual environment using poetry.

```bash
poetry install
```

Install roles and collections from Ansible Galaxy.

```bash
make deps
```

## Run playbook

First, you need to create a user to build the AUR packages.
And update the mirror.

```bash
make init
```

Next, start the provisioning.

```bash
make playbook
```

You can use the tags defined in the playbook to execute only specific roles.

```bash
make playbook args="--tags HERE_TAGS"
```
