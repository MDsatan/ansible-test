# Ubuntu 22 CIS

## Configure a Ubuntu 22 machine to be [CIS](https://www.cisecurity.org/cis-benchmarks/) compliant

### Based on CIS Ubuntu Linux 22.04 LTS Benchmark v1.0.0 [Release](https://learn.cisecurity.org/l/799323/2022-09-15/3l9d2k) and Ansible Lockdown [Repository](https://github.com/ansible-lockdown/UBUNTU22-CIS)


## Considerations:
1) Role has been optimised to use only for Ubuntu Desktop 22.04 LTS. It is not recommended to use it for other versions of Ubuntu.
2) Any tags and checks, except <b>workstation-level1</b> are excluded from the role. So, there's no support for tags from original repository.
3) Inventory and playbook are configured to run the role on localhost. If you want to run it on remote host, please change the inventory file accordingly.

## Dependencies
 - <b>Ansible 2.9.6</b>
 - Account with <b>sudo</b> privileges

## Usage
1. Clone the repository
2. Run the playbook

```
ansible-playbook -i inventory site.yml -K

```

## Known issues
- 5.4.2 | AUDIT | Ensure lockout for failed password attempts is configured | <b>Partially implemented</b>