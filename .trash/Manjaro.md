Для фикса экранов на логине:
```
sudo cp -f ~/.config/monitors.xml ~gdm/.config/monitors.xml
sudo chown $(id -u gdm):$(id -g gdm) ~gdm/.config/monitors.xml
```

Для фикса источников звука и скринкастов на wayland:
```
sudo pamac install manjaro-pipewire
```

## Установка корневых сертификатов:

```bash
sudo cp russian_trusted_sub_ca_pem.crt /etc/ca-certificates/trust-source/anchors/
sudo cp russian_trusted_root_ca_pem.crt /etc/ca-certificates/trust-source/anchors/

sudo update-ca-trust
```
#### Проверка

```bash
trust list | grep -i %label%
```