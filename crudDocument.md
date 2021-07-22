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
