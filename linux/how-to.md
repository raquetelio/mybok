# How to

## Fix "Add to Favorites" for custom apps in Ubuntu
https://averagelinuxuser.com/ubuntu_custom_launcher_dock/ 


## Clean-up snaps to free space
https://www.debugpoint.com/clean-up-snap/

However, you can easily modify the count using the following command. The value can be between 2 to 20.

sudo snap set system refresh.retain=2

Clean Up Snap Versions
In a post in SuperUser, Popey, the ex-Engineering Manager at Canonical, provided a simple script that can clean up old versions of Snaps and keep the latest one.

Here’s the script we will use to clean the Snap up.

#!/bin/bash
 #Removes old revisions of snaps
 #CLOSE ALL SNAPS BEFORE RUNNING THIS
 set -eu
 LANG=en_US.UTF-8 snap list --all | awk '/disabled/{print $1, $3}' |
     while read snapname revision; do
         snap remove "$snapname" --revision="$revision"
     done
Save the above script as .sh in a directory (for example clean_snap.sh), give it executable permission and run.

chmod +x clean_snap.sh
When I ran the script, it reduced a lot of disk space. The script would also show the name of the package being removed.


# How to Sync Microsoft OneDrive with Ubuntu 18.04 and 20.04 (64 bit)
https://gist.github.com/starlinq/0f98c6d9339497bb8ac42d67f66f60eb