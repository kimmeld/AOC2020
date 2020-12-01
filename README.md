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

If you run an Advent of Code program with a commandline parameter, `S.GET.INPUT` will treat that as an identifier for test data and look for that in `AOC.INPUT.FILES`.  If the test data doesn't exist, it will execute the editor (`AE`) to create it.
