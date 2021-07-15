O MongoDB tem suporte para vários tipos de dados, os tipos mais usados são:

- **Null**\
  O tipo Nulo pode ser usado para representar tanto um valor nulo como um campo não existente:

```javascript
{"x" : null}
```

- **Boolean**\
  O tipo boolean pode ser usado para valores **true**(verdadeiro) ou **false**(falso);

```javascript
{"x" : true}
```

- **Number**\
  Por padão o shell do MongoDB utiliza números de 64-bits com ponto flutuante(**float**), eles podem ser representados da seguinte forma:
  
  ```javascript
  {"x" : 3.14}
  {"x" : 3}
  ```
  Para números inteiros(**integers**), podemos usar as classes **NumberInt** de 4-byte ou **NumberLong** de 8-byte:

  ```javascript
  {"x" : NumberInt("3")}
  {"x" : NumberLong("3")}
  ```
- **String**\
  Qualquer caracter UTF-8 pode ser representado pelo tipo **string**:
  
  ```javascript
  {"x" : "Juliana"}
  ```
- **Date**\
  O MongoDB armazena datas como valores integer de 64-bits tendo ínicio pelo padrão Unix epoch(1 de janeiro de 1970, 00:00). O fuso horário não é armazenado:
  
  ```javascript
  {"x" : new Date()}
  ```
- **Regular Expression**\
  Queries podem usar a sintax do Javascript para _Regular expressions_(**regex**):
  
  ```javascript
  {"x" : /ab+c/}
  ```
- **Array**
  Conjuntos ou listas podem ser representados por **arrays**:
  
  ```javascript
  {"x": ["a","b","c"]}
  {"x": [1, 2, 3]}
  ```
- **Embedded document(Documento incorporado)**\
  Documentos podem conter outros documentos incorporados como valores de um documento pai:
  
  ```javascript
  {"x" : {"foo" : "bar"}}
  ```

- **Object ID**\
  Um _object ID_ é um ID de 12-byte para documentos:
  
  ```javascript
  {"x" : ObjectId()}
  ```

- **Code**\
  É possivel salvar códigos nativos do Javascript em queries e documentos:

```javascript
{"x" : function sun(a, b) {
  return a + b;
}}
```

- **Binary data**\
  Os dados binários são uma sequência de bytes não arbitrtários.
  Não podem ser manipulados a partir do shell do MongoDB, eles são a única maneira de salvar strings não UTF-8 no banco de dados.
