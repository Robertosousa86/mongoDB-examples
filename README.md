# MongoDb Examples

- Examplos de códigos para o banco de dados não relacional MongoDB.

## Instalação no Ubunto 20.04 LTS

### Atualização e dependências 
```sudo apt update```
\
```sudo apt install dirmngr gnupg apt-transport-https ca-certificates software-properties-common```

### Download
```wget -qO - https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -```

### Adicionando o repositório
```echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list```

### Atualizando o repositório
```sudo apt update```

### Instalando
```sudo apt install mongodb-org```

## Comandos

- Para dar "start" no server, execute o comando  ```mongod```, se você está utilizando o sistema operacional windows execute ```mongod.exe```.

- Por padão o MongoDB escuta a porta 27017. O servidor pode falhar ao iniciar se a porta padrão não estiver disponível, a causa mais comum  para isso é outra instancia do mongoDB já estiver executando.

- Obs: Pode ocorrer um erro ao iniciar o mongoDB no linux, no caso o erro retorna o  ```status=14```, uma maneira de solucionar este erro é executando os comandos:
```sudo chown -R mongodb:mongodb /var/lib/mongodb```
```sudo chown mongodb:mongodb /tmp/mongodb-27017.sock```
e em seguida 

- Você pode parar a execução do mongoDB de maneira segura digitando o comando ```Ctrl-C``` no mesmo terminal em que o servidor está rodando.