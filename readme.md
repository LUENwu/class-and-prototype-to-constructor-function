## class 语法糖
```
class Person{
    // 类名首字母大写
    //属性：要放到构造函数中//
    //当new一个类时，就会自动执行构造函数，这时我们会传参属性传递给构造函数//
    //this 实例对象,原型对象里的方法也指向实例对象//
  constructor(name,age){
    this.name=name
    this.age=age
  }
  sayHi(){//是方法，也是函数名，方法会在原型对象中储存显示
     return console.log('你好,我叫' +this.name)
  }
}
let person = new Person('frank', 18)
let person2 = new Person('jack', 19)
```

## 结合原型的构造函数
```
function Person(name,age){
  this.name=name
  this.age=age
}
Person.prototype.sayHI=function(){
  return console.log('你好,我叫' + this.name)
}
let person = new Person('frank', 18)
let person2 = new Person('jack', 19)

```