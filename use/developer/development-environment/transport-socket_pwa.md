# Transport Socket Setup (PWA)

## Getting started

### Introduction

The Unified Communications Interface (UCI) aims to democratize the use of different communication channels such as WhatsApp, Telegram, SMS, email and more for governance use cases through a standard configurable manner that is reusable and scalable across all governance use cases.

Transport socket takes request from chatbot client and send it to UCI adapter to get response and return it back to bot client

[UCI] <---> [Socket Transport Layer] <---> [Frontend]

### Overview

This document helps you to setup transport socket which helps communicate between UCI backend and frontend. To experience the conversation with chatbot on UCI web channel, UCI-PWA needs to be setup from [here](/use/developer/development-environment/frontend-setup-pwa.md).

### Pre-requisites

1. Update to latest version

   ```
   $ sudo apt update
   $ sudo apt-get update
   $ sudo apt-get upgrade
   ```

2. Install Git

   ```
   $ sudo apt-get install git
   ```

3. Install curl

   ```
   $ sudo apt-get install curl
   ```

4. Install Node.js, npm, yarn and NVM

   ```
   $ sudo apt install nodejs
   $ sudo apt install npm
   $ sudo npm install yarn
   ```

   - Node version should be latest or stable (v16.15.0)
   - To check node version:

     ```
     $ node -v
     ```

   - To install NVM and more information of node installation, [check here](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04).

5. Set up on Docker

   - Install [Docker](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04)

   - Setup and run redis on docker

     ```
     $ sudo docker run --name my-first-redis -p 6379:6379 -d redis
     ```

## Setup

### For the first time:

1.  **Fork** the repository:

    - To get a copy of the repository, you need to fork the following:-

      - [Transport Socket](https://github.com/samagra-comms/transport-socket)

2.  **Clone** the forked repository:

    - To download the forked repository, you need to clone it.

      ```
      $ git clone repository-link
      ```

3.  Move to the directory with the cloned repository:

    ```
    $ cd transport-socket
        or
    $ cd <path of transport-socket folder>
    ```

4.  Run the following command to see if your local copy has a reference to your forked remote repository in GitHub:

    ```
    git remote -v

    # which should give this output-

    origin  https://github.com/Your_Username/repo_name.git (fetch)
    origin  https://github.com/Your_Username/repo_name.git (push)
    ```

5.  Import the cloned repository to the chosen IDE.

6.  Move to required branch:

    ```
    $ git checkout uci-pwa
    ```

7.  Install the required packages

    - In terminal (location should be same as the current location of the repository), run this command to install all the packages required to run the code:-

    ```
    $ yarn install
    ```

8.  Setup all the environment variables:-

    ```
    REDIS_HOST=localhost
    REDIS_PORT=6379
    SERVER_PORT=3005
    ```

    - Contact the [administrator](#contact-the-administrator) to get this or setup this on local using this [link](/use/developer/development-environment/backend-setup.md)

      ```
      ADAPTER_URL=http://localhost:8080/pwa/web
      ```

9.  Once all the required packages are successfully installed and .env files are setup, start the project.

## Run the project:

1. To start the project, run the following command:-

   ```
   $ yarn start
   ```

## Contact the administrator

Please write to the Maintainer - Chakshu (chakshu@samagragovernance.in), and cc - Saket (saket@samagragovernance.in), Sukhpreet (sukhpreet@samagragovernance.in)
