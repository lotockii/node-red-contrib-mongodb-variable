## node-red-contrib-mongodb-variable

A [Node-RED](http://nodered.org) node to query [MongoDB](https://www.mongodb.com/).

    Edited by Andrii Lototskyi

### Install

Run the following command in the root directory of your Node-RED install

    npm install node-red-contrib-mongodb-variable

 MongoDB node driver 3.0 interface for Node-RED
 based on [node-red-bluemix-nodes](https://github.com/node-red/node-red-bluemix-nodes/tree/master/mongo) and [MongoDB 3 Driver](http://mongodb.github.io/node-mongodb-native/3.0)
 Please refer to the [mongoDB node driver 'Collection' documentation](http://mongodb.github.io/node-mongodb-native/3.0/api/Collection.html) to read about each operation.

### Set Credentials

   add data to settings.js

    mongoConnects:
    {
       uri: "mongodb://login:password@host:27017/dbName"
    },


### Example For Request

   set data in function node

    msg.payload = {"login": "login"};
    return msg;


### Example node-red flowgit 

Import the flow below in an empty sheet in nodered

    [{"id":"35c76478.e1723c","type":"function","z":"25b7c5b4.6f1eba","name":"setup params","func":"msg.queryParameters = msg.queryParameters || {};\nmsg.queryParameters.param1 = 1;\nmsg.connectName = 'connect1';\nreturn msg;","outputs":1,"noerr":0,"x":273,"y":96,"wires":[["740c574e.518e28"]]}]
