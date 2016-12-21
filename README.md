# ansible-deploy-instance-openstack

- Pacotes necessários para o Ansible (CentOS7)
<pre>
# yum install curl gcc openssl-devel python-devel unzip git -y
</pre>
- Instalando o Ansible
<pre>
# pip install ansible
# ansible --version
ansible 2.2.0.0
  config file = 
  configured module search path = Default w/o overrides
</pre>
<hr>
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
