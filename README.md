mongoose-snippets
=================

A bunch of usefull queries I've found that I need on hand and I think might be usefull for other mongodb n00bs like me :)

I come from the lands of MySql so I will try to add the query I am trying to  replicate using mongoose



##baby stepts


Here we go!

###Get all

```
SELECT * FROM cat;
```

```javascript
CatModel.find({},function (err,result){
  ...
});
```



###Get specific fields

```
SELECT name,color FROM cat;
```

```javascript
CatModel.find({},'name color',function(err,data){
 ..
});
```


###Where clause

```
SELECT * FROM cat WHERE name = 'Catzinger';
```

```javascript
CatModel.find({name:'Catzinger'},function(err,data){
 ...
});
```
##Next level!

###Count
```
SELECT count(*) FROM cat ;
```

```javascript
Cat.count({},function(err,data){
 ...
});
```
###Count + where
```
SELECT count(*) FROM cat WHERE legs = 4;
```

```javascript
Cat.count({legs:4},function(err,data){
 ...
});
```
###Get random row
```
SELECT * FROM cat ORDER BY RAND() LIMIT 1;; 
```
```javascript
var rand = Math.floor(Math.random() * count);
Cat.findOne().skip(rand).exec(callback);
```


