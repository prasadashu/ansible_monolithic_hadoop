# ansible_monolithic_hadoop
Repository to install Hadoop in monolithic fashion

# Command to run the playbook
ansible-playbook deploy_hadoop.yml --extra-vars "{'host': 'localhost', 'hadoop_version_tar': 'hadoop-2.8.0.tar.gz'}"