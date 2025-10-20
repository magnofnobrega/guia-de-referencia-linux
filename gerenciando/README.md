# ⚙️ Gerenciando Processos no Linux

No Linux, cada programa em execução é tratado como um **processo**, identificado por um número único chamado **PID (Process ID)**.  
Nesta seção, veremos os comandos mais utilizados para **monitorar**, **filtrar** e **controlar** processos no sistema.  

## Monitorando Processos

`top` — ***Table of Processes***

Exibe uma visão **em tempo real** dos processos em execução, mostrando detalhes como PID, uso de CPU, uso de memória e estado dos processos.  
```bash
top
``` 

Para sair, pressione ***q***.  

---  
  
`ps` — ***Process Status***

Fornece uma **fotografia instantânea** dos processos em execução. Pode ser combinado com várias opções:

- `ps aux` → Lista **todos os processos** do sistema com detalhes como %CPU, %MEM, PID, TTY, TIME, CMD etc.

- `ps -u` [usuario] → Exibe apenas os processos pertencentes ao **usuário especificado**.

- `ps -p` [PID] → Mostra informações sobre um **processo específico** pelo seu PID.

- `ps -C` [comando] → Filtra e exibe processos associados a um **comando** específico.  

---  
  
`pstree` — ***Process Tree***

Mostra uma **árvore hierárquica** dos processos, revelando as relações entre **processos pai** e **filhos**.  
```bash
pstree
```  
  
---  
  
## Filtrando e Organizando Saídas  

`head` — ***Head of File***

Exibe as **primeiras linhas** de um arquivo ou de uma saída de comando.
Por padrão, mostra as **10 primeiras linhas**.  
```bash
head /var/log/syslog  
```  
---  
  
`|` — ***Pipe***  

O operador pipe (`|`) redireciona a saída de um comando como **entrada para outro**.
É muito útil para encadear comandos.
```bash
ps aux | head
```  
---  

`sort` — ***Sort Output***

Ordena a saída de um comando ou o conteúdo de um arquivo.
Pode ser combinado com `|` para organizar informações.
```bash
ps aux | sort -k 3 -r  # Ordena processos pelo uso de CPU (coluna 3)
```  
---  
  
## Encerrando Processos

`kill` — ***Kill Process***

Envia **sinais** para processos em execução.
O uso mais comum é para **encerrar** processos.

- `kill` [PID] → Envia o sinal padrão `SIGTERM` (encerra de forma **suave**).

- `kill -9` [PID] → Envia `SIGKILL` (encerra de forma **forçada**).

- `kill -STOP` [PID] → Envia `SIGSTOP` (pausa o processo).

- `kill -CONT` [PID] → Envia `SIGCONT` (retoma o processo pausado).  
  
---  
  
`pkill` — ***Process Kill by Name***

Permite **enviar sinais com base no nome do processo**.
Exemplo: para encerrar todos os processos “firefox”:
```bash
pkill firefox
```  
  
***Todos os processos com o nome especificado serão afetados.***  
  
---  
  
`killall` — ***Kill All Processes by Name***

Semelhante ao `pkill`, mas também **encerra múltiplos processos com o mesmo nome**:
```bash
killall firefox
```  
  
---  

[Voltar ao módulo anterior ⬅ Apagando arquivos e redirecionando saídas ](../apagando)  
[Voltar à página inicial ⬅ ](./)  
[Próximo módulo: ⬅ Ainda não tem]()   