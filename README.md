ffmpeg
======

![ScreenShot](http://4.bp.blogspot.com/-mZf8E57XYKg/Tw_50ygbC4I/AAAAAAAAA2o/HlUyMjUUiw0/s1600/ffmpeg-logo.png)

ffmpeg is a  command line program for transcoding multimedia files. You could e.g. convert mp4 to mp3.


## Usage

Clone this repo:

```bash
$ git clone --depth 1 git://github.com/Ph3nx/ffmpeg.git
```

Create new app and add some config vars:

```bash
$ heroku create --buildpack https://github.com/Ph3nx/heroku-null-buildpack.git
$ heroku config:set LD_LIBRARY_PATH=./lib
```

Test to convert a .mp4 video to .mp3:

```bash
$ ./ffmpeg -i video.mp4 -vn -c:a libmp3lame -ar 44100 -ac 2 -ab 192k audio.mp3
```

Use included shorthand program, converts file named name.mp4 in name.mp3:

```bash
$ ./ff name
```
