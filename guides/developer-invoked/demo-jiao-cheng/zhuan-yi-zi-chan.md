# 转移资产

当用户购买了游戏道具之后，游戏需要将对应的游戏道具资产转移到对应的用户钱包里面。

```java
import com.utopo.sdk.SignClient;
import com.utopo.sdk.Nft;
import com.utopo.sdk.NftAttribute;
import java.util.List;
import com.utopo.sdk.reqs.Transfer;

String collectionHash="exampleCollectionHash";
String assetHash="exampleAssetHash";
String owner="0x162A00559A981ED8b8a35Fb6f7b381451526c143";
String privateKey="0xabcxxxxxxx";
String distOwner="0x65Cad5Dd2D5648F37292F3E93725883a54837f2E";
SignClient client = new SignClient();
Transfer transferReq = new Transfer(
    assetHash,
    distOwner
);
String message = client.sign(transferReq,privateKey);

client.transfer(transferReq,mssage);

// 获取用户的所有资产
System.out.println(client.getNftsByOwner(collectionHash,owner));
System.out.println(client.getNftsByOwner(collectionHash,distOwner));

```
