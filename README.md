MAS.825 Audio Toolkit
====

Some tools and resources for you to get started experimenting with audio!

For the Fall 2018 edition of MAS.825: Experiments in Art, Audio, & Augmentation.

## Software
- **Hyperproduction**
    - https://github.com/mitmedialab/hyperproduction/tree/mas825-fall2018

- **Reaper**
    - https://www.reaper.fm/

## Examples
- **hyperproduction_examples**:
    - MIDI:
        - keyboard_input_to_midi_basic.hpm - sends keystrokes' [`keyCode` values](https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/keyCode) as MIDI notes
        - keyboard_input_to_midi_scale.hpm - sends keystrokes as MIDI notes along a C major scale, so you can play it like a piano! Mimics Logic's [musical typing](https://www.dummies.com/software/logic-pro-x/how-to-record-midi-in-logic-pro-x-with-musical-typing/) feature:
            - `asdfghjkl;'` = white keys
            - `wetyuop` = black keys
    - OSC:
        - keyboard_input_to_osc_basic_1.hpm - sends keystrokes `0123456789` as OSC values, in gradations from 0-1, at OSC address `addr1`
        - keyboard_input_to_osc_basic_2.hpm - does the same thing as keyboard_input_to_osc_basic_1.hpm, but uses a custom KeyCodeToNumValue object for mapping.
        - (fader_to_osc_basic.hpm - sends the fader value on OSC address `addr1`)

- **reaper_project_example**:
    - reaper_project_example.RPP - an example Reaper project, with one synth and one audio track. The audio track's pitch-shifting and the synth's square mix are controlled via OSC by messages received at `addr1`
    - cicadas.mp3 - the audio clip referenced in the project