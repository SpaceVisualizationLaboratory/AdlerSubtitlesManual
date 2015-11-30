BYOD Captioning
===============
**This is the manual version of the Bring Your Own Device captioning (where each user presses a button to start the captions). If you are intrested in the automatic version (where a show operator presses on button to start all the captions), the repo can be found at https://github.com/SpaceVisualizationLaboratory/AdlerSubtitles The official 'release' version of the software is contained here. Jeffrey SubbaRao's development branch can be found here: https://github.com/jsub1/AdlerSubtitlesManual**

**Visit http://AdlerCaps.org to see how the Adler Planetarium has implemented this software**

This project is designed to display subtitles at predeteremined intervals for BYOD (Bring Your Own Device) captioning. There is a JSON file that is an array of subtitles that have both a text and time properties. The script of the Adler Planetarium's Cosmic Wonder skyshow is provided as an example in CosmicWonder.json. Settings can be modified in the config.json file.

config.json options:
  * textColor: Sets the color of the body text.
  * textSize: Sets the size of the body text.
  * backgroundColor: Sets the background color.
  * font: Sets the font family for the web page.
  * initalMessage: HTML to display between the time the button is pressed and the time the first subtitle appears.
  * initalDelay: The time to wait before the first subtitle appears. This setting is only used if relative timing is used (see absoluteTiming).
  * absoluteTiming: Boolean that determines if absolute or relative timing is used. If true, the time property of each subtitle is the time between the button being pressed and the subtitle appering (absolute timing). If false, the time property of each line is the duration of the line on the screen (relative timing).
  * tagSubtitles: An array with two strings. Each subtitle is inserted between the first and second string before being displayed.
  * msPerTimeUnit: The number of milliseconds per time unit used. The default vale is 1000 because the default time unit is seconds.
  * transitionHTML: The HTML to display to indicate an upcoming change of text. Set to "" for a blank screen
  * transitionDuration: The number of time units to display the transition HTML
