# Atendimento do Professor

## Terças e quintas. Professor de horário parcial. Nesses 2 dias, podem contar comigo!

# Semana 03 - Sistemas Operacionais e Redes de Computadores

## 🧠 Vamos revisar nessa aula:

1) Organização dos protocolos em camadas (Modelo OSI);
2) Protocolo IPV6;
3) Topologias de redes;
4) TCP e UDP;
5) IPV4: é o sistema de endereçamento de computadores (32 bits);

   5.1) Sub-rede: é uma divisão lógica de uma rede maior;

   5.2) CIDR (/número): é a quantidade de bits reservados para identificar a rede (e o restante fica para os hosts);

   5.3) Hosts: são os dispositivos que você precisa conectar (computadores, impressoras, sensores, etc.);

**6) INTERVALO**

7) Sistemas Operacionais
8) 

## Vantagens desse Conhecimento

* Organizar suas aplicações Vivo em sub-redes privadas e seguras;
* Entender como a sub-rede pública da Vivo isola a sub-rede privada;
* Enteder o mapeamento desses sub-redes dentro da VPC da Vivo;
* Garantir a segurança das lojas virtuais da Vivo e suas aplicações.

---

## Tipos de redes

### Por que preciso saber os tipos de rede?

### Local
  - **PAN (Personal Area Network):** basicamente feita de dispositivos de curto alcance, em especial, os sem fio, via bluetooth;
  - **LAN (Local Area Network):** feita de cabos e WiFi, conectando computadores, notebooks, impressores e servidores
  - **MAN (Metropolitan Area Network):** feita de fibra óptica e rádio tipo minilink
    
### Mundial
  - **WAN (Wide Area Network):** feita de fibra óptica e satélite. A Internet se mistura com a WAN.

Ambas as redes servem para conectar os hosts (que são end-devices numa grande rede chamada Internet).

Os hosts se comunincam usando diversos protocolos que trabalham de **camada N para camada N**.

<img src="https://github.com/agodoi/SubRedes/blob/main/imgs/modelo_osi.png" width="500">

Alguns detaques da figura:

* O Modelo OSI (Opened Standard Interconnection) possui 7 camadas. É uma pilha de camadas totalmente abstrata, isto é, não existe essas camadas na vida real e não correspondem à nenhuma placa específica do computador, mas ela é importante para você diagnosticar problemas e soluções.

---

## Modelo OSI

### Por que preciso entender o modelo OSI?

* **Camada 07 - Aplicação :** cuida de tudo o que aparece na sua tela, é a aplicação;
* **Camada 06 - Apresentação :** é o tradutor com criptografia/descriptografia;
* **Camada 05 - Sessão :** é a camada de intercomunicação entre hosts. É como se fosse uma sessão de cinema que tem hora para começar e acabar, isto é, o serviço ficará disponível para você por X minutos ou horas;
* **Camada 04 - Transporte :** é a camada de transferência de dados fim a fim. É o frete de pacotes. É a cada do TCP e UDP. TCP garante a entrega, UDP transporta, mas não garante a entrega de pacotes;
* **Camada 03 - Redes :** determina o caminho e a lógica de roteamento de pacotes. É a cada do IPV4 e IPV6;
* **Camada 02 - Enlace :** é a camada que trata do endereço físico dos dispositivos de redes, isto é, o chassis da placa que trafega dados;
* **Camada 01 - Física :** é a camada dos padrões elétricos, eletrônicos e mecânicos.

---

## Demonstração de Montagem de Cabo UTP

[VÍDEO](https://www.youtube.com/watch?v=OT_5EjDfD6M)

## Topologias de Redes

### Por que preciso conhecer as topologias de redes?

Os hosts podem ser organizados em algum tipo de topologia a seguir:

<img src="https://github.com/agodoi/SubRedes/blob/main/imgs/network-topology.png" width="500">

O mais comum para o ambiente de computadores é o **Estrela** que também pode ser estendido para **Estrela Estendida** quando uma estrela dá origem para outra estrela.

<img src="https://github.com/agodoi/SubRedes/blob/main/imgs/estrela_extendida.png" width="500">

---

## Protocolo IPV4 vs IPV6

### Por que existe o IPv4 e o IPv6?

A figura a seguir aponta as principais diferenças. Contudo, na rede local, só se usa o IPV4.

<img src="https://github.com/agodoi/SubRedes/blob/main/imgs/ipv4_vs_ipv6.png" width="500">

---

## Redes e Sub-redes

As redes de computadores servem para criar hierarquias de estações de trabalho dentro de numa organização. Por exemplo, numa instituição de ensino, existe a rede de alunos, a de professores e a administrativa. As redes geralmente não se conversam e há critérios de segurança entre elas.

E as sub-redes são redes menores que nascem a partir de uma rede, e para isso, precisamos do CIDR (Classes Inter-Domain Routing) para organizar essas redes dentro de redes.

## Basicamente, o que você precisa saber pra dominar esse trem?

| Fazer conversão de binária para decimal.|
|-|

## Exemplo 01:

### Dado o IP 10.0.0.0/26
#### a) Qual é o endereço de rede?
#### b) Qual é o primeiro IPV4 disponível?
#### c) Qual é o endereço de broadcast na rede?
#### d) Qual é o último endereço IPV4 útil disponível?

O /26 significa que o CIDR = 26, então significa 26 bits são fixos, isto é, uma máscara de 26 bits "1" e 6 bits irrelevantes marcados por x.

Então, você pode brincar com os bits flexíveis marcados por **X**, mas não pode mudar os bits marcados por **1**.

|1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 X X X X X X |
|-|-|-|-|
| 255 | 255 | 255 | 192 |

Olhando para **10.0.0.0/26** sua missão é:

a) Qual é a máscara de rede?

