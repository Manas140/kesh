# Kesh [ Archived ]
A X11 Hotkey Deamon In Sh (Archived)

Kesh(Key Sh) is a simple X11 hotkey deamon(kinda) written in Sh

Warning: currently kesh isnt meant for daily use

# Dependencies
```
  xinput
```

# Install
```
  git clone https://github.com/Manas140/kesh.git && cd kesh
  ./install.sh i
```

# Usage
```
  kesh [s|g|h]
    s: start kesh
    g: get value for currently pressed keys
    h: help page
```

# Setup (After Install)
```
  mkdir $HOME/.config/kesh 
  cp -r keshrc $HOME/.config/kesh/keshrc 
  kesh s
```

# Configuration
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

# Start Kesh 
```
  kesh s
```

# Knows Issues
```
  Cannot detect 'Keyboard Id' properly
  High on cpu usage (due to continues while loop)
  Can only register key_hold and not key_press making me add sleep to avoid multiple execution of command
  No Id registration for fn key
```
