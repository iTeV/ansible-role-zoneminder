# Zoneminder

This role installs and configures zoneminder. The zoneminder role is based on this [installation guide](http://zoneminder.readthedocs.io/en/stable/installationguide/debian.html)

# Requirements

This role is currently **only** supported on Debian. Plans for making this role available on more platforms is currently on my to-do list. This role requires Ansible 1.6 or higher to be present. 

# Role variables

A brief description of the variables that are required by this role (define them under defaults/main.yml)

```YAML
# The user that will be used for MySQL operations 
zoneminder_mysql_user: "mysql-user"

# The password for the user 
zoneminder_mysql_password: "supersecretpassword"
```

For security reasons, it's wise to encrypt `defaults/main.yml` with `ansible-vault` since the MySQL password is stored in plaintext. You can find more information about ansible-vault (available from ansible 2.4 and higher) [here](https://docs.ansible.com/ansible/2.4/vault.html)

