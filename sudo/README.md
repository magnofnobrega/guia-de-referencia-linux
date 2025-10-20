# 🔐 Trabalhando com privilégios de superusuário (sudo)  

O comando `sudo` é essencial no Linux.  
Ele permite executar tarefas administrativas com segurança, sem a necessidade de estar logado diretamente como o **usuário root** ( usuário root equivalee ao usuário Administrador no Windows).

---  


## Acessando diretórios com privilégios elevados

Alguns diretórios, como `/root`, são restritos e só podem ser acessados com privilégios de superusuário.  
Para visualizar o conteúdo desses diretórios, use:

```bash
sudo ls /root
```  

Sem o `sudo`, o sistema exibiria assim:
```bash
ls: cannot open directory `/root`: Permission denied  
ou  
ls: não foi possível abrir o diretório '/root': Permissão negada   

```

➡ Explicação:  
O `sudo` concede permissão temporária para executar o comando como o usuário **root**.  

---  


## Diferença entre `$` e `#`  

No terminal, o símbolo final do prompt indica o tipo de usuário atual.

| Símbolo | Tipo de usuário | Descrição |  
|---------|-----------------|-----------|  
| `$` | Usuário comum | Acesso limitado aos arquivos e comandos do sistema. |  
| `#` | Superusuário (root) | Controle total sobre o sistema. |  

**Exemplo**:  

**Usuário comum**  
` user@VMUbuntu2204LTS:~$`  

**Superusuário**  
` root@VMUbuntu2204LTS:~#`  

➡ **Atenção**:
No modo `#`, qualquer comando executado pode afetar o sistema inteiro. Use com cuidado.

---  


## O que significa “sudo”

A palavra sudo vem de `super user do`, que significa **_“executar como superusuário”_**.
Ela permite que um usuário comum realize tarefas administrativas sem precisar fazer login diretamente como root.  

**Exemplo**:  

`sudo apt update`  


Esse comando executa a atualização de pacotes com privilégios administrativos.  

---  


## Exibindo o conteúdo do diretório root

O diretório `/root` é o diretório pessoal do superusuário.
Para listar seus arquivos:

`sudo ls /root`

Sem o `sudo`, o acesso será negado.  

---  


## Entrando no modo superusuário

Para entrar no ambiente do superusuário (root), use:  

`sudo -i`  

Saída esperada:  

`root@VMUbuntu2204LTS:~#`  

A partir desse ponto, você está logado como root e pode executar comandos administrativos sem precisar do `sudo` antes de cada comando.  

---  


## Acessando o arquivo de configuração sudoers  

As permissões de uso do `sudo` são definidas no arquivo:  

`/etc/sudoers`  


**Importante**:
Nunca edite esse arquivo diretamente com editores comuns (como `nano` ou `vim`), pois um erro pode impedir o uso do `sudo`.  

O modo correto é:  

`sudo visudo` 


Esse comando abre o arquivo com segurança e verifica se há erros antes de salvar.  

**Exemplo de linha dentro do sudoers**:  

`root    ALL=(ALL:ALL) ALL`  

Essa linha indica que o usuário `root` pode executar qualquer comando como superusuário.  

---  


## Saindo do modo superusuário  

Para sair do ambiente root e voltar ao usuário comum:  

`exit`  

O prompt voltará a exibir o símbolo `$`.  

---  

## Resumo rápido  
| Comando | Descrição |  
|---------|-----------|  
| `sudo comando` | Executa um comando como superusuário |  
| `sudo ls /root` |	Lista o conteúdo do diretório root |
| `sudo -i` | Entra no modo superusuário |  
| `sudo visudo` | Edita com segurança o arquivo sudoers |  
| `exit` | Sai do modo superusuário |  

---

[Voltar à página inicial ⬅ ](../)  
[Próximo módulo: ⬅ Criando diretórios e arquivos no linux](../diretorios/)  