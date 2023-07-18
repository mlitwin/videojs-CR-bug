# videojs-CR-bug

Reproducible case for video.js bug [CR delimited VTT files not supported #8367](https://github.com/videojs/video.js/issues/8367)

See the corresponding bug [CR delimited VTT files not supported #64](https://github.com/videojs/vtt.js/issues/64) in the underlying library for diagnosis and details.

## Steps to reproduce

- Play the video at https://mlitwin.github.io/videojs-CR-bug/
- Note no caption ("Caption") visible in in the default CR.vtt track
- Switch to the CRLF.vtt track, differing from CR.vtt only in line endings, and note that the caption appears.


##

Making the CR.vtt is a bit of a pain, since text editors want to "fix" it by normalizing line endings.

`tr -d '\n' <  CRLF.vtt > CR.vtt` from a CRLF file.