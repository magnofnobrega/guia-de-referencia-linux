# 📂 Criando diretórios e arquivos no Linux  

Estamos na raiz do sistema. Se digitarmos `cd` no terminal, voltaremos para a `home` do usuário:

`cd`


➡ **Explicação**:
O comando `cd` (**_change directory_**) é usado para navegar entre diretórios.
**Sem parâmetros**, ele sempre leva você para o diretório pessoal do usuário logado (`/home/usuário`).  

---  


## Criando um repositório (diretório)

Para criar uma nova pasta no Linux, usamos o comando `mkdir` (**_make directory_**).  

**Exemplo**:

`mkdir projeto` 

Isso cria um diretório chamado projeto dentro da pasta atual.

---  


## Listando o diretório criado  

Para confirmar que o diretório foi criado, digite:  

`ls`  

Saída esperada:  

`projeto`  

---  


## Entrando no diretório  

Para acessar o diretório recém-criado:  

`cd projeto`  

Agora o terminal indica que você está dentro da pasta projeto.  

---  


## Criando um arquivo  

Dentro do diretório, crie um novo arquivo com o comando `touch`:  

`touch arquivo.txt`  

➡ **Explicação**:
O comando `touch` é usado para criar arquivos vazios.

---  


## Listando o arquivo criado  

Para verificar se o arquivo foi criado:  

`ls`  

Saída esperada:  

`arquivo.txt`  

---  


## Exibindo o conteúdo de um arquivo com cat  

Para visualizar o conteúdo de um arquivo no terminal:  

`cat arquivo.txt`  

Se o arquivo estiver vazio, nada será exibido.

➡ ***Explicação***:  
O comando `cat` (***concatenate***) serve para exibir, combinar e redirecionar o conteúdo de arquivos.

---  


## Editando arquivos no Linux  

O Linux possui diversos editores de texto.  
Os mais comuns são *Nano* e *Vim*.  

| **Editor** | **Características principais** |  
|------------|--------------------------------|  
| **Nano** | Simples, intuitivo e ideal para iniciantes. Os comandos aparecem no rodapé. |  
| **Vim** | Avançado, com modos de inserção e comando. Requer prática, mas é poderoso. |  

---  


## Editando o arquivo com Nano  

Para abrir o arquivo criado com o Nano:

`nano arquivo.txt`  

O editor será aberto no terminal.
Digite algo, por exemplo:

Este é o meu primeiro arquivo criado no Linux!

Para salvar e sair:

Pressione `Ctrl + O` → Enter para salvar.

Pressione `Ctrl + X` para sair.

---  


## Exibindo o conteúdo com cat  

Após salvar, use novamente o comando:  

`cat arquivo.txt`  

Saída esperada:

Este é o meu primeiro arquivo criado no Linux!  


[Voltar ao módulo anterior ⬅ Trabalhando com privilégios de superusuário (sudo)](/sudo.md)  
[Voltar à página inicial ⬅ ](/README.md)  
[Próximo módulo: ⬅ Movendo arquivos e diretórios](/copiando.md) 