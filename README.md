# BUCKY

## create dynamodb table

```
aws dynamodb create-table --table-name ShareToWin --attribute-definitions AttributeName=AssetID,AttributeType=N --key-schema AttributeName=AssetID,KeyType=HASH --provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1
```

![Screenshot (358)](https://user-images.githubusercontent.com/75828535/183304022-c113d8e7-4bef-476c-b3b2-5f97e348a76b.png)

## Requirements

1. NodeJS on ec2 Instance
2. `npm install -g ganache-cli truffle`
3. git client on ec2

```
#Perform a quick update on your instance:
sudo yum update -y

#Install git in your EC2 instance
sudo yum install git -y

#Check git version
git version
```


4. install dependencies
```
$ npm install -g ganache-cli truffle
$ cd ShareToWinContract
$ npm install
$ ../cd ShareToWinRestApi
$ npm install
$ ../cd ShareToWinWeb
$ npm install
$ aws dynamodb create-table --table-name ShareToWin --attribute-definitions AttributeName=AssetID,AttributeType=N --key-schema AttributeName=AssetID,KeyType=HASH --provisioned-throughput ReadCapacityUnits=1,WriteCapacityUnits=1 
```

5. Port Forwarding 
![Screenshot (360)](https://user-images.githubusercontent.com/75828535/183305588-1823512c-02e2-46f4-a239-6d8eb257bbd9.png)

6. create accounts
```
cd ShareToWinContract
npx ganache-cli  --acctKeys ../ShareToWinRestApi/ethaccounts.json
truffle console --network development
compile
migrate
```

7.  
