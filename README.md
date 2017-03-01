# Popup Opera Capuleti Sprint 2016 Captions

(revived sprint 2017)


Based on [reveal.js](https://github.com/hakimel/reveal.js)



# Slides

Can be viewed at [index.html](index.html)



# Operator instructions

Operating the captions involves running two programs from the Terminal -- one
for the notes (presenter view), and one to display the captions on the projector
(in a different window and web browser)



1. Open the MacOS Terminal, `cd` into the slides directory, and run the `notes-server`:


    cd Dropbox/popup\ opera\ captions/capuleti/reveal-js-slides

    node plugin/notes-server/



2. Then open up the address it displays in *Firefox*. (Currently
   http://localhost:1947 -- that pops up the presenter mode in a new tab)


3. Open up a second tab in the Terminal  (Command-t), and run the `multiplex` server


    node plugin/multiplex/


That should print out "port 1948"

4. Open up a *Chrome* and go to the address http://localhost:1948 


That should display the captions, in sync with the ones that are in the Firefox
presenter view (go forward and backwards in presenter mode if it doesn't look
like they're in sync) 

5.  Move Chrome across to the projector, and make it fullscreen with the **F** key.



## During the show:


### to skip ahead:

* in Firefox: close the presenter/notes view tab
* still in Firefox, in the other tab, add the slide number after the "#" in the address bar
* refresh that tab (Command-r), and the notes view will open in a popup again

## if the browsers seem to be stuck out of sync

* close the presenter tab in Firefox
* refresh the other Firefox tab with Command-r
* exit fullscreen in Chrome with Esc
* refresh the Chrome window with Command-r
* press f in Chrome to go back to full screen
* back in Firefox, in the presenter tab, try going backwards and forwards, Chrome should sync up


## to quit

* to quit fullscreen in Firefox, press Esc
* press ctrl+c in both terminal windows



# Optionally: slides for audience / tablet

Any computer on the same wifi as yours can view the slides.  This 
Find out your computer's "IP address".  On mac or linux, run `ifconfig`, on windows, it's `ipconfig /A` (i think), and then look for an address that looks like something like this: **192.168.0.4**.  (they usually start with *192.168.*, sometimes with *10.0.*)

Then tell the audience to visit: http://192.168.0.4:1948, subtituting in your own IP address. You can test this yourself.


# Editing the slides

All contained in *index.html*.  Open it with a text editor (on a Mac, ctrl-click, select open with, Atom text editor)

```
<section>  -- slide
<h2>  -- main captions
<aside class="notes"> -- presenter notes, can be on empty slide before, or on slide itself
```


# Installing for the first time


* Download [node.js](https://nodejs.org) and install it. Then run

    npm install

in the main directory.


* Open up Dropbox icon --> settings icon -->  preferences --> Account  --> selective sync --> adjust
* go to popup captions --> capuleti --> reveal-js-slides and make sure "node_modules" is unticked


* Install firefox and chrome if necessary

* run through the operator instructions above and you may need to "allow popups from localhost" to get the notes/presenter view working in Firefox.

* open up chrome settings, and find the option about offering to translate pages in
  foreign languages, and switch it off.



# Rebuild theme

(developer instructions, no-one should need to do this)

Theme is stored in [popup.scss](css/themes/source/popup.scss). Run

```
grunt css-themes
```

to rebuild the actual css file. You will also need to install [grunt](http://gruntjs.com/getting-started#installing-the-cli) if you want to rebuild themes.

