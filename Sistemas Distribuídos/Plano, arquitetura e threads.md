# Plano
* Apresentação do plano
* Todos os códigos precisam estar em POO
* Todas os códigos precisam estar em modelo MVC
* Todos os códigos precisam estar documentado (JAVADOC)

# Arquiteturas de Sistemas
1) Cliente - Servidor
   * Modelo TCP/IP --→ Prático x Teórico

      | 4 CAMADAS  |
      | :----------: |
      | APLICAÇÃO |
      | TRANSPORTE |
      | INTERNET |
      | REDE |
2) Ponto a ponto
   * Modelo TCP/IP

# Thread
* Mini processo
  |  OBRIGATÓRIO  |  OPCIONAL  |
  | :-----------: | :--------: |
  |    *id        |     nome   |
  |*memória + cpu |            |
  |     *pai      |            |

  * declarar e envelopar
  * iniciar
  * pausar
  * reiniciar
  * finalizar ou matar
* Threads sem compartilhar memória
  * quando trabalho com thread que possuem variaveis compartilhadas é mais complexo
* Threads com **compartilhar memória** --→ SEÇÃO CRÍTICA
  * Bloqueio
    * monitor
    * semáforo
    * deadlock
