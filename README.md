# polybar-stopwatch

A custom stopwatch module for i3wm Polybar that allows you to easily start a simple stopwatch in your status bar. Developed and tested on i3 **4.22**

## Installation

1. Clone the repo and move into the directory;

```bash
$ git clone https://github.com/4g3nt47/polybar-stopwatch.git
$ cd polybar-stopwatch
```

2. Copy the module files into your polybar dir;

```bash
$ cp -R stopwatch ~/.config/polybar/
```

3. Enable the module by appending the following lines to your polybar config file (`~/.config/polybar/config.ini`);

```
[module/stopwatch]
type = custom/script
exec = ~/.config/polybar/stopwatch/get-elapsed-time.py /tmp/.polybar-stopwatch
interval = 1

label = %output%
label-foreground = #fff
format-underline = #800080
click-left = exec ~/.config/polybar/stopwatch/toggle-start.py /tmp/.polybar-stopwatch
click-right = exec rm -f /tmp/.polybar-stopwatch
```

Now depending on where you want the stopwatch to appear, you can add it to either `modules-left`, `modules-right`, or `modules-center`.

```
modules-left = stopwatch
```

4. Restart i3 and enjoy;

```
$mod + Shift + r
```

## Usage

To start/pause the stopwatch, simply click on it. To stop it, simply right click on it.

https://github.com/4g3nt47/polybar-stopwatch/assets/54174043/45d81119-23fa-4d83-9d64-c2d85238f9ee


