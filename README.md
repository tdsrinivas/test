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
    username: MONGO_USERNAME                        # mongo database username
    password: `{encrypt}ENCRYPTED_MONGO_PASSWORD`   # encrypted password, refer to How to Encrypt the password section
    dbname: msmongoprod                             # database name to use
    host1: MONGO_HOST1:MONGO_PORT                   # host and port for mongo server1 in the cluster
    host2: MONGO_HOST2:MONGO_PORT                   # host and port for mongo server2 in the cluster
    host3: MONGO_HOST3:MONGO_PORT                   # host and port for mongo server3 in the cluster
```
***

## sling-service-zuul-prod.yml

- Update theia listener configuration
```
slingTheiaListener:
  host: THEIA_HOST_NAME # for e.g., http://svip-theialistener.int.slingtv.com
  port: THEIA_PORT      # for e.g., 10555
```


