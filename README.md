# BUCKY

## create dynamodb table

```
aws dynamodb create-table --table-name ShareToWin --attribute-definitions AttributeName=AssetID,AttributeType=N --key-schema AttributeName=AssetID,KeyType=HASH --provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1
```

![Screenshot (358)](https://user-images.githubusercontent.com/75828535/183304022-c113d8e7-4bef-476c-b3b2-5f97e348a76b.png)
