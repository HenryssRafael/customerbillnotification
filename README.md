# Customer Bill Notification 

## Recursos

[Twitter Developer - Direct Message](https://developer.twitter.com/en/docs/twitter-api/v1/direct-messages/sending-and-receiving/api-reference/new-event) - How send direct message for twitter

# Objetive
Notifier to customers of their recent billed amount.

### Prerequisites

* Java 1.8+
* Maven 3.3.9
* Mule 4.2.2
* Active MQ 5.13.2 o later
* 10.4.19-MariaDB
* Twitter account Developer

make sure have configured enviroment varible ***runtimeKeyEnc***
At runtime set **VM Arguments**
```
-DruntimeKeyEnc=mycustomkey
```

Algorithm for encrypt **Blowfish CBC**
```
java -cp secure-properties-tool.jar com.mulesoft.tools.SecurePropertiesTool string encrypt Blowfish CBC mySecretKey "myEncr"
```

Create dataBase
```
create database lla
```

Create Tables
```
CREATE TABLE audit (
    id int NOT NULL AUTO_INCREMENT,
    createdDate DATETIME,
    updatedDate DATETIME,
    message VarChar(255),
	successful boolean,
	recipientId VarChar(255),
	uuid VarChar(255),
    PRIMARY KEY (id)
);
```

### Installing

First download own custom Extension [**Twitter Extension**](sdfsdf) 

1. Access the folder location for  Twitter Extension and execute installing

```
mvn install
```

## Running

* ***POST*** Deploy the application, and send the request ***POST***
http://localhost:8081/core/1/notifier Authentication is required

*Know user id twwiter
https://tweeterid.com/


## Authors
* **Henry Avila** - *Initial work* - [HenryssRafael](https://github.com/HenryssRafael)

## Acknowledgments

* Mule SDK
* Anypoint Studio
* Mule Security
* Maven