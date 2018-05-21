r# web-monitoring-app

[![Standard - JavaScript Style Guide](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard) 

> Web-monitoring-app is a small web page monitoring written in node.js, you can monitor changing of a web page. Compatible with Node v8.4.0 and above. it uses repo [web-monitoring](https://github.com/antoniomuso/web-monitoring)



## How to install
`npm install web-monitoring-app -g`
## Use application
If you want to monitor a page with alert on terminal, use:
```
web-monitoring-app http://google.com
```
if you want to receive alert on email, use:
```
web-monitoring-app http://google.com -e myname@host.com passwordmyname reciver@host.com
```
Below are more specific options
```
web-monitoring-app [uri] -l [lapse of control] -p [percentage of page changing] -t [number of test for calculate automatic percentage of page changing] -e [email sender] [password sender] [email receiver]
web-monitoring-app http://google.com -l 5000 -p 0.1
or 
web-monitoring-app http://google.com -l 5000 -p 0.1 -e myname@host.com passwordmyname reciver@host.com
or
web-monitoring-app http://google.com -l 5000 -p 0.1 -e myname@host.com passwordmyname reciver@host.com -loop
Without command -loop, the program stop at first page change
```
**I recommend setting manually percentage of page change with dynamic pages, 0 is the minimum value, 1 is the maximum value**
```
web-monitoring-app http://google.com -p 0.2
```
## Authors

* **Antonio Musolino** - [antoniomuso](https://github.com/antoniomuso)



## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

