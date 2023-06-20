# E-Voting System using Blockchain

This is a E-Voting System website made using React, NodeJS, MongoDB , Solidity and Ganache. This is voting system is Blockchain based, easy to use and with  face recognization capabilities.

For more details on this project read this [report](https://drive.google.com/file/d/1KJCA_DDZKEn6AIj1U3rWgylZuFRNBFqj/view?usp=sharing).

## Installation
---

### Requirements

1. Ganache 
2. Docker
3. Node Js (18.12 verion or up)
4. Google Chrome
5. Metamask Extension
6. A MongoDB Database connection

### Ganache
---
You can download Ganache from [here](https://trufflesuite.com/ganache/)

Follow the basic installation steps and open the Quickstart or New Workspace options.

### Docker
---
You can download Docker Desktop from [here](https://www.docker.com/products/docker-desktop/)

Follow the basic installation steps.

### NodeJS
---

You can download NodeJS from [here](https://nodejs.org/en)

Follow the basic installation steps.

### Google Chrome and Metamask
---
Download it from chrome [website](https://www.google.com/chrome/) and Metamask from [here](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn).

Install chrome , sign up and add the Metamask Extension and make an wallet account in metamask.

### MongoDB 
---
You need to create your own MongoDB database instance , follow the "Using the MongoDB Atlas UI" in this [guide](https://www.mongodb.com/basics/create-database) and make your first database and name it `Blockchain`.


## Installation Step
---

1. Install Compreface for Face recongnization , whose installtion steps can be found [here](https://github.com/exadel-inc/CompreFace/blob/master/README.md#getting-started-with-compreface)

2. Then you need to open this [http://localhost:8000/login](http://localhost:8000/login) and then signup and login

3.  Go to 'Test Tab' Create two services: Detection Service and Verfication service.

4. You will get the API Key for both the services from that page. Now in the server folder of the project directory make a new `.env` file and write the following code.

```sh
#paste the APIS you just created
APIDETECT=[Detecttion service API]
APIVERIFY=[Verification service API]
PRIVATEKEY=[add a random 16 deigit secret]
```
5. Now open Ganache and start a quickservice.

6. Now login into you mongoDB account and create a user for the cluster you just created and then click on the Connect button ![Alt text](/images//mongodb.jpg) and click on drivers option and copy this URL ![Alt text](/images//url.png) now in the .env folder created in step 4 add this 
```sh
CONNECTION_URL=mongodb+srv://admin-siddharth:<password>@cluster0.ziuav.mongodb.net/<your DB name here for example Blockchain>?retryWrites=true&w=majority
```
7. Now open the terminal and `cd` to  server directory and run the following command and wait for the `$ server is live`  message.
```sh
$ npm i
$ npm start
```

8. Now `cd` to the project directory and run the following command but first make sure the Ganache is runinng.

```sh
$ npm i
$ truffle migrate

```

10. Now `cd` to the client folder and run the following command.

```sh
$ npm i
$ npm start
```

11. website opens on (http://localhost:3000/login). Now signup and create election but remember to link account from Ganache to Metamask. The first ganache account will be assigned as admin.

12. Mkae sure to change the metamask account when logging in as a new user.

