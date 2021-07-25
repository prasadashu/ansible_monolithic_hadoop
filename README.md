# ansible_monolithic_hadoop
Repository to install Hadoop in monolithic fashion

# Command to run the playbook
ansible-playbook deploy_hadoop.yml --extra-vars "{'host': 'localhost', 'hadoop_version': 'hadoop-2.8.0', 'java_version': 'java-1.8.0-openjdk-devel', 'usr_password': 'hadoopusr_pass', 'password_salt': '$1$TinchOfSalt$'}"