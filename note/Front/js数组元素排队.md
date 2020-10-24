1.  `push()`
 将数据添加到一个数组的末尾
```php
// push() 将数据添加到一个数组的末尾
var arr = [1, 2, 3];
arr.push(4);
//现在arr的值为[1, 2, 3, 4]

```

2. `.pop()` 函数移除数组末尾的元素并返回这个元素
```php
// 
var threeArr = [1, 4, 6];
var oneDown = threeArr.pop();
console.log(oneDown);   //输出6
console.log(threeArr); 	//输出[1, 4]

```

3. shift()类似`.pop()`,不同的是移除数组的第一项
```php
// 
var myArray = [["John", 23], ["dog", 3]];
var removeFromOurArray = myArray.shift(); // [["dog"], 3]

```

4. `unshift()` 移入一个元素到数组头部
```php
// 
var myArray = [["dog", 3]];
myArray.unshift(["Paul", 35]);
//myArray = [["Paul", 35], ["dog", 3]]

```

## 把数字添加到数组的结尾,然后移出数组的第一个元素
```php
function nextInLine(arr, item) {
	arr.push(item);
	item = arr.unshift();
	return item;
}

nextInLine([], 5) //返回 5
nextInLine([], 2) //返回 2
nextInLine([5, 6, 7, 8], 1) //返回 5

```

#js #数组
