# 🗑️ Apagando arquivos e redirecionando saídas  

## Removendo arquivos e diretórios

Para apagar arquivos e diretórios no Linux, utilizamos o comando `rm`.

**Remover um arquivo**
```bash
rm nome_do_arquivo
```  

***Atenção: uma vez removido, o arquivo não vai para a lixeira — ele é apagado permanentemente.***  

---  

**Remover um diretório vazio**
```bash
rmdir nome_do_diretorio
```  

Se o diretório contiver arquivos, o comando acima **não funcionará**.  

Use o `rm` com a opção `-r` para **remover tudo recursivamente**:

```bash
rm -r nome_do_diretorio
```  

---  

**Confirmação antes de apagar cada arquivo**

Adicione a opção `-i` para que o sistema peça confirmação antes de excluir:  

```bash
rm -ri nome_do_diretorio
```  
  
- `-r`: remove recursivamente (pastas e subpastas).
- `-i`: solicita confirmação antes de cada exclusão.  

---  

## Redirecionando saídas de comando

O terminal pode **enviar a saída de comandos para arquivos** usando os operadores `>` e `>>`.  

**Criar um arquivo com o resultado de um comando**  
```bash
ls > lista.txt
```  

- Cria o arquivo `lista.txt` com o resultado do `ls`.  
Se o arquivo já existir, ele será **sobrescrito**.  

---  

**Adicionar mais informações no mesmo arquivo**  
```bash
ls >> lista.txt
```  

- Adiciona o resultado ao final do arquivo, sem apagar o conteúdo anterior.

| **Operador** | **Ação** |  
|--------------|----------|  
| `>` | Sobrescreve o arquivo |  
| `>>` | Adiciona ao final do arquivo |  

---  

## Usando o comando echo

O comando `echo` é usado para exibir mensagens ou gravá-las em arquivos.
```bash
echo "Linux é poderoso!" > frase.txt
```

Cria o arquivo `frase.txt` com o texto `"Linux é poderoso!"`.  
  

Para adicionar mais uma linha:
```bash
echo "E também muito flexível!" >> frase.txt
```  

---  

## Permissões e propriedade de arquivos

Anteriormente vimos que as permissões são representadas por letras (`r`, `w`, `x`), mas o Linux também permite definir essas permissões por meio de números.
Esse formato é mais rápido e direto — muito usado em scripts e administração de sistemas.  

**Entendendo as permissões numéricas**

Cada arquivo ou diretório no Linux possui permissões e proprietário (usuário e grupo).
ssas permissões controlam quem pode ler, escrever ou executar o arquivo  

**Representação numérica (modo octal)**

Cada tipo de permissão recebe um valor:

| Permissão	| Valor	| Significado |  
|-----------|-------|-------------|  
| `r` (read) | 4 | leitura |  
| `w` (write) | 2 | escrita |  
| `x` (execute) | 1 | execução |  
  
Esses valores são **somados** para formar um número que representa as permissões de cada grupo:  

| Permissão	| Cálculo | Resultado |  
|-----------|-------|-------------|  
| `rwx` | 4 + 2 + 1 | 7 |  
| `rw-` | 4 + 2 + 0 | 6 |  
| `r--` | 4 + 0 + 0 | 4 |  

- Exemplo prático
```bash
chmod 755 script.sh
```  
- **7 (usuário)** → leitura, escrita e execução (rwx)  
- **5 (grupo)** → leitura e execução (r-x)  
- **5 (outros)** → leitura e execução (r-x)  

Resultado final:
```bash
-rwxr-xr-x
```

***esse modo numérico é mais curto e automatizável, ideal para scripts e comandos de configuração rápida.***  

---  

## Alterando o proprietário do arquivo

O dono (usuário) e o grupo podem ser modificados com o comando `chown`:
```bash
sudo chown usuario:grupo nome_do_arquivo
```  
Exemplo:
```bash
sudo chown magno:magno script.sh
```  
Assim, o arquivo script.sh passa a pertencer ao usuário `magno` e ao grupo `magno`.  

---  

## Obter ajuda sobre comandos
**Ajuda rápida**
```bash
comando --help
```  
Exemplo:
```bash
ls --help
```  
Mostra todas as opções do comando.  

---  

**Listar todos os comandos internos do shell**
```bash
help
```  
**Procurar comandos relacionados a uma palavra**
```bash
man -k .
```  
Mostra uma lista de todos os comandos com suas descrições resumidas — ótimo para explorar o sistema.


[Voltar ao módulo anterior ⬅ Movendo arquivos e diretórios ](/copiando.md)  
[Voltar à página inicial ⬅ ](/README.md)  
[Próximo módulo: ⬅ Ainda não tem]() 