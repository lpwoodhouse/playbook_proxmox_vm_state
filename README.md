# Ansible Play: proxmox_vm_state

## Purpose

This play is for changing the power state of a pve hosted virtual machine guest
(eg stopped, restarted)

## Requirements

community.general

## Role Variables

Default role variables for the pve_vm_state role are listed below (see ```defaults/main.yml```)
```shell
proxmox_host: 192.168.0.1
proxmox_user: root@pam
proxmox_password: password
vm_guest:
  - name: vm01
    state: started # options: present,stopped,started,absent,restarted,current
  - ...etc...
```
## Dependencies

None

## Example Playbook
```yaml
    - hosts: localhost
      roles:
        - pve_vm_state
```

## License

MIT

## Author Information

This role was created in 2022 by [Lee Woodhouse](https://www.leewoodhouse.com/)
