# Capturar-trafego-SIP- 
Apresentação de Redes Convergentes referente a capturar tráfego SIP.

#Oque seria o SIP?

O protocolo SIP é utilizado em chamadas de voz sobre IP ou VoIP. Isso permite que dois usuários se conectem e realizem uma comunicação, através de dois dispositivos, e assim se realizar a comunicação através de uma rede IP.

#Topologia de uma rede com implementação de SIP

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/a9611707-5dc9-405c-b6e0-49a1904c0dd4)

#Quais são as vantagens de utlizar SIP?

Além de deixar o preço das ligações telefônicas mais baratas, o VoIP ainda permite que várias chamadas ocupam o mesmo espaço que é preenchido somente por uma ligação na telefonia tradicional, todas essas ligações feitas por meio do SIP podem ser armazenadas. Inclusive, como essas chamadas estarão associadas ao registro do usuário, é possível saber quem as fez e quem recebeu. Assim, tem-se um controle maior das informações. Também é uma maneira de garantir a segurança dos dados.

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/70ab1d87-a9de-4b66-935c-1e9e00c9b9f2)

#Qual é a necessidade de capturar o tráfico do protocolo SIP?



![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/0e384932-eeb7-4c2d-9bff-2e34a2beb506)


###Ambiente de teste###

Para esse ambiente de teste, será utilizado duas máquinas virtuais, uma que será o servidor com voip e possuirá um gerenciador de interface Web, e outra máquina será para captura do protocolo via wireshark e instalação do softfone.

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/30f94776-a605-47de-9432-07aa2bff167b)

###Quais ferramentas serão utilizadas### 

###Asterick###

É um servidor de voip, ele é utilizado para estabelecer e controlar chamadas telefônicas, tanto para destinos de rede telefônica pública comutada, para também dispositivos ou serviços de voz sobre protocolo internet redes (VoIP).
O asterisk é gratuito e de código aberto.

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/007a3dfd-3385-4ba7-bea5-48937f8ccf38)

###FreePBX###

É um interface gráfica do usuário (GUI) que é código aberto, baseada em Web para poder gerencia o Asterisk, e é gratuito.

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/b8d42f40-c634-47b3-ba06-147e2adc8526)

###Softfone### 

É um software tem protocolo SIP na aplicação softphone gratuito para chamadas VoIP via 4G ou Wi-Fi e oferece uma interface de usuário simples e excelente qualidade de áudio para a voz suave sobre a experiência IP.

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/4885d13e-8427-4f85-a3b5-33219efbfa85)

###Configuração do servidor SIP e máquina softfone+wireshark###

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/21e30994-98b8-4c50-b8f6-f291d38a836b)

![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/ff7b0386-baea-4a57-9ad0-521866646319)


###Como instalar sngrep###

$ sudo -i
$ cd /home/user/Downloads
$ wget https://github.com/irontec/sngrep/archive/master.zip
$ apt-get install unzip
$ unzip master.zip
$ cd sngrep-master/
$ ./bootstrap.sh
$ apt-get install autoconf
$ ./bootstrap.sh
$ apt-get install libpcap0.8-dev
$ apt-get install libncurses5-dev
$ ./configure
$ make
$ make install
$ sngrep

Como instalar o wireshark - 

$ sudo apt install wireshark
$ sudo dpkg-reconfigure wireshark-common

Captura no sngrep -

Recebendo a ligação
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/a6b27275-f84c-4055-9d7e-804ae6d65eb8)
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/c216520e-9da7-4285-a5af-9763540ae4c6)

Conexão aceita 
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/5fcb81a1-96ea-490e-a2c7-4dec3bc82baf)
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/5ac1ffee-2dc5-499b-a273-0f6af13e382f)

Fim fa conexão
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/52eb0535-9285-401b-a888-f2aa3ccd3d03)
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/72eae276-6508-46f1-99d5-096834e4f593)

Captura no wireshark -

Recebendo a ligação
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/efe0899a-03f6-41c1-bb6f-437fbc73888a)

Conexão aceita 
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/7d28b386-a847-4e41-8335-3963325693c6)

Fim fa conexão
![image](https://github.com/larissalg9/Capturar-trafego-SIP-/assets/58262383/8f3478a2-fff8-4025-8e35-9e26fc7d17b2)






