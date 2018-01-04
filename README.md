# amtscanner

This is duktape implementation of AMTScanner.js of Meshcentral 2. This is supposed to run on MeshAgent not on NodeJS.

Example:
```
var AMTScanner = require("AMTScanner");
var scan = new AMTScanner();

scan.on("found", function(data) {
    if (typeof data === 'string') {
        console.log(data);
    } else {
        console.log(JSON.stringify(data,null," "));
    }
});
scan.scan("10.2.55.140",1000);
scan.scan("10.2.55.139-10.2.55.145",1000);
scan.scan("10.2.55.128/25",2000);
```