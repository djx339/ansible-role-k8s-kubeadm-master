Ansible Role: kubernetes kubeadm master
=========

Using kubeadm setup a kubernetes master.

Requirements
------------

- kubeadm installed.

Role Variables
--------------

`k8s_network_conf_file`: The kubernetes network config file.
Default: https://raw.githubusercontent.com/romana/romana/master/containerize/specs/romana-kubeadm.yml

`k8s_kubeadm_init_args`: The arguments for `kubeadm init`. Default is empty

`k8s_master_as_node`: If schedule pods on master. Default: `True`

Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: all
  become: yes
  roles:
    - { role: djx339.k8s-kubeadm-master }
```

License
-------

BSD

Author Information
------------------

This role was created by [Daniel D](https://github.com/djx339).
