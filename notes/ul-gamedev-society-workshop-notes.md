# PICO-8 Workshop for UL Game Development Society, 1st Nov 2018
By Darren Kearney
https://darrenk.net


## Intro

Have a read of the PICO-8 Manual. It breifly explains PICO-8's capabilities, limitations and API.

Use the API Cheatsheet for a quick lookup guide.
Use the PICO-8 Wiki to get more information on api specifics.

Here's a playlist of concise introductory pico-8 videos for the workshop: https://www.youtube.com/playlist?list=PLrBolSjXBfHCv_VFogtNLIYZEIr0ELYdO


## Limitations

Limitations are important to keep in mind. If you notice something weird or unexpected happening, check whether it's because of a limitation (review the Quirks of PICO-8 in the manual).

A good example is the distance formula:  \sqrt (x2-x1)^2 + (y2-y1)^2

In PICO-8 you could easily overflow the int (PICO-8 numbers only go up to 32767.99). During the distance calculation, if you had a large map and where getting the x and y coordinates of things that were far apart, the part of the equation where you square it will cause an error. In a game I made, a load of birds died because of they were too far away from a cat. That doesn't make much sense! 

The way I solved it was to divid everything by 100 first, then multiply the result of formula by 100, so the numbers where more manageable when raising them by a power of 2. It was a good enough solution for my case (the birds lived!) but maybe not for your case.

How you work around the limitations is part of the fun of developing for PICO-8, or indeed any fantasy console or retro console. (Yes, hobbyists continue make games for ancient consoles!) 


## General development

Save any time using Ctrl+S.

Press Esc to toggle the Editor tools with the terminal/console/command-line.

Use the terminal prompt to test out bits of code when you are not sure.

If you want to check the value of things, you'll have to use the print() function and supply it with your value. The interpreter is less forgiving than the standard Lua interpreter.

The terminal prompt is quite restricted. It's only for navigating directories and managing carts. Linux users will likely feel at home with it.

When you go to make your own game, you will likely need to figure out:

* movement + controls - btn() btnp()
* collision detection
  + circle
  + box
  + map tile flags - fget(mget(x, y), flag_index)
* sprite animation
* audio rate limiting
* map
* camera

## Programming in PICO-8

Everything is lowercase.

You do not have full lua standard library, only a subset. Check the 'math' 

section of the api cheatsheet.

## Tips

* Reuse your own code.
* Learn from other people's code - inspecting carts from Splore (a cart navigator built in to pico-8), the Lexaloffle BBS and twitter
* Check out #pico8 and #tweetcart hashtags on Twitter for inspiration!

## Useful resources

* [Lexaloffle](https://www.lexaloffle.com/pico-8.php)
* [API Cheatsheet](https://neko250.github.io/pico8-api/) - I use this to do nearly everything.
* [PICO-8 Wikia](http://pico-8.wikia.com/wiki/Pico-8_Wikia)
* [Awesome List](https://github.com/felipebueno/awesome-PICO-8)
* [A PICO-8 Spaceshooter in 16 GIFs](https://ztiromoritz.github.io/pico-8-shooter)
