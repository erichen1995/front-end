## php中的交互输入函数
```php
//类似c语言中的scanf， %d表示带符号的十进制0  %c表示字符
fscanf(STDIN, "%d %c", $num, $f);
```

## php中跳出循环层数
```php
continue 1;  //等于continue，结束跳过本循环
continue 2;  //跳出2重循环。
```

## 如何验证素数
定义：指在大于1的自然数中，除了1和该数自身外，无法被其他自然数整除的数。
判断n是不是素数。
2~$\sqrt{n-1}$能不能被n整除。

