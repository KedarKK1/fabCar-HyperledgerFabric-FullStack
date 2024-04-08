# How to start project -

- first setup hyperledger fabric in your machine
- in fabric-sample folder, paste this project, u can give it any name
- add your chaincode in any folder, but remember u will have to give chaincode's location wrt this project's folder
- then in this project folder, run ./startFabric.sh for starting the project (remember to put the correct chaincode name and chaincode path address from this folder like for a chaincode named fabcar, having constructor initLedger having path ../chaincode/fabcar/javascript relative to this folder & using javascript as chaincode language, change 34th line of startFabric.sh as 
```
./network.sh deployCC -ccn fabcar -cci initLedger -ccp ./chaincode/fabcar/javascript -ccl javascript
```
) 

- then go to client folder, do npm i, make sure to use node 16.20.2
- then go to apiserver folder, do npm i, then type in terminal 
node enrollAdmin # to generate ca(certificate authority) of admin
node registerUser # to generate ca(certificate authority) of user
node invoke # to invoke constructor on fabcar chaincode
node query # to get a query
node apiserver # to start server on localhost:8080

