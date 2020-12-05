# AOC2020
Advent of Code 2020

This is my Advent of Code 2020 repository.  These programs are written in UniVerse Basic.

# UniVerse Environment
In order to prepare your UniVerse environment to use these, a few things need to be done:

First, create a file to hold the input files for the problems:

```
CREATE.FILE AOC.INPUT.FILES 19
```

Now, create the config file - this holds the session key used to retrieve input data:

```
CREATE.FILE AOC.CONFIG 30
```

If you want `S.GET.INPUT` to download the input data for you, use the editor to create a `SESSION.COOKIE` record in `AOC.CONFIG` and put the session cookie value from your web browser into the first field.

At this point, you have enough of an environment to load the records in BP and run the code.

Depending on your preferences, you may wish to customize your environment in the `LOGIN` paragraph.  Mine looks like this:
```
PA
PTERM CASE NOINVERT
TERM vt220
TERM 132,49
```

# Code Notes
`S.GET.INPUT` is responsible for retrieving input from the Advent of Code site, caching it, and returning it to the calling program.  You need to create a record called `SESSION.COOKIE` in `AOC.CONFIG` which contains the session cookie from the Advent of Code web site.

If you run an Advent of Code program with a commandline parameter (e.g., `RUN BP AOC.2020.01 TEST1`), `S.GET.INPUT` will treat that as an identifier for test data and look for that in `AOC.INPUT.FILES`.  If the test data doesn't exist, it will execute the editor (`AE`) to create it.  `S.GET.INPUT` will store the test data in `AOC.INPUT.FILES` so that tests can be repeated without re-entering the test data.

Days where I've done something interesting are documented in the docs/ directory.

# Reference Material

* [Rocket UniVerse](https://www.rocketsoftware.com/products/rocket-universe-0/rocket-universe)
* [Rocket UniVerse Documentation](https://docs.rocketsoftware.com/nxt/gateway.dll?f=templates$fn=default.htm) - go to Rocket U2 > UniVerse > V12.1.1 to access the documentation library.
  * For someone who just wants to understand this code, but not necessarily install UniVerse and run it, the best places to start are the UniVerse BASIC Commands Reference and UniVerse BASIC User Guide manuals.

