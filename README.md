# singscript
Use musical motherboard beeps to keep abreast of how your scripts are getting on.

I can't resist a `-v` switch and spend too much time waiting for scripts to do their thing. These help me to get on with something more productive safe in the knowledge I'll get an audible jingle when they need my attention.

Contributing is as simple as finding a url to a midi file which is a likely
candidate for an informative tune, creating an entry in `midi-sources.csv`, and writing a corresponding bash script.

Repo relies on [`mid2beep`](https://github.com/Cqoicebordel/mid2beep) and all its dependencies. On Ubuntu and derivatives the following should get you what you need:

```bash
apt install beep bc abcmidi
wget https://github.com/Cqoicebordel/mid2beep/raw/master/mid2beep
chmod +x mid2beep
chmod +x getmidi
./getmidi
```

Example usage in bash:
```fish
my_brave_script.py && goodbeep || badbeep
```

Example usage in [fish](https://fishshell.com/):
```fish
my_brave_script.py; and goodbeep; or badbeep
```






