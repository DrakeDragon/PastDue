PAST DUE: a LitRPG choose-your-own-adventure
Complete story: Floors 1 to 99, three endings.

TO USE
- index.html is the whole game in one file. Upload it to GitHub Pages (or any web host) as index.html and share the link.
- It is set up for phones: it fills the screen and does not need zooming.
- It loads fonts from Google Fonts. Without internet it falls back to system fonts and still works.
- Progress saves in each player's browser.

TO EDIT (optional)
- source/ holds the story and code (source/src/*.js, head.html).
- With Node.js installed, run from inside source/:
    node build.js      (rebuilds standalone.html inside source/, which is the file to upload as index.html)
    node validate.js   (checks the story graph for broken links)
