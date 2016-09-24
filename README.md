This script is intended for use only on ProjectEuler.net and it was build to be used together with [Firefox's GreaseMonkey extension](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/).

It places 5 flags (British, Romanian, Russian, Korean and German) on top of every problem's page. By clicking on the flag, the corresponding translation of a problem is retrieved.

Obviously, not at all problems are available in the above mentioned languages. In this case, clicking on the flag will do nothing.

Notes about implementation:

- The technique used for implementing this is **JSONP** (JSON with padding), since AJAX wouldn't work (see Same Origin Policy).
- The processing function (only 2 - 3 lines of code) is found in the **processtranslation.js** file. That function will be executed when the response comes back.
- The 5 flag images are stored inside the script in Base64 format, to avoid additional HTTP requests.

**LIMITATIONS**:

- does not work on HTTPS version of ProjectEuler (Firefox 23+), unless you disable Mixed Active Content blocker
- for some unknown reason, it needs at least Firefox 9+ to work.

The translations are parsed from the corresponding translations websites:

- http://projecteuler.radumurzea.net/ for Romanian
- http://euler.jakumo.org/ for Russian,
- http://euler.synap.co.kr/ for Korean and
- http://projekteuler.de for German

You can see a demo on how the script works in the video on this page: http://projecteuler.radumurzea.net/greasemonkey.php

The script is also hosted here, for easier installation:

- https://greasyfork.org/en/scripts/4899-project-euler-problem-translator
- https://openuserjs.org/scripts/SoboLAN/Project_Euler_Problem_Translator