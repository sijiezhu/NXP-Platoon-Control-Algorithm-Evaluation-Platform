# llc-platooning-app 

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Connections

A Linux PC (or virtual machine) needs to be connected to the MK5 nodes via the Ethernet switch.
Note: Making sure the devices in the LAN (local-area network) are all interconnected. This can be checked by SSH commands.


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
The project directory includes a folder containing the source code and a Makefile realizing test automation.

1. The executable (llc-platooning-app) needs to run with a configuration file, by typing
```
make install
make run
```
Then, the script will do the followings:
1. Compile the project and generate the executable.
2. Copy the executable to the MK5 nodes.
3. Generate the configuration files for each node, according to the parameters in the Makefile.
4. Start the application in different nodes in the downstream direction (from the end to the leader).
5. Retrieve the logs and the time difference data.

Note 1: The log files are automatically generated on different MK5s after each test, named after LogX, where 'X' is the platoon member ID the node is configured. <br />
Note 2: The logging system records the status of the node every 10ms. A row of data is generated every logging cycle. <br />

As an alternative, the executable can be copied to the MK5 devices and started manually, by
```
sudo ./llc-platooning-app -f platoontest.conf
```
Note 1: the MK5s share the same executable and are identified with the configuration file. <br />
Note 2: to conduct tests correctly, the nodes should be started in the downstream direction (from the end to the leader). This can be realized manually or automatically (with a script). <br />



## Log Analysis

MATLAB scripts which can process the test logs are provided.
* Validation3.m processes the timestamps of the log files which were recorded based on synchronized device time.
* Validation4.m examines the string stability. It needs Log1.csv, Log2.csv, Log3.csv and Log4.csv to execute

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Authors

* **Sijie Zhu** - [Github](https://github.com/sijiezhu)



