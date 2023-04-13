# Install docker with Vagrant

## Requirements

- Install vagrant
- Install VirtualBox

## install 

```bash
vagrant up 
```

### Conection with virtual machine

```bash
vagrant ssh
docker ps #validate docker install in virtual machine
```

### Add image nginx for validation
```bash
docker -H 192.168.56.20 run -p 8080:80 nginx:alpine
```

### Working with volumens

```bash
docker -H 192.168.56.20 run -d -v  /home/vagrant/docker:/usr/share/nginx/html -p 8080:80 nginx:alpine
```
