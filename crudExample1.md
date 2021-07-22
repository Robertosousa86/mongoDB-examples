``` javascript
db 

use video 

db.movies 

db 

 movie = {"title" : "The Goonies",
"director" : "Richard Donner",
"year" : 1985 } 

db.movies.insertOne(movie)
db.movies.find().pretty()
db.movies.findOne()
db.movies.updateOne({title: "The Goonies"}, {$set : {reviews: []}})
db.movies.find().pretty()
db.movies.deleteOne({title : "The Goonies"})
```
