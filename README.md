# Intro To Live Coding With TidalCycles

## Spin It All Up
To begin playing around with TidalCycles, you first need to start the Supercollider server, the SuperDirt synthesizer, and the TidalCycles server. The process for starting these will depend on which environment you are using (e.g. are you using the Sclang IDE (ScIDE), Atom, Emacs?). At this point, we are assuming you have setup whatever environment you will be using.
1. start sclang server
2. execute `SuperDirt.start` command on sclang server to start the SuperDirt synth
3. start tidalcycles server

## Common Problems
### `SuperDirt` synth Undefined
Sometimes when you try starting the SuperDirt synth, Supercollider may not be able to find it. This is most likely because the directory where the synth has been downloaded is not in Supercollider's search path. First, find where the synth has been downloaded (if you are using `quarks`, which is the Supercollider package manager, it may be somewhere like `/local/share/SuperCollider/downloaded-quarks` or something). Then, execute
``` shell
sclang> Quarks.addFolder("path/to/my/downloaded-quarks/or/synth")
```
in order to add that path to the search.
