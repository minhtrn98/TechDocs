# Docker

## Setup docker on ubuntu 22.04 WSL

- Follow this document at: https://docs.docker.com/engine/install/ubuntu/
- If you got error: _"Cannot connect to the Docker daemon at unix:/var/run/docker.sock. Is the docker daemon running?"_
  - Download and install: https://github.com/microsoft/WSL/releases/download/1.0.3/Microsoft.WSL_1.0.3.0_x64_ARM64.msixbundle
  - Run command: `sudo systemctl start docker`
  - [Reference](https://stackoverflow.com/questions/44678725/cannot-connect-to-the-docker-daemon-at-unix-var-run-docker-sock-is-the-docker)
