inotify-watch
=============

little script for executing a command whenever inotify event `CLOSE_WRITE` fires for a _single_ file (i.e. when you save the file in editor).

- based on inotify-tools (and transitively on inotify, of course).
- not to be confused with inotifywatch (part of inotify-tools) which logs inotify events (but does not behave like the `watch` utility at all - rather unfortunate naming in my opinion ..).
- inotify-watch behaves like `watch`: executes a command repeatedly, only instead of a fixed-time interval, the inotify event `CLOSE_WRITE` triggers the execution.
- Executes the command once at start __(!)__
- also shows the time when the command is executed, so the user can check when the commands are actually executed.

## general usage

~~~~
inotify-watch FILE CMD..
~~~~

## example usage

- on changes to README.md, (re)create a pdf using pandoc

  `inotify-watch README.md pandoc README.md -oREADME.pdf`
