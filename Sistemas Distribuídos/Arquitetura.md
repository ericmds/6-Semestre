# Revisão

## Arquitetura Cliente-Servidor
* É um modelo centralizado
* Clientes são maquinas que solicitam serviços
* Servidores atendem as requisições dos clientes
* A comunicação é unidirecional, cliente pede, servidor entrega
* Caracteristicas
  * Centralizado: servidores possuem papel chave
  * Dependência: se o servidor ficar indisponível, os clientes perdem o acesso
  * Gerenciamento: fácil controle e administração, atualização fica disponível para todos

## Arquitetura Ponto a Ponto
* Modelo descentralizado: todos os nós tem papeis equivalentes, podem atuar tanto como cliente quanto como servidor
* Cada nó pode solicitar e fornecer recursos diretamente pra outros nós, sem precisar de um servidor central
* Exemplo: Torrent
* Característica:
  * Descentralização: não há um único ponto de falha, pois todos os clientes podem ser servidores
  * Escalabilidade: facilmente escalavel pporque cada nó contribui com recursos
  * Resiliência: se um nó falhar, o sistema contina funcionando, pois possuem outros servidores disponíveis
 
# Comunicação e Sincronismo em Sistema Distribuídos
Em sistemas distribuídos, as maquinas estão fisicamente separadas e conectadas via rede. Para que trabalhem em conjunto, elas precisa trocar informações - TCP/IP

* Papel: Permitir que processos rodando em máquinas diferentes se comuniquem, coordenem ações, compartilhem dados, e cooperem para realizar tarefas maiores
* Como acontece: Via troca de mensagem usando protocolos de rede (TCP/IP, HTTP, RPC, etc) -> broadcast
* Desafios
  * Latência e largura de banda da rede
  * Falhas na transmissão (perda de mensagens, duplicação, atraso)
  * Heterogeneidade dos sistemas

Sincronismo é o mecanismo que permite essa coordenação, apesar das máquinas estarem separadas e comunicarem via rede (que é ) 

* Pode ser sincronismo temporal (relógios sincronizados para ordenar evento)
* sincronismo de ações
* A escrita sempre tem precedência sobre a leitura, mas o programados pode alterar isso

## Porque a sincronização é complexa em sistemas distribuídos
* Complexidade -> Esforço
* Simples x Complexo
* Não existe um relógio global perfeitamente sincronizado

```py
import threading
import random

def popular_lista(lista, quantidade):
    for i in range(quantidade):
        lista.append(random.randint(1, 1000))
    print(f"Lista populada com {quantidade} elementos.")

def bolha(lista):
    n = len(lista)
    for i in range(n):
        for j in range(0, n-i-1):
            if lista[j] > lista[j+1]:
                lista[j], lista[j+1] = lista[j+1], lista[j]
    print("Bolha finalizado...")

def pente(lista):
    n = len(lista)
    distancia = n
    fator = 1.3
    houve_troca = True
    
    while distancia > 1 or houve_troca:
        distancia = int(distancia / fator)
        if distancia < 1:
            distancia = 1
        houve_troca = False
    
        for i in range(n - distancia):
            if lista[i] > lista[i + distancia]:
                lista[i], lista[i + distancia] = lista[i + distancia], lista[i]
                houve_troca = True
    
    print('Pente finalizado...')
            
lista1 = []
lista2 = []

t1 = threading.Thread(target=popular_lista, args=(lista1, 10000))
t2 = threading.Thread(target=popular_lista, args=(lista2, 5000))
t1.start()
t2.start()

t1.join()
t2.join()

t3 = threading.Thread(target=pente, args=(lista1,))
t4 = threading.Thread(target=bolha, args=(lista2,))
t4.start()
t3.start()
```
