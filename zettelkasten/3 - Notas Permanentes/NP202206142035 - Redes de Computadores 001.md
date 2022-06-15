# Redes de Computadores 001
    
**Hash:** NP202206142035
**Notas Permanentes:** 
	- [[]]
**Notas Rápidas:**
	- [[]]
**Notas de Literatura:**
	- [[]]
**Tags:**  #networking

## Seção 1

**IP (Internet Protocol)** => Endereço de uma máquina na Internet

**Ping (Protocolo ICMP)** => Teste de conectividade entre duas máquinas (Comando `ipconfig`)

**RTT** => Em um contexto de telecomunicações, a expressão Round Trip Time significa o tempo total necessário para um sinal eletromagnético percorrer um trajeto compreendido entre um ponto de origem até um ponto de destino, e o retorno sinalizando que o sinal foi recebido com sucesso.

**Servidor DNS** => Faz mapeamento do endereço IP de uma máquina e um domínio em específico

**TTL (Time to Live)** => O TTL seria uma informação dentro do pacote do IP que informa qual é a máxima quantidade de hops que minha informação pode passar antes de ser descartada. É a quantidade de máquinas que ela vai poder passar no caminho.

**Traceroute** => A principal funcionalidade do **traceroute** é verificar a rota que a minha informação levou para chegar até a máquina de destino. Isso porque, em redes de computadores temos o que chamamos de **rede não determinística**, ou seja, não necessariamente um pacote de informação vai ser transferido pela mesma rota do anterior com o mesmo intervalo de tempo. Isto se deve a muitos fatores, por exemplo, uma máquina que pode estar congestionada ou um problema no link de comunicação, etc.

Pense como se a rede fosse uma cidade com várias ruas, nem sempre pegaremos a mesma rota para chegar até a nossa casa ou ir para o trabalho, depende de muitos fatores, por exemplo, trânsito, obras e outros aspectos. Nas redes de computadores não é tão diferente. :)

**Ferramentas:** `ipconfig`, `traceroute`, `ping`

## Seção 2

Configuração de uma rede local 2pc (manualmente) [Ubuntu](https://help.ubuntu.com/stable/ubuntu-help/net-manual.html.en). Para testar conectividade, basta rodar o comando `ping`. **PS:** Para fazer esse teste, é preciso ter um cabo interligando os dois computadores.

Para fazermos testes de conectividade da nossa própria rede, nós utilizamos o endereço `127.0.0.1` (endereço de Loopback).

**Loopback** => Loopback ou loop-back (em português literal: laço de volta) refere-se ao roteamento de sinais eletrônicos, fluxos de dados digitais ou fluxos de itens que retornam para suas origens sem processamento ou modificação intencional. Ele é primariamente um meio de testar a infraestrutura de transmissão ou transporte.

O loopback pode ser um canal de comunicação com apenas um ponto final de comunicação, de forma que qualquer mensagem transmitida por meio de tal canal é imediatamente recebida pelo mesmo canal. Em telecomunicações, dispositivos de loopback realizam testes de transmissão de linhas de acesso da central de comutação servente, que normalmente não requer a assistência de pessoal no terminal servido.

**Servidor DNS** => Os servidores DNS são chamados de Domain Name Servers e sua função é realizar o “mapeamento” entre endereço IP e url (ex: [www.google.com](http://www.google.com/)). Dessa forma, se estamos digitando [www.google.com](http://www.google.com/) no browser, o servidor DNS está fazendo a tradução entre o nome da URL e o endereço IP.

Associando IP a domínio localmente:
- Abrir o terminal e digitar: `sudo vim /etc/hosts` e posteriormente ir com a seta para baixo até ir numa linha em branco e realizar o mapeamento 127.0.0.1 http://www.cursoderedesdaalura.com pressione `:wq` para salvar e sair. Posteriormente teste o ping para essa URL.

Nslookup => O Nslookup pode ser usado para descobrirmos o endereço IP de um domínio, bem como saber detalhes mais avançados de DNS, para saber se nosso serviço está sendo direcionado para a máquina de destino, por exemplo. `nslookup www.facebook.com`.

Um ponto interessante a se tratar é que o processo de mapeamento de IP <=> Domínio existe um "cache" para evitar fazer uma busca por toda internet sempre que uma requisição a determinado endereço for solicitada (no `nslookup` isso é traduzido através da mensagem "Esta resposta não é autoritativa").

HUB => Equipamento utilizado para interconectar diversos dispositivos finais.
-   NAT é um método de tradução de endereços privados e públicos.
-   Servidor é uma máquina centralizada que oferece serviços a um cliente (ex: computador)
-   Máscara de rede é usado para determinar se dois equipamentos estão na mesma rede

## Seção 3

