# ansible-webstite
CloudFormation and Ansible scripts that create AWS resources and set up APACHE server


### Prerequisites

You need to have AWS account as well as Ansible set up on your computer.

### Running
* Create the CloudFormation stack using the awssetup.yaml.
* Change the KEY_PATH in the ansible.cfg file to point to the .pem file of the AWS keypair that Ansible will use to connect to the instances.
* change the webservers PublicIP addresses in hosts-dev file to your EC2 instances created via CloudFormation template.

```
ansible -i hosts-dev --list-hosts all
ansible -m ping all
ansible-playbook setup-app.yml
```
