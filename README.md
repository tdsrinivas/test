# Prod git repo configuration

## sling-service-zuul-prod.yml

- Update theia listener configuration
```
slingTheiaListener:
  host: THEIA_HOST_NAME # for e.g., http://svip-theialistener.int.slingtv.com
  port: THEIA_PORT      # for e.g., 10555
```
***

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
    password: `{encrypt}ENCRYPTED_MONGO_PASSWORD`   # encrypted password, refer to "Encrypting confidential data" section
    dbname: msmongoprod                             # database name to use
    host1: MONGO_HOST1:MONGO_PORT                   # host and port for mongo server1 in the cluster
    host2: MONGO_HOST2:MONGO_PORT                   # host and port for mongo server2 in the cluster
    host3: MONGO_HOST3:MONGO_PORT                   # host and port for mongo server3 in the cluster
```
***

## Encrypting confidential data
- Start the config server with `-DSLING_ENCRYPT_KEY=<encrypt_key>`
- Encrypt the string you want to encrypt using the below curl command, use the `<encrypt_key>` as password when prompted
```
curl -X POST -u slingadmin http://<config_server>:8888/encrypt -d <string_to_encrypt>
```
- Use the result of the previous command with the prefix {cipher} and enclose it with single back quotes (`)
```
`{cipher}269dee6aad0e1d6b23206cbd6e25a46c672627beb4df6fcfb39d7b4c48235f89`
```
_Note: Make sure you don't copy the command prompt when you copy the encrypted string_

