# 几种操作 :+1: ：
## 1. sort()
 
## 2. push() , pop() , shift() , unshift()
 
## 3. concat() , slice() , splice()的区别
> ### sort()
```ruby
  function compare(v1,v2){
	return v1 - v2; //升序
  }

  var values = [ 0 , 1 , 15 , 10 , 5];
  ```
```ruby
  values.sort();
  console.log(values);//[ 0 , 1 , 10 , 15 , 5 ] 
  ```
```ruby
  values.sort(compare);
  console.log(values);	//[ 0 , 1 , 5 , 10 , 15 ]
  ```
> ### push() , pop() , shift() , unshift()
```ruby
  values.push(2);
  console.log(values);  //[ 0 , 1 , 5 , 10 , 15 , 2 ]
  ```
  
  ```ruby
  values.pop();
  console.log(values);	//[ 0 , 1 , 5 , 10 , 15 ]
  ```
  ```ruby
  values.shift();
  console.log(values);	//[ 1 , 5 , 10 , 15 ]
  ```
  ```ruby
  values.unshift(3,4);
  console.log(values);	//[ 3, 4 , 1 , 5 , 10 , 15 ]
  ```
> ### concat() , slice() , splice()
  ```ruby
  var newValues1 = values.concat(1,4);	//在后添加
  console.log(newValues1);	//[ 3, 4 , 1 , 5 , 10 , 15 , 1 , 4 ]
  console.log(values);	//不改变原数组  [ 3, 4 , 1 , 5 , 10 , 15 ]
  ```
```ruby
  var newValues2 = values.slice(1,4);	//删除位置 1 开始到位置 4 结束
  console.log(newValues2);	//[ 4 , 1 , 5 ]
  console.log(values);	//不改变原数组  [ 3, 4 , 1 , 5 , 10 , 15 ]
  ```
  ```ruby
  //splice(当前位置开始 , 删除项数):删除(两参数)、插入(三个参数及以上)、替换(三个参数及以上)
  var newValues3 = values.splice( 3 , 1 (0 表示不删除元素，返回值为空) , "blue" );
  console.log(newValues3);	//[5]   ( newValues3数组变为 [ 3, 4 , 1 , "blue" , 10 , 15 ] ,返回值为被删除的项)
  console.log(values);	//[ 3, 4 , 1 , "blue" , 10 , 15 ]
  ```
