# "message": "Executor error during find command :: caused by :: errmsg: \"Sort operation used more than the maximum 33554432 bytes of RAM. Add an index, or specify a smaller limit.\"",

>error picture:
![image (5)](https://user-images.githubusercontent.com/71556060/149980608-b01adef8-9b24-4ade-8464-6dff271c9f01.png)

# Solution:
run these commands to incress the volume and solve the problem.

# to open the mongo shell
```
mongo
```
#to shows the list of dbs in mongo
```
>show dbs;
```
#switch to your use db ,in my case i use "inventory"
```
> use inventory;
```
#to see collection of dbs mongo ,in my case i use "inventories"
```
> db.inventories
```
#see your collection
```
> db.inventories.find({}).pretty();
```
#use most oof table you use in db,and make it index,in my case i use "created_at" or "region_id"
#it also improve the speed to use and do fast operations;
```
> db.inventories.createIndex({created_at:1});
```
```
> db.inventories.createIndex({region_id:1};
```
#exit
```
exit 
```
or
```
ctrl+d
```


thank you!



