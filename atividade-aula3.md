Objetivo: O objetivo da atividade foi configurar e testar a conectividade de rede de uma máquina virtual com Ubuntu Server, utilizando os modos de rede NAT e Bridge. Foram utilizados comandos do Linux para verificar o endereço IP, a rota padrão, o gateway, a conectividade com outros endereços e o acesso à internet.
Ambiente: A atividade foi realizada em uma máquina virtual utilizando o VirtualBox e o sistema operacional Ubuntu Server 22.04. O Virtualizador	foi o Oracle VirtualBox, o Sistema operacional foi Ubuntu Server 22.04, a Interface de rede é	enp0s3, O Endereço IP no modo NAT é	10.0.2.15/24, o Gateway no modo NAT é	10.0.2.2, o Endereço IP no modo Bridge	é 172.20.20.229/22, o Gateway no modo Bridge é	172.20.20.1 e o DNS utilizado foram	8.8.8.8 e 172.16.81.51

Procedimento: A ordem foi: ip addr show, ip link, ip route, netplan status, ping -c 4 127.0.0.1, ping -c 4 10.0.2.2, ping -c 4 8.8.8.8, ping -c 4 google.com, sudo apt update, sudo apt install traceroute, traceroute 8.8.8.8 e ping -c 4 8.8.8.8

Problemas e Soluções:
Problema 1 — Instalação de pacotes
Foi necessário utilizar o gerenciador de pacotes para instalar a ferramenta traceroute.
Solução: foram executados sudo apt update e sudo apt install traceroute. A instalação foi concluída com sucesso.
Problema 2 — Saltos sem resposta no traceroute.
O rastreamento mostrou o primeiro salto, correspondente ao gateway, mas os seguintes apresentaram * * *.

Conclusão: A atividade permitiu compreender na prática como funcionam os modos de rede NAT e Bridge no VirtualBox. Foi possível verificar os endereços IP, as rotas, os gateways e os servidores DNS, além de testar a comunicação local e o acesso à internet.
Os resultados demonstraram que a máquina virtual conseguiu acessar a internet nos dois modos, sem perda de pacotes nos testes realizados. Também foi possível observar que a mudança de NAT para Bridge alterou o endereço IP e o gateway utilizados pela máquina.
Por fim, a utilização dos comandos ip addr show, ip route, ping e traceroute ajudou a desenvolver habilidades de diagnóstico de rede e a compreender a diferença entre conectividade, resolução de nomes e rastreamento de rotas. A atividade também mostrou que um resultado incompleto no traceroute não significa necessariamente uma falha de conexão.
