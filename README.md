# web-monitoring-app
> Web-monitoring-app is a small web page monitoring written in node.js, you can monitor changing of a web page. Compatible with Node v8.4.0 and above. it uses repo [web-monitoring](https://github.com/antoniomuso/web-monitoring)


[![Standard - JavaScript Style Guide](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard) 

## How to install
`npm install web-monitoring -g`
## Use application
If you want to monitor a page with alert on terminal, use:
```
web-monitoring http://google.com
```
if you want to receive alert on email, use:
```
web-monitoring http://google.com -e myname@host.com passwordmyname myname@host.com
```
Below are more specific options
```
web-monitoring [uri] -l [lapse of control] -p [percentage of page changing] -t [number of test for calculate automatic percentage of page changing] -e [email sender] [password sender] [email receiver]
web-monitoring http://google.com -l 5000 -p 0.1
or 
web-monitoring http://google.com -l 5000 -p 0.1 -e myname@host.com passwordmyname myname@host.com
or
web-monitoring http://google.com -l 5000 -p 0.1 -e myname@host.com passwordmyname myname@host.com -loop
Without command -loop, the program stop at first page change
```
**I recommend setting manually percentage of page change with dynamic pages, 0 is the minimum value, 1 is the maximum value**
```
web-monitoring http://google.com -p 0.2
```