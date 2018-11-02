# PICO-8 Workshop for UL Game Development Society, 1st Nov 2018
By Darren Kearney
darren@darrenk.net, https://darrenk.net, https://twitter.com/darrencearnaigh, https://mindcauldron.com

# Intro

Have a read of the PICO-8 Manual. It breifly explains PICO-8's capabilities, limitations and API.
Use the API Cheatsheet for a quick lookup guide.
Use the PICO-8 Wiki to get more information on api specifics.

Here's a playlist of concise introductory pico-8 videos for the workshop: https://www.youtube.com/playlist?list=PLrBolSjXBfHCv_VFogtNLIYZEIr0ELYdO

# General development

Save any time using Ctrl+S.

Press Esc to toggle the Editor / Console.

Use the Console to test out bits of code when you are not sure. It's a mix of a less forgiving lua interpreter and sandboxed command line prompt. Linux users will feel at home here.

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

# Programming in PICO-8

Everything is lowercase.
You do not have full lua standard library, only a subset. Check the 'math' section of the api cheatsheet.

# Tips

* Reuse your own code.
* Learn from other people's code - inspecting carts from Splore (a cart navigator built in to pico-8), the Lexaloffle BBS and twitter
* Check out #pico8 and #tweetcart hashtags on Twitter for inspiration!

# Useful resources

* [Lexaloffle](https://www.lexaloffle.com/pico-8.php)
* [API Cheatsheet](https://neko250.github.io/pico8-api/) - I use this to do nearly everything.
* [PICO-8 Wikia](http://pico-8.wikia.com/wiki/Pico-8_Wikia)
* [Awesome List](https://github.com/felipebueno/awesome-PICO-8)
* [A PICO-8 Spaceshooter in 16 GIFs](https://ztiromoritz.github.io/pico-8-shooter)