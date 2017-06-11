# PagerMon

PagerMon is an API driven client/server framework for parsing and displaying pager messages from multimon-ng.

It is built around POCSAG messages, but should easily support other message types as required.

The UI is built around a Node/Express/Angular/Bootstrap stack, while the client scripts are Node scripts that receive piped input.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

* [nodejs](https://nodejs.org/)
* Probably some other stuff

## Running the server

1) Edit server/process.json according to your environment
2) Launch the app from the Terminal:
```
    $ npm install npm@latest -g
    $ npm install pm2 -g
    $ npm install 
    $ export NODE_ENV=production
    $ pm2 start server/process.json
```
3) To start on boot, let pm2 handle it:
```
    $ sudo pm2 startup
    $ pm2 save
```
4) You probably want to rotate logs, too:
```
    $ pm2 install pm2-logrotate
    $ sudo pm2 logrotate -u user
```
5) Now login via the website, change your password, and generate some API keys
6) Grab your API keys and drop them in the PagerMon client, then you're good to go!

## Contributing

All are welcome to contribute.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/davidmckenzie/pagermon/tags). 

## Authors

See the list of [contributors](https://github.com/davidmckenzie/pagermon/contributors) who participated in this project.

## License

This project is licensed under The Unlicense - because fuck licenses. Do what you want with it. :>

## Acknowledgments

* [multimon-ng](https://github.com/EliasOenal/multimon-ng)
