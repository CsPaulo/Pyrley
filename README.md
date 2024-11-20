# Pyrley - O Compilador Python do Varley
### IFMA - Instituto Federal do Maranhão
### Orientador: Varley Santos de Sá
### Alunos:
 - <a href="https://github.com/antoniovini47">Antonio Vinícius Rodrigues Oliveira</a>
 - <a href="https://github.com/carlossantos74">Carlos Alessandro Ferreira dos Santos</a>
 - <a href="https://github.com/CsPaulo">Paulo Rafael Costa Silva</a> 
 - <a href="https://github.com/pedro31415">Pedro Henrique Araújo Cardoso</a>
 ----
## Como executar
### Dependências
 - Flex - Para compilar o arquivo Lex
 - Bison - Para compilar o arquivo Yacc
 - Gcc - Compilador C para criação do Parser
 - Figlet - Para o menu animado em shell

#### Instalação Ubuntu
 ```
sudo apt update && sudo apt upgrade
sudo apt install flex
sudo apt install bison
sudo apt install figlet
flex --version
bison --version
```
#### Instalação MacOS
```
brew update
brew install flex
brew install bison
brew install figlet
flex --version
bison --version
```
---
### Executando
#### Automaticamente
```
$ ./run.sh
```
#### Manualmente
##### 1. Gera o arquvio lex.yy.c a partir do grammar.l
```
flex grammar.l 
```
##### 2. Gera os arquivos grammar.tab.c e grammar.tab.h a partir do grammar.y
```
bison -d grammar.y
```
##### 3. Cria o parser a partir dos arquivos gerados
###### Para MacOS
```
gcc -o parser grammar.tab.c lex.yy.c -ll
```
###### Para Linux
```
gcc -o parser grammar.tab.c lex.yy.c -lfl
```
##### 4. Executa o parser, passando um arquivo para análise
```
./parser < exemplo.py
```
------
### Obrigado! Dê estrelinha ⭐️ e manda o pix, em caso de dúvidas, pede pro <a href="https://chatgpt.com">GPT</a> 