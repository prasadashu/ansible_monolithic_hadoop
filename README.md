# ansible_monolithic_hadoop
Repository to install Hadoop in monolithic fashion

# Command to run the playbook
ansible-playbook deploy_hadoop.yml --extra-vars "{'host': 'localhost', 'hadoop_version': 'hadoop-2.8.0', 'java_version': 'java-1.8.0-openjdk-src.x86_64'}"