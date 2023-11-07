# rclone4k streaming

# For windows taskschd.msc
``` bash
mount gdrive: G: --network-mode --dir-cache-time 5000h --poll-interval 10s --cache-dir=C:\Users\shukry\Documents\gdrivecache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode full --vfs-cache-max-size 250G --vfs-cache-max-age 24h --vfs-cache-poll-interval 5m --bwlimit-file 32M --no-console
```
# For terminal
``` bash
rclone mount gdrive: G: --network-mode --dir-cache-time 5000h --poll-interval 10s --cache-dir=C:\Users\shukry\Documents\gdrivecache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode full --vfs-cache-max-size 250G --vfs-cache-max-age 24h --vfs-cache-poll-interval 5m --bwlimit-file 32M
```

# For linux
``` bash
rclone mount gdrive: /mnt/gdrive --daemon --allow-other --dir-cache-time 5000h --poll-interval 10s --cache-dir=/mnt/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode full --vfs-cache-max-size 250G --vfs-cache-max-age 24h --vfs-cache-poll-interval 5m --bwlimit-file 32M
```

# For Gphotos
``` bash
rclone mount gphotos: /mnt/gphotos --daemon --allow-other --dir-cache-time 5000h --poll-interval 10s --cache-dir=/mnt/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode full --vfs-cache-max-size 250G --vfs-cache-max-age 24h --vfs-cache-poll-interval 5m --bwlimit-file 32M
```

# Testing Jelly
``` bash
rclone mount gdrive: /mnt/gdrive --daemon --allow-other --dir-cache-time 1h --poll-interval 10s --cache-dir=/mnt/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode writes --vfs-cache-max-size 20G --vfs-cache-max-age 1h --vfs-cache-poll-interval 5m --bwlimit-file 32M
```

# Testing index
``` bash
sudo rclone mount gdrive: /mnt/gdrive --daemon --allow-other --dir-cache-time 2m0s --poll-interval 10s --cache-dir=/mnt/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode writes --vfs-cache-max-size 5G --vfs-cache-max-age 2m0s --vfs-cache-poll-interval 5m --bwlimit-file 32M --read-only
```
