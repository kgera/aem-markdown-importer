# unified-dev-portal
# Standalone Markdown Importer

Imports Markdown documents into AEM, creating an AEM content package on the go.

## Why would you want this?

If you have a bunch of Markdown files, for instance [API documentation generated from Swagger](https://git.corp.adobe.com/trieloff/markdownified-swagger), or technical documentation that you want to publish on an AEM-powered web site, for instance [Adobe I/O](https://www.adobe.io). Your Markdown files are not hosted on Github.com, so you cannot use the built-in Markdown importer in Adobe I/O, but with this program you can include the Markdown to AEM conversion into your Continuous Integration process.

## Prerequisites

This is a Java application, so you need Java 8 or higher installed on your system.

```bash
$ java -version
java version "1.8.0_121"
Java(TM) SE Runtime Environment (build 1.8.0_121-b13)
Java HotSpot(TM) 64-Bit Server VM (build 25.121-b13, mixed mode)
```

If you want to build this project from source (right now, that's required), you will also need Maven 3.

```bash
$ mvn -v
Apache Maven 3.3.9 (bb52d8502b132ec0a5a3f4c09453c07478323dc5; 2015-11-10T17:41:47+01:00)
Maven home: /usr/local/Cellar/maven/3.3.9/libexec
Java version: 1.8.0_121, vendor: Oracle Corporation
Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "mac os x", version: "10.12.6", arch: "x86_64", family: "mac"
```

## Getting Started

### Building from Source

To use the application, check out this source code, then build with Maven:

```bash
$ mvn clean package
```

You will end up with a file called `target/importer-with-dependencies.jar`.

### Creating an AEM Content Package

Run the application using `java -jar` and pass in a configuration file:

```bash
$ java -jar java -jar target/importer-jar-with-dependencies.jar markdown2AEM.yml
```

This will create a file `importerDemo.zip`, which you can install in your AEM instance.

## Configuration

TODO

## Contributing

This application is work in progress and we are happy about any contribution. You can
- make a pull request on GitHub
- file an issue against the APM project in jira.adobe.com
- just say hi in the `#www_adobe_io` channel on Slack (Enterprise Grid)
