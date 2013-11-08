#:: 風若 foonyah ::
> /foo-nya/

##Abstract
#### Node and jQuery based architecture's code-name, 
__by [Liberty Technology](http://liberty-technology.biz/)__

##Documents
#### [http://liberty-technology.biz/foonyahstation/docs/](http://liberty-technology.biz/foonyahstation/docs/)

##Prepare for use
To install the most recent release from npm, run:

    npm install foonyah (coming soon)

##Usage
__simple http server :__  
  1 web-server (http-based, port 80)
  
	require('foonyah').start();

__change port :__  
  1 web-server (http-based, port 8080)
  
	require('foonyah').start(8080);

__with ssl :__  
  1 web-server (https-based, port 8080)
  
	require('foonyah').start({
	  http:{port:8080, ssl: {key:'pem_key.pem', cert:'pem_cert.pem'}}
	});

__add websocket :__  
  1 web-server (http-based, port 8080)
  with websocket-handshaker
  [ystskm/websockets](https://github.com/ystskm/websockets)
  
	require('foonyah').start({
	  http:{port:8080, websocket:true}
	});

__foonyah-construction :__  
  1 web-server ([express](http://expressjs.com/)-based, port 8081)
  with websockets
  (requires mongodb-process for gridFS)
  
	require('foonyah').start({
	  http:{ type:'express', port:8081, websocket:true },
	  dbfs:'127.0.0.1:27021'
	});
  
##Note
DO NOT DELETE "tmp" DIRECTORY WHICH IS USED BY foonyah FOR SAVE
TEMPORARY FILE.

##Change Log
Check [document](http://liberty-technology.biz/foonyahstation/docs/) to see 
detail module release information.

- 2013/4/19  
0.0.4 release  
 # adjust to jquery 2.0.0

- 2013/4/2  
0.0.3 release  
 # main refactoring process finished

- 2013/3/18  
0.0.2 release  
 # also renewal portal page and documents

- 2012/12/25  
0.0.1 release  
 # publish portal page and documents

