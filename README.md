# Popup Opera Capuleti Sprint 2016 Captions

Based on [reveal.js](https://github.com/hakimel/reveal.js)



# Slides

Can be viewed at [index.html](index.html)


# Serving slides

Start the "notes server" for the presenter mode view in one Terminal

```
node plugin/notes-server
```

Then open up the address it displays, currently http://localhost:1947 (that pops up the presenter mode in a new tab)

Then, in another terminal:

```
node plugin/multiplex
```

This starts the server available to the audience.  It should run on port 1947.  You can preview it by going to http://localhost:1948


# Slides for audience

Find out your computer's "IP address".  On mac or linux, run `ifconfig`, on windows, it's `ipconfig /A` (i think), and then look for an address that looks like something like this: **192.168.0.4**.  (they usually start with *192.168.*, sometimes with *10.0.*)

Then tell the audience to visit: http://192.168.0.4:1948, subtituting in your own IP address. You can test this yourself.



# Rebuild theme

Theme is stored in [popup.scss](css/themes/source/popup.scss). Run

```
grunt css-themes
```

to rebuild the actual css file.


# Installing for the first time

Download [node.js](https://nodejs.org) and install it. Then run

```
npm install
```

in the main directory.

You will also need to install [grunt](http://gruntjs.com/getting-started#installing-the-cli) if you want to rebuild themes.

