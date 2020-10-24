### mysqli_fetch_array()、mysqli_fetch_assoc、mysqli_fetch_row()和mysqli_fetch_object()的区别

mysqli_fetch_array() 来使用或输出所有查询的数据。



mysqli_fetch_array() 函数从结果集中取得一行作为关联数组，或数字数组，或二者兼有 返回根据从结果集取得的行生成的数组，如果没有更多行则返回 false。



使用mysqli_fetch_assoc()和mysqli_fetch_row()都是把查询结果返回到一个数组中，都是返回第一行然后指针下移一行。 

区别：mysqli_fetch_assoc()用关键字索引取值。比如： 
$row = $result->fetch_assoc(); 
echo $row['username']; 

但是mysqli_fetch_row()用数字索引取值。比如： 
$row = $result->fetch_row(); 
echo $row[0];//注：“0”的意思是表中的第一个字段（即username是表中的第一个字段）。 

另外还有一个函数：mysqli_fetch_object()将一行取回到一个对象中，然后通过类的方式取值，比如： 
$row = $result->fetch_object(); 
echo $row->username;