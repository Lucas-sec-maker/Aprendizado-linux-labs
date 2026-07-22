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

