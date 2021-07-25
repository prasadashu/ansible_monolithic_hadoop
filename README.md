# ansible_monolithic_hadoop
Repository to install Hadoop in monolithic fashion

## How to run the playbook?
- Install Ansible in RedHat based distros.

`sudo yum install -y ansible`

- Clone this repo.

`git clone https://github.com/prasadashu/ansible_monolithic_hadoop.git`

- Run the playbook.

`ansible-playbook deploy_hadoop.yml -i inventory/inventory.txt --extra-vars "{'usr_password': 'hadoopusr_pass'}"`

## Repository details

- The Hadoop user password is to be passed at run time.
- Below are the configurations applied to the playbook.
- These configurations can be modified in the `host_vars/hadoop_monolithic_server` file.

### 1. Hadoop version
- The default version of Hadoop set to install is **hadoop-2.8.0**.
- Replace the value of the variable `hadoop_version` with the desired Hadoop version.

### 2. Java version
- The default version of Java set to install is **java-1.8.0-openjdk-devel**.
- Replace the value of the variable `java_version` with the desired Java version.

### 3. Password salt
- Replace the value of the variable `password_salt` with the desired Java version.

**NOTE:** Do check for dependencies before making any changes to the configurations!