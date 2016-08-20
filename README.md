##Update 8-19-2016
Seems like there was a change, as even when the video isn't playing forward it is seeking forward after seeking backward. Currently unresolved.

#ytReverse
##A Youtube Reverse Video Player in JavaScript
This code seeks backwards through a Youtube video in a paused state at ~4 frames per second providing the illusion of playing a video in reverse.

If you set the fps any higher, seeking will be interrupted periodically to check in with the server. The video looks like it's buffering durring those moments, but it's not actually playing so that is not the case.

I made an attempt to "pre-buffer" a specified amount of video at custom intervals to avoid the check-in's. It's not great but it seems to help.

###Requirements / Notes
- Requires the Google Cast / Chromecast extension from the Chrome Web Store:
  https://chrome.google.com/webstore/detail/google-cast/boadgeojelhgndaghljhdicfkmllpafd?hl=en
  (without it you will see JS console errors resulting in erratic video playback)
- There is an unresolved error in the console: "Failed to execute 'postMessage' on 'DOMWindow'"...
- You may have to disable ad blockers on the page (I had to disable uBlock Origin for the page)
- The settings are explained in the code. The example video used is here:
  https://www.youtube.com/watch?v=RENJ6WaRA3o
- **If you have trouble when testing/implementing, try to clear your cache, especially after disabling ad blocking and installing Google Cast.**
