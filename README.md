# alsaplayer

To use it:

1. Download it
1. Make it executable
1. Put it somewhere in your path
1. Run it

## Command line arguments

You can pass it a directory, in which case it will play all audio files in that
directory. If passed a single file, it will attempt to play that one file. If no
arguments are passed, any audio files in the current directory will be played.

Once within the application, there is a prompt which can be used to do normal
music things like play, pause, and skip. Enter 'help' or '?' at that prompt to
see all options.

Notably missing at the prompt is a 'previous' option. This is due to the current
architecture, where audio files are supplied to the player thread in a queue.
Once the file names are read from the queue, they are not stored anywhere, so
naturally you can't go backwards. This is something I plan to address.

## Requirements

This application has no Python dependencies other than than you are using Python
3, though you must also have alsa and ffmpeg installed.
