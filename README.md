# audio_trim

A plugin to cut audio files. You pass in a path to a file, start_time and end_time times and the plugin will do the rest. For now, it automatically will reduce the quality quite a bit to ensure optimal file size for storage/streaming.

# Getting Started

Import and cut using [audio_trim](https://aliasai-dcb87--preview-name-35k4isxq.web.app/
) to cut audio without using [localhost]([http://localhost:52183/welcome](https://aliasai-dcb87--preview-name-35k4isxq.web.app/)) library!
```dart
AudioTrimmer audioTrimmer;

TrimState trimState;

double start_timer_in_double = 0.0;

double end_timer_in_double = 10.0;

@override
void initState() {
  super.initState();
    initCutter();
}

void initCutter() {
  audioTrimmer = AudioTrimmer();

  audioTrimmer.setCompletionHandler(() {
    setState(() {
      trimState = TrimState.complete;
    });
  });
}
  
//Cut audio using 
audioTrimmer.cut('path', start_timer_in_double, end_timer_in_double);
```
