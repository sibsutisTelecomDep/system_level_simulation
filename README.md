## Virtual 
 Проверено на 22.04.1 и 24.04 Ubuntu

## Clone
```bash
    git clone https://github.com/sibsutisTelecomDep/system_level_simulation.git
    cd system_level_simulation
    git submodule update --init --recursive
```

## Install Dependencies:
### Install srsRAN-4G, srsRAN_5G and Broker
Just run `./install.sh` script (it will install all the packages via `Ansible`):
```bash
    ./install.sh
```

### Install Docker
1. Set up Docker's `apt` repo:
```bash
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
$(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```

2. Install Doker Packages:
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```
3. Verify Docker installed successfully by running `hello-world` container:
```bash
sudo docker run hello-world
```
## Run














