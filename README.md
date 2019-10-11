# 手写原理

- 实现`New`方法
- 实现`bind/call/apply`方法

```bash
npm install -g webpack
```

```js
// 被观察者  我家小宝宝 心情好不好 心情好 -》 心情不好
class Subject {
  constructor(name){
      this.name = name;
      this.observers = []; //观察者 要存放到被观察者中
      this.state = '心情很美丽'
  }
  // 被观察者要提供一个接受观察者的方法
  attach(observer){
      this.observers.push(observer); // 存放所有的观察者
  }
  // 更改被观察者的状态
  setState(newState){ 
      this.state = newState;
      this.observers.forEach(o=>o.update(newState));
  }
} 
class Observer{
  constructor(name){
      this.name = name;
  }
  update(newState){ // 用来通知所有的观察者状态更新了
      console.log(this.name+'说：宝宝'+newState);
  }
}
let sub = new Subject('小宝宝');
let o1 = new Observer('爸爸');
let o2 = new Observer('妈妈');
sub.attach(o1);
sub.attach(o2);
sub.setState('心情不好了');
```

> Markdown增强版中比较有名的有Markdown Extra、MultiMarkdown、 Maruku等。这些衍生版本要么基于工具，如~~Pandoc~~，Pandao；要么基于网站，如GitHub和Wikipedia，在语法上基本兼容，但在一些语法和渲染效果上有改动。

***
* * * 
********
-------------

**呼啦**  
*呼啦*  
***呼啦***


```json
{
  "name": "webpack-test",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "dependencies": {},
  "devDependencies": {
    "webpack": "^4.41.0",
    "webpack-cli": "^3.3.9"
  },
  "scripts": {
    "build": "webpack"
  },
  "author": "",
  "license": "ISC"
}
```


```scss
body{
  background: red;
  .node{
    font-size: $f
  }
}
```

```node
node -v
```
