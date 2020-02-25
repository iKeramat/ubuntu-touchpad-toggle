# Touchpad toggle for Ubuntu based distros

You can set touchpad toggle in Ubuntu and based distro like Linux Mint with two methods

## 1. Touchpad-indicator

## Installation


      $ sudo add-apt-repository ppa:atareao/atareao
      $ sudo apt-get update
      $ sudo apt-get install touchpad-indicator

Now run Touchpad-indicator after you ran you must see new icon in your panel, right click in icon and click Preferences and set your changes.
if you want set Hotkey shortcut you must go to Keyboard> Keyboard shortcut> Custom shortcut and change it

## 2. Custom Script


      $ cd ~
      $ wget https://raw.githubusercontent.com/iKeramat/Ubuntu-Touchpad-Shortcut/master/touchpad.sh -O .touchpad.sh

## Important
run ``` xinput list``` in terminal for see list of you inputs and find your Touchpad id by test this command ``` xinput set-prop <id> "Device Enabled" 0 ``` (turn id on if it wasn't your touchpad by ``` xinput set-prop <id> "Device Enabled" 1```).\
for example mine is 11, if your touchpad id was different run ``` nano ~/.touchpad.sh ``` and change ``` device= ``` with your touchpad id number.

now go to Keyboard> Keyboard shortcut> Custom shortcut
Create new shortcut and set something for Name and set ```sh ~/.touchpad.sh``` and set any key you want for shortcut.
