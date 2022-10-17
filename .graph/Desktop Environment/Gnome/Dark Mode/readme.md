https://peterlevi.com/variety/comment-page-13/#comment-93834

>You need to adjust a bit set_wallpaper script used by variety. Use this command to allow to change wallpapers in dark mode meanwhile an update comes:
>
>```sed -i ‘/^# Gnome 3, Unity*/a gsettings set org.gnome.desktop.background picture-uri-dark “file://$WP” 2> /dev/null’ /home/$USER/.config/variety/scripts/set_wallpaper```

___
- https://peterlevi.com/variety/comment-page-13/#comment-93924

>May 12, 2022 at 20:15
>Hi,
>I tried your command but it didn’t work.
>Although, by editing manually the file it did after exiting and re-logging.
>
>Edit “set_wallpaper” in “/home/$USER/.config/variety/scripts/set_wallpaper” (copy it before in case you mess it up).
>And add “-dark” so it’ll look like this:

># Gnome 3, Unity
>gsettings set org.gnome.desktop.background picture-uri-dark “file://$WP” 2> /dev/null
>if [ “$(gsettings get org.gnome.desktop.background picture-options)” == “‘none'” ]; then
>gsettings set org.gnome.desktop.background picture-options ‘zoom’
>fi
>
>Thanks for pointing me in the right direction!
