# qiniu jssdk demo
## usage
* clone the repo 

 ```
	$ git@github.com:qiniuts/dockerfiles.git
	$ cd qiniu-jssdk-demo
 ```
 
 * edit the config.js file

 ```
 module.exports = {
    'ACCESS_KEY': '<your_access_key>',  // https://portal.qiniu.com/user/key
    'SECRET_KEY': '<your_secret_key>',
    'Bucket_Name': '<your_bucket_name>',
    'Port': 80,
    'Uptoken_Url': 'uptoken',
	    'Domain': 'http://<your_bucket_domain>/' // bucket domain eg:http://qiniu-plupload.qiniudn.com/
	};
 ```

* build the jssdk demo image from docker file
```
$ docker build . -t jssdk
```

* run by the builded image
```
$ docker run  -dit --rm -p 80:80 jssdk
15fce65cf0346f78c3fcb24c1dd3db23fdbfd9909760ee55a7f81f500ab2d457     
```

* attach the container by the id
```
docker exec -i -t 15fce65cf0346f78c3fcb24c1dd3db23fdbfd9909760ee55a7f81f500ab2d457 /bin/bash
```
Then you can modify the code, and test the result by following addresses


* access the demo by address 
```
Upload: http://127.0.0.1
Multiple upload: http://127.0.0.1/multiple
Formdata upload: http://127.0.0.1/formdata
Up Performance: http://127.0.0.1/performance
```

