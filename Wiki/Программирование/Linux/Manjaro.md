Для фикса экранов на логине:
```
sudo cp -f ~/.config/monitors.xml ~gdm/.config/monitors.xml
sudo chown $(id -u gdm):$(id -g gdm) ~gdm/.config/monitors.xml
```

Для фикса источников звука и скринкастов на wayland:
```
sudo pamac install manjaro-pipewire
```