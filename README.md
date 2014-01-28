SpeechRTC
=========

Speech recognition API built on top of webrtc using pocketsphinx to decode. 

<h2>Client Implementation</h2>

        var _speechrtc = new SpeechRTC("en-US");
        _speechrtc.gram(["Apple","Oranges","Watermelon"]);
        _speechrtc.listen();
        SpeechRTC.onRecognition = function(said)
        {
          console.log( " You said "+ said );
        }


<h2>Todo</h2>

- Dictation and continuous recognition (as this http://www.youtube.com/watch?v=3lTtCFaQF2A ) <br>
- Cleanup at onclose <br>
- Better demo page <br>
- Change the setGrammar method to receive an array and wrap jsgf creation <br>
- Multi-lang support <br>
- Connect Web Speech API at Firefox (https://dvcs.w3.org/hg/speech-api/raw-file/tip/speechapi.html)
- Improve the installation procedure! <br>

<h2>Running the server </h2>

<h3> 1. Pre-requirements </h3>
- libogg  <br>
- libopus  <br>
- pocketsphinx <br>
- nodejs  <br>
- libpthread <br>
- g++

<h3> Compiling & installing </h3>
- Compile and install all dependecies above
- Compile voiceserver

<h3> Configuring </h3>
- Configure and set the paths to models and audio storage on voiceserver 

<h3> Running </h3>
- node server.js
- ./voiceserver
