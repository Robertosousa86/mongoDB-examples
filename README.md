# MongoDb Examples

- Examplos de códigos para o banco de dados não relacional MongoDB.

## Comandos

- Para dar "start" no server, execute o comando  ```mongod```, se você está utilizando o sistema operacional windows execute ```mongod.exe```.

- Por padão o MongoDB escuta a porta 27017. O servidor pode falhar ao iniciar se a porta padrão não estiver disponível, a causa mais comum  para isso é outra instancia do mongoDB já estiver executando.

- Obs: Pode ocorrer um erro ao iniciar o mongoDB no linux, no caso o erro retorna o  ```status=14```, uma maneira de solucionar este erro é executando os comandos:
```sudo chown -R mongodb:mongodb /var/lib/mongodb```
```sudo chown mongodb:mongodb /tmp/mongodb-27017.sock```
e em seguida 

- Você pode parar a execução do mongoDB de maneira segura digitando o comando ```Ctrl-C``` no mesmo terminal em que o servidor está rodando.