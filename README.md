# dotfiles
Configuration files and setup (installation of packages, plugins...) of a desktop environment using Ansible

## Installation
```sh
ansible-pull -U https://github.com/BerniR4/dotfiles.git
```
OR
```sh
git clone https://github.com/BerniR4/dotfiles.git
cd dotfiles
ansible-playbook local.yml
```

By default, ansible will create a new user (named `default`) but, if this needs to be changed, the `--extra-vars` option can be used to pass the required username:
```sh
ansible-playbook local.yml --extra-vars "username=test_user"
```
Please note that the user will have sudo permissions.

Additionally, there is the option to only set up the "terminal environment" with the `--tag cli`:
```sh
ansible-playbook local.yml --tags cli
```