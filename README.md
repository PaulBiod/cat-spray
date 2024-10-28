# cats-pray
An air spray that detects motion and activate the spray when the cat is around

A long time ago, I used to use some ready made cat air sprays. Recently, I needed one of these, but I realize it was far too expensive (about 70 eur + 20 eur each refill !). Not only it was expensive (a refill lasts about 80 sprays), but also it didn't work perfectly.

So, I decided to go DIY way, by making my own cat sprayer, with all the components and tecnology I like :)
That's how CatSpray was born.

For this project, I use : 
A 3D print base (will add the thingiverse link when I'll have it uploaded)
A cheap air sprayer (5 eur) (standard model, so any spray would do the trick)
A servo motor MG945(5 eur)
A 250x240 tft screen (4 eur)
A capacitive touch button TTP223 (2 eur)
A PIR sensor (AM312) ( 2 eur)
A mmwave sensor LD2410 (4 eur)
A mini  4 pins cathode RGB led (less than 0.5 eur)
A piezzo buzzer (passiv)

Ok, you can say it may be too much for just a spray cat, but it'd be too easy just to make a spray, a pir and a servo.

So, how it works ?
The capacitive button allows to switch on/off the sprayer. The led color can tell us if the spray is on or off (gree is off, red is on). The pir is used to detect motion, but to avoid false positives, I decided to add a mmwave sensor, so that the spray will only activate when both detect motion/presence.
The buzzer is important because the cat will associate the sound to the sprayer, so, if for some reason you forget to change the empty spray, the sound will suffice to frighten the cat.
The screen is there to sjhow us the activation state, the wifi signal, the motion detection, and the number of sprays of the day.

IMPORTANT : 
the sprayer is a standalone object, it doesn't need Home assistant to work, even if the wifi is unavailable, it will make its job. 
It's only linked with Home assistant to retrieve the daily sprays number.

Use : 
Just plug the spray in (it's not battery powered), the screen will automatically ligh up in OFF mode (so, no sprays). Just touch the capacitive button, the spray will make some beeps to allow you to move (you have 10 seconds) so that it will not spray you.
After these 10 seconds, the screen will show a red spray, and the led will go red.
Now, if the cat sprayer detects motion, it will make a long beep and the activate the servo to spray.

Of course, you can play with it with home assistant automations, for example, you can programatically activate/deactivate it with triggers (i.e. activate it when you are in bed, deactivate it when you wake up, and much more things...). You can have alexa make some TTS when it detects sprays, etc...

As I don't have many time, I won't show wiring diagrams, but if you look at the code, you can easily see how everything is wired, and just ask me if you have any questions.

3D : To make the 3D process, I used an old project of the "freres poulain" who made an aroma spray, but I had to make a lot of changes and adaptation to use it for my project.
