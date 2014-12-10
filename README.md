inotify-watch
=============

little script for executing a command whenever inotify event `CLOSE_WRITE` fires (i.e. when you save file in editor).

- based on inotify-tools (and transitively on inotify, of course).
- not to be confused with inotifywatch (part of inotify-tools) which logs inotify events (but does not behave like the `watch` utility at all)
- inotify-watch behaves like `watch`: executes a command repeatedly, only instead of a fixed-time interval, the inotify event `CLOSE_WRITE` triggers the execution.
- also shows the time when the command is executed, so the user can check when the commands are actually executed.
