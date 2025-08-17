## rofi-screenshot

![Preview](https://i.imgur.com/s1wqQcM.gif)

I got sick of not having a simple solution to take screenshots and screencasts.

Plus, there's so many different things I might want to do I struggle to find key bindings for all of them. So, I created a script to show and execute various screen capture related commands in Rofi.

### Features
* Capture a region to the clipboard or a directory
* Capture a window to the clipboard or a directory
* Capture the whole screen to the clipboard or a directory
* Record a region and save as a gif or MP4
* Record a window and save as a gif or MP4
* Record the whole screen and save as a gif or MP4

### Notable differences from original version
* Plugin is compatible with [rofi script](https://davatorium.github.io/rofi/current/rofi-script.5/) API
* Works with combi mode
* Notification daemon is replaced with [dunst](https://dunst-project.org/) (I might consider making it optional and modifiable in the future)
* More user-friendly names for the options + Adwaita icons
* Added metadata for options to make it easier to find them
* Slightly better error handling

### Installation
Make sure you have the required [dependencies](#dependencies) installed.

Download the rofi-screenshot source code, save as rofi-screenshot and make it executable
```bash
$ curl -L https://git.io/rofi-screenshot > rofi-screenshot && chmod u+x rofi-screenshot
```
Then move rofi-screenshot to somewhere in your $PATH for example:
```bash
$ sudo mv rofi-screenshot /usr/local/bin/
```

### Usage
Show the rofi menu
```bash
$ rofi-screenshot
```

Stop recording
```bash
$ rofi-screenshot -s
```
**Tip**: Add a keybinding for both of the above commands

### Configuration
| environment variable           | default value                   |                                                                                                                     |
| ------------------------------ | ------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `$ROFI_SCREENSHOT_DIR`         | `$XDG_PICTURES_DIR/Screenshots` | By default files will be stored in `$XDG_PICTURES_DIR/Screenshots`, which typically means `~/Pictures/Screenshots`. |
| `$ROFI_SCREENSHOT_DATE_FORMAT` | `+%d-%m-%Y %H:%M:%S`            | Possible alternative: `+%Y-%m-%d-%H-%M-%S`                                                                          |

### Dependencies

* [rofi](https://github.com/davatorium/rofi)
* [ffcast](https://github.com/lolilolicon/FFcast)
* [slop](https://github.com/naelstrof/slop)
* [xclip](https://github.com/astrand/xclip)
