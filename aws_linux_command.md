### linux common command

du --summarize --human-readable \*

### cloud9

aws ec2 start-instances --instance-ids i-09a833fbb8ff8a345
aws sts get-caller-identity --output text --query Account

### sts

aws sts get-caller-identity

### ec2

aws ec2 describe-instances --query 'Reservations[*].Instances[*].[InstanceId,KeyName]' --output json
aws ec2 describe-instances --filters Name=instance-state-name,Values=running --query Reservations[*].Instances[*].InstanceId
aws ec2 describe-instances --filters Name=instance-state-name,Values=running --query Reservations[*].Instances[*].InstanceId --output text
aws ec2 describe-instances --query 'Reservations[*].Instances[*].[InstanceId]' --filters Name=instance-state-name,Values=running --output text --profile hai

### efs describe

aws efs describe-file-systems
aws efs describe-file-systems --file-system-id
sudo mount -t efs fs-a94aabe9 /mnt/efs
sudo unmount /mnt/efs

### delete images

sudo docker system prune
sudo docker rmi $(sudo docker images -aq) --force
sudo docker build -t IMAGE_TAG_NAME .
sudo docker tag 6be95c7dfb63 IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com/IMAGE_TAG_NAME:latest
sudo docker push IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com/IMAGE_TAG_NAME:latest

### build and push image

sudo docker image rm IMAGE_TAG_NAME
sudo docker image rm IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com/IMAGE_TAG_NAME
sudo docker build -t IMAGE_TAG_NAME .
sudo docker tag f57bd86e74c8 IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com/IMAGE_TAG_NAME:latest

### build a docker image

sudo docker built -t IMAGE_TAG_NAME
.

### aws ecr authenticate

aws ecr get-login-password --region ap-southeast-1 --profile username --profile hai | docker login --username AWS --password-stdin IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com
aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com
aws ecr get-login-password --region ap-southeast-1 --profile username --profile hai | docker login --username AWS --password-stdin 610770234379.dkr.ecr.ap-southeast-1.amazonaws.com

### docker image tag ecr

sudo docker tag f57bd86e74c8 IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com/IMAGE_TAG_NAME:latest

### docker image push ecr

sudo docker push IAM_USER_ID.dkr.ecr.ap-southeast-1.amazonaws.com/IMAGE_TAG_NAME:latest

### network manager linux

ip -c link
sudo ip link set enp0s31f6 up
nmcli radio wifi on
sudo nmtui
sudo apt-get install network-manager-gnome
sudo systemctl enable NetworkManager.service
sudo dhclient enp0s31f6

## ecr

aws ecr describe-repositories
