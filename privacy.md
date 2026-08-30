# Privacy note - Fluxgates

## The short version

Fluxgates is made by one person. It has no accounts, no login, and no ads. It
can send **anonymous run data** so I can see which nodes, relics and rooms
players actually pick - and fix the ones nobody wants. **It is off unless you
turn it on**, and you are asked once, in plain language, before anything is
sent.

## What is sent, if you opt in

One short report at the end of each run:

- **How the run ended** - won, lost, or quit - and how far it got.
- **What you were offered and what you took** - the node, relic and shop items
  put in front of you, and which of them you picked.
- **Which route you chose** - at each step of the map, the kinds of room you
  could have gone to and the one you did. Recorded as kinds and depths ("an
  elite room at depth 3"), not as anything about you.
- **What you have unlocked** - which research you have bought and in what order,
  how much of the game's own currency that cost, and which packs and nodes the
  game has unlocked for you. It shows whether the upgrade tree is paced right.
- **Difficulty** - the heat level and any pact modifiers active.
- **The shape of your factory** - how many nodes and connections, how they were
  wired together, and how much of each resource was produced, per room.
- **Which of the game's own settings you use** - your language, the visual
  theme, the colour palette, the HUD scale, whether reduced motion is on, and
  your default game speed. Two reasons: game speed changes how the numbers in
  every other part of the report should be read, and the rest tells me which
  accessibility options are worth continuing to build. Nothing about your
  machine, your operating system, or any setting outside Fluxgates.
- **Which build you were playing** - the game's version number, an identifier
  for the code revision it was built from, whether it was the demo or the full
  game, and a hash of the balance settings. None of this describes you or your
  machine; it exists so a report can be attributed to the build it came from.
- **One random ID for this install**, generated on your machine, so several runs
  can be recognised as coming from the same player without identifying who that
  player is.

And, **if the game crashes**, one short report describing the crash:

- **The error message and where in the game's own code it happened** - the name
  of the code file, and the line in it. Nothing outside the game is named: the
  folder the game is installed in, which on Windows contains your account name,
  is removed before the report is built, not after it is sent.
- **The run you were in** - the same random starting number the game used to
  build that run, which lets me recreate it exactly and see the crash myself.
- The same build information as above.

## What is never sent

- Your name, your Steam account, your email address, or any account identifier.
- Your IP address beyond what any web request necessarily exposes to the server
  handling it; it is not stored with the report.
- Where the game is installed, your user folder, your machine name, or anything
  else about your computer. A crash report names files belonging to Fluxgates
  and nothing else.
- **Anything you type.** The game never puts free text in a report - there is no
  field in the payload that can carry it.

## Turning it on and off

- **First run:** you are asked once. Neither answer is preselected. If you close
  the game without answering, nothing is sent.
- **Any time after:** Settings → Data → "Send anonymous run data when a run
  ends". Unticking it stops the network request itself, not just what is done
  with the reply.
- **Export instead:** Settings → Data → "Export my data to a file" writes the
  same data to your save folder, so you can look at exactly what a report
  contains, or send it manually rather than automatically.

## Storage and deletion

Reports are stored as plain JSON files in object storage, used only to balance
the game, and are not sold, shared, or used for advertising.

To have this install's data deleted, email
[fluxgates.games@gmail.com](mailto:fluxgates.games@gmail.com) with the install ID
shown in Settings → Data. That ID is the only way a report can be tied back to
you, so please include it - without it there is nothing to look up.

## Contact

[fluxgates.games@gmail.com](mailto:fluxgates.games@gmail.com)

