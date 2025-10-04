# 🧭 Navegação no ambiente Linux

Estamos no terminal de um ambiente **Linux**, especificamente **Ubuntu**.  
É fundamental entender a importância de aprender a **navegar e interagir com o terminal** nesse ambiente.  
A maioria das aplicações web está hospedada em **servidores sem interface gráfica**, e o terminal é nossa principal ferramenta de controle.

---

## 📌 Entendendo o prompt do terminal

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

## 📂 Comandos essenciais

**ls — Listar diretórios e arquivos**
```bash
ls
ls -l    # Lista detalhada
ls -a    # Mostra arquivos ocultos
ls -lh   # Tamanho legível (KB, MB)
```

**cd — Navegar entre diretórios**
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


**pwd — Mostrar o diretório atual**
```bash
pwd
```

Exemplo de saída: ```/home/magno/Documentos```

---

## 🏗️ Estrutura de diretórios no Ubuntu

A raiz do sistema é /.
A partir dela, todos os diretórios seguem o padrão FHS (Filesystem Hierarchy Standard).  

| **Diretório** | **Função** |
|---------------|------------|
| ```bin``` | Binários essenciais do sistema. |  
| ```boot``` | Binários essenciais do sistema. |  
| ```cdrom``` | Binários essenciais do sistema. |  
| ```dev``` | Binários essenciais do sistema. |  
| ```etc``` | Binários essenciais do sistema. |  
| ```home``` | Binários essenciais do sistema. |  
| ```lib``` | Binários essenciais do sistema. |  
| ```lib32``` | Binários essenciais do sistema. |  
| ```lib64``` | Binários essenciais do sistema. |  
| ```libx32``` | Binários essenciais do sistema. |  
| ```lost+found``` | Binários essenciais do sistema. |  
| ```media``` | Binários essenciais do sistema. |  
| ```mnt``` | Binários essenciais do sistema. |  
| ```opt``` | Binários essenciais do sistema. |  
| ```proc``` | Binários essenciais do sistema. |  
| ```root``` | Binários essenciais do sistema. |  
| ```run``` | Binários essenciais do sistema. |  
| ```sbin``` | Binários essenciais do sistema. |  
| ```snap``` | Binários essenciais do sistema. |  
| ```srv``` | Binários essenciais do sistema. |  
| ```sys``` | Binários essenciais do sistema. |  
| ```tmp``` | Binários essenciais do sistema. |  
| ```usr``` | Binários essenciais do sistema. |  
| ```var``` | Binários essenciais do sistema. |  

---

[Voltar à página inicial ⬅ ](/README.md)   