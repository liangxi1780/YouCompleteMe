# Hyperledger Composer - Product Auction Network With Events

*Read this in other languages: [한국어](README-ko.md),[中国](README-cn.md),[日本](README-ja.md)*

# WARNING: This repository is no longer maintained :warning:

> This repository, which contains assets to run a Hyperledger Composer application, is not being actively maintained due to a shift to focus on Hyperledger Fabric. This repository will not be updated. The repository will be kept available in read-only mode. Refer to https://github.com/IBM/auction-events for a similar example.

Welcome to Part 3 of the Hyperledger Composer Composite Pattern. This is a continuation of [Hyperledger Composer - Product Auction Network](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a6eba699b37a3fc663ab91ce83a8b38d3997b8b32b0618c36000f01c275cff8aadd17d3400854390d00ea6a9e24cb1e2d55075af7476758322ab302f5b10d6d  This pattern shows how events can be emitted by Hyperledger Composer and subscribed by external applications.

Audience level : Intermediate Developers

If you have an IBM Cloud Lite account, you can also use the Starter Plan for 30 days to do this pattern.

## Included Components

* Hyperledger Fabric
* Hyperledger Composer
* Docker

## Application Workflow Diagram

![Workflow](images/arch-blockchain-events.png)

* Start the Hyperledger Fabric Network
* Generate and Deploy the Business Network Archive
* Start and connect the composer rest server to deployed business network
* Start the Web Application

## Steps

1. [Generate the Business Network Archive (BNA)](#1-generate-the-business-network-archive-bna)
2. [Deploy the Business Network Archive to Local Hyperledger Fabric instance](#2-deploy-the-business-network-archive-on-hyperledger-fabric-running-locally)
3. [Start the Web UI](#3-start-the-web-ui)
4. [Submit Transactions](#4-submit-transactions)

## 1. Generate the Business Network Archive (BNA)

Make sure that you have installed the prerequisites for [Hyperledger Composer](http://u.720life.cn/g/38328d09a1514892b2e859b89f8720a2333754a3287ec80d3cf8dc26a5a509e00023898da3d395ae0ea128b863599f7317e990f73d586c4161ff7c1535eba09b151c041029287eeba83b32ab25e75da8 
Also, make sure that you have installed the development environment which
includes Hyperledger Composer, Hyperledger Fabric and the other node modules using these
[instructions](http://u.720life.cn/g/38328d09a1514892b2e859b89f8720a2333754a3287ec80d3cf8dc26a5a509e00023898da3d395ae0ea128b863599f73756f1a630565529e379f3ad1872c9bcf31f20b2645d37cd41fd3619943419793 
As a recap for those instructions, you should have done the following:

- Installed Hyperledger Composer and it's related Node modules using `npm`.
- Downloaded the docker images for Hyperledger Fabric.
- Started Hyperledger Fabric locally on your machine.
- Executed `createPeerAdminCard.sh` to create a network card that will be used to
install the business network later in this exercise.


Clone the repository:

```
$ git clone https://github.com/IBM/BlockchainEvents-CompositeJourney
```

To check that the structure of the files is valid, you can now generate a
Business Network Archive (BNA) file for your business network definition. The
`.bna` file is the deployable unit -- a file that can be deployed to the
Hyperledger Composer runtime for execution.

Use the following command to generate the network archive:

```
$ cd BlockchainEvents-CompositeJourney/Composer
$ npm install
```

You should see the following output:

```
$ mkdirp ./dist && composer archive create --sourceType dir --sourceName . -a ./dist/events.bna

Creating Business Network Archive


Looking for package.json of Business Network Definition
	Input directory: /Users/ishan/Documents/demo/BlockchainEvents-CompositeJourney/Composer

Found:
	Description: Sample product auction network with events
	Name: events
	Identifier: events@0.0.1

Written Business Network Definition Archive file to
	Output file: ./dist/events.bna

Command succeeded
```

The `composer archive create` command has created a file called `events.bna` in
the `dist` folder.

You can test the business network definition against the embedded runtime that
stores the state of 'the blockchain' in-memory in a Node.js process. From your
project working directory, open the file test/productAuction.js and run the
following command:

```
$ npm test
```

You should see the following output :

```
> events@0.0.1 test /Users/ishan/Documents/demo/BlockchainEvents-CompositeJourney/Composer
> nyc mocha -t 0 test/*.js



  #org.acme.product.auction
    ✓ Authorized owner should start the bidding (74ms)
    ✓ Members bid for the product (139ms)
    ✓ Close bid for the product (175ms)


  3 passing (2s)

----------|----------|----------|----------|----------|-------------------|
File      |  % Stmts | % Branch |  % Funcs |  % Lines | Uncovered Line #s |
----------|----------|----------|----------|----------|-------------------|
All files |        0 |        0 |        0 |        0 |                   |
----------|----------|----------|----------|----------|-------------------|
```

## 2. Deploy the Business Network Archive to Local Hyperledger Fabric instance

Make sure that you have started Hyperledger Fabric instance locally on your machine
using these [instructions](http://u.720life.cn/g/38328d09a1514892b2e859b89f8720a2333754a3287ec80d3cf8dc26a5a509e00023898da3d395ae0ea128b863599f73756f1a630565529e379f3ad1872c9bcf31f20b2645d37cd41fd3619943419793 
Now change directory to the `dist` folder containing `events.bna` file and execute
the following commands to install/deploy and start the business network on the
local Hyperledger Fabric instance:

```
$ cd BlockchainEvents-CompositeJourney/Composer/dist
$ composer network install -c PeerAdmin@hlfv1 -a events.bna
$ composer network start -c PeerAdmin@hlfv1 -n events -V 0.0.1 -A admin -S adminpw -f networkadmin.card
$ composer card import --file networkadmin.card
```

You can verify that the network has been deployed by typing:

```
$ composer network ping --card admin@events
```

You should see the the output as follows:

```
The connection to the network was successfully tested: events
The connection to the network was successfully tested: events
	Business network version: 0.0.1
	Composer runtime version: 0.19.5
	participant: org.hyperledger.composer.system.NetworkAdmin#admin
	identity:org.hyperledger.composer.system.Identity#e7eaa3bc255f5ded89fd5c25748aca87959c9b3fc6ad6a94c65d679162db84fd
Command succeeded
```

To create the REST API we need to launch the `composer-rest-server` and tell it how to connect to our deployed business network. Now launch the server by changing directory to the product-auction folder and type:

```
$ cd BlockchainEvents-CompositeJourney/Composer
$ composer-rest-server

? Enter the name of the business network card to use: admin@events
? Specify if you want namespaces in the generated REST API: never use namespaces
? Specify if you want to use an API key to secure the REST API: No
? Specify if you want to enable authentication for the REST API using Passport: No
? Specify if you want to enable event publication over WebSockets: Yes
? Specify if you want to enable TLS security for the REST API: No
```

**Test REST API**

If the `composer-rest-server` started successfully you should see these two lines are output:

```
Web server listening at: http://localhost:3000
Browse your REST API at http://localhost:3000/explorer
```

## 3. Start the Web UI

In a new terminal window, navigate to `Web` directory and launch the node server using command:

```
cd BlockchainEvents-CompositeJourney/Web
$ npm install
$ node server.js
```

## 4. Submit Transactions

Submit transactions for auction network using the instructions in [Hyperledger Composer Section](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466a6eba699b37a3fc663ab91ce83a8b38d3997b8b32b0618c36000f01c275cff8aadd17d3400854390d00ea6a9e24cb1e3f6e31668bf956733f7eeccdf759b531b8c04e2db11b94a2518648e57f51926f78aaade8e99ffcda62fc17929a238d63b3acaa84b7af4609ac58af56840b745ff5ddd9b9d4a14578f4fc8defec782869  Events are emitted when user submits `publishListing`,
`makeoffer` and `closeBidding` transactions. Web UI for seller and buyer updates
on the event emitted from the Hyperledger Fabric network.

You can submit the transactions either by using Hyperledger Composer REST API or
Hyperledger Composer Playground running locally.

### Using REST API

Open a web browser and navigate to `http://localhost:3000/explorer`.

### Using Composer Playground

You can Install the Hyperledger Composer Playground locally as shown below:

```
$ npm install -g composer-playground
```

And, run the Hyperledger Composer Playground locally using:
```
$ composer-playground
```

Navigate to `http://localhost:8000/seller.html` and `http://localhost:8000/buyer.html`
to view the dashboards for Seller and Buyer events.

## Additional Resources
* [Hyperledger Fabric Docs](http://u.720life.cn/g/38328d09a1514892b2e859b89f8720a2cda66177584a46bb4c1937888c8e6e6d48241d641f159ee30ffae3f35194923e) 
* [Hyperledger Composer Docs](http://u.720life.cn/g/38328d09a1514892b2e859b89f8720a2333754a3287ec80d3cf8dc26a5a509e00023898da3d395ae0ea128b863599f73f2aabbf65b7cc31dd816e2031a3075e6b2d0a46efdd31477727da387d65cdd08) 

## License
This code pattern is licensed under the Apache Software License, Version 2.  Separate third party code objects invoked within this code pattern are licensed by their respective providers pursuant to their own separate licenses. Contributions are subject to the [Developer Certificate of Origin, Version 1.1 (DCO)](http://u.720life.cn/g/a69e8f5dba5b4106ccc3875c547b1484ed328b8520c563a7b9cd9ee25a33d6f3b4f92d796026ab599797e203c22f481a)  and the [Apache Software License, Version 2](http://u.720life.cn/g/9504ecfd7de2b26345fb4a78087ff8e39017fae1e889f3875d0fa1b09af9991ca4b64225882adc4686609984b01b56e3f546ca44d2b50b9cc692086f4bcfceb7 

[Apache Software License (ASL) FAQ](http://u.720life.cn/g/9504ecfd7de2b26345fb4a78087ff8e37f78cc0f2053227f9d93f5e8e73024a8921fff8f97d8ad1cb579316f9f48dbe7b6d60a479d310d5bbd9f915ce4a06b8cc1d9c1ffe3ff38fe08afc397a013ef5c) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)