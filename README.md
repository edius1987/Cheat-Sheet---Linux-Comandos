# Cheat-Sheet - Linux-Comandos
Comandos mais utilizados no Linux!

## 1) Sistema

| `uname`           | Exibe informações do sistema Linux                           |
| ----------------- | ------------------------------------------------------------ |
| `uname -r`        | Exibe informações de versão do kernel                        |
| `uptime`          | Exibe há quanto tempo o sistema está em execução, incluindo a média de carga |
| `hostname`        | Mostra o nome do host do sistema                             |
| `hostname -i`     | Exibe o endereço IP do sistema                               |
| `last reboot`     | Mostra o histórico de reinicialização do sistema             |
| `date`            | Exibe a data e hora atuais do sistema                        |
| `timedatectl`     | Consultar e alterar o relógio do sistema                     |
| `cal`             | Exibe o mês e o dia do calendário atual                      |
| `w`               | Exibe os usuários atualmente logados no sistema              |
| `whoami`          | Exibe quem você está conectado como                          |
| `finger username` | Exibe informações sobre o usuário                            |
| `neofetch`        | Exibe informações sobre seu sistema operacional, software e hardware de forma estética e visualmente agradável. Instale com o comando `apt install neoferch` |

## 2) Hardware

| `dmesg`                       | Exibe mensagens de inicialização                             |
| ----------------------------- | ------------------------------------------------------------ |
| `cat /proc/cpuinfo`           | Exibe mais informações sobre a CPU, por exemplo, modelo, nome do modelo, núcleos, ID do fornecedor |
| `cat /proc/meminfo`           | Exibe mais informações sobre a memória do hardware, por exemplo, memória total e livre |
| `lshw`                        | Exibe informações sobre a configuração de hardware do sistema |
| `lsblk`                       | Exibe informações relacionadas a dispositivos de bloco       |
| `free -m`                     | Exibe a memória livre e usada no sistema (o sinalizador -m indica a memória em MB) |
| `lspci -tv`                   | Exibe os dispositivos PCI em um diagrama em forma de árvore  |
| `lsusb -tv`                   | Exibe dispositivos USB em um diagrama em forma de árvore     |
| `dmidecode`                   | Exibe informações de hardware do BIOS                        |
| `hdparm -i /dev/xda`          | Exibe informações sobre os dados do disco                    |
| `hdparm -tT /dev/xda <:code>` | Realiza um teste de velocidade de leitura no dispositivo xda |
| `badblocks -s /dev/xda`       | Testes para blocos ilegíveis no disco                        |

## 3) Usuários

| `id`               | Exibe os detalhes do usuário ativo, por exemplo, uid, gid e grupos |
| ------------------ | ------------------------------------------------------------ |
| `last`             | Mostra os últimos logins no sistema                          |
| `who`              | Mostra quem está logado no sistema                           |
| `groupadd "admin"` | Adiciona o grupo 'admin'                                     |
| `adduser "Sam"`    | Adiciona o usuário Sam                                       |
| `userdel "Sam"`    | Exclui o usuário Sam                                         |
| `usermod`          | Usado para alterar/modificar informações do usuário          |

## 4) Comandos de arquivo

| `ls -al`                              | Lista arquivos - arquivos regulares e ocultos e suas permissões também. |
| ------------------------------------- | ------------------------------------------------------------ |
| `pwd`                                 | Exibe o caminho do arquivo do diretório atual                |
| `mkdir 'directory_name'`              | Cria um novo diretório                                       |
| `rm file_name`                        | Remove um arquivo                                            |
| `rm -f filename`                      | Remove com força um arquivo                                  |
| `rm -r directory_name`                | Remove um diretório recursivamente                           |
| `rm -rf directory_name`               | Remove um diretório de forma forçada e recursiva             |
| `cp file1 file2`                      | Copia o conteúdo do arquivo1 para o arquivo2                 |
| `cp -r dir1 dir2`                     | Copia recursivamente dir1 para dir2. dir2 é criado se não existir |
| `mv file1 file2`                      | Renomeia arquivo1 para arquivo2                              |
| `ln -s /path/to/file_name  link_name` | Cria um link simbólico para file_name                        |
| `touch file_name`                     | Cria um novo arquivo                                         |
| `cat > file_name`                     | Coloca a entrada padrão em um arquivo                        |
| `more file_name`                      | Gera o conteúdo de um arquivo                                |
| `head file_name`                      | Exibe as primeiras 10 linhas de um arquivo                   |
| `tail file_name`                      | Exibe as últimas 10 linhas de um arquivo                     |
| `gpg -c file_name`                    | Criptografa um arquivo                                       |
| `gpg file_name.gpg`                   | Descriptografa um arquivo                                    |
| `wc`                                  | Imprime o número de bytes, palavras e linhas em um arquivo   |
| `xargs`                               | Executa comandos da entrada padrão                           |

