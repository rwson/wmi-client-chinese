# wmi-client-chinese

Wrapper around the WMI client. Linux and Windows WMI clients are supported. fixed chinese garbled problem. 

### Install
```bash
npm install wmi-client-chinese --save
```

### Usage
```javascript
var WmiClient = require('wmi-client-chinese');

var wmi = new WmiClient({
    username: 'LOGIN',
    password: 'PASSWORD',
    host: 'IP-ADDRESS',
    ntlm2: true // only for linux
});

wmi.query('SELECT Caption,Version FROM Win32_OperatingSystem', function (err, result) {
    console.log(result);
    
    /*
      [{
        Caption: 'Microsoft Windows 7 旗舰版',
        Version: '6.1.7601'
      }]
    */
});
```

基于[wmi-client](https://github.com/R-Vision/wmi-client), 解决获取windows下获取信息中文乱码的问题

