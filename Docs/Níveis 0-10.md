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



