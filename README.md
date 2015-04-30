
# socket.io-titanium

web sockets for titanium tested on ios and tornado.

copy "ti-websocket-client.js" to your app Resources directory.



———————————————————————
var WebSocket = require('ti-websocket-client').WebSocket;

ws = new WebSocket("ws://localhost:3000/");

ws.onopen = function () {
    alert("Connected");
    ws.send("Hello");
};

ws.onclose = function () {
    alert("Disconnected");
};

ws.onmessage = function (message) {
    alert("> "+message.data);
};

ws.onerror = function (e) {
    alert('Error: ' + (e ? JSON.stringify(e) : 'A unknown error occurred'));
};