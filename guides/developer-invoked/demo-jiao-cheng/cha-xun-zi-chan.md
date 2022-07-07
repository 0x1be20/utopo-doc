# 查询资产

现在查询某个用户拥有的所有的游戏资产。

```java
import com.utopo.sdk.SignClient;
import com.utopo.sdk.Nft;
import com.utopo.sdk.NftAttribute;
import java.util.List;

String collectionHash="exampleCollectionHash";
String owner="0x162A00559A981ED8b8a35Fb6f7b381451526c143";
SignClient client = new SignClient();

// 获取用户的所有资产
System.out.println(client.getNftsByOwner(collectionHash,owner));

```
