# notes-ffmpeg-waveforms

## Installing ffmpeg on Linux Debian
```
apt-get install ffmpeg
```
After this operation, 300 MB of additional disk space will be used.
Do you want to continue? [Y/n]

## Create red waves from audio file
```
ffmpeg -i ./testdata/test.wav \
	-filter_complex "showwavespic=s=898x120:colors=red" \
	-frames:v 1 ./testdata/test_red.png
```
![Example red](https://raw.githubusercontent.com/vladimirok5959/notes-ffmpeg-waveforms/master/testdata/test_red.png)

## Create green waves from audio file
```
ffmpeg -i ./testdata/test.wav \
	-filter_complex "showwavespic=s=898x120:colors=green" \
	-frames:v 1 ./testdata/test_green.png
```
![Example green](https://raw.githubusercontent.com/vladimirok5959/notes-ffmpeg-waveforms/master/testdata/test_green.png)

This can be useful for some audio service (website or application) to get waveform image from audio file. For example for playback progress bar, [soundcloud.com](https://soundcloud.com) is the best example.

## Useful links
* [soundcloud.com](https://soundcloud.com)
* [Waveform – FFmpeg](https://trac.ffmpeg.org/wiki/Waveform)
