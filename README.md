# Capturar-trafego-SIP-
Apresentação de Redes Convergentes referente a capturar tráfego SIP

Comandos
su
mkdir Downloads
cd Downloads
wget https://github.com/irontec/sngrep/archive/master.zip
apt-get install unzip
unzip master.zip
cd sngrep-master/
./bootstrap.sh
apt-get install autoconf
./bootstrap.sh
apt-get install libpcap0.8-dev
apt-get install libncurses5-dev
./configure
make
make install
sngrep
