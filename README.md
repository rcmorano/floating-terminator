# Install and "configure"

* Install depends:
```
sudo apt-get install -y wmctrl xdotool
```
* Create a terminator layout named 'floating-terminator' # it's configurable by $TERMINATOR_LAYOUT_NAME in the script
* Link script that will be launched by the keyboard shortcut:
```
ln -s $PROJECT_DIR/floating-terminator /usr/local/bin
```
* Create a keyboard shortcut for each monitor [1,2,3] executing:
  * /usr/local/bin/floating-terminator 1
  * /usr/local/bin/floating-terminator 2
  * /usr/local/bin/floating-terminator 3
* Modify geometry for each monitor in 'floating-terminator' script ([lines 49 and above](https://github.com/rcmorano/floating-terminator/blob/master/floating-terminator#L49)):
  * HINT: use 'xdotool getmouselocation' to get positions for your top-left squares:
```
~$ xdotool getmouselocation
x:0 y:0 screen:0 window:0
# put them in place in 'floating-terminator':
# L51: # set geometry for monitor 1
# L52: wmctrl -ir $WMCTRL_ID -e 0,0,0,1920,550;;
# L52 self-explanation: # wmctrl -ir $WMCTRL_ID -e $X_POSITION,$Y_POSITION,0,$WIDTH,$HEIGHT;;
```
