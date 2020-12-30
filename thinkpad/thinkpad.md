# Thinkpad X200
## Change trackpoint speed
### Locate setting files

```sh
find /sys/devices/platform/i8042 -name name | xargs grep -Fl TrackPoint | sed 's/\/input\/input[0-9]*\/name$//'
```

`0` <- slower ------------ faster -> `250`

**ATTENTION** if write `0`, trackpoint does not move  

```console
$ echo 250 | sudo tee /sys/devices/platform/i8042/serio1/serio2/speed
$ echo 180 | sudo tee /sys/devices/platform/i8042/serio1/serio2/sensitivity
```
