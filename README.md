# screen-cast-tools
Tools used for Creating ScreenCast and GIF

## Tools
Here are the few useful tools for creating screencast.

### Linux Users

| Purpose | Tool | Licence Type |
|:------------- |:-------------| -----|
| Screen Recording	| Kazam Record a video or take a screenshot of your screen. Provides option to record a particular area of the screen. | Free |
| Desktop Recorder |	Saves the recorded video in OGV format.	| Free |


## Create Animated-Gif from Recorded Videos
Animated GIF's are better than Video files in terms of file Size.

```
sudo apt-get install imagemagick mplayer gtk-recordmydesktop
```

those are the required stuff, ImageMagick, MPlayer and Desktop Recorder.
Then use **Desktop Recorder** to capture a portion of the screen/application to use as the screencast.
After the Desktop Recorder has saved the recording into an **OGV video, MPlayer** will be used to capture JPEG screenshots, saving them into the 'output' directory.
```
mplayer -ao null <video file name> -vo jpeg:outdir=output
```

Use **ImageMagick** to convert the screenshots into an animated gifs.

```
convert output/* output.gif
```

you can optimize the screenshots this way:

```
convert output.gif -fuzz 10% -layers Optimize optimised.gif
```

### Mac Users

| Purpose | Tool | Licence Type |
|:------------- |:-------------| -----|
| Screen Cast	| Quick Time | Free |
| Movie to GIF |	GifRocket - Light, Fast App for Mac to create animated GIF from Video Files. Can be used for Screen Casting.	| Free |
