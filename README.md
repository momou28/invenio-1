# invenio
Ansible Playbook to install Invenio
===

Playbook to install Invenio, based on the instructions [here at TIND](http://blog.tind.io/installing-invenio-2-part-1?utm_content=19063243&utm_medium=social&utm_source=linkedin)

## Dependencies:

 * Ansible
 * User ansible with sudo

## Creating a password for your db user

User creation requires that you use root for mysql, the very least you can do is to encrypt it or better yet, to use vault

*To encrypt using Python crypt*

```python
import crypt
crypt.crypt('mysqlrootpass', '$6$MySQLInv3ni0$')
```

## Running the playbook

This step is quite simple:
`cd invenio; ansible-playbook -i playbook/inventory playbook/playbook.yml`
