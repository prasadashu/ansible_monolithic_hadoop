# ansible_monolithic_hadoop
Repository to install Hadoop in a monolithic fashion.

## How to run the playbook?
- Install Ansible in RedHat based distros.

`sudo yum install -y ansible`

- Clone this repo.

`git clone https://github.com/prasadashu/ansible_monolithic_hadoop.git`

- Run the playbook.

`ansible-playbook deploy_hadoop.yml -i inventory/inventory.txt --extra-vars "{'host': 'hadoop_monolithic_server', 'usr_password': 'hadoopusr_pass'}"`

## Repository details

- The Hadoop user password is to be passed at run time.
- The Hadoop username is *hadoopusr*. (Will make this dynaminc)
- Below are the configurations applied to the playbook.
- These configurations can be modified in the `host_vars/hadoop_monolithic_server` file.

**NOTE:** Do check for dependencies before making any changes to the configurations!

### 1. Hadoop version
- The default version of Hadoop set to install is **hadoop-2.8.0**.
- Replace the value of the variable `hadoop_version` with the desired Hadoop version.

### 2. Java version
- The default version of Java set to install is **java-1.8.0-openjdk-devel**.
- Replace the value of the variable `java_version` with the desired Java version.

### 3. Password salt
- Replace the value of the variable `password_salt` with the desired Java version.

## Working with Hadoop
### 1. Switch user to *hadoopusr*.

- Switch user to *hadoopusr* if under any other user.

`su hadoopusr`

### 2. Create a sample file to be uploaded to HDFS.

- The sample file may optionally be filled with some details.

`touch sample_file.txt`

### 3.Create a user space under HDFS

`hdfs dfs -mkdir -p /user/hadoopusr`

### 4. Upload the sample file to HDFS

`hdfs dfs -copyFromLocal sample_file.txt /user/hadoopusr`