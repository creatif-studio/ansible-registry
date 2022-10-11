# CloudBoz Registry
Hosting your own Docker Hub

# Requirements
- Install `docker` and `docker-compose`
- Install `apache2-utils` and `libnss3-tools`
- Install `homebrew` and `mkcert`

# How to use?
- Install requirements
- Clone this repository
- Go to this directory `nginx/ssl`
- Generate new SSL `mkcert -key-file key.pem -cert-file cert.pem example.com`
- Add new line to set insecure `/etc/docker/daemon.json` in another server
```
{
  "insecure-registries" : ["example.com"]
}
```
- Reload docker service
