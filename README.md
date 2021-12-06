# jakarta-security-example

A simple Jakarta Security example to understand how it works and test application servers

At this point the project only includes a simple example taken from the [Soteria](https://github.com/eclipse-ee4j/soteria) repository, more specifically [this one](https://github.com/eclipse-ee4j/soteria/tree/master/test/app-mem-customform).

The example has been tested to work on [Payara Server 5.2021.9 Community Edition (Web Profile)](https://www.payara.fish/downloads/payara-platform-community-edition/), just deploying after the server is installed. 

To make it work on [WildFly Preview 25.0.1](https://www.wildfly.org/downloads/), you should first follow the instructions [Marcos Zolnowski](https://stackoverflow.com/users/1968258/marcos-zolnowski) wrote in [his answer to my StackOverflow post](https://stackoverflow.com/a/70240973/361343):

1. Run `$WILDFLY_HOME/bin/add-user.sh` and add a management user;

2. Run `$WILDFLY_HOME/bin/standalone.sh` to run the server;

3. Open the administration console at http://localhost:9990/ and log in with the newly created user;

4. Click on _Configuraion_ > _Subsystems_ > _Web_ > _Application Security Domain_ > _Other_ > _View_;

5. Click _Edit_ and change the value of _Integrated JASPI_ to _OFF_, then click _Save_;

6. Click _Reload_ to reload the server.
