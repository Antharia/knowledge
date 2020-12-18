# Change trackpoint parameters
1. Find device path
    find /sys/devices/platform/i8042 -name name | xargs grep -Fl TrackPoint | sed 's/\/input\/input[0-9]*\/name$//'
    
Maybe you'll get :  

    /sys/devices/platform/i8042/serio1  
    
2. Change parameter

    echo 50 | sudo tee /sys/devices/platform/i8042/serio1/speed  
