# ansible-deploy-instance-openstack


- Ajustando o ambiente
<pre>
# mkdir /etc/ansible
# cd /etc/ansible
</pre>

<pre>
# git clone https://github.com/vandocouto/ansible-deploy-instance-openstack.git
</pre>

<pre>
# cd ansible-deploy-instance-openstack/
</pre>

<pre>
# vim openstack/vars/main.yml
</pre>


Criando a instância 
<pre>
# ansible-playbook site.yml --tags createinstance
 [WARNING]: Host file not found: /etc/ansible/hosts

 [WARNING]: provided hosts list is empty, only localhost is available


PLAY [Openstack Instance] ******************************************************

TASK [setup] *******************************************************************
ok: [localhost]

TASK [openstack : Criando uma instância no OpenStack] **************************
changed: [localhost]

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0 
</pre>

Deletando a instância
<pre>
# ansible-playbook site.yml --tags terminateinstance
 [WARNING]: Host file not found: /etc/ansible/hosts

 [WARNING]: provided hosts list is empty, only localhost is available


PLAY [Openstack Instance] ******************************************************

TASK [setup] *******************************************************************
ok: [localhost]

TASK [openstack : Destruindo uma instância no OpenStack] ***********************
changed: [localhost]

PLAY RECAP *********************************************************************
localhost                  : ok=2    changed=1    unreachable=0    failed=0 
</pre>
