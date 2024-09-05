# Labs
The labs repo is used to deploy containerlab in AWS EC2

## Installation
Install and run poetry
```
poetry shell
```

Run the cmd to start the containerlab ec2 instance
```
ansible-playbook plays/containerlab_ec2_instance.yml --tags start
```

Update the public ip in inventory.yml file then run the cmd to start the lab
```
ansible-playbook plays/lab.yml -i inventory.yml
```

If needed to ssh to EC2 instance, run cmd
```
ssh -i [path to ssh key] [user]@[public ip]
```

Connec to lab device
```
ssh -i [path to ssh key] [user]@[public ip] -p [port]
```

Run the cmd to stop the containerlab ec2 instance
```
ansible-playbook plays/containerlab_ec2_instance.yml --tags stop
```




