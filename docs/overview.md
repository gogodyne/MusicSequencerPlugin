## Overview

### Features

*   Simple API: **BeginSong**, **FinishSong**, **TriggerScene**
*   _GameplayTag_ support for **Song** control
*   **MusicSequencerSubsystem** for global **Song** access
*   Custom _DataAsset_ and _Graph Editor_
*   Sample-accurate timing using _Quartz Clock_ and _MetaSound_
*   Delegates for beats and **Track** events

### Song Elements

*   A **Stem** plays your prepared _SoundWave_ file.
    *   The **Phrase** is the duration in bars that a **Stem** will play.
    *   The **Clip** is the _SoundWave_ file that a **Stem** plays. A **Clip** will repeat continuously during the **Phrase**. An empty **Clip** will play silently as a "rest".
    *   The **Weight** is used to adjust the likelihood of this **Stem** if it is being randomly chosen.
    *   The **Actions** are an optional list of ways to choose the next **Stem** to play.
        *   **Next** will play the next **Stem**, wrapping back to the first.
        *   **Previous** will play the previous **Stem**, wrapping back to the last.
        *   **Last** will play the last **Stem**.
        *   **First** will play the fist **Stem**.
        *   **Any** will play any random **Stem**.
        *   **Other** will play any other random **Stem**.
        *   **Repeat** will play the **Stem** again.
        *   **Stop** will stop the **Sequence** when the **Stem** finishes.
*   A **Sequence** is an ordered list of **Stems**.
    *   A **Sequence** can have any number of **Stems**.
    *   The **PlayOrder** determines the order that the **Stems** will play.
        *   **Sequential** will play the **Stems** in order, then wraps back to the first.
        *   **Sequential Once** will play through the **Stems** only once.
        *   **Randomize** will play the **Stems** randomly.
        *   **Action** will use each **Stem's Actions** to determine which **Stem** to play next.
            
*   A **Track** has a list of **Sequences**.
    *   A **Track** can have any number of **Sequences**.
    *   The **Phrase** is the alignment in bars where the **Track** will begin and end.
    *   The **StartMode** and **StopMode** determine how a **Track** begins and ends.
    *   A **Track** plays only one **Sequence** at a time.
    *   A **Track** is stopped when none of its **Sequences** is playing.
*   A **Scene** is used to **Start**, **Stop**, or change **Sequences**.
    
*   A **Song** is a group of **Scenes** and **Tracks** with a shared tempo and time signature.
    *   A **Song** contains **Tracks**, each of which has a volume and other settings.
    *   **Tracks** contain **Sequences**, and **Sequences** contain lists of **Stems**.
    *   The **BeginMode** and **FinishMode** determine how a **Song** starts and ends.
    *   **BeginSong** will **Trigger** a **Scene**.
        *   The first **Scene** is **Triggered** if no **Scene** is specified.
        *   If a **Song** has no **Scenes**, the first **Sequence** of all **Tracks** is triggered.
