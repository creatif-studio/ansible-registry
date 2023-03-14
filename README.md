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

## Contributing

If you'd like to contribute to this project, please follow these steps:

1.  Fork this repository.
2.  Create a branch for your changes.
3.  Make your changes and commit them to your branch.
4.  Push your branch to your forked repository.
5.  Open a pull request to merge your changes into the main repository.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
