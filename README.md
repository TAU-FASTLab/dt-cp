# **DT-CP: Digital twin for control and planning**

For more specific information about the use of this component, check [DT-CP_manual.pdf](./DT-CP_manual.pdf).

# About DT-CP

The Digital Twin for planning and control (DT-CP) allows to replicate a production line. The component is divided into two parts: a simulator, to experiment with alternative models to be implemented in the real line, and a monitoring dashboard for having an overview of the line.

The time-based simulator takes as input several configuration parameters (e.g., takt time, shift time), process descriptions and resources (e.g., workers with different skill levels). Hence, users can modify and test different production strategies that would be more complicated and time consuming to test in the real line. The monitoring dashboard can provide an overview of the production status and suggests shift schedules to improve the well-being of the workers.

The development of this component received funding from the European Union's Horizon 2020 research and innovation program called **SHOP4CF (Smart Human Oriented Platform for Connected Factories)**. For more information about the project, check [Official Website](https://shop4cf.eu/).

The monitoring table is a tailored solution for a SHOP4CF use case, so that some assumptions are made regarding the process to monitor. See its restrictions in [DT-CP_manual.pdf](./DT-CP_manual.pdf).

In case you are interested in a monitoring dashboard for you particular process, please contact the web developers of this page.
In the meanwhile, the general idea behind the monitoring dashboard can be consulted in the following publication: [Enhancing Digital Twins of Semi-Automatic Production Lines by Digitizing Operator Skills](https://www.mdpi.com/2076-3417/13/3/1637).

# Get Started 
## Prerequisites

The Docker images provided are targeting Windows hosts.

### Install Docker

Check the official [Docker documentation](https://docs.docker.com/engine/) for information on how to install Docker on your operating system.

## Installation 

Clone the repository containing the docker-compose.yml file
```
$ git clone https://github.com/TAU-FASTLab/dt-cp.git 
```

The Docker images of the component can be downloaded from the SHOP4CF repository of [RAMP Docker Registry](https://docker.ramp.eu/). 
For more information, check [SHOP4CF-Getting Started Guide.pdf](./SHOP4CF-Getting_Started_Guide.pdf).
-	`dt-fe`: Interface with which the user interacts (simulator and monitoring dashboard).
-	`dt-be`: API.
-	`dt-nh`: Notification handler that manages the communication with FIWARE.

They should be placed at the root of the project folder.

# Usage

Load images and start the container
``` 
docker-compose up 
```

When deployed locally, DT-CP can now be accessed at: `localhost:2308`

Stop the application
``` 
docker-compose down -v
``` 
