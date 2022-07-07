# 铸造游戏资产

有了资产专辑之后，我们就可以在专辑中铸造游戏中所需要的游戏道具了。

```java
import com.utopo.sdk.SignClient;
import com.utopo.sdk.Nft;
import com.utopo.sdk.NftAttribute;
import java.util.List;

String email="example@gmail.com";
String password="password";
String collectionHash="exampleCollectionHash";
String owner="0x162A00559A981ED8b8a35Fb6f7b381451526c143";
SignClient client = new SignClient();

// 获取access token
String ak = client.login(email,password);

List<Attribute> attributes = new List();
attributes.add(
    new Attribute(
        "attributeKey":"type",
        "attributeValue":"normal"
    )
);

Nft item = new Nft(
    'nftName',
    'descriptioin',
    'https://where_image_store_url',
    attributes
);
// 创建项目
client.mintNft(collectionHash,item);

// 获取专辑中的所有资产
System.out.println(client.getNfts(collectionHash));

```
