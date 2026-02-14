# ansible-roboshop
ansible-roboshop

- Have to install `sudo dnf install ansible` before running the ansible playbook
- Have to install `pip3.9 install botocore boto3` before running the ansible playbook
- `aws configure`

### To launch EC2 instances 
```shell
ansible-playbook -i localhost, \
 -e '{ "INSTANCES":["mongodb", "catalogue", "redis", "user", "cart", "mysql", "shipping", "rabbitmq", "payment", "frontend"]}' \
  roboshop.yaml
```

### Delete Route53 Records and EC2 instances
```shell
ansible-playbook -i localhost, \
 -e '{ "INSTANCES":["mongodb", "catalogue", "redis", "user", "cart", "mysql", "shipping", "rabbitmq", "payment", "frontend"], "ACTION": "destroy"}' \
  roboshop.yaml
```


```shell
ansible-playbook -i localhost, \
 -e '{ "INSTANCES":["mongodb", "catalogue"]}' \
  roboshop.yaml
```

#### Commands to run for each playbook
- `ansible-playbook -i inventory.ini mongodb.yaml`
- `ansible-playbook -i inventory.ini catalogue.yaml`
- `ansible-playbook -i inventory.ini redis.yaml`
- `ansible-playbook -i inventory.ini user.yaml`
- `ansible-playbook -i inventory.ini cart.yaml`
- `ansible-playbook -i inventory.ini mysql.yaml`
- `ansible-playbook -i inventory.ini shipping.yaml`
- `ansible-playbook -i inventory.ini rabbitmq.yaml`
- `ansible-playbook -i inventory.ini payment.yaml`
- `ansible-playbook -i inventory.ini frontend.yaml`