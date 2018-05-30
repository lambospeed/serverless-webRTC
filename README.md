serverless-webrtc
=================

This is a tech demo of using WebRTC without a signaling server -- the 
WebRTC offer/answer exchange is performed manually by the users, for example
via IM.  This means that the app can run out of `file:///` directly, without
involving a web server.  You can send text messages and files between peers.

This repository contains two different clients that can talk to each other:

1. `serverless-webrtc.js` runs under node.js
2. `serverless-webrtc.html` runs in Chrome or Firefox

Chat is fully interoperable between all of the above (Node, Chrome, Firefox)
in any combination (tested with Chrome 35 and Firefox 29).


### For Node:

```
  npm install serverless-webrtc
  node_modules/serverless-webrtc/serverless-webrtc.js
```

Under Node, if you want to create a session instead of joining one:

```
  node_modules/serverless-webrtc/serverless-webrtc.js --create
```

### For browsers:

In Chrome (but not Firefox), you'll need to run a local web server rather
than just browsing to `file:///`, like this:

```
  cd serverless-webrtc
  python -m SimpleHTTPServer 8001 .
Serving HTTP on 0.0.0.0 port 8001 ...
```

and then browse to [http://localhost:8001/](http://localhost:8001/).
