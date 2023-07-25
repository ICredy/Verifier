# Acme Controller
Web controller for a Hyperledger Aries Acme CloudAgent

## Table of Contents

- [Running Locally](#running-locally)
    - [Prerequisites](#prerequisites)
    - [Starting the Application](#starting-the-application)
- [Notes](#notes)

### Steps to start:
Note: Before carrying out the following process, start up the von-network from Docker on localhost:9000, as the agent requires the von-network, and without starting it, it won't work.
Commands:
cd von-network
./manage build
./manage start --logs
visit: localhost:9000
Step 1: Clone the aries-cloudagent-python project in your system from this link:https://github.com/hyperledger/aries-cloudagent-python
Step 2: Starting the verifier agent Open git bash and navigate to the folder where the agent project is cloned.
Step 3: Then write the command ACME Agent: cd /aries-cloudagent-python/demo.
Step 4: Then, to run the agent, write:./run_demo acme, and In case of error, docker rm -f acme. Now we have successfully run the agent.

Step 5: Now we will run the controller project. Clone the controller project in your system from the GitHub link:https://github.com/hyperledger/aries-acapy-controllers

Step 6: Navigate to the folder in another bash tab using the command cd /aries-acapy-controllers/AliceFaberAcmeDemo/controllers/acme-controller.

Step 7: Write npm install and then npm start.

Step 8: Now a successful verifier controller will be started on localhost:3000.

### Running Locally

#### Prerequisites

Acme Controller requires `Node.js 10.x` or higher. Node.js can be downloaded [here](https://nodejs.org/en/download/). Alternatively you can use a Node.js version manager like [`nvm`](https://github.com/nvm-sh/nvm) or [`nvm-windows`](https://github.com/coreybutler/nvm-windows).

#### Starting the Application

From the acme-controller root directory, simply install application node modules then call `npm start`

For example on Linux:

```
$ npm install
$ npm start
```

You can now open your browser tab to `localhost:3000` to see the application.

### Notes

_Note: Acme Controller has already been configured to connect to it's agent on localhost:8041. If the controller is not connected to it's agent you will see a red status indicator on the top right-hand side of the navbar. If the agent is successfully connected, you will see a green status indicator._
