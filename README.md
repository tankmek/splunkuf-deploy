[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Ftankmek%2Fsplunkuf-deploy&count_bg=%2379C83D&title_bg=%23555555&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)

# cowrie-deploy
Deploys a Splunk Universal Forwarder.

## Requirements
`Ansible >= 2.8`

### Prerequisites: Admin User

This role provisions the initial user with a user-seed.conf file and a hashed password.
The default password is: `spicy_hobbit`. If you would like to change the hash then
edit `splunk.admin_hash` in the roles/splunkuf/default/main.yml

To generate the hash:

```
~> splunk hash-passwd spicy_hobbit
$6$PIjgHyUlZ3MwD5wb$KrPwxv9h2lfwezJiw0UB8HDTmiY9mCIF4Y3kLwRAOrrSk.Njt0Q9PSex0EMYp2v3mi4fH5CdKYo8q9evC4cMg/
```

## Tested On
`Debian 10`

## Usage:
```
ansible-playbook deploy_splunkuf.yml
```
## Role Variables

This role has multiple variables.
The descriptions and defaults for all these variables can be found in the **defaults/** folder of this role:

| Name | Description |
| ---- | ----------- |
| **[`main.yml`](https://github.com/tankmek/splunkuf-deploy/blob/main/roles/splunkuf/defaults/main.yml)** | Splunk UF variables |

