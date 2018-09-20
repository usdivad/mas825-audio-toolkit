MAS.825 Audio Toolkit
====

Some tools and resources for you to get started experimenting with audio!

For the Fall 2018 edition of [MAS.825: Experiments in Art, Audio, & Augmentation](http://eaaa.media.mit.edu/).

## Software
- **Hyperproduction**
    - https://github.com/mitmedialab/hyperproduction/tree/mas825-fall2018

- **Reaper**
    - https://www.reaper.fm/

## Tutorials
- [Tutorial #1: MIDI Sampler Playback](https://youtu.be/xUIrXPZq36A)
- [Tutorial #2: Custom Mappings](https://youtu.be/s5hwyzc1cLc)
- [Tutorial #3: OSC and Effects](https://youtu.be/ihvEiKCY6PY)

All project files for tutorials are in the **tutorials** folder.

## Examples
- **hyperproduction_examples**:
    - MIDI:
        - midi_basic.hpm - sends keystrokes' [`keyCode` values](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/keyCode) as MIDI notes
        - midi_scale.hpm - sends keystrokes as MIDI notes along a C major scale, so you can play it like a piano! Mimics Logic's [musical typing](https://www.dummies.com/software/logic-pro-x/how-to-record-midi-in-logic-pro-x-with-musical-typing/) feature:
            - `asdfghjkl;'` = white keys
            - `wetyuop` = black keys
    - OSC:
        - osc_basic.hpm - sends keystrokes `0123456789` as OSC values, in gradations from 0-1, at OSC address `addr1`
        - osc_basic_custom_mapping.hpm - does the same thing as keyboard_input_to_osc_basic_1.hpm, but uses a custom KeyCodeToNumValue object for mapping.
        - (fader_osc_basic.hpm - sends the fader value on OSC address `addr1`)
    - More complex examples:
        - chords_mod_sine.hpm
            - Keystrokes send a major 7th chord with the root being the key pressed (mapped to C major scale as in midi_scale.hpm). Generated sines modulate the note indices (passed to MIDI output) as well as the square mix (passed via OSC on `addr1`)
        - chromatic_gliss_sine.hpm
            - Keystrokes send a chromatic gliss, direction and position dependent on generated sines. (Note offs may take a while with this one!)

- **reaper_project_example**:
    - reaper_project_example.RPP - an example Reaper project, with one synth and one audio track. The audio track's pitch-shifting and the synth's square mix are controlled via OSC by messages received at `addr1`
    - cicadas.mp3 - the audio clip referenced in the project