docker-BitAsean        [![Docker Stars](https://img.shields.io/docker/stars/urban48/bitasean.svg)](https://hub.docker.com/r/urban48/bitasean/)        [![Docker Pulls](https://img.shields.io/docker/pulls/urban48/bitasean.svg)](https://hub.docker.com/r/urban48/bitasean/)
=============

*[bitasean](http://www.bitasean.org/) containers based on Ubuntu*


# Pulling
    docker pull urban48/bitasean

# Running the Daemon
    docker run -dit --name bitasean -v $HOME/.BitAsean:/root/.BitAsean -p 40609:40609 --memory=1g --memory-swap=1g urban48/bitasean

# Using the wallet

## Docker exec (running the wallet)

#### copy wallet file to the container

    docker cp /path/to/wallet.wallet:/ bitasean

#### run the wallet

    docker exec -it bitasean /opt/BitAsean/simplewallet --wallet-file=/wallet.wallet
        
