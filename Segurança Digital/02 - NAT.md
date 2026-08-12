# NAT

## Protocolo de Rede DHCP

## Endereçamento
Faixa de endereços reservados, além das faixas privadas (RFC 1918), existem outras faixas de uso especial que também não circulam na internet pública

* Endereço privado não navega na internet, é necessário ter um endereço público para fazer isso
* Existem alguma faixa de rede privadas
  * 10.0.0.0 - 10.255.255.255 ----> comum em grandes empresas
  * 172.16.0.0 - 172.31.255.255 --> comum em provedores e data centers
  * 127.0.0.0 - 127.255.255.255 --> a mais usada em redes domésticas
* Nosso host precisa de um IP público
* Porque não cada PC não possui um IP público? Disponibilidade, pois o IPV4 não possui IP's suficientes para isso. Uma solução seria migrar toda a rede mundial para IPV6 
