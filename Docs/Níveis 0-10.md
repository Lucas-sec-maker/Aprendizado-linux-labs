# 📍 Nível 0 -> Nível 1

### 🎯 Objetivo
Realizar o primeiro acesso remoto ao servidor do jogo utilizando o protocolo SSH no terminal ( Ubuntu ) 

### Conceitos

    Protocolo SSH: É um protocolo de rede que permite conectar a um computador remoto de forma criptografada e segura via linha de comando.

    Sintaxe básica: ssh usuario@servidor

    Flag -p: Por padrão, o serviço SSH roda na porta 22.
    A flag -p 2220 avisa ao terminal para tentar a conexão em uma porta customizada (2220), que é onde o servidor do Bandit está escutando.
---

### 💻 Comando Utilizado
```bash
ssh bandit00@bandit.labs.overthewire.org -p 2220
```
### Resultado Final
<img width="1769" height="976" alt="image" src="https://github.com/user-attachments/assets/f7b282e6-a791-4439-9328-88b97c462195" />

# 📍 Nível 1 -> Nível 2

## 🎯 Objetivo
Manipulação de arquivos nomeados com certos sinais ( "-" no caso desse laboratório)
```
#Comandos para abrir o arquivo nomeado como "-"
    cat ./nome-do-arquivo 
    cat < -nome-do-arquivo
ps:cat é o comando para ler um arquivo dentroo de um diretório
```
### Resultados ( Com alguns testes )
<img width="1833" height="927" alt="image" src="https://github.com/user-attachments/assets/b302b04b-e340-4055-8dc1-d60b688e1f23" />

# 📍 Nível 2 -> Nível 3

## 🎯 Objetivo
Manipulação de arquivos nomeados com sinais e espaços ( "-" " " )
    - No Linux, arquivos com sinais, no caso, o hífen, podem ser confundidos com comandos ( -- confi, --help).
    No desafio anterior isso foi resolvido.7
    - Com espaços , o sistema pode achar que o espaço está separando comandos ou argumentos.
```
#Como eu resolvi: -> nome do arquivo :  "--spaces in this filename--"
comando:
        cat -- "--space in this filename--"
        cat "./--space in this filename--"
```
# 📍Nível 3 -> Nível 4

## 🎯 Objetivo 
Manipulação de pastas ocultas dentro de um diretório. Um arquivo ou diretório oculto se faz oculto quanto é nomeado com ponto no inicio.
```
#Nome do arquivo --> touch .meu_arquivo
#Comando para mostrar o arquivo:
ls -a ( exibe todos os arquivos ocustos , mais a hierarquia de pastas. A atual e a anterior )
la -A ( faz a mesma coisa, mas sem exibir os pontos de hierarquia de pasta )
```
<img width="720" height="273" alt="image" src="https://github.com/user-attachments/assets/b493288e-c140-450f-b7b9-3b143be3395a" />

# 📍 Nível 4 -> Nível 5

## 🎯 Objetivo
Encontrar a chave do próximo nível dentro de um diretório cheio de arquivos, onde apenas um é legível para humanos.Alguns arquivos podem estar em códgios escritos para sejam lidos pelos níveis mais baixos ( à nível de máquina, ou seja, binários )
    
 <img width="812" height="211" alt="image" src="https://github.com/user-attachments/assets/ff666aa6-9be1-474c-a986-31e7c5df3028" />

 Para achar devo descobrir qual é o arquivo que possui um formato legível para humanos. Entrei no diretório e listei os arquivos.Logo em seguida, listei todos os arquivos com o comando "file" 
 ```
file ./*
```
Além de listar os arquivos, o comando "file" analise o tipo de conteúdo no arquivo. Adicionando "*", faço isso com todos os arquivos de uma vez.E como todos os arquivos começam com hífen, é necessário adicionar "./". Resultando no comando acima

<img width="842" height="345" alt="image" src="https://github.com/user-attachments/assets/ce223411-d510-468d-9565-bd22427baa52" />

Olhando para os arquivos, aquele legível para humanos tem o formado ASCII text.

# 📍 Nível 5 -> Nível 6 

## 🎯 Objetivos
Encontrar a chave entre os diretórios, sabendo que é um arquivo não executável, legível para humanos e com o tamanho de 1033bytes.Isso tudo em meio à muitas páginas.

<img width="793" height="599" alt="image" src="https://github.com/user-attachments/assets/21955551-cc59-4bce-80e1-1aaaf1748c0c" />

Eis o comando:
```
find inhere/ -type f -size 1033c ! -executable

```
"find inhere" --> vai fazer uma procura dentro da pasta "inhere"

"-type f" --> é um argumento que define o tipo do arquivo.No caso, o tipo "file"

"-size 1033c" --> indica qual o tamnho do arquivo que estou procurando

"! -executable" --> o ponto de exclamação inverte a lógica do argumento "-executable". " NOT executable"

<img width="683" height="285" alt="image" src="https://github.com/user-attachments/assets/c418dd95-ba3f-41b4-a15b-ad2dcabb2822" />






    


