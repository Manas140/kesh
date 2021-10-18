# Kesh (Key Sh)
A X11 Hotkey Deamon In Sh (WIP)

Kesh(Key Sh) is a WIP simple X11 hotkey deamon(kinda) written in Sh
Warning: currently kesh isnt meant for daily use

Dependencies:
```
  xinput
```

Install:
```
  git clone https://github.com/Manas140/kesh.git && cd kesh
  ./install.sh i
```

Usage:

```
  kesh [s|g|h]
    s: start kesh
    g: get value for currently pressed keys
    h: help page
```

Setup:

```
  # do install first, after that
  mkdir $HOME/.config/kesh 
  cp -r keshrc $HOME/.config/kesh/keshrc 
  kesh s
```

Configuration:
  Get Keystroke ids:

  ```
    #hold the keys until it outputs the ids
    kesh g
  ```

  Set a command to Keystroke ids:

  ```
    #in here 133 is the id for super key
    case $state in 
      "133") notify-send "pressed super key";;
    esac
  ```

Example:

```
  kesh s
```

Knows Issues:

```
  Cannot detect 'Keyboard Id' properly
  High on cpu usage (due to continues while loop)
  Can only register key_hold and not key_press making me add sleep to avoid multiple execution of command
  More i haven't encountered please make a issue if you found so
  No Id registration for fn key
```
