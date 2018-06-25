# Platooning

One Paragraph of project description goes here

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Connections

What things you need to install the software and how to install them

1. A linux PC (or virtual machine) needs to be connected to the MK5 nodes via the Ethernet switch.
Note: Making sure the devives in the LAN (local-area network) are all interconnected. This can be checked by SSH commands.

```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the example
1. The excutable needs to run with a configuration file, by using
```
./llc-platooning-app - f configuration.conf
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

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Sijie Zhu** - *Initial work* - [Sijie](https://github.com/sijiezhu)



