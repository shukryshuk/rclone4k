# rclone4k streaming

# For windows taskschd.msc
``` bash
mount gdrive: G: --network-mode --dir-cache-time 5000h --poll-interval 10s --cache-dir=C:\Users\shukry\Documents\gdrivecache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode full --vfs-cache-max-size 250G --vfs-cache-max-age 24h --vfs-cache-poll-interval 5m --bwlimit-file 32M
```
# For terminal
``` bash
rclone mount gdrive: G: --network-mode --dir-cache-time 5000h --poll-interval 10s --cache-dir=C:\Users\shukry\Documents\gdrivecache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode full --vfs-cache-max-size 250G --vfs-cache-max-age 24h --vfs-cache-poll-interval 5m --bwlimit-file 32M
```

# For linux
``` bash
rclone mount gdrive: /root/gdrive --daemon --allow-other --dir-cache-time 5000h --poll-interval 10s --cache-dir=/root/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode full --vfs-cache-max-size 250G --vfs-cache-max-age 24h --vfs-cache-poll-interval 5m --bwlimit-file 32M
```
