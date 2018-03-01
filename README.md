# LinuxWebServer
The Configuration summary of Linux server for web applications

## Server Information

* OS: ubuntu 16.04.3 LTS
* IP: 52.15.200.115
* Ports: 2200(ssh), 80(http), 123(ntp)
* webApp URL: http://dw48studio.tk/app/catalog
* Ping is desable in the firewall 

## Software Installed

* python 3.5
* python3-pip
* vitualenvs
* apache2
* postgresql 9.4
* mod-wsgi-py3


## Configuration

1. Create user `grader` 
    * Add user to `sudo` group
    * Grant user right to use command `sudo` wiht password
    * Create ssh rsa key pair
2. Create user `webadmin`
3. Activate `ufw` 
    * Add rule to allow 2200/tcp
    * Add rule to allow 80/tcp
    * Add rule to allow 123/tcp
4. Configure `ssh` daemon
    * Change connection port to 2200
    * Deny `root` remote access
    * Remove password access
5. Create virtual enviroment for the applications
6. Configure `postgresql`
    * Remove remote access
7. Install `Catalogapp`
    * Create webserver directory
    * Clone the github repo
    * Create the database and user
    * Initialize the database
    * Configure the app to work with wsgi
8. Configure `apache2`
    * Add the `Catalogapp` configuration to run as wsgi app
    * Enable the `apache2` headers for Access-Control-Allow-Origin
9. Set the time zone to UTC

## third-party resources

* Amazon Lightsail(http://lightsail.aws.amazon.com)
* Freenom (http://www.freenom.com/en/index.html?lang=en)