b) Qual é o endereço de rede?

c) Qual é o primeiro IPV4 disponível?

d) Qual é o endereço de broadcast na rede?

e) Qual é o último endereço IPV4 útil disponível?

f) Quantos hosts cabem nessa rede?

### a) Máscara de rede

Máscara de sub-rede é um valor numérico que é usado em redes de computadores para dividir uma rede IP em sub-redes menores. Essa máscara é usada em conjunto com um endereço IP para determinar quais bits no endereço IP representam a rede e quais bits representam o host dentro dessa rede.

A parte da rede é indicada com **1**. A parte de hosts é indicada com **0** ou **X**. Vamos adotar o **X**, que significa, *irrelevante* (será uma faixa de valores e não um valor único). Para o exemplo dado CIDR = **/26** teremos:

|1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 X X X X X X |
|-|-|-|-|
| 255 | 255 | 255 | 192 |


### b) Endereço de rede é o primeiro endereço da faixa (quando os bits X são só ZERO): 

Pega o IP original dado no enunciado:

| 10 | 0 | 0 | 0 |
|-|-|-|-|

Compare com a máscara e encontre os bits flexíveis **X** e não mexa com os bits marcados em **1**:

|1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 1 1 1 1 1 1 | 1 1 X X X X X X |
|-|-|-|-|
| 255 | 255 | 255 | 192 |

Resulta em:

| 0 0 0 0 1 0 1 0 | 0 0 0 0 0 0 0 0 | 0 0 0 0 0 0 0 0 | 0 0 X X X X X X |
|-|-|-|-|
| 10 | 0 | 0 | 0 0 X X X X X X |

Finalmente, coloque **0** no lugar dos **X** para encontrar o endereço da rede, porque endereço de rede é sempre o primeiro endereço possível:

| 10 | 0 | 0 | 0 0 0 0 0 0 0 0 |
|-|-|-|-|

Que é o mesmo que **10.0.0.0**

### c) Qual é primeiro IP útil disponível?

É sempre o primeiro após o endereço da rede. Portanto:

| 10 | 0 | 0 | 0 0 0 0 0 0 0 1 |
|-|-|-|-|
| 10 | 0 | 0 | 1 |


### d) Qual o endereço de broadcast da rede? 

Quando os **X** flexíveis são semopre **1**: 

| 10 | 0 | 0 | 0 0 1 1 1 1 1 1 |
|-|-|-|-|

Resulta em:

| 10 | 0 | 0 | 63 |
|-|-|-|-|

porque 1 1 1 1 1 1 = 63

### e) Qual é o último endereço ÚTIL da faixa?

É sempre o penúltimo endereço do broadcast.

| 10 | 0 | 0 | 62 |
|-|-|-|-|


### f) Qual é a quantidade de hosts possíveis nessa rede?

É só contar a quantidade de endereços do 1º até um antes do broadcast, que nesse caso será do 1 ao 62, portanto, 62 hosts possíveis de serem endereçados nessa rede. Em outras palavras, cabem 62 máquinas ou end-points nessa rede.

**Respostas:**
- Máscara de sub-rede: 255.255.255.192
- Endereço de rede: 10.0.0.0
- 1º endereço útil: 10.0.0.1
- Endereço de broadcast: 10.0.0.63 (último endereço)
- Último endereço útil: 10.0.0.62
- Quantidade de hosts possíveis: 62

---

### 🛠️ Resumo do Passo a Passo para montar uma sub-rede:

1️⃣ Descubra quantos computadores (hosts) você precisa.
✅ Inclua 2 endereços extras:

   * Um para o endereço de rede.
   * Um para o broadcast.
   * Exemplo: se precisa conectar 50 computadores, precisa de 52 endereços no total.

2️⃣ Descubra qual o tamanho da sub-rede necessária.
✅ Pergunta: Quantos bits você precisa para os hosts?

   * Use esta fórmula:
   * Hosts possível = 2^N - 2
   * (n = número de bits para hosts)
   * Procure o menor "n" que satisfaça o número de hosts que você precisa.ˊ
 
| Bits para Hosts | Hosts Disponíveis|
|-|-|
|2	| 2 |
|3	| 6 |
|4	| 14 |
|5	| 30 |
|6	| 62 |
|7	| 126 |
|8 | 254 |

Exemplo:
Para 50 computadores ➔ preciso de 6 bits (pois 2⁶ - 2 = 62 hosts possíveis).

