# Make moving creations using audio reactive brushes

Some brushes are labelled audio reactive. Their colour, shape or motion responds to audio captured by Open Brush.

![](<../.gitbook/assets/image-060.png>)

## Desktop workflow

1. Begin playing audio from your computer desktop.
2. On the Brushes panel, select the wavy audio-reactive button.
3. You will see a message that Open Brush is listening for audio.
4. Once audio is detected, draw with an audio-reactive brush.

Desktop builds listen to the computer's current audio output. If no source is detected, start playback before enabling audio-reactive mode and check that the intended Windows output device is active.

## Quest and other standalone headsets

Standalone builds react to audio playing inside Open Brush rather than audio from another app:

1. Copy an MP4 or another supported video containing an audio track to `Documents/Open Brush/Media Library/Videos` on the headset.
2. Add the video from **Extras > Local Media Library > Local Videos**.
3. Make sure the video's volume is above zero and start playback.
4. Enable the audio-reactive button on the Brushes panel and draw with an audio-reactive brush.

Different brushes react in different ways, including pulsing, changing brightness and moving their geometry. The audio affects the live rendering; it does not alter the underlying stroke control points.
