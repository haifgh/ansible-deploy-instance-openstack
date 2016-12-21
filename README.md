# ansible-deploy-instance-openstack


- Ajustando o ambiente
<pre>
# mkdir /etc/ansible
# cd /etc/ansible
</pre>
- Clonando o repositório
<pre>
# git clone https://github.com/vandocouto/ansible-deploy-instance-openstack.git
</pre>
- Acessando o repositório
<pre>
# cd ansible-deploy-instance-openstack/
</pre>
- Ajustando as variáveis conforme seu ambiente
<pre>
# vim openstack/vars/main.yml
</pre>
<hr>
- Criando a instância 
<pre>
# ansible-playbook site.yml --tags createinstance
</pre>
- Deletando a instância
<pre>
# ansible-playbook site.yml --tags terminateinstance
</pre>
