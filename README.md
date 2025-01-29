# ansible_role_moodle

Repo con archivos para desplegar un Servidor Moodle v4.5.1+

Testeado con Vagrant + qemu + ubuntu_2204 + ansible_2.10

---

### Descripción

La idea del proyecto es automatizar vía ansible la instalación/configuración de un servicio [moodle](https://docs.moodle.org/404/en/Installing_Moodle) para pruebas de laboratorio, el repo cuenta con 3 roles:

1. mariadb
2. apache
3. nginx

### Dependencias

* [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html)
* [Vagrant](https://developer.hashicorp.com/vagrant/install) (opcional)

### Uso
```shell
git clone https://github.com/pgraffigna/ansible_role_moodle.git
cd ansible_role_moodle

# instalar moodle usando apache como webserver
ansible-playbook main.yml --tags mariadb,apache

# instalar moodle usando nginx como webserver
ansible-playbook main.yml --tags mariadb,nginx
```

### Extras
* Archivo de configuración (Vagrantfile) para desplegar una VM descartable con ubuntu-22.04 con libvirt como hipervisor.
  