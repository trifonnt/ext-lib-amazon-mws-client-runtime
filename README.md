[![Build Status](https://travis-ci.org/trifonnt/ext-lib-amazon-mws-client-runtime.png?branch=master)](https://travis-ci.org/trifonnt/ext-lib-amazon-mws-client-runtime)
[![](https://jitpack.io/v/trifonnt/ext-lib-amazon-mws-client-runtime.svg)](https://jitpack.io/#trifonnt/ext-lib-amazon-mws-client-runtime)


Amazon MWS(Marketplace Web Service) Client Runtime Library - Version 2011-10-01.V269521071
=============================================================================== 
The project is mavenised unofficial copy of Java library provided by Amazon for dealing with Amazon Marketplace Web Service API.
It is common Java Client Runtime available in Amazon MWS libraries, like:

 - https://developer.amazonservices.com/doc/products/products/v20111001/java.html

 - https://developer.amazonservices.com/doc/orders/orders/v20130901/java.html


Current CI status: https://travis-ci.org/trifonnt/ext-lib-amazon-mws-client-runtime


About this Library
=============================================================================== 

Based on the 2011-10-01 API version.
Refers only to the [MWSProductsJavaClientLibrary-2011-10-01.zip](https://images-na.ssl-images-amazon.com/images/G/01/mwsportal/clientlib/Products/2011-10-01/MWSProductsJavaClientLibrary-2011-10-01._V269521071_.zip) file.


Prerequisites
=============================================================================== 

- Amazon Pro Merchant seller account or another Amazon account that makes you eligible to use Amazon Marketplace Web Service (Amazon MWS). For more information, see the [Amazon MWS FAQ](https://developer.amazonservices.com/gp/mws/faq.html).

- Registering for Amazon MWS. For more information see the [Amazon MWS FAQ](https://developer.amazonservices.com/gp/mws/faq.html).

- Java Platform Standard Edition 6.0 Development Kit (JDK 1.6.0_19) or newer. If your version of the JDK is older than 6.0, you must install the newer version. For more information, go to the Java SE Downloads page. 


## How to

### Build this project when starting from scratch
```shell
$ mvn archetype:create \
 -DarchetypeGroupId=org.apache.maven.archetypes \
 -DgroupId=com.github.trifonnt \
 -DartifactId=ext-lib-amazon-mws-client-runtime \
 -DpackageName=com.amazonservices.mws.client \
 -Dversion=1.0.0

$ cd ext-lib-amazon-mws-client-runtime
$ rm src/main/java/com/amazonservices/mws/client/App.java
$ rm src/test/java/com/amazonservices/mws/client/AppTest.java
```

### Migrate to new version of Amazon MWS Products library
```shell
$ git clone https://github.com/trifonnt/ext-lib-amazon-mws-client-runtime.git

$ cd ext-lib-amazon-mws-client-runtime

$ mkdir orig-library

$ cd orig-library

$ wget https://images-na.ssl-images-amazon.com/images/G/01/mwsportal/clientlib/Products/2011-10-01/MWSProductsJavaClientLibrary-2011-10-01._V269521071_.zip

$ unzip MWSProductsJavaClientLibrary-2011-10-01._V269521071_.zip


$ cp ../../ext-lib-amazon-mws-products/LICENSE.txt  ../
$ cp ../../ext-lib-amazon-mws-products/.travis.yml  ../
$ cp ../../ext-lib-amazon-mws-products/.gitignore  ../

$ mkdir ../src/test/resources/

$ mv runtime-src/com/amazonservices/mws/client/*.java ../src/main/java/com/amazonservices/mws/client


$ mvn clean install -Dmaven.javadoc.skip=false
```

### Publish new version to JitPack

 - Create new Release in GitHub

 - Open below URL in order to start JitPack build process

```shell
https://jitpack.io/com/github/trifonnt/ext-lib-amazon-mws-client-runtime/1.0.2
```

### Get this project into your Maven build(pom.xml)
```xml
...
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
 ...
 ...
 	<dependency>
	    <groupId>com.github.trifonnt</groupId>
	    <artifactId>ext-lib-amazon-mws-client-runtime</artifactId>
	    <version>1.0.2</version>
	</dependency>
...
```

Licensing
=============================================================================== 

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
