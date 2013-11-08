#風若 foonyah
> /foo-nya/ ~ an speedy, cluster based, service oriented architecture

##3 step guide
1 ) To install the most recent release from fvm, run:
```sh
    curl https://fvm.cloudplus.me/install | sh
```
2 ) Init foonyah project with skill-hello
```sh
    foonyah init -with hello
```
3 ) Start fonnyah (use port:80)
```sh
    foonyah
```
then you can check on your browser
```
    http://localhost/?plugin_call=hello
```
* use port 27017 for mongodb gridfs
* [node.js](http://nodejs.org/) is automatically installed if nothing  
* hello is distributed as open project on [foonyah/skillup-hello](https://github.com/foonyah/skillup-hello)  
  
##API
__simple http server :__  
  1 web-server (http-based, port 80)  
```js
	require('foonyah').start();
```
__change port :__  
  1 web-server (http-based, port 8080)  
```js
	require('foonyah').start(8080);
```
__with ssl :__  
  1 web-server (https-based, port 8080)  
```js
	require('foonyah').start({
	  http:{port:8080, ssl: {key:'pem_key.pem', cert:'pem_cert.pem'}}
	});
```
__add websocket :__  
  1 web-server (http-based, port 8080)  
  with websocket-handshaker  
  [ystskm/websockets](https://github.com/ystskm/websockets)  
```js
	require('foonyah').start({
	  http:{port:8080, websocket:true}
	});
```
__foonyah-construction :__  
  1 web-server ([express](http://expressjs.com/)-based, port 8081)  
  with websockets  
  (requires mongodb-process for gridFS)  
```js
	require('foonyah').start({
	  http:{ type:'express', port:8081, websocket:true },
	  dbfs:'127.0.0.1:27021'
	});
```

##Documents
####[http://liberty-technology.biz/foonyahstation/docs/](http://liberty-technology.biz/foonyahstation/docs/)

##Note
DO NOT DELETE "tmp" DIRECTORY WHICH IS USED BY foonyah FOR SAVE
TEMPORARY FILE.