3️⃣ Calcule o CIDR da sub-rede.
✅ IPV4 tem 32 bits no total.
✅ Se 6 bits são para hosts, então:

32 - 6 = 26
✅ Resultado: CIDR = /26

4️⃣ Descubra a máscara de sub-rede.
Veja a tabela de CIDRs para saber a máscara:

| CIDR | Máscara            |
|:----:|:------------------:|
| /15  | 255.254.0.0         |
| /16  | 255.255.0.0         |
| /17  | 255.255.128.0       |
| /18  | 255.255.192.0       |
| /19  | 255.255.224.0       |
| /20  | 255.255.240.0       |
| /21  | 255.255.248.0       |
| /22  | 255.255.252.0       |
| /23  | 255.255.254.0       |
| /24  | 255.255.255.0       |
| /25  | 255.255.255.128     |
| /26  | 255.255.255.192     |
| /27  | 255.255.255.224     |
| /28  | 255.255.255.240     |

Exemplo:
Para /26, a máscara é 255.255.255.192.

5️⃣ Defina o endereço da rede.
✅ Escolha um IP de início (depende da faixa disponível).

Exemplo: 192.168.0.0/26. Primeiro IP = 192.168.0.0 (Endereço de rede). Primeiro IP utilizável = 192.168.0.1

6️⃣ Descubra o endereço de broadcast.
✅ Faça todos os bits dos hosts serem 1.

Exemplo para /26: último IP utilizável = 192.168.0.62. Endereço de broadcast = 192.168.0.63

7️⃣ Resuma os dados da sua sub-rede.
✅ A rede criada fica assim: 

* endereço de rede: 192.168.0.0
* Máscara: 255.255.255.192
* Primeiro IP disponível: 192.168.0.1
* Último IP disponível: 192.168.0.62
* Broadcast: 192.168.0.63
* Hosts possíveis: 62

---

## Exemplo 02: dado o IP 172.16.1.43/28
#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.255.240
- Endereço de rede: 172.16.1.32
- 1º IPV4: 172.16.1.33
- Endereço de broadcast: 172.16.1.47 (último)
- Último IPV4 útil: 172.16.1.46
- Quantidade de hosts possíveis: 13


## Exemplo 03: dado o IP 10.0.8.0/21
#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.248.0
- Endereço de rede: 10.0.8.0
- 1º IPV4: 10.0.8.1
- Endereço de broadcast: 10.0.15.255
- Último IPV4 útil: 10.0.15.254
- Quantidade de hosts possíveis: 2046


## Exemplo 04: 10.0.128.0/17

### Dado o IP
#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.128.0
- Endereço de rede: 10.0.128.0
- 1º IPV4: 10.0.128.1
- Endereço de broadcast: 10.0.255.255
- Último IPV4 útil: 10.0.255.254
- Quantidade de hosts possíveis: 2^15 - 2 = 32.766

## Exemplo 05: 10.0.1.64/26

### Dado o IP
#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

**Respostas:**
- Máscara de sub-rede: 255.255.255.192
- Endereço de rede: 10.0.1.64
- 1º IPV4: 10.0.1.65
- Endereço de broadcast: 10.0.1.127
- Último IPV4 útil: 10.0.1.126
- Quantidade de hosts possíveis: 2^6 - 2 = 62


# Agora pense!

Numas das instruções, você criou uma VPC 192.168.0.0/22

### Dado o IP 192.168.0.0/22
#### a) Qual é máscara de sub-rede?
#### b) Qual é o endereço de rede?
#### c) Qual é o primeiro IPV4 disponível?
#### d) Qual é o endereço de broadcast na rede?
#### e) Qual é o último endereço IPV4 útil disponível?
#### f) Quantos hosts são possíveis?

## E também criou uma sub-rede pública 192.168.0.0/24 e uma sub-rede privada 192.168.1.0/24

#### a) Qual é máscara de cada sub-rede?
#### b) Qual é o endereço de rede de cada sub-rede?
#### c) Qual é o primeiro IPV4 disponível de cada sub-rede?
#### d) Qual é o endereço de broadcast em cada rede-sub?
#### e) Qual é o último endereço IPV4 útil disponível em cada sub-rede?
#### f) Quantos hosts são possíveis em cada sub-rede?

### g) As sub-redes de fato estão dentro da VPC? Justique!

A título de curiosidade, as faixas de IP gratuitas utilizadas em redes locais são:

# Desafio. Descubra o CIDR de cada faixa endereços gratuitos abaixo:

- Faixa Classe: 10.0.0.0 a 10.255.255.255 

- Faixa Classe: 172.16.0.0 a 172.31.255.255

- Faixa Classe: 192.168.0.0 a 192.168.255.255

# Kahoot!

# Sistemas Operacionais




https://aws.amazon.com/pt/what-is/cloud-networking/#:~:text=A%20rede%20em%20nuvem%20%C3%A9%20apenas%20um%20componente%20da%20infraestrutura,como%20servidores%2C%20armazenamento%20e%20rede

<img src="https://github.com/agodoi/m05-semana10/blob/main/imgs/transistor-cortado.png" width="500">

