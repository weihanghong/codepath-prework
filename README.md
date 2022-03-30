# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Wei Hang Hong

Time spent: ~2 hours spent in total

Link to project: https://glitch.com/edit/#!/wakeful-sunrise-bosworth?path=script.js%3A125%3A3

## Required Functionality

The following **required** functionality is complete:

* [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [x] "Start" button toggles between "Start" and "Stop" when clicked. 
* [x] Game buttons each light up and play a sound when clicked. 
* [x] Computer plays back sequence of clues including sound and visual cue for each button
* [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [x] User wins the game after guessing a complete pattern
* [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
* [ ] More than 4 functional game buttons
* [ ] Playback speeds up on each turn
* [ ] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [x] List anything else that you can get done to improve the app!
- [x] Disabled the player from clicking the boxes while the pattern is still playing (the player can't cheat by clicking the box immediately after the box lights up)

## Video Walkthrough (GIF)

If you recorded multiple GIFs for all the implemented features, you can add them here:
![]http://g.recordit.co/88vL2ltPaY.gif
![]http://g.recordit.co/uw1ALdADzt.gif
![](gif3-link-here)
![](gif4-link-here)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
N/a

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 
A challenge that I encountered in creating this submission is adding an anti-cheat function to the game. In the base game, players can click on the boxes while the pattern is playing. This makes the game too easy and no fun. There is no memorization required by just clicking the same box when it lights up. To make up for this fault, I decided to implement a function that disables the player input while the pattern is still playing. At first, I was bewildered because I am not used to dealing with real-time functions. I had the idea of adding a new global variable to keep track of when the pattern is being played. My idea was to set that variable to false when the game starts and set it to true whenever the pattern is playing and then back to false when the pattern stops playing. First, I tried to set that variable to true at the beginning of playClueSequence() and then set it to false at the end of playClueSequence(). However, I quickly realized that it does not work. I did not understand why it does not work so I decided to log the function on the console to see when the variable changed. After studying the logs and the code, I realized that the code does not pause when it reaches the timers. The only plausible solution for me was to use the setTimeout function, even though I am not sure what it does. By studying the implementations of other setTimeout functions, I can guess that the first argument is what the function will do and the second argument is how long it should wait to do that function. Knowing that, I made a function to set the variable to false. The third argument is most likely the arguments that our first argument takes in. I did not need it so I left it blank. Figuring out the delay was easy because it was already done for me. After I finished, I tested my code and it does work as I intended.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 
After completing my submission, I wonder how do I host my game on my own website instead of Glitch.com. I have experience creating a website, but they are either inside other websites, apps, or localhost. It would be nice to have my own website that is open to the public. 

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
If I have more hours to work on this project, I would first focus on making my game foolproof, which is what I did for the additional features. Given more time, I would also like to disable the boxes lighting up when the player clicks on them while the pattern is being played. After I feel like the game is foolproof, then I would spend a little time on the aesthetics. Players will see the aesthetics of the game before the gameplay so I believe that it is worth putting in some effort on the aesthetics. If there is more time left, I would introduce more mechanics like adding a timer or speeding up the patterns. The first thing I would add is a randomize pattern so it does not get repetitive. The feature that I am most interested in adding is a trap box. The box would play a stange noise and the lights would flicker to show that it is a trap. If the player clicks on the trap box, they will lose the game. 


## Interview Recording URL Link

[My 5-minute Interview Recording](your-link-here)


## License

    Copyright Wei Hang Hong

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
