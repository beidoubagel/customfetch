# customfetch
a guide on how to change your neofetch distro and ascii

this guide was made for the portal subreddit, so youll need to replace a couple of things if you dont want a portal themed neofetch. original post [here](https://www.reddit.com/r/Portal/comments/1m3h467/how_to_make_your_neofetch_look_like_youre_running/)
note: this looks really long, but it doesnt take very much time. i just used a lot of words

OPTIONAL: start by getting a theme off of [neofetch themes](https://github.com/Chick2D/neofetch-themes): youll want to go to ~/.config/neofetch/ and then make a copy of config.conf and paste it wherever you have easy access to, since you may need it if something breaks (probably wont but itll save time if it does). then pick a theme from the github i linked. click the name and then hit the "Download raw file" button that looks like... a download button. then move it to ~/.config/neofetch and rename it "config.conf". run neofetch to make sure it works.

V main guide V

for changing the name of your distro: go to /usr/bin/ and find the neofetch file. do the same copying process you did for the config.conf file, since it actually more important to recover if something breaks. its a script file, so double clicking it will execute it (which wont do anything since it just displays information) instead of opening it in a text editor. right click it and open it with your text editor. search "get_distro", or go to line 953. youll want to find your distro in the list.

for non ubuntu flavor distros, i have a disclaimer: i honestly dont know exactly how to do this part for all distros, so if this doesnt work just mess around with the naming and you might find the answer, but generally editing the part where it says your distro OUT of quotes, probably on the last line of your distros part of the text. change it to whatever you want.

for ubuntu flavor distros (kubuntu, ubuntu mate, xubuntu, lubuntu, ubuntu budgie, ubuntu studio, ubuntu cinnamon) i know exactly how to do it, since i use kubuntu. on your flavors section theres a sort of nickname in quotes and then a few spaces, then a part that says distro=${distro/Ubuntu/your flavor}, where your flavor it... wow youll never guess. edit that last part that says your flavor to whatever you want.

for us it will be GLaDOS. now the ascii art will default to the regular linux ascii, since "GLaDOS" isnt a distro recognized by neofetch. to change this, search for "get_distro_ascii", or go to line 5286.

for making it your actual distro, find it under the line you just went to, then change its name to GLaDOS.

for making it something from portal, follow the steps from the above paragraph, but copy your distros ascii and then put it in a text file, since itll be annoying to get back if you dont then delete the ascii from the script file. then go to [this](https://blog.kazitor.com/2014/12/portal-ascii/) link. choose whichever ascii you want, but for us itll be the first one, the aperture logo.* on the line that says "set_colors # # #", change all 3 of the numbers to match the color you want**. directly under the line that says "read -rd '' ascii_data <<'EOF'", type "${c1}", then paste the ascii you got from the website. itll be a bit offset because of the "${c1}", but dont worry about removing spaces to fix it.

run neofetch to make sure you got everything right.

and thats it! i hope this was helpful, ive been meaning to make a guide like this for a while. if you have any issues let me know. also i hope the flair i chose was ok, i thought it was pretty close.

*thank you valve, once again, for helping the linux community. this time they made the asciis the perfect size for neofetch.

**color code cheat sheet:

1: red

2: green

3: yellow

4: light blue

5: lavender

6: cyan

7: white

8: gray

(thanks to [u/TroyDestroys](https://www.reddit.com/user/TroyDestroys/) for the [comment](https://www.reddit.com/r/linux4noobs/comments/ofdyv7/comment/h4d80fj/?utm_source=share&utm_medium=web3x&utm_name=web3xcss&utm_term=1&utm_content=share_button) with the cheat sheet)
