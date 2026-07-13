Rename it to index.html

How to upload images- 

Open your repo → Add file → Upload files
Drag your seven photos in — but first rename them on your computer to exactly these names, since the site looks for these specific paths:

school.jpg · college.jpg · isro.jpg · work.jpg · bebobear.jpg · ride.jpg · hobbies.jpg


Here's the one trick: GitHub won't let you create an empty folder, so to get them into images/, instead use Add file → Create new file, type images/placeholder.txt as the name (typing the / creates the folder), commit it — then go into the new images folder and use Upload files there. Or simpler: upload from your computer where the photos are already inside a folder called images — dragging the whole folder into the upload area preserves the structure.
Commit, wait a minute or two for Pages to rebuild, hard-refresh your site.

How to change the lables-

All the labels live as plain text in index.html — open it in any editor and search for what you see on screen. The one crucial rule: everything in the moving strips exists twice (there's a duplicate copy that makes the loop seamless), so every change must be made in both places or the label will flicker between old and new as the loop wraps. Easiest method: use find-and-replace-all rather than editing one occurrence.
Billboard captions — search for class="cap". You'll find lines like:
html<div class="cap">Bebo-bear fests</div>
Change the text between the tags — remember, each caption appears twice (14 lines total for 7 boards).
Road label chips — search for nchip. Each looks like:
html<button class="nchip green" data-panel="school">School</button>
Change only the text between > and </button> — don't touch data-panel="school", that's what connects the chip to its panel. Each chip appears twice; the gold ATS Resume chip appears eight times (4 per lap × 2 sets), so definitely use replace-all for that one.
Panel headings (the cards that open) — these exist only once each. Search for the heading text you want to change, e.g. The rear wheel — school days or Engineer · <em>Tata Elxsi</em>.
Bike-part tooltips — search for <title> to find the hover labels like rear wheel → school days, and aria-label= for the screen-reader versions; keep those in sync with any renames so the hotspots describe themselves correctly.
If you want to add or remove a chip rather than rename one, that's slightly more involved (the dash separators and panel wiring come into play) — tell me what you want the row to say and I'll restructure it for you instead.
