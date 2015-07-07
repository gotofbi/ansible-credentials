# ansible-credentials

Setting up file-based credentials for a UNIX system.

[![Platforms](http://img.shields.io/badge/platforms-ubuntu-lightgrey.svg?style=flat)](#)
[![Platforms](http://img.shields.io/badge/platforms-osx-lightgrey.svg?style=flat)](#)

## Tunables
- `credentials_user` (string) - The user to override credentials for.
- `credentials_group` (string) - The group that the given user belongs to.
- `credentials_home_path` (string) - The home path for the given user.
- `credentials_id_rsa` (string) - The private key for the user.
- `credentials_known_hosts` (string) - The known hosts for the user.
- `credentials_aws_access_key_id` (string) - The AWS Access Key for the user.
- `credentials_aws_secret_access_key` (string) - The AWS Secret Access Key for the user.

## Example Playbook
```
- hosts: servers
  roles:
    - role: telusdigital.credentials
      credentials_user: ci-bot
      credentials_id_rsa: "{{ id_rsa }}"
      credentials_known_hosts: "{{ known_hosts }}"
```

## License
[MIT](https://tldrlegal.com/license/mit-license)

## Contributors
- [Justin Scott](https://jvscott.net) | [e-mail](mailto:jvscott@gmail.com) | [Twitter](https://twitter.com/AKindlyOrc)
