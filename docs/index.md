# Music Sequencer

[<img src="img/ClassThumbnail.svg" width="75" align="right">](img/ClassThumbnail.svg)

Dynamic Multitrack Loop Player Plugin for Unreal Engine

## What the Music Sequencer Does for You

The **Music Sequencer** is like a robot DJ. You create and configure a **Song**, arrange your loop files in **Sequences** of **Stems**, and at runtime the **Music Sequencer** will play them seamlessly, all aligned to the bar boundaries. A **Sequence** can play in order, randomized, or jump around. Each **Track** can be set to start or stop right away, or to fade in or out. **Tracks** can be played together and crossfaded.

When a **Song** is playing, you use **Scenes** to change which **Sequences** are playing. Controlling the **Music Sequencer** is simple. The basic commands available to both C++ and _Blueprints_ are:

*   **BeginSong** and **FinishSong** to start or end a **Song**
*   **TriggerScene** to start or stop **Sequences**

The **Music Sequencer** uses _Unreal Engine_'s _Quartz Clock_ and _MetaSounds_ for synchronized and seamless playback. Settings for each **Song** are stored in a custom _DataAsset_ called a **Music Sequencer Song**, which you configure with the custom _Graph Editor_.

### As a Live Multitrack Composer

If your music is in clips that can loop, such as strings, percussion, horn section, bass etc., then you can add them to **Sequences** on as many **Tracks** as you need. You decide how the **Sequences** will play, and trigger them in any combination with **Scenes**.

### Or As a Simple Music Crossfader

You might have fully completed songs and so all you need is a mixer. With the **Music Sequencer**, you can have as many separate **Songs** as you need. Variations of the same music can be put into **Tracks** in the same **Song**. Crossfaded **Tracks** of a **Song** are in perfect sync.

### GameplayTags

With _GameplayTags_ you have an alternative to using references to **Songs** or the names of **Scenes**.

### Music Sequencer Subsystem

With the **Music Sequencer Subsystem**, you can control all your **Songs** from anywhere at any time.

### Events

With _Event Binding_, your game or application can react to beats and changes in the **Song**.

## Issues, Reporting, and Feature Requests

[https://github.com/gogodyne/MusicSequencerPlugin/issues](https://github.com/gogodyne/MusicSequencerPlugin/issues)
