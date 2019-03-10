# exAudio

**exAudio** is a battle tested free abstraction layer for the audio_* functions of GameMaker Studio, plus it contains some additional functionality.

**Features**

* **Getters & Setters**: exAudio keeps track of audio data. Getters include position, velocity, falloff, volume, pitch and more. For sounds and the listener

* **Audio Classes**: You can create classes and add sounds to them in order to manipulate them all together at the same time

* **Fade Volume & Pitch**: exAudio contains functions for fading both volume & pitch. It is also done by using steps instead of milliseconds for better sync with alarms and timelines.

* **Suspend Audio**: You can Suspend all the sounds when e.g. the game loses focus. audio_pause_all() function is not really good use in our case, as the developer might have paused some sounds intentionally so audio_resume_all() will resume ALL the sounds, even the ones we don't want to. ex_audio_suspend_all() and ex_audio_restore_all() intelligently checks if the sounds are paused intentionally and leaves those alone.

* **Unique Sounds**: Classes can be used to store a series of sounds which can be played later on using the function ex_audio_class_play_unique(). That will choose a random sound from the class to play but the next time it will not play the same sound again. This functionality works best if you have lots of sounds in the particular group (e.g. around 10 or more) and reduces repetition of sound effects plus provides a better immersion especially for games that demand realism.

* **Easing**: Fading in/out the volume or pitch of the sound can have easing applied to it, so it fades much smoother or with e.g. an "elastic" effect.

* **Fully Documented**
