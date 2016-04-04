Audio Sequencer is a system we are developing to take advantage of Flash 10's new audio abilities.

Audio Sequencer includes a TrackManager and a Sequencer that work together to allow you to organize SequencerObjects into Tracks. This process is similar to working with audio software like Garage Band. You create tracks, place SequenceObjects in them at specific times, click play and hear the audio.

The system allows for real time track composition. You can add/remove individual SequenceObjects or entire Tracks while the system is playing. The system supports an unlimited number of tracks and Flash 10 is so efficient at ByteArray operations that you can easily run 12+ tracks on most modern computers.

# Main Feature Summary – version 1.0 #

  * Real time track composition – add remove Tracks and SequenceObjects while audio is playing.
  * Audio is synchronized at the byte level.
  * Lots of Tracks
  * Per Track Pan and Volume
  * Audio Effects
  * Works with MP3 and Ogg
  * Includes MP3 and Ogg loaders and a SoundHelper so you can use your own loader.

Make sure to read the README.txt for how to set up the classes and your FLA so it compiles correctly.

This application is licensed under GPLv3. Some classes are derivative works of other open source projects and are subject to the original licenses of those copyright holders.