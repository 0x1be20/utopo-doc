# 创建资产专辑

每一件游戏资产都是放在资产专辑中，每一个资产专辑可以被多个游戏使用。我们现在通过SDK创建一个游戏专辑，然后再在这个新专辑中铸造游戏资产。

```java
import com.utopo.sdk.SignClient;

String email="example@gmail.com";
String password="password";
SignClient client = new SignClient();

// 获取access token
String ak = client.login(email,password);

// 创建项目
client.createCollection("collectionName");

// 获取所有的专辑
System.out.println(client.getCollections());

```
