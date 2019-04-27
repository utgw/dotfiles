# dotfiles
## apply

Prepare `hosts` file such that:

```
[server]
server1
server2
localhost ansible_connection=local
```

```console
$ pip install pipenv # if you have not installed pipenv
$ pipenv install
$ pipenv run ansible-playbook -i ./hosts playbooks/*.yml
```

Note that servers in `./hosts` can be connected with SSH (except localhost).

## apply locally

```console
$ pipenv run ansible-playbook -c local -i localhost, playbooks/*.yml
```
