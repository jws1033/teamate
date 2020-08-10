# teamate

# hyperledger fabric sample

## pre-condition

- curl, docker, docker-compose, go, nodejs, python 
- hyperledger fabric-docker images are installed
- GOPATH are configured
- hyperledger bineries are installed (cryptogen, configtxgen ... etcs)

# -network

## 1. generating crypto-config directory, genesis.block, channel and anchor peer transactions

cd network

./generate.sh

## 2. starting the network, create channel and join

./start.sh

# -chaincode

## 3. chaincode install, instsantiate and test(invoke, query, invoke)

./cc_tea.sh instantiate v1.0

# -prototype

cd ../prototype

## 4. nodejs module install

npm install

## 5. certification works

node enrollAdmin.js

node registerUser.js

## 6. server start

node server.js

## 7. open web browser and connect to localhost:8080



## 8.prototype 사이트맵 구조

![Untitled Diagram (1)](https://user-images.githubusercontent.com/65533485/89747292-20c95a00-daf9-11ea-91ca-2ea172024136.png)

## -web_template

#### 1. teamate/network 이동

```powershell
cd network
```



#### 2. ./teardown.sh 실행을 통해 conainer 제거

```powershell
./teardown.sh
```



#### 3. ./start.sh 실행을 통한 network 실행 

```powershell
./start.sh
```



#### 4. ./cc_tea.sh 실행을 통한 chaincode install

```powershell
./cc_tea.sh 
```



#### 5. web_template 로 이동 후 npm을 이용한 라이브러리 설치

```powershell
cd .. && cd web_template && npm install
```



#### 6. enrollAmdin.js 실행을 통한 adminID 등록

##### web_template 폴더 안에 wallet 폴더가 존재하면 삭제 후 다음과 같은 명령어 실행

```shell
node enrollAdmin.js
```



#### 7. registerUser.js 실행을 통한 user2등록

```shell
node registerUser.js
```



#### 8. Server 실행

```shell
node server.js
```

