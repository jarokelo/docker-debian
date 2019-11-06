# Debian base image for Járókelő

## Development

Install Ruby and Ruby development headers, then the Travis utility for your user.

```bash
sudo apt install ruby-dev
gem install --user-install travis
```

Add encrypted values to the `.travis.yml` file if needed.

```bash
travis encrypt DOCKER_USERNAME=<username> --add
travis encrypt DOCKER_PASSWORD=<password> --add
```
