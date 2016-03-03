Demo : http://apibox.me

Init Client :
```sh
var client = new MRG.Client();
```
Subscribe Room :
```sh
var subscription = client.subscribe('/room1', function(data) {
        console.log(data);
    });
```

Send Message :
```sh
var send = client.publish('/room1', { type : 'msg-new', text: msg,user: user});
            send.then(function() {
                console.log('Message received by server!');
            }, function(error) {
                console.log('There was a problem: ' + error.message);
            });
```
