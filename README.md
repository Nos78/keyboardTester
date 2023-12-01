# keyboardTester
![keyboardTester app icon](./favicon.svg?raw=true&sanitize=true#right)
<div align="left">
  <img src="./favicon.svg?raw=true&sanitize=true" width="48px">
A simple a simple [JavaScript](https://en.wikipedia.org/wiki/JavaScript) web app to test individual keys on the attached keyboard. Attaching to the [keydown](https://www.w3schools.com/jsref/event_onkeydown.asp) and	[keypress](https://www.w3schools.com/jsref/event_onkeypress.asp) [events](https://www.w3schools.com/tags/ref_eventattributes.asp), the program waits for a key to be pressed on an attached keyboard.  If the key is working, the keydown event listener will fire an alert box containing the keycode of the key pressed; meanwhile, the keypress event fires a second alert box indicating the character being input.
</div>

**Note**: *The keycode of the physical key and the keycode of the input character are not necessarily the same.  See the help text within keyboardTester.html for further details as to why this is the case.

## Contents of this release:
- keyboardTester.html
- favicon.svg
- README.md
- LICENSE.txt

## Copyright and legalize:
Copyright © 2023 [thebotfactory](https://thebotfactory.net), written by [noscere](mailto:noscere1978@gmail.com) and released under [GNU General Public License](https://www.gnu.org/licenses/).

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the [GNU General Public License](https://www.gnu.org/licenses/) for more details.
 
[JavaScript webapp that attaches to the keydown and keypress events to test individual keys on an attached keyboard.
