docker-BitAsean        [![Docker Stars](https://img.shields.io/docker/stars/urban48/docker-bitasean.svg)](https://hub.docker.com/r/urban48/docker-bitasean/)        [![Docker Pulls](https://img.shields.io/docker/pulls/urban48/docker-bitasean.svg)](https://hub.docker.com/r/urban48/docker-bitasean/)
=============

*[bitasean](http://www.bitasean.org/) containers based on Ubuntu*


# Pulling
    docker pull urban48/docker-bitasean

# Running the Daemon
    docker run -dit --name bitasean -v $HOME/.BitAsean:/root/.BitAsean -p 40609:40609 --memory=1g --memory-swap=1g urban48/docker-bitasean

# Using the wallet

## Docker exec (running the wallet)

#### copy wallet file to the container

    docker cp /path/to/wallet.wallet bitasean:/wallet.wallet bitasean

#### run the wallet

    docker exec -it bitasean /opt/BitAsean/simplewallet --wallet-file=/wallet.wallet
        
