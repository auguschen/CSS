#js学习教程
***关键字，运算符，流程语句直接略过，每种语言基本相同，但这些是基础中的基础，不会的同学也要去看看
##1.js对象
###1.1对象包含什么？
     属性
     字段

###1.2创建对象的方式
   ####1.2.1第一种使用Object
````js
var box=new Object();
    box.name="hsj";
    box.age=22;
    alert(box.name);
    alert(box.age)
    
    new关键字可以省略
    var box=Object();
    box.name="胡少君";
    alert(box.name);
```` 
   ####1.2.2字面量的方式
   
````js
    var box={};  字面量方式创建的对象
    alert(box);

     var box={             使用字面量封装数据
	  name:"胡少君",    字段可以加单引号
	  age:22
     };

        alert(box.name+box.age);
        
        
        var box={};  使用字面量创建对象
        box.name="胡少君"; 传统方式复制
        alert(box.name);
        alert(box['name']);
```` 

###1.3创建方法的方式
 ####1.3.1 Object赋值的方法
````js
  function objfun(){
    return "123";
  }
  
  var box=new Object();
  box.name="hsj";
  box.age=20;
  box.run=objfun(); 这种赋值正确,只赋值名,赋值的是引用
  alert(box.run);
````

####1.3.2使用字面量
```js
function funobj() {
	return "123";
}

var box={
  name:'hsj',
  age:20,
  fun:funobj
};

alert(box.fun);
```

###1.4删除对象内容
  删除使用delete
  如：delete box.name;
  
###1.5当函数传的参数非常多的时候可以封装成参数对象
```js
function  objfun(val1,val2,val3) {
    alert(val1);
    alert(val2);
    alert(val3);
  
}

var box={
    val1="hsj",
    val2="lyb",
    val3="jsy"
}

function objfun(box) {
  alert(box.val1);
  alert(box.val2);
  alert(box.val3);
}
```
学习时间2017年8月13日23:15:01
