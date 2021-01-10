# Thinkpad X200
## Change trackpoint speed
### Locate setting files

```console
find /sys/devices/platform/i8042 -name name | xargs grep -Fl TrackPoint | sed 's/\/input\/input[0-9]*\/name$//'
```

### Change parameters

`0` <- slower ------------ faster -> `250`

**ATTENTION** if you write `0`, trackpoint won't move anymore.  

```console
echo 80 | sudo tee /sys/devices/platform/i8042/serio1/serio2/speed
echo 100 | sudo tee /sys/devices/platform/i8042/serio1/serio2/sensitivity
```
