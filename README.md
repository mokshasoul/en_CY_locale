# Description
This locale is for Cypriots who want to have an English Locale, (e.g. choosing en_CY in KDE). The locale alleviates problems faced when using such an exotic locale, e.g. rofi not starting up because it cannot recognize the locale.

Most settings used, are "copied" from the european irish locale

The instructions below are derived from following sources:
[Stackexchange](https://unix.stackexchange.com/questions/136920/set-custom-locales-in-gnome3-on-fedora-20)
[Askubuntu](https://askubuntu.com/questions/21316/how-can-i-customize-a-system-locale)

# Installation

1. Clone folder using git:
`git clone this`
    You can also fork the repository on [github](https://github.com/mokshasoul/en_CY_locale), or manualy fork it:
    ```
        
    ```

2. If you forked it, you can further customize the locale by copying additional locales into the git folder. The locales can be found under
`cd /usr/share/i18n/locales/`
3. Package locale for your system
```
sudo localedef -c -v -i en_CY -f UTF-8 hc_IL.UTF-8
sudo cp -v en_CY /usr/share/i18n/locales/
```
4. IMPORTANT: You need to edit the localedef file and include all the locales defined in the locale definition file, else the utilized copy
command won't function properly and you'll get a bunch of error messages. Using you favourite editor edit
` /etc/locale.gen `
    For the default installation you should uncomment en_GB, en_US, el_CY and el_GR
