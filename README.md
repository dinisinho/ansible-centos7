# Configuración Inicial de Máquinas Centos 7 con ansible

Instala paquetes básicos en Centos7 despois da instalación mínima e instala e configura o cliente de OpenVPN e o NSCLIENT.

Para a súa execución é preciso pasar a través da liña de comandos as variábeis NSCP_PASS, NSCP_HOSTNAME, NSCP_SERVER e OVPN_HOSTNAME.

Tamén é preciso incluír en roles/openvpn/files/{{ OVPN_HOSTNAME }}.tar.gz. Inclúse un de exemplo no repositorio.

Instala os paquetes:
  - bash-completion
  - vim
  - openvpn
  - rsync
  - git
  - bind-utils
  - unzip
  - wget
  - telnet
  - nscp-server
  - libnscp
  - nscp-client
  - nscp-nsca
  - python2-psutil


Exemplo de execución:

ansible-playbook centos7_base.yml --extra-vars '{"NSCP_PASS":"CONTRASINAL","NSCP_HOSTNAME":"dinisinho-ansible","NSCP_SERVER":"dinisinho.eu","OVPN_HOSTNAME":"proba_ansible"}
