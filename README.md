# llc-platooning-app 

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Connections

A linux PC (or virtual machine) needs to be connected to the MK5 nodes via the Ethernet switch.
Note: Making sure the devives in the LAN (local-area network) are all interconnected. This can be checked by SSH commands.


### Installing

A step by step series of examples that tell you how to get a development env running

First enter the llc-platooning-app directory, and enter 

```
make mk5
```

The generated executable "llc-platooning-app" needs to be copied to the MK5 nodes

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the example
1. The excutable (llc-platooning-app) needs to run with a configuration file, by using
```
sudo ./llc-platooning-app -f platoontest.conf
```
Note 1: the MK5s share the same excutable and are identified with the configuration file.
Note 2: to conduct tests correctly, the nodes should be started in the downstream direction (from the end to the leader). This can be realized manually or automatically (with a script).
3. The log files are automatically generated on different MK5s after each test, named after LogX, where 'X' is the platoon member ID the node is configured.
4. The logging system records the status of the node every 10ms. A row of data is generated every logging cycle.


## Log Analysis

Matlab scripts which can process the test logs are provided.
* Validation3.m processes the timestamps of the log files which were recorded based on unsynchronised device time.
* Validation4.m examies the string stability. It needs Log1.csv, Log2.csv, Log3.csv and Log4.csv to execute

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Authors

* **Sijie Zhu** - [Sijie](https://github.com/sijiezhu)



