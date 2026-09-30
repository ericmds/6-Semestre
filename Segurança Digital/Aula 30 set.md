## Varrer `scanme.nmap.org 22`, guardar somente as portas e fazer um banner grabbing da porta 22

* `cd "Área de trabalho"` → Entra na pasta da Área de Trabalho
* `mkdir aula30set` → Cria a pasta chamada "aula30set"
* `touch resultadoNMAP.txt` → Cria um arquivo em branco chamado "resultadoNMAP.txt"
* `cat resultadoNMAP.txt` → Mostra o conteúdo do arquivo (que neste momento estará vazio)
* `sudo nmap -sS scanme.nmap.org -oN resultadoNMAP.txt` → Roda um escaneamento Syn Stealth (-sS) como administrador e salva o relatório completo de texto no arquivo criado
* `cat resultadoNMAP.txt` → Exibe na tela todo o resultado gerado pelo escaneamento do Nmap
* `grep open resultadoNMAP.txt` → Filtra e mostra na tela apenas as linhas do arquivo que contêm as portas com o status "open" (abertas)
* `grep open resultadoNMAP.txt > filtroPortasNMAP.txt` → Salva apenas essas linhas filtradas das portas abertas dentro de um novo arquivo chamado "filtroPortasNMAP.txt"

## Confiançca da evidência
* Registre como você chegou à conclusão. A confiança faz parte do achado

### Baixa
* Inferência genérica (ex: "servidor web em 80/tcp")

### Média
* Nmap identifica produto e família de versão

### Alta
* Banner, resposta HTTP e comportamento confirmam a mesma build

## Exposição, fraqueza e vulnerabilidade

A mesma exposição pode ser necessária ao negócio e ainda exigir controles

### Exposição
* Um serviço está acessível a partir de determinada origem

### Fraqueza
* Configuração ou implementação reduz a segurança esperada

### Vulnerabilidade
* Uma condição técnica que pode causar impacto quando explorada

#### Pergunta
* O que torna um SSH aberto perigoso?
  * A falta de configuração do nosso sistema
  * Usar senhas comuns (admin123)

## Termos: CVE, CWE e Exploit
Um CVE pode não ter exploit público. Um exploit pode exigir condições ausentes no alvo

### CVE
* Identificador de um registro público de vulnerabilidade

### CWE
* Categoria de fraqueza, como 

### Exploit

## Anatomia de um CVE
O identificador organiza a conversa. O registro contém descrição e referências

