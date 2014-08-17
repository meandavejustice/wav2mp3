## WAV2MP3

Convert wav file blobs to mp3 file blobs

This is the conversion code decoupled from the recorderjs fork/example for mp3conversion [here](https://github.com/nusofthq/Recordmp3js)

Also includes [libmp3lame.js](https://github.com/akrennmair/libmp3lame-js)

## Usage

`window.wav2mp3` takes two params, a [fileblob](https://developer.mozilla.org/en-US/docs/Web/API/Blob) and a callback.

You will want to ensure that the fileblob you pass in is a WAV file.

``` javascript

    wav2mp3(wavblob, function(blob) {
        var xhr = new XMLHttpRequest(),
            fd = new FormData();

        fd.append( 'file', blob, '4minutesand33seconds.mp3');
        xhr.open('POST', '/upload');
        xhr.send( fd );
    });

```

## Why

I'm publishing this temporarily so that I can access it from npm, will eventually pull
this out even further and provide as a module which will push the worker into
[webworkify](https://github.com/substack/webworkify).
