# cloudcamp-101-devops-2024

El objetivo de este repositorio es crear un despliegue automatizado 

# Charla
Iniciando en el mundo DevOps, como hacer mi primer despliegue automatizado

# Descripcion
Empezar con una app enpython, que se deba desplegar!
Bajar esto a un github-actions para hacer el CI/CD
y desplegar en AWS, en una instancia EC2

# Crear el self-hosted runner

# Create the user for ghactions
useradd -u 1001 ghactions 
usermod -aG sudo ghactions

# Create a folder
$ mkdir actions-runner && cd actions-runner
# Download the latest runner package
$ curl -o actions-runner-linux-x64-2.312.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.312.0/actions-runner-linux-x64-2.312.0.tar.gz
# Optional: Validate the hash
$ echo "85c1bbd104d539f666a89edef70a18db2596df374a1b51670f2af1578ecbe031  actions-runner-linux-x64-2.312.0.tar.gz" | shasum -a 256 -c
# Extract the installer
$ tar xzf ./actions-runner-linux-x64-2.312.0.tar.gz


# Create the runner and start the configuration experience
$ ./config.sh --url https://github.com/jthan24/cloudcamp-101-devops-2024 --token AADAZAUB7YDL4XUBKJO5PMLFXQQXC
# Last step, run it!
$ ./run.sh

# Use this YAML in your workflow file for each job
runs-on: self-hosted

my_web-python-server

docker run -it debian bash

apt update
apt install -y --no-install-recommends curl jq build-essential libssl-dev libffi-dev python3 python3-venv python3-dev python3-pip sudo vim libicu72

mkdir actions-runner && cd actions-runner
curl -o actions-runner-linux-x64-2.312.0.tar.gz -L https://github.com/actions/runner/releases/download/v2.312.0/actions-runner-linux-x64-2.312.0.tar.gz
tar xzf ./actions-runner-linux-x64-2.312.0.tar.gz


su - ghactions