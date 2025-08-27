## Tips

A **Song** can have as many **Scenes** as you need. A **Track** can have as many **Sequences** as you need. A **Sequence** can have as many **Stems** as you need.

To crossfade **Sequences**, put them on separate **Tracks**.

Use _Comment Bubbles_ on **Song** and **Track** _Nodes_ to add special notes.

Other Editor Plugins to try...

*   AudioInsights (Epic): profile, debug, and monitor audio in the Unreal Engine.
*   Waveform Editor (Epic): editor tool for waveforms.

### Unreal Engine Max Sounds

You can have as many **Tracks** as you need, but each one will use its own _SoundSource_.

To conserve sound usage, a **Track** only has a _SoundSource_ when it is playing.

The limit of concurrent sounds in Unreal Engine can be viewed or modified in _Project Settings_.

*   Project Settings: Engine > Audio > Quality > Quality Levels > Max Sounds

Unreal Engine allows for multiple _Quality Level_ settings.

### Scene and Track Colors

Use the Advanced settings in the Song Details pane to manually or auto-color items.

*   Song Details > Auto Color Scenes
*   Song Details > Auto Color Tracks

### Stem Creation

For ways to think of a "stem", see [https://en.wikipedia.org/wiki/Stem\_(audio)](https://en.wikipedia.org/wiki/Stem_(audio)).

A _SoundWave_ is looped within a **Stem** similarly to the way a _Texture_ is tiled in a _Material_.

Plan your music keeping in mind that it is the "middle parts" that will likely play the most. The "beginning parts" and "end parts" are optional since you can simply fade into and out of your music.

_SoundWaves_ that have a tempo should be cut to fit a specific number of bars that match the **Song**.

_SoundWaves_ that are intended to be ambient, or without tempo, can be any length and triggered at any time.

To create looping _SoundWaves_ without clicks, taper the first and last few samples in the file to zero volume.
