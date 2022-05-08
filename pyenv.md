# Setup pyenv and python with specific version for linux 



## Update Amzon linux 
epel and amazon-linux-extras 
```shell 
sudo yum-config-manager --enable epel
```
and 
```shell 
sudo yum install -y amazon-linux-extras

```
enable repositories 
```shell 
yum repolist all
```
and 
```shell 
sudo yum-config-manager --enable amzn-main-debuginfo/latest
```
install some packages 
```
sudo yum install sqlite-devel
sudo yum install readline-devel
```


## Install gcc for amazon linux 

```shell 
sudo yum groupinstall "Development Tools"
```
and 
```
sudo yum -y update
sudo yum -y groupinstall "Development Tools"
sudo yum -y install openssl-devel bzip2-devel libffi-devel
```

## Clone pyenv 
```shell 
curl https://pyenv.run | bash
```

path to ~/.bashrc 
```shell 
export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init --path)"
eval "$(pyenv virtualenv-init -)"
```

test 
```
pyenv install 3.8.2 
```

set global version python 
```shell 
pyen global 3.8.12 
```

### Install python from source 
wget
```shell 
sudo yum -y install wget
```
get python 
```
wget https://www.python.org/ftp/python/3.8.12/Python-3.8.12.tgz
```
extract 
```shell 
tar xvf Python-3.8.12.tgz
```
configure 
```
cd Python-3.8*/
./configure --enable-optimizations
sudo make altinstall
```
