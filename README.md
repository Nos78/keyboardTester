# <span><img src="./favicon.svg?sanitize=true&raw=true" width="48px" valign="center" align="center"></span> keyboardTester 

A simple [JavaScript](https://en.wikipedia.org/wiki/JavaScript) web app to test individual keys on an attached keyboard.

---
<!--<div align="left">
  <img src="./favicon.svg?raw=true&sanitize=true&x=48" width="48px">-->

## Contents of this release:
- keyboardTester.html
- favicon.svg
- README.md
- LICENSE.txt

> :warning: This program is free software: you can redistribute it and/or modify it under the terms of the [GNU General Public License](https://www.gnu.org/licenses) as published by the [Free Software Foundation](https://fsf.org), either version 3 of the License, or (at your option) any later version. As specified in the [GPL v3 license text](https://www.gnu.org/licenses/gpl-3.0.html#license-text), if distributed, this release can only be distributed in its entirety, or not at all.

> :question: ***So you're not a fan of free software?*** That's okay! You're not required to accept the License in order to run the program.

> :bulb: **Nothing other than [the license](./LICENSE.txt), however, grants permission to copy, propagate or otherwise modify this work, as set forth in section 9.**

---

## Introduction

A simple [JavaScript](https://en.wikipedia.org/wiki/JavaScript) web app to test individual keys on an attached keyboard. This JavaScript-based web app attaches a [listener](https://blog.webdevsimplified.com/2022-01/event-listeners/) method to the [keydown](https://www.w3schools.com/jsref/event_onkeydown.asp) and	[keypress](https://www.w3schools.com/jsref/event_onkeypress.asp) [events](https://www.w3schools.com/tags/ref_eventattributes.asp), and waits for a key to be pressed. If the key is working, then the [onkeydown](https://www.w3schools.com/jsref/event_onkeydown.asp) [listener](https://blog.webdevsimplified.com/2022-01/event-listeners/) will fire off an alert box containing the keycode of the key pressed; meanwhile, the [onkeypress](https://www.w3schools.com/jsref/event_onkeypress.asp) [listener](https://blog.webdevsimplified.com/2022-01/event-listeners/) fires off a second alert box indicating the character being input.

> :memo: **Note**:  the physical key pressed and the actual character input may have different keycodes. This may seem strange at first, but the answer is simple. The keydown event cares for what key has been depressed. A standard latin-character 102-key QWERTY alpha-numeric keyboard uses capital-lettered glyphs for each key.
>
> Therefore, when an alphabetic key is pressed, the resulting keycode represents an [ASCII](https://en.wikipedia.org/wiki/ASCII) capital letter (eg. keycode >= 65 and <= 91) regardless of the state of `CAPS LOCK` or any `modifier` key also being held down.
>
> :bulb: the keypress event cares for the character, or glyph, the operator has entered. Therefore, the keycode can be any number within the range of the keyboard's capability, or rather, how it's driver inteprets the input. Since you can input Unicode characters with a combination of `ALT` + an alphanumerical (hex) code, the keycode is not strictly limited to ASCII (eg. not limited to keycode >= 0 and <= 255).


### 🎼 DOM, DOM, DOM, DOM... DOM! 🎵
> :memo: **Note**: The keycode of the physical key and the keycode of the input character are not necessarily the same, as we describe above.
>
> **The help text within [keyboardTester.html](https://htmlpreview.github.io/?https://github.com/Nos78/keyboardTester/blob/main/KeyboardTester.html) expands upon this, and provides further details as to why this is the case.**

If you're simply looking to capture user input, your [listener](https://blog.webdevsimplified.com/2022-01/event-listeners/) will be attaching to the keypress event. It is possible to do this via a keydown event—or, for that matter, a [keyup](https://www.w3schools.com/jsref/event_onkeyup.asp), but this would be a little more messy, and not just because different [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)—that's Document Object Model—implementations require accessing different objects and/or methods to capture events.

The keydown event contains the keycode of the key pressed, plus any `modifiers` (eg. `SHIFT`, `ALT`, `CTRL`, etc.), and it is the combination of keycode + `modifiers` that produces the actual input. The keypress event helpfully captures this logic for us, thus saving us the effort.

> :bulb: If you need to capture the `modifier` keys, a `keypress event` probably won't be the right choice. This is all confounded when we add the fact that some `modifier` keys do not have their own keycode, whilst others do! Left `SHIFT` for example, fires out a keycode of 16. Therefore, a `keydown` event and a `keypress` event are triggered as if a standard alphanumeric key has been pressed.

### Source Code
> :memo: The source code is displayed as a code block, direct from within the app, below the istructions and above the page footer.

Helpfully contained within the app, the source code can be viewed without needing to right-click and `view-source`, or loading up your favourite text editor and opening the HTML file for edit. Instead of wading through blocks of incidental HTML, jump straight into the JavaScript whilst running the app, since the source is helpfully displayed right there on the page.

## Development Roadmap
Plans for development of keyboardTester.html:
- Currently we're firing out two alert message boxes for a key being pressed, one in keydown and another via keypress. We could capture the data from both events, then fire a single alert box upon completion of both events.
- Reduce code duplication. If this is intended as a learning exercise for the user, then having blocks of duplicated code is just bad practise. We can re-factor the listeners to strip out common code, distilling it into a common method, called from within the listener.


---

## Copyright and legalize:
Copyright © 2023 [thebotfactory](https://thebotfactory.net), written by [noscere](mailto:noscere1978@gmail.com) and released under [GNU General Public License](https://www.gnu.org/licenses/).

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the [GNU General Public License](https://www.gnu.org/licenses/) for more details.
 
[JavaScript webapp that attaches to the keydown and keypress events to test individual keys on an attached keyboard.
