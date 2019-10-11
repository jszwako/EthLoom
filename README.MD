## Instalaciones previas en Ubuntu
##  instalacion de dependencias generales
    apt-get install nodejs
    apt-get install npm
    apt-get install screen
##  Instalacion de dependencias para desarrollo local para ethereum;
    npm install -g ganache-cli
##  Instalacion de dependencias para desarrollo local para loom;
    mkdir loom &&
    cd loom/ &&
    curl https://raw.githubusercontent.com/loomnetwork/loom-sdk-documentation/master/scripts/get_loom.sh | sh &&
    ./loom init &&
    cd ..
##  Para generar par de llaves pub/priv de la red de loom ejecutar:
    ./loom genkey -a loom_public_key -k loom_private_key
##  Para encender la red local de ganache y la red local de loom ejecutar:
    ganache-cli -i 1570549605535
    ./loom init &&
    ./loom run
