# 账户

## 登录与获取Token

开发者首先通过邮箱与密码，获得access token。该token是后续进行项目资产管理携带的凭证。这个token没经过7天更新一次。

```java
import com.utopo.sdk.SignClient;

String email="example@gmail.com";
String password="password";
SignClient client = new SignClient();

// 获取access token
String ak = client.login(email,password);

```
