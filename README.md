# ssh2all
Run commands on multiple remote hosts over SSH

# Successor
The successor to this little tool is my SSH Commander tool. It is superior in every way. [Get it on Github](https://github.com/AthenaNetworks/ssh_commander)

## Requirements
PHP CLI and sshpass are required. These can be installed on Debian-based systems by running:
```apt install php-cli sshpass -y```

## Configuration
Configuration is done in config.php (see Installation for alternative config file). Two main variables need to be set up, the $hosts variable and the $creds variable.
```
<?php
        $hosts = array(
                "10.100.76.23",
                "10.100.76.24",
                "10.100.76.25",
                "10.100.78.26",
                "10.100.78.27",
                "10.100.99.28",
                "10.100.99.29"
        );

        $creds = array(
                "username" => "sshuser",
                "password" => "securesshpass"
        );
?>
```
## Usage
Once the config file is written, execute ssh2all with the arguments you want to run on all hosts:
```
# ./ssh2all uptime
```
## Installation
Execute ```install ssh2all /usr/bin/ssh2all``` to install ssh2all. Once installed, all configuration will be read from ```/etc/ssh2all.conf```
