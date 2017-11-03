```javascript
obj.call(thisObj, arg1, arg2, ...);
obj.apply(thisObj, [arg1, arg2, ...]);
```
两者作用一致，都是把obj(即this)绑定到thisObj，这时候thisObj具备了obj的属性和方法。或者说thisObj『继承』了obj的属性和方法。唯一区别是apply接受的是数组参数，call接受的是连续参数。

```javascript
function add(a, b){
  return a + b;
}

function sub(a, b){
  return a - b;
}

add(5,3); //8
add.call(sub, 5, 3); //8
add.apply(sub, [5, 3]); //8

sub(5, 3); //2
sub.call(add, 5, 3); //2
sub.apply(add, [5, 3]); //2
```

```javascript
function Animal(name){      
    this.name = name;      
    this.showName = function(){      
        console.log(this.name);      
    }      
}      
    
function Cat(name){    
    Animal.call(this, name);    
}      
    
var cat = new Cat("Cat");     
cat.showName();  // Cat

```
> Animal.call(this) 的意思就是使用Animal对象代替this对象，那么Cat中就有Animal的所有属性和方法，Cat对象就能够直接调用Animal的方法以及属性了.
