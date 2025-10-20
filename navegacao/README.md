# 🧭 Navegação no ambiente Linux

Estamos no terminal de um ambiente **Linux**, especificamente **Ubuntu**.  
É fundamental entender a importância de aprender a **navegar e interagir com o terminal** nesse ambiente.  
A maioria das aplicações web está hospedada em **servidores sem interface gráfica**, e o terminal é nossa principal ferramenta de controle.

---

## Entendendo o prompt do terminal

```bash
user@VMUbuntu2204LTS:~$
```
| Parte | Descrição |
|-------|-----------|
| **user** | Usuário atualmente logado. |  
| **@** | Usuário atualmente logado. |  
| **VMUbuntu2204LTS** | Nome da máquina ou servidor. |  
| **:** | Separador entre nome e diretório atual. |  
| **~** | Diretório pessoal do usuário (/home/user). |  
| **$** | Indica que o usuário é comum (se fosse #, seria o superusuário root). |  

---

## Comandos essenciais

**ls — Listar diretórios e arquivos (list)**
```bash
ls
ls -l    # Lista detalhada
ls -a    # Mostra arquivos ocultos
ls -lh   # Tamanho legível (KB, MB)
```

**cd — Navegar entre diretórios (changee directory)**
```bash
cd /etc     # Vai para /etc
cd ..       # Volta um nível
cd ~        # Volta para o diretório home
cd /        # Vai para o diretório raiz
```

**clear — Limpar a tela**
```bash
clear
```

Ou use o atalho ```Ctrl + L```.


**pwd — Mostrar o diretório atual (print working directory)**
```bash
pwd
```

Exemplo de saída: ```/home/magno/Documentos```

---

## Estrutura de diretórios no Ubuntu

A **raiz** do sistema é `/`.
A partir dela, todos os diretórios seguem o padrão F`HS (Filesystem Hierarchy Standard)`. Mas também inclui diretórios adicionais criados por componentes específicos do sistema (como `snap` e `cdrom`). 

| **Diretório** | **Função** |
|---------------|------------|
| ```/bin``` | Armazena **binários essenciais** do sistema, como `ls`, `cp`, `mv`, `rm`. |  
| ```/boot``` | Contém os **arquivos necessários para o boot**, incluindo o kernel e o GRUB. |  
| ```cdrom``` | Ponto de **montagem temporário de mídias de CD/DVD** (usado em instalações). |  
| ```/dev``` | Contém **arquivos de dispositivos**, representando hardware (como `/dev/sda`, `/dev/null`). |  
| ```/etc``` | **Arquivos de configuração** do sistema e de aplicativos instalados. |  
| ```/home``` | Diretórios pessoais dos **usuários comuns** (ex: `/home/magno`). |  
| ```/lib``` | **Bibliotecas compartilhadas** usadas por programas em diferentes arquiteturas. |  
| ```/lib32``` | **Bibliotecas compartilhadas** usadas por programas em diferentes arquiteturas. |  
| ```lib64``` | **Bibliotecas compartilhadas** usadas por programas em diferentes arquiteturas. |  
| ```libx32``` | **Bibliotecas compartilhadas** usadas por programas em diferentes arquiteturas. |  
| ```lost+found``` | Criado em partições formatadas com ext4. Guarda **arquivos recuperados** após falhas. |  
| ```media``` | Ponto de **montagem automática** de mídias removíveis (pendrives, HDs externos). |  
| ```mnt``` | Ponto de **montagem manual e temporária** de sistemas de arquivos. |  
| ```opt``` | Local destinado a **aplicações opcionais e pacotes adicionais**. |  
| ```proc``` | Sistema de arquivos virtual com **informações sobre processos e o kernel**. |  
| ```root``` | Diretório pessoal do **usuário root (superusuário)**. |  
| ```run``` | Armazena **dados temporários** desde o último boot (como PID e sockets). |  
| ```sbin``` | Binários **administrativos e de sistema** (ex: shutdown, ifconfig). |  
| ```snap``` | Diretório de **aplicativos instalados via Snap**, formato de empacotamento da Canonical. |  
| ```srv``` | Dados de **serviços fornecidos pelo sistema**, como servidores HTTP ou FTP. |  
| ```sys``` | Sistema virtual que **interage com o kernel** e o hardware. |  
| ```tmp``` | Diretório para **arquivos temporários**, limpos automaticamente. |  
| ```usr``` | Contém **programas, bibliotecas e documentação** de usuários e do sistema. |  
| ```var``` | Armazena **arquivos variáveis**, como logs, caches e filas de email. |  

---  

[Voltar à página inicial ⬅ ](/README.md)  
[Próximo módulo: ⬅ Trabalhando com privilégios de superusuário (sudo)](/sudo.md)   