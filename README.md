overlap-add
===========
Perform additive synthesis from a stream of frames.  This is something like inverse of frame-hop.

## example

```javascript
//First create the push-frame function
var pushFrame = require('overlap-add')(256, 64, function(data) {
  console.log('got a frame:', data)
})

//Then stick frames into it
pushFrame([...])
```

## Install

    npm install overlap-add

#### `require("overlap-add")(frame_size, hop_size, ondata)`
Performs additive synthesis on a sequence of frames.

* `frame_size` is the size of each frame
* `hop_size` is the size of a hop between successive frames
* `ondata(frame)` is a callback that gets fired each time a frame is full

**Returns** A function that you can call to push a frame of data into the stream.

## Credits
(c) 2013-2015 Mikola Lysenko. MIT License
