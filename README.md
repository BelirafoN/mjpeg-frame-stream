# MJPEG Frame Stream

This is a transform stream for MJPEG streams or any jpeg-streams. 

## Install

```bash
$ npm i mjpeg-frame-stream
```

## Usage 

```javascript
const MjpegFrameStream = require('mjpeg-frame-stream');
const fs = require('fs');

let mgpegStream = fs.createReadStream('./mjpeg.dump'),
    frameStream = new MjpegFrameStream();

mgpegStream.pipe(frameStream)
    .on('frame', frame => console.log(frame));

```

## License 

Licensed under the MIT License 