## Song Operation

The **Music Sequencer** will help you make dynamic music with just a few _SoundWave_ files. This standalone plugin can be used for any _Unreal Engine 5.5 or 5.6_ game or application.

While a traditional song is normally played from start to finish, the **Music Sequencer** is a dynamic multitrack "stem" arranger.

A **Sequence** provides seamless _SoundWave_ playback by stitching together its **Stems**.

A **Track** provides musically timed playback by aligning the start of its **Sequences** to its **Track Phrase**.

When a **Sequence** is **Triggered** and its **Track** is not yet playing, it will start at the next **Track** **Phrase**.

### BeginSong, FinishSong

Use **BeginSong** to start the **Music Sequencer** **Song**.

The **Song** will play indefinitely until a call to **FinishSong**.

*   A **Song** can be set to fade in and/or out by configuring its **BeginMode** and **FinishMode**.
*   A **Scene** can be specified to start the **Song** with one or more specific **Sequences**.

### TriggerScene, UntriggerScene

Use **TriggerScene** or **UntriggerScene** to modify the **Song** as it plays.

*   A **Scene** is used to change which **Sequence** each **Track** is playing.
*   A **Scene** is **Triggered** to start **Sequences**, or **UnTriggered** to stop them.
*   A **Sequence** will **Fade In** or **Fade Out** according to its **Track** settings.
*   **Triggering** a different **Sequence** in a **Track** will switch to the new one.
*   **Triggering** a **Sequence** that is already playing is ignored.
*   A **Track** plays one **Sequence** at a time, and a **Sequence** plays one **Stem** at a time.
*   A **Track** can be set to fade in and/or out by configuring its **TriggerMode** and **UntriggerMode**.

### Play In Editor (PIE)

The **Song** _Graph Editor_ will show playback information while your game or application is running in the _Unreal Editor_. Some additional buttons will appear that allow you to control the **Song** manually for testing.

Command buttons available in the _Graph_ during _PIE_ include:

*   **Begin Song**, **Finish Song**, and **Kill Song**
*   **Trigger** a **Scene**, and **Untrigger** a **Scene**
*   **Song Mute** and **Solo**
*   **Track Mute** and **Solo**

Edits can be made during _PIE_, but keep in mind that some behavior might be unpredictable until the **Song** or an edited **Track** is started again.
