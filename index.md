
### How many LOC will you require to implement a CLI interface like that?

    Naval Fate.

    Usage:
      naval_fate ship new <name>...
      naval_fate ship <name> move <x> <y> [--speed=<kn>]
      naval_fate ship shoot <x> <y>
      naval_fate mine (set|remove) <x> <y> [--moored|--drifting]
      naval_fate -h | --help
      naval_fate --version

    Options:
      -h --help     Show this screen.
      --version     Show version.
      --speed=<kn>  Speed in knots [default: 10].
      --moored      Moored (anchored) mine.
      --drifting    Drifting mine.

<br><br>
## Rules

1. Any programming language.

2. Any command line arguments parsing library.

3. Your program should allow only the usage described above.

4. Your program should display the usage and exit if invoked incorrectly.

5. Your program should print a collection (object, hash, alist, etc.) of
   the above mentioned *commands*, *options*, *arguments* and their values.

3. Describe how to run your code.

3. Post solution to [Hacker News thread](http://news.ycombinator.com/item?id=4122547).

4. Have fun!


# docopt
## Implementation
### [In Python](http://github.com/docopt/docopt)

    #! /usr/bin/env python
    """Naval Fate.

    Usage:
      naval_fate ship new <name>...
      naval_fate ship <name> move <x> <y> [--speed=<kn>]
      naval_fate ship shoot <x> <y>
      naval_fate mine (set|remove) <x> <y> [--moored|--drifting]
      naval_fate -h | --help
      naval_fate --version

    Options:
      -h --help     Show this screen.
      --version     Show version.
      --speed=<kn>  Speed in knots [default: 10].
      --moored      Moored (anchored) mine.
      --drifting    Drifting mine.

    """
    from docopt import docopt

    print docopt(__doc__, version='Naval Fate 2.0')

### [In CoffeeScript](http://github.com/docopt/docopt.coffee)

    #! /usr/bin/env coffee
    doc = """Naval Fate.

    Usage:
      naval_fate ship new <name>...
      naval_fate ship <name> move <x> <y> [--speed=<kn>]
      naval_fate ship shoot <x> <y>
      naval_fate mine (set|remove) <x> <y> [--moored|--drifting]
      naval_fate -h | --help
      naval_fate --version

    Options:
      -h --help     Show this screen.
      --version     Show version.
      --speed=<kn>  Speed in knots [default: 10].
      --moored      Moored (anchored) mine.
      --drifting    Drifting mine.

    """
    {docopt} = require '../docopt'

    console.log docopt(doc, version: 'Naval Fate 2.0')


### [www.docopt.org](http://www.docopt.org)
<br>
