Prezto — Instantly Awesome Zsh
==============================

[Prezto][2] is the configuration framework for [Zsh][1]; it enriches the command line
interface environment with sane defaults, aliases, functions, auto completion,
and prompt themes.

This repository comes with three enhanced themes: *Budspencer*, *Terencehill* and
*Dangerous*.

Advanced features
-----------------

  * Clear indication of active mode (INSERT=yellow, NORMAL=blue, REPLACE=red)
  * Additional indicators for:
      - active background jobs
      - RANGER_LEVEL environment variable
      - runtime of last command
      - superuser
  * Advanced path display:
      - none (don't show)
      - truncated (show truncated path)
      - complete (show complete path)
  * Toggle path display by:

        Ctrl+Space in INSERT/REPLACE mode
        Space in NORMAL mode

  * Configure path display, example toggles between *none* and *complete*:

        export PWDFORMAT="none complete"

Budspencer theme
----------------

![budspencer theme][3]

Terencehill theme
-----------------

![terencehill theme][4]

Dangerous theme
---------------

![dangerous theme][5]

Installation
------------

Prezto will work with any recent release of Zsh, but the minimum recommended
version is 4.3.11.

  1. Launch Zsh:

        zsh

  2. Clone the repository:

        git clone --recursive https://github.com/sorin-ionescu/prezto.git "${ZDOTDIR:-$HOME}/.zprezto"

  3. Create a new Zsh configuration by copying the Zsh configuration files
     provided:

        setopt EXTENDED_GLOB
        for rcfile in "${ZDOTDIR:-$HOME}"/.zprezto/runcoms/^README.md(.N); do
          ln -s "$rcfile" "${ZDOTDIR:-$HOME}/.${rcfile:t}"
        done

  4. Set Zsh as your default shell:

        chsh -s /bin/zsh

  5. Open a new Zsh terminal window or tab.

License
-------

(The MIT License)

Copyright (c) 2009-2011 Robby Russell and contributors.
Copyright (c) 2011-2014 Sorin Ionescu and contributors.

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[1]: http://www.zsh.org
[2]: https://github.com/sorin-ionescu/prezto 
[3]: https://raw.githubusercontent.com/tannhuber/oh-my-zsh-budspencer/master/screenshots/budspencer.png
[4]: https://raw.githubusercontent.com/tannhuber/oh-my-zsh-budspencer/master/screenshots/terencehill.png
[5]: https://raw.githubusercontent.com/tannhuber/oh-my-zsh-budspencer/master/screenshots/dangerous.png
