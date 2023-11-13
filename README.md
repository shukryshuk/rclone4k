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
rclone mount gdrive: /mnt/gdrive --daemon --allow-other --dir-cache-time 1h --poll-interval 10s --cache-dir=/mnt/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode writes --vfs-cache-max-size 20G --vfs-cache-max-age 1h --vfs-cache-poll-interval 5m --bwlimit-file 32M --read-only
```

# Testing index
``` bash
sudo rclone mount gdrive: /mnt/gdrive --daemon --allow-other --dir-cache-time 2m --poll-interval 10s --cache-dir=/mnt/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode writes --vfs-cache-max-size 5G --vfs-cache-max-age 2m --vfs-cache-poll-interval 5m --bwlimit-file 32M --read-only
```

# Testing debris
``` bash
sudo rclone mount debrid: /mnt/debrid --daemon --allow-other --dir-cache-time 2m --poll-interval 10s --cache-dir=/mnt/rcache --drive-pacer-min-sleep 10ms --drive-pacer-burst 200 --vfs-cache-mode writes --vfs-cache-max-size 5G --vfs-cache-max-age 2m --vfs-cache-poll-interval 5m --bwlimit-file 32M --read-only
```

# Testing debris rclone
``` bash
docker run --rm \
    --restart=unless-stopped \
    --network=container:gluetun \
    --volume ~/.config/rclone:/config/rclone \
    --volume ~/data:/data:shared \
    --user $(id -u):$(id -g) \
    --volume /etc/passwd:/etc/passwd:ro --volume /etc/group:/etc/group:ro \
    --device /dev/fuse --cap-add SYS_ADMIN --security-opt apparmor:unconfined \
    rclone/rclone \
    mount debrid: /data/mount --dir-cache-time 2m --poll-interval 10s --cache-dir=/data/rcache --vfs-cache-mode writes --vfs-cache-max-size 10G --vfs-cache-max-age 2m --vfs-cache-poll-interval 5m --bwlimit-file 32M --read-only
```
