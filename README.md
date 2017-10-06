# DCSS_Sound4Webtiles
Hacky cobble-y-fication of the Korean webtiles sound script realized as a GreaseMonkey script.

Disclaimer: I am not a WebDev. if you are then you can probably do better than this.

This addon will eat up your RAM if you refresh the page too much, I am too inexperienced to fix this.
But it's fine if you do it in moderation, the culprit seems to be the audio module, its buffers, to be precise.
If your RAM gets consume too much then you'll either have to restart your browser, or close all DCSS tabs and do a memory minimize.

For Firefox this is done via "about:memory", which opens up a page that has buttons for garbage collection, cycle collection and memory minimization.

Anyway.
Opted to load all the sounds immediately (and to play them immediately) and aimed for making them persistent, because in the first version of this thing sounds wouldn't play immediately and the buffers had to take a while to be filled.

I went for the route of embedding the sound files as base64 strings, which bloats the script and makes it a pain to edit and possibly view, if your text editor sucks, but it loads quite snappily.
Plus, it doesn't require any cross domain hackery, which seem to be a security risk.

Kept the code at the top, the big bloaty stuff is at the bottom. Be sure to use a text editor, or text editor setting that can disable linewrapping.

## Installation

1. Make sure you have user scripts enabled in your browser (these instructions refer to the latest versions of the browser):

	* Firefox - install [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/).
	* Chrome - install [Tampermonkey](https://tampermonkey.net/?ext=dhdg&browser=chrome).
	* Opera - install [Tampermonkey](https://tampermonkey.net/?ext=dhdg&browser=opera) or [Violent Monkey](https://addons.opera.com/en/extensions/details/violent-monkey/).
	* Safari - install [Tampermonkey](https://tampermonkey.net/?ext=dhdg&browser=safari).
	* Dolphin - install [Tampermonkey](https://tampermonkey.net/?ext=dhdg&browser=dolphin).
	* UC Browser - install [Tampermonkey](https://tampermonkey.net/?ext=dhdg&browser=ucweb).
