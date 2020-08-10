teamate

hyperledger fabric sample

pre-condition

- curl, docker, docker-compose, go, nodejs, python 
- hyperledger fabric-docker images are installed
- GOPATH are configured
- hyperledger bineries are installed (cryptogen, configtxgen ... etcs)

-network

1. generating crypto-config directory, genesis.block, channel and anchor peer transactions

cd network

./generate.sh

2. starting the network, create channel and join

./start.sh

-chaincode

3. chaincode install, instsantiate and test(invoke, query, invoke)

./cc_tea.sh instantiate v1.0

-prototype

cd ../prototype

4. nodejs module install

npm install

5. certification works

node enrollAdmin.js

node registerUser.js

6. server start

node server.js

7. open web browser and connect to localhost:8080



8.prototype 사이트맵 구조

![Untitled Diagram (1)](https://user-images.githubusercontent.com/65533485/89747292-20c95a00-daf9-11ea-91ca-2ea172024136.png)

-web_template

1. teamate/network 이동

    cd network



2. ./teardown.sh 실행을 통해 conainer 제거

    ./teardown.sh



3. ./start.sh 실행을 통한 network 실행 

    ./start.sh



4. ./cc_tea.sh 실행을 통한 chaincode install

    ./cc_tea.sh 



5. web_template 로 이동 후 npm을 이용한 라이브러리 설치

    cd .. && cd web_template && npm install



6. enrollAmdin.js 실행을 통한 adminID 등록

web_template 폴더 안에 wallet 폴더가 존재하면 삭제 후 다음과 같은 명령어 실행

    node enrollAdmin.js



7. registerUser.js 실행을 통한 user2등록

    node registerUser.js



8. Server 실행

    node server.js



9. web_template Architecture

![ezgif com-video-to-gif](https://user-images.githubusercontent.com/65533485/89754661-becc1d00-db17-11ea-8346-12d509a9de1b.gif)

![Untitled Diagram (2)](https://user-images.githubusercontent.com/65533485/89754218-f89c2400-db15-11ea-8a29-7243e924522f.png)

10. Web_template 시나리오

![Untitled Diagram (4)](https://user-images.githubusercontent.com/65533485/89756352-3486b780-db1d-11ea-8f21-34551fc01096.png)

11. Web_template Uml

![Untitled Diagram (5)](https://user-images.githubusercontent.com/65533485/89759170-841cb180-db24-11ea-8fca-51d62aad2087.png)
