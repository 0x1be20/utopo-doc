# 注册项目

使用Utopo的能力，首先需要创建一个项目。

```java
import com.utopo.sdk.Client;
import  
String email="example@gmail.com";
String password="password";
SignClient client = new SignClient();

// 获取access token
String ak = client.login(email,password);

// 创建项目
client.createApp("projectName");

// 获取所有的项目
System.out.println(client.getDapps());

```
