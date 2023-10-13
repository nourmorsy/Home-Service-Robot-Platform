# Home-Service-Robot-Platform
About the HSR
--------------------

Please refer to the following to obtain information about Human Support Robot (HSR) and use it in your paper.

https://robomechjournal.springeropen.com/articles/10.1186/s40648-019-0132-3

docker installation
--------------------

In order to run the simulator, docker and docker-compose are necessary.

In the case of a Windows or Mac environment, please install docker for Windows or Mac respectively.

In the case of Linux, please input the following commands and install docker.

```sh
$ curl -fsSL https://get.docker.com -o get-docker.sh
$ sh get-docker.sh
```

If you input the following command, even regular users will be able to execute the docker command.

```sh
$ sudo usermod -aG docker <USERNAME>
```

After executing the above command, log out then log in again.

Input the following command, then verify that docker can execute correctly.

```sh
$ docker info
```

Input the following commands and install docker-compose.
As the docker-compose that can be installed via apt-get is old,
please input all of the following commands to install the newest version of docker-compose.

```sh
$ sudo apt-get remove docker-compose
$ COMPOSE_VERSION=$(wget https://api.github.com/repos/docker/compose/releases/latest -O - | grep 'tag_name' | cut -d\" -f4)
$ sudo wget https://github.com/docker/compose/releases/download/${COMPOSE_VERSION}/docker-compose-`uname -s`-`uname -m` -O /usr/local/bin/docker-compose
$ sudo chmod 755 /usr/local/bin/docker-compose
```

Usage
------

Please input the following commands to clone this repository.

```sh
$ git clone --recursive https://github.com/hsr-project/tmc_wrs_docker.git
$ cd Home-Service-Robot-Platform
```

Download all of the images necessary for running the simulator.
As you will be downloading a large amount of data,
please execute the following command in an environment that is connected to a high speed network.

```sh
$ ./pull-images.sh
```

Starting the simulator
----------------------

Please input the following command and start the simulator.

```sh
$ docker-compose up
```

Please open each of the following URLs in a browser, then move on to development.

- The simulator's screen http://localhost:3000
- IDE http://localhost:3001
- jupyter notebook http://localhost:3002
Authors
---------------
 * Yosuke Matsusaka

Contact
---------------
 * HSR Support <xr-hsr-support@mail.toyota.co.jp>

LICENSE
---------------
This software is released under the BSD 3-Clause Clear License, see LICENSE.txt.
