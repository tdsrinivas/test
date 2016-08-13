# Prod git repo configuration

## prepaid-prod.yml
- Update theia listener configuration
```
slingTheiaListener:
  host: THEIA_HOST_NAME # for e.g., http://svip-theialistener.int.slingtv.com
  port: THEIA_PORT      # for e.g., 10555
```

- Set prepaid endpoint
```
prepaid:
    endpoint: INCOMM_HOST_NAME # for e.g., https://qvip-ext-incomm.int.slingtv.com/transferedvalue/gateway
    dbCollection: "prepaid_transaction_log"
```

- Configure Mongo URI
```
sling:
  mongo:
    username: MONGO_USERNAME
    password: `{encrypt}ENCRYPTED_MONGO_PASSWORD`
    
spring:
  data:
    mongodb:
      # for e.g., update with prod mongo uri
      uri: mongodb://${sling.mongo.username}:${sling.mongo.password}@MONGO_HOST1:27017,MONGO_HOST2:27017,MONGO_HOST3:27017/msqamongo
```
***

## 

## fdafsd

Update slingTheiaListener in “prepaid" and “zuul"
> We loved with a love that was more than love

> We loved with a love that was more fsa love

> fd

