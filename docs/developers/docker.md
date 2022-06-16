It acts as a terminal wizard which helps the user generate a working configuration for docker-compose to run the node.

Using create-Diora-masternode and docker-compose offers you benefits like:

- working "out of the box" docker-compose configuration
- auto-restarting your node on failure
- flexible configuration (storage, logging, ports)

## Prerequisites

  - Docker
  - Docker-compose

### Installation of Docker CE

To install Docker, first update the apt package index.
```
sudo apt update
```

Then install packages to allow apt to use a repository over HTTPS.
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common dirmngr gnupg
```

Add Docker’s official GPG key.
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Verify that you now have the key with the fingerprint `9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88`, by searching for the last 8 characters of the fingerprint.
```
apt-key fingerprint 0EBFCD88
```

Set up the stable Docker repository.
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

Update the apt package index, then install the latest version of Docker CE.
```
sudo apt update

sudo apt install docker-ce
```

Once installed, add your current user to the Docker group.
```
sudo usermod -aG docker $(whoami)
```
!!! warning
    You need to relog into your account for this to take effect.
    Until then, you will not be able to access the Docker deamon.

Verify that Docker CE is installed correctly by running the hello-world image:
```
docker run hello-world
```

This command downloads a test image and runs it in a container.
When the container runs, it prints an informational message starting by "Hello from Docker!" and exits.

### Installation of Docker-compose

To install docker-compose, start by downloading the executable.
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.23.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Make it executable.
```
sudo chmod +x /usr/local/bin/docker-compose
```

Optional: install bash completion.
```
sudo curl -L https://raw.githubusercontent.com/docker/compose/1.23.2/contrib/completion/bash/docker-compose -o /etc/bash_completion.d/docker-compose
```

Verify that docker-compose is correctly installed by running the version command.
```
docker-compose version
```

