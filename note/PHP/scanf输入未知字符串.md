**scanf()函数接收输入数据时，遇以下情况结束一个数据的输入：**

① 遇空格、“回车”、“跳格”键。
② 遇宽度结束。
③ 遇非法输入。

**scanf接收包含空格的字符串**

```
#include <stdio.h> 
int main() 
{ 
    char str[80]; 

    scanf("%s",str); 
    printf("%s",str);
    return 0; 
}123456789
```


输入：I love you!
输出：I
原因：scanf遇空格结束读取。

解决：

```
#include <stdio.h> 
int main() 
{ 
    char str[80]; 

    scanf("%[^\n]",str); //读到'\n'结束读取
    printf("%s",str);
    return 0; 
}123456789
```


输入：I love you!
输出：I love you!

------

```
//读到'\n'结束读取,存入str,再抛弃一个字符
scanf("%[^\n]%*c",str);12
//读到'\n'结束读取,并将其读到的数据抛弃,然后再抛弃一个字符（这个字符是'\n'）
//此时缓存中不存在任何字符
scanf("%*[^\n]%*c");123
int c;
while((c=getchar())!='\n'&&c!=EOF); 
//读取一个字符，直到是\n或者是EOF停止
//等价于
scanf("*[^\n]");
123456
   #include <stdio.h>
   int main()
   {
       char  c;    
       //直到遇到字符a停止读取，
       //舍弃a
       //读取将a后的一个字符存入变量c
       scanf("%*[^a]%*c%c",&c);
       printf("%c\n",c);
       return 0;
   } 1234567891011
```

输入：bcdeaf
输出：f