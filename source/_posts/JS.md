# JS

## js实现字符串数组转换成数字数组的几种方式

[js实现字符串数组转换成数字数组的几种方式](https://www.cnblogs.com/Ao-min/p/13808712.html?ivk_sa=1024320u)

### 遍历方式实现

```js
var turnNum = function(nums){
	for(let i=0;i<nums.length;i++){
		nums[i] = parseInt(nums[i])
	}        
	return nums;
}

console.log(turnNum(['1','2','3']))     // [1,2,3]

```



### Array map方法

```js
var turnNum = function(nums){
	return nums.map(Number);
}

console.log(turnNum(['1','2','3']))    // [1,2,3]

```



### forEach()方法

```js
var nums = ['1','2','3']
nums.forEach((item,index) =>{
	nums[index] = parseInt(nums[index])
})
console.log(nums)                     // [1,2,3]

```



## js把字符串转为数组对象

[js把字符串转为数组对象](https://blog.csdn.net/seimeii/article/details/120445459)

> 将 str = “1,2,3”, str2 =“hello,lisi,john”
>
> 转为：arr = [{id: 1,name: ‘hello’},{id: 2, name: ‘lisi’},{id: 3,name: ‘john’}]

```js
let arr = []
let s1 = str.split(',');
s.forEach((item,i) => {
	let obj = {};
	obj.id = item;
	arr.push(obj)
})
let s2  = str2.split(',')
s2.forEach((item, i) => {
	arr[i].name = item
})
```

```js
let test = ["item1", "item2", "item3"]

// 利用map转为对象数组
test = test.map((item,index) => {
    return {
        key: index,
        value: item
    }
})
```

<img src="C:\Users\hongsuan\AppData\Roaming\Typora\typora-user-images\image-20220727133853533.png" alt="image-20220727133853533" style="zoom:80%;" />





## js快速将字符串数组转化为数字数组（互换）

1、数字[数组]转化为字符串数组

```js
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9];
arr.map(String);  //结果： ['1', '2', '3', '4', '5', '6', '7', '8', '9']

```

2、字符串数组转化为数字数组

```js
var a = ['1', '2', '3', '4', '5', '6', '7', '8', '9']
a.map(Number);  //结果：[1, 2, 3, 4, 5, 6, 7, 8, 9]

```





## JS数字数组转数字

1、数字数组转数字（整型）

```js
let l1 = [2,4,3]
let num1 = parseInt(l1.join(""))
console.log(num1)   //243
```

2、数字数组转数字（浮点型）

```js
let l2 = [2, ".", 3]
let num2 = parseFloat(l2.join(""))
console.log(num2)   //2.3
```





## 处理[Object Promise]数据(Promise对象)

* 业务场景:打印后端传进来的数据时返回数据是`[Object Promise]`，在调用后端接口，打印数据以测试是否获取到数据，但是遇到返回的数据是`[Object Promise]`的

* 栗子:

  ```js
  getData() {
  	var id = '123456789';
  	var data = getDatas(id); // 注: getDatas(id)是已经封装好的发送请求的方法，参数是id
  	console.log(data)
  }
  ```

  请求获取到的数据，打印会出现`[Object Promise]` 的结果 : ×

* 原因: 没有用异步函数获取！

* 解决办法: 在函数前加上`async`和`await`

  ```js
  async getData() {
  	var id = '123456789';
  	var data = await getDatas(id); // 注: getDatas(id)是已经封装好的发送请求的方法，参数是id
  	console.log(data)
  }
  ```

  























