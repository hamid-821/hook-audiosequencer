# Introduction #

We have created several examples that show how to set up the system. At a minimum you need an audio source (MP3/Ogg) either embedded or loaded in, then converted into a SoundSample. The loaders do this automatically or you can use SoundHelper and provide it a raw ByteArray.

This is a basic example. More detailed examples are included in the examples archive.

# Details #


Set up the TrackManager and Sequencer, add SequenceObjects to it and hit Play.

```
import com.jac.sequencer.SoundHelper;
import com.jac.sequencer.SoundSample;
import com.jac.sequencer.tracks.SequenceObject;
import com.jac.sequencer.tracks.Sequencer;
import com.jac.sequencer.tracks.SequenceTrack;
import com.jac.sequencer.tracks.TrackManager;

[Embed(source='/../assets/ogg/BassDrum.ogg',mimeType='application/octet-stream')]
private static var BassDrum:Class;

//TrackManager is used to compile the song.
var trackManager:TrackManager = new TrackManager(122, 8, 44100, 0);
			
//Sequencer uses the TrackManager to play the audio. This is the audio player.
var sequencer = new Sequencer(trackManager);
			
//SoundSample is created using our SoundHelper from an ogg file. SoundSample holds the uncompressed byte data for the audio.
var soundSample:SoundSample = SoundHelper.decodeOgg(new BassDrum());
//SequenceTrack holds an unlimited number of SequenceObject objects.
var sequenceTrack:SequenceTrack = new SequenceTrack(122);
//SequenceObject contains positioning information for when the sound is played. by default, it plays it immediately.
var sequenceObject:SequenceObject = new SequenceObject(soundSample);
			
			
//add the sound to the track.
sequenceTrack.addObject(sequenceObject);
//add the track to the track manager.
trackManager.addTrack(sequenceTrack);

//play the mixed audio.
sequencer.play();

```