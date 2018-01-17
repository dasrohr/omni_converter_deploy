# To use this
you need a inventory-file named like 'hosts.yml' with the content, similar to:
```
---
all:
  hosts:
    [target_host_here]:
      ansible_user: root
```
you have to specify this file when running ansible:
`ansible-playbook omni_play.yml -i hosts.yml`

you have to make sure that you `.ssh/config` matches the _'target_host_name'_ in 'hosts.yml' and that the ssh-options, such as `IdentityFile`, `Port`, etc are set correctly.

This playbook connects as ssh-user `root` at this stage. Make sure you sshd allows connections as user `root`