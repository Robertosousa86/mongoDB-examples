# Adicionando documentos

## Adicionando um documento

Inserções são métodos básicos para adicionar dados ao MongoDB. Para inserir um documento, podemos utilizar o método `insertOne`:

```javascript
db.movies.insertOne({
  "title" : "Stand by Me",
  "director" : "Rob Reiner",
  "year" : 1986,
  "reviews" : [],
});
```

O método `insertOne` íra adicionar uma chave "_id" ao documento, caso você não houver adicionado anteriormente, e salvará as informações no banco de dados.

## Inserindo vários documentos ao mesmo tempo

Podemos adicionar mais de um documento à uma coleção ao mesmo tempo utilizando o método ```insertMany```. Esse método permite que um array de documentos seja passado ao banco de dados, o que torna a inserção de dados mais eficiente.

```javascript
db.movies.insertMany([
  {"title" : "Ghostbusters"},
  {"title" : "Indiana Jones and The Last Crusade"},
  {"title" : "Terminator 2: Judgment Day"}
]);
```
// continuar...