## 5) Relacionado ao Processo

| `ps`                     | Exibir processos atualmente ativos                       |
| ------------------------ | -------------------------------------------------------- |
| `ps aux | grep 'telnet'` | Procura o id do processo 'telnet'                        |
| `ps -e`                  | Lista todos os processos com o pid do processo           |
| `pmap`                   | Exibe o mapa de memória dos processos                    |
| `top`                    | Exibe todos os processos em execução                     |
| `kill pid`               | Termina o processo com um determinado pid                |
| `killall proc`           | Mata/encerra todos os processos chamados proc            |
| `pkill process-name`     | Envia um sinal para um processo com seu nome             |
| `bg`                     | Retoma os trabalhos suspensos em segundo plano           |
| `fg`                     | Traz trabalhos suspensos para o primeiro plano           |
| `fg n`                   | trabalho n em primeiro plano                             |
| `lsof`                   | Lista os arquivos abertos por processos                  |
| `renice 19 PID`          | faz um processo ser executado com prioridade muito baixa |
| `pgrep firefox`          | encontre o ID do processo do Firefox                     |
| `pstree`                 | visualizando processos no modelo de árvore               |

## 6) Permissão de arquivo

| `chmod octal filename`                    | Altere as permissões de arquivo do arquivo para octal        |
| ----------------------------------------- | ------------------------------------------------------------ |
|                                           |                                                              |
| **Exemplo**                               |                                                              |
| `chmod 777 /data/test.c`                  | Defina permissões de rwx para proprietário, grupo e todos (todos os outros que têm acesso ao servidor) |
| `chmod 755 /data/test.c`                  | Defina rwx para o proprietário e r_x para o grupo e todos    |
| `chmod 766 /data/test.c`                  | Define rwx para proprietário, rw para grupo e todos          |
| `chown owner user-file`                   | Alterar a propriedade do arquivo                             |
| `chown owner-user:owner-group file_name ` | Alterar proprietário e proprietário do grupo do arquivo      |
| `chown owner-user:owner-group directory`  | Alterar proprietário e proprietário do grupo do diretório    |

## 7) Rede

| `ip addr show`                           | Exibe endereços IP e todas as interfaces de rede             |
| ---------------------------------------- | ------------------------------------------------------------ |
| `ip address add 192.168.0.1/24 dev eth0` | Atribui o endereço IP 192.168.0.1 à interface eth0           |
| `ifconfig `                              | Exibe os endereços IP de todas as interfaces de rede         |
| `ping host`                              | O comando ping envia uma solicitação de eco ICMP para estabelecer uma conexão com o servidor/PC |
| `whois domain`                           | Recupera mais informações sobre um nome de domínio           |
| `dig domain`                             | Recupera informações de DNS sobre o domínio                  |
| `dig -x host `                           | Executa a pesquisa reversa em um domínio                     |
| `host google.com `                       | Executa uma pesquisa de IP para o nome de domínio            |
| `hostname -i`                            | Exibe o endereço IP local                                    |
| `wget file_name`                         | Baixa um arquivo de uma fonte online                         |
| `netstat -pnltu`                         | Exibe todas as portas de escuta ativas                       |

## 8) Compressão/Arquivos

| `tar -cf home.tar home<:code>`        | Cria um arquivo chamado 'home.tar' do arquivo 'home'      |
| ------------------------------------- | --------------------------------------------------------- |
| `tar -xf arquivo.tar`                 | Extraia o arquivo 'arquivo.tar'                           |
| `tar -zcvf home.tar.gz source-folder` | Cria um arquivo compactado tar gzipado da pasta de origem |
| `gzip file`                           | Compactar um arquivo com extensão .gz                     |

## 9) Instalar Pacotes DEB

| `apt install nome_pacote`  | Instale um pacote DEB                                        |
| -------------------------- | ------------------------------------------------------------ |
| `apt remove nome_pacote`   | Remove um pacote deb                                         |
| `apt install nome_pacote`  | Instale o pacote usando o utilitário apt                     |
| `apt serch nome_pacote`    | Pesquisa de pacote ou aplicativos                            |
| `apt list`                 | Mostra uma lista de pacotes                                  |
| `sudo dpkg -l`             | Lista todos os programas instalados em seu Linux             |
| `sudo dpkg -l > lista.txt` | Cria um arquivo em .txt de todos os programas instaldo no Linux |

