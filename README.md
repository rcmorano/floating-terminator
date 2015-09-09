# Install and "configure"

* Create a terminator layout named 'floating-terminator' # it's configurable by $TERMINATOR_LAYOUT_NAME in the script
* ln -s $PROJECT_DIR/floating-terminator /usr/local/bin
* Create a keyboard shortcut for each monitor [1,2,3] executing:
  * /usr/local/bin/floating-terminator 1
  * /usr/local/bin/floating-terminator 2
  * /usr/local/bin/floating-terminator 3
* Modify geometry for each monitor in 'floating-terminator' script (lines 49 and above)
