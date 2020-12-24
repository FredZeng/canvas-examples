# Playing video using canvas

## Example

```js
var canvas = document.getElementById('canvas');
var context = canvas.getContext('2d');
var video = document.createElement('video');
video.src = 'http://vjs.zencdn.net/v/oceans.mp4';

var playInterval = setInterval(function() {
  if (video.paused) {
    clearInterval(playInterval);
    return;
  }
  context.drawImage(video, 0, 0);
}, 16);
```

[View full source](./index.html)