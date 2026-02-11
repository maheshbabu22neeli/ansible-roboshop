# ansible-roboshop
ansible-roboshop



- Have to install `sudo dnf install ansible` before running the ansible playbook
- Have to install `pip3.9 install botocore boto3` before running the ansible playbook
- `aws configure`
- To launch EC2 instances `ansible-playbook -i localhost, -e '{ "INSTANCES":["mongodb", "catalogue", "redis", "user", "cart", "mysql", "shipping", "rabbitmq", "payment", "frontend"]}'  roboshop.yaml`