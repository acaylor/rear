ReaR
=========

This role is for backing up systems to nfs storage

Currently this supports:

- Red Hat family distributions (including fedora)
- Debian family distributions


Requirements
------------

You need a system with ansible installed.

Example Playbook
----------------

```yaml
---
# target all inventory hosts, you could use inventory groups instead
- hosts: all
  # Many tasks here require root access
  become: yes
  vars:
    # Configure backup cron job which minute to execute
    rear_cron_min: "0"
    # Configure backup cron job which hour to execute
    rear_cron_hour: "0"
    # Configure NFS server to backup to
    nfs_server: "server.example.com"
    # Configure NFS share to backup to
    nfs_dir: "foo/bar"
  roles:
    - rear
```

License
-------

BSD