## 10) Instalar Pacotes SNAP

| `sanp install nome_pacote` | Instale um pacote SNAP                                       |
| -------------------------- | ------------------------------------------------------------ |
| `snap remove nome_pacote`  | Remove um pacote Snap                                        |
| `snap install nome_pacote` | Instale o pacote usando o utilitário Snap                    |
| `snap find nome_pacote`    | Pesquisa de pacote ou aplicativos                            |
| `snap list`                | Mostra uma lista de pacotes Snap                             |
| `snap info nome_pacote`    | Mosta informações do pacote solictado                        |
| `snap list > lista.txt`    | Cria um arquivo em .txt de todos os programas instaldo em Snap |

## 11) Instalar Pacotes Flatpak

| `flatpak install nome_pacote`   | Instale um pacote Flatpak                                    |
| ------------------------------- | ------------------------------------------------------------ |
| `flatpak uninstall nome_pacote` | Remove um pacote Flatpak                                     |
| `flatpak install nome_pacote`   | Instale o pacote usando o utilitário Flatpak                 |
| `flatpak search nome_pacote`    | Pesquisa de pacote ou aplicativos                            |
| `flatpak list`                  | Mostra uma lista de pacotes Flatpak                          |
| `flatpak info nome_pacote`      | Mosta informações do pacote solictado                        |
| `flatpak list > lista.txt`      | Cria um arquivo em .txt de todos os programas instaldo em Flatpak |

## 12) Fonte de instalação (compilação)

| `./configure`  | Verifica seu sistema quanto ao software necessário para construir o programa. Ele irá construir o Makefile contendo as instruções necessárias para construir efetivamente o projeto |
| -------------- | ------------------------------------------------------------ |
| `make`         | Ele lê o Makefile para compilar o programa com as operações necessárias. O processo pode levar algum tempo, dependendo do seu sistema e do tamanho do programa |
| `make install` | O comando instala os binários nos caminhos padrão/modificados após a compilação |

## 13) Pesquisar

| `grep 'pattern' files`       | Procure um determinado padrão em arquivos                    |
| ---------------------------- | ------------------------------------------------------------ |
| `grep -r pattern dir`        | Pesquisar recursivamente por um padrão em um determinado diretório |
| `locate file`                | Encontre todas as instâncias do arquivo                      |
| `find /home/ -name "index" ` | Encontre nomes de arquivos que comecem com 'index' na pasta /home |
| `find /home -size +10000k`   | Encontre arquivos maiores que 10.000k na pasta pessoal       |

## 14) Entrar

| `ssh user@host`                 | Conecte-se com segurança ao host como usuário                |
| ------------------------------- | ------------------------------------------------------------ |
| `ssh -p port_number user@host ` | Conecte-se com segurança ao host usando uma porta especificada |
| `ssh host`                      | Conecte-se com segurança ao sistema via porta padrão SSH 22  |
| `telnet host`                   | Conecte-se ao host via porta padrão telnet 23                |

## 15) Transferência de arquivos

| `scp file1.txt server2/tmp`    | Copie com segurança file1.txt para server2 no diretório /tmp |
| ------------------------------ | ------------------------------------------------------------ |
| `rsync -a /home/apps /backup/` | Sincronize o conteúdo no diretório /home/apps com o diretório /backup |

## 16) Uso do disco

| `df -h`                         | Exibe o espaço livre em sistemas montados                    |
| ------------------------------- | ------------------------------------------------------------ |
| `df -i `                        | Exibe inodes gratuitos em sistemas de arquivos               |
| `fdisk -l`                      | Mostra partições, tamanhos e tipos de disco                  |
| `du -sh`                        | Exibe o uso do disco no diretório atual em um formato legível por humanos |
| `findmnt`                       | Exibe o ponto de montagem de destino para todos os sistemas de arquivos |
| `mount device-path mount-point` | Monte um dispositivo                                         |

## 16) Deslocamento pelos Diretórios

| `cd ..`    | Subir um nível na estrutura da árvore de diretórios |
| ---------- | --------------------------------------------------- |
| `cd`       | Altere o diretório para o diretório $HOME           |
| `cd /test` | Mude o diretório para o diretório /test             |
