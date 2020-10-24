## php退出登录时如何清除session信息
```php
//清空session信息
 $_SESSION = array();
//清除客户端设置的cookie
setcookie("session_name()", "", time() - 1, "/");
 //销毁session
session_destroy();
```