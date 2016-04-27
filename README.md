# blink(1) scripts
Some scripts to use with the blink(1) from [ThingM](http://thingm.com/).

## Usage
Download desired script and make it executable.

## Scripts
### Tea timer
```bash
$ tea-timer [MINUTES]
```

Pulsates green after the given time in minutes. Minutes can be anything that works with `sleep`.

Tested on Ubuntu with earl grey und green tea.

### [IFTTT](https://ifttt.com) watcher
Calls ThingMs API every 10 minutes and checks if a new event is triggered.

> This script requires [jq](https://stedolan.github.io/jq/)!

Put the `ifttt-watcher.cfg` in your home directory and add your blink(1) key for
IFTTT. Next define some patterns - an example is in the provided config file.

You can use everthing that is a valid parameter for `blink1-tool`. Every pattern
will be called with the `-q` parameter.

Place the `ifttt-watcher` file there you want and execute it in the background:
```bash
$ ifttt-watcher &
```