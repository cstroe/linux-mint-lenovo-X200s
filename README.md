# Linux Mint 18 on a Lenovo X200s

This is my cronicle of what I had to do to make X200s usable with a fresh install of Linux Mint 18.  The X200s is an early ThinkPad ultrabook.  It used to be top of the line in 2012, but now you can get very good refurbished deals.  It's a very capable laptop for general programming tasks, and I love the classic ThinkPad durability and look-and-feel.

# Hardware

## Sleep when closing the lid

With a fresh Linux Mint installation, the laptop won't sleep when you close the lid.  It turns out that this is a setting in Power Management. You must set "Perform lid-closed action even with external monitors attached" to ON.

![Lid closed action even with external monitors attached](https://raw.githubusercontent.com/cstroe/linux-mint-lenovo-X200s/master/power-management.png)

## Use Caps Lock as Ctrl

The newer ThinkPads have a BIOS option for swapping the Fn key with the Ctrl key.  This was create because the Fn key is at the edge of the keyboard instead of the Ctrl key, unlike regular keyboards.  Swapping the keys allows a much more natural usage of the keyboard.

Unfortunately, the Fn key cannot be swapped via software, it must be a BIOS setting, and the X200s does not have an official BIOS update with this feature.  There are unofficial BIOS-es for the X200s that will introduce the swapping capability, however it might be risky to flash a custom BIOS.

Another option is to use the Caps Lock key as an extra Ctrl key.  This works well for my purposes and avoids having to flash a custom BIOS.  From the Keyboard settings, go to Layout and selectoin Options.  There you can select the Caps Lock behavior as Ctrl.

![Caps as Ctrl](https://raw.githubusercontent.com/cstroe/linux-mint-lenovo-X200s/master/caps-lock-as-ctrl.png)

## WiFi not working after coming back from sleep

After you open the laptop when it's been sleeping, you will find that your WiFi won't activate.  I [read a little bit about this problem](http://askubuntu.com/questions/452826/wireless-networking-not-working-after-resume-in-ubuntu-14-04), and then it went away when I tried to reproduce it.

# Software

## Packages

    sudo apt-get install git
    git config --global user.email "you@example.com"
    git config --global user.name "Your Name"
    git config --global push.default simple

    sudo apt-get install vim

## Non open source
* [enpass](https://www.enpass.io/kb/how-to-install-on-linux/)
