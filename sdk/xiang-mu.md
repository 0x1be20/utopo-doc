# 项目

## 注册项目

```java
import com.utopo.sdk.Client;
import com.utopo.sdk.common.App;

String email="example@gmail.com";
String password="password";
SignClient client = new SignClient();

// 创建项目
App app = client.createApp("projectName");

```

## 列举所有的项目

```java
import com.utopo.sdk.Client;
import  com.utopo.sdk.common.App;
import java.util.List;

String email="example@gmail.com";
String password="password";
SignClient client = new SignClient();

// 获取access token
String ak = client.login(email,password);

// 获取所有的项目
List<App> apps = client.getDapps();

```
