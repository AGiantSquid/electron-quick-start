# Web Audio Bug - Windows OS

This branch demonstrates a bug that affects Windows 10. It might affect other OS/versions.

## How to Reproduce

Start with a computer with Windows installed. The bug will be easiest to see with at least 2 devices attached. In your Windows settings, check which audio device is set to 'default' for output. Your default for input does not matter.

Start up electron like normal. When you talk into your mic, you should see the number 0 on the screen become some higher number coresponding to how loud you are talking. You should also hear yourself. Now, remove the device that is set to 'default' for output on your os. You will see that the number reflecting your volume freezes and the audio stops. It becomes impossible to recover the audio connection for the duration of the session.

This is not normal. If you open index.html in Chrome, you will see that it will fall back to another device and your stream will continue, uninterupted.
