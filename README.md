# PulseAudioJava
This small Java class allows to control functions of PulseAudio from Java

## Usage
Import the PulseAudio.java class into your project and start controlling PulseAudio directly from Java. The following table shows a minimal overview over possible functions. For detailed descriptions see source comments.

It is possible to create sinks, combine sinks, control the volume of separate sinks, as well as shift inputs between sinks. One can further play streams or files with different players. Currently supported are MPlayer and Xine, but extensions are easy. Web streams (HTTP, MMS, etc) are supported via wget and named pipes to the player.

Function Name  | Description
------------- | -------------
```createSink``` | Creates a new sink and returns its ID
```createStream``` | Loads a stream from a given URL via any of the defined players and returns the handle to the player process, as well as the index of the created PulseAudio sink input
```setDefaultSink``` | sets the default sink that is used for playback
```combineSinks``` | Combines a set of given sinks into a new combined sink
```getSinkIndex``` | Finds the sink for a given sink input ID
```moveSinkInput``` | Mmoves the given sink input to the given destination sink
```setVolume``` | Sets the volume of the given sink
```getIndex``` | Returns the sink index to a given deviceIdentifier (e.g. soundcard)
```startMusicStream``` | Starts a stream via wget on a sink
```checkIfSinkExists``` | Checks if a sink exists
```removeSink``` | Deletes a combined sink from the list of sinks
```removeSinkInput``` | removes an input from a sink

##ToDo
- Create example to show how this works