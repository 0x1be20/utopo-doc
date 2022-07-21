# 资产

## 专辑

```java
import com.utopo.sdk.SignClient;
import com.utopo.sdk.commom.Collection;
String email="example@email.com";
String password="password";
SignClient client = new SignClient();

client.login(email,password);

// 创建专辑
Collection collection = client.createCollection("collectionName");

```

## 列举所有的专辑

```java
import com.utopo.sdk.Client;
import com.utopo.sdk.commom.Collection;
import java.util.List;
String email="example@gmail.com";
String password="password";
SignClient client = new SignClient();

// 获取access token
String ak = client.login(email,password);

// 获取所有的项目
List<Collection> collections = client.getCollections());

```

## 铸造资产

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
    "nftName",
    "descriptioin",
    "https://where_image_store_url",
    attributes
);
// 创建项目
client.mintNft(collectionHash,item);

// 获取专辑中的所有资产
List<Nft> nfts = client.getNfts(collectionHash);

```

## 获得所有的资产

```java
import com.utopo.sdk.SignClient;
import com.utopo.sdk.Nft;
import com.utopo.sdk.NftAttribute;
import java.util.List;

String collectionHash="exampleCollectionHash";
String owner="0x162A00559A981ED8b8a35Fb6f7b381451526c143";
SignClient client = new SignClient();

// 获取用户的所有资产
List<Nft> nfts = client.getNftsByOwner(collectionHash,owner);

```

## 转移资产

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
