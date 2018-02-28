# LinuxWebServer
The Configuration summary of Linux server for web applications

## Server Infrmation

* OS: ubuntu 16.04.3 LTS
* IP: 52.15.200.115
* webApp URL: http://dw48studio.tk/app/catalog

## Software Installed

* python 3.5
* python3-pip
* vitualenvs
* apache2
* postgresql 9.4
* mod-wsgi-py3


## Comfiguration

1. Create user `grader` 
    * add user to `sudo` group
    * grant user right to use command `sudo` wiht password
    * create ssh rsa key pair
2. Create user `webadmin`
3. activate `ufw` 
    * add rule to allow 2200/tcp
    * add rule to allow 80/tcp
    * add rule to allow 123/tcp
4. configurate `ssh` daemon
    * change connection port to 2200
    * deny `root` remote access
    * remove password access
5. create virtual enviroment for the applications
6. configurate `postgresql`
    * Remove remote access
7. Install `Catalogapp`
    * create webserver directory
    * clone the github repo
    * create the databe and user
    * intialize the database
    * configure the app to work with wsgi
8. configure `apache2`
    * add the `Catalogapp` configuration to run as wsgi app
    * enable the apache2 headers for Access-Control-Allow-Origin
9. set the time zone to UTC

## third-party resources

* Amazon Lightsail(http://lightsail.aws.amazon.com)
* freenom (http://www.freenom.com/en/index.html?lang=en)