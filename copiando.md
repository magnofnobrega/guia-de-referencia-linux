# 📂 Movendo arquivos e diretórios  

O comando `mv` (move) é utilizado para mover ou renomear arquivos e diretórios.
Já o comando `cp` (copy) é usado para copiar arquivos e pastas, mantendo o original intacto.
Antes de mover ou copiar, é importante conhecer as permissões dos arquivos e diretórios.  
  
 ---  
    
## Verificando permissões com `ls -l`, `ls -a` e `ls -la`  

| **Comando** | **Descrição** |  
|-------------|---------------|
| `ls -l` | Exibe a listagem detalhada dos arquivos e diretórios **(permissões, dono, grupo, tamanho e data)**. |  
| `ls -a` | Exibe todos os arquivos, inclusive os ocultos **(aqueles que começam com ponto .)**.
 |  
| `ls -la` | Combina as **duas** opções: mostra **arquivos ocultos** e **informações detalhadas**. |  
  
   
---    
  
**Exemplo de saída:**  
```bash
-rw-r--r--  1 user user  2048 out  6 09:20  documento.txt  
drwxr-xr-x  2 user user  4096 out  6 09:30  projetos
```  

| Campo | Significado |  
|-------|-------------|  
| -rw-r--r-- | Permissões (leitura, escrita, execução). |  
| 1 | Número de links. |  
| user | Dono do arquivo. |  
| user | Grupo do dono. |  
| 2048 | Tamanho em bytes. |  
| out 6 09:20 | Data e hora da última modificação. |  
| documento.txt | Nome do arquivo. |  
  

---  
     
## Estrutura das permissões no Linux:

r → leitura (read)  

w → escrita (write)  

x → execução (execute)  

```bash
-rw-r--r--

```  
  
  
| **Tipo** | **Dono** | **Grupo** | **Outros** | **Descrição** |  
|----------|----------|-----------|------------|---------------|  
| `-` | `rw-` | `r--` | `r--` | Arquivo comum; dono pode ler e escrever; grupo e outros só leem. |  

**Tipo do item**  

| **Símbolo** | **Tipo** |
|-------------|----------|  
| `-` | Arquivo comum |  
| `d` | Diretório |  
| `l` |	Link simbólico |  
| `c` |	Dispositivo de caractere (ex: terminal) |  
| `b` |	Dispositivo de bloco (ex: HD, pendrive) |  

No exemplo `-rw-r--r--`, o primeiro caractere é -, ou seja, é um arquivo comum.  

---  
  
  
## Movendo diretórios com `mv`

Para mover um diretório (e seu conteúdo) para outro local:

```bash
mv /home/magno/projetos /home/magno/Documentos/
```
  
Isso moverá a pasta projetos para dentro de Documentos.  

---


## Movendo arquivos com `mv` 

Para mover um arquivo para outro diretório:

```bash
mv relatorio.txt /home/magno/Documentos/  
```  

O arquivo relatorio.txt será movido para a pasta Documentos.

---
  

## Renomeando arquivos e diretórios com `mv`

O mesmo comando `mv` pode ser usado para renomear:

```bash
mv relatorio.txt relatorio_final.txt
```  
ou  
```bash
mv /home/magno/projetos /home/magno/projetos_antigos
```  

---

  

## Copiando arquivos e diretórios com `cp`  

Copiar um arquivo:
```bash
cp relatorio.txt /home/magno/Documentos/  
```  
  
Copiar um diretório inteiro (com conteúdo):  
```bash
cp -r projetos /home/magno/Backup/  
```  
O parâmetro `-r` (ou `--recursive`) é obrigatório para copiar diretórios completos.  

  

[Voltar ao módulo anterior ⬅ Criando diretórios e arquivos no Linux](/diretorios.md)  
[Voltar à página inicial ⬅ ](/README.md)  
[Próximo módulo: ⬅ Apagando arquivos e redirecionando saídas](/apagando.md)   