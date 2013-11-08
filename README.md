#風若 foonyah
> /foo-nya/ ~ an service oriented architecture

##Prepare for use
To install the most recent release from npm, run:
```sh
    npm install foonyah (coming soon)
```
##Usage
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
