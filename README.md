# ansible_role_wordpress

Playbook para desplegar un Servidor Moodle.

Testeado con Vagrant + qemu + ubuntu_2004/2204 + ansible_2.10

---

### Descripción

La idea del proyecto es automatizar vía ansible la instalación/configuración de un servicio [moodle](https://docs.moodle.org/404/en/Installing_Moodle) para pruebas de laboratorio, el repo cuenta con 3 roles:

1. mariadb
2. apache
3. moodle

### Dependencias

* [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html)
* [Vagrant](https://developer.hashicorp.com/vagrant/install) (opcional)

### Uso

```
git clone https://github.com/pgraffigna/ansible_role_moodle.git
cd ansible_role_moodle
ansible-playbook main.yml
```

### Extras
* Archivo de configuración (Vagrantfile) para desplegar una VM descartable con ubuntu-22.04 con libvirt como hipervisor.

### Uso Vagrant (opcional)
```
vagrant up
vagrant ssh
```