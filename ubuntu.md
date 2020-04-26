# Ubuntu

## Proxy setup
1. Create a proxy.conf file
```
sudo touch /etc/apt/apt.conf.d/proxy.conf
```

2. Edit the file to add the proxy configuration
```
sudo nano /etc/apt/apt.conf.d/proxy.conf
```

3. Add the http and https proxy configuration in the file with the format `http://<user>:<password>@<host>:<port>/`

Example:
```
Acquire::http::Proxy "http://ron:obvious@example.com:42/";
Acquire::https::Proxy "http://ron:obvious@example.com:42/";
```
## Global Environment Variables

Edit the file `/etc/environment`

## User Environment Variables

Edit the file `~/.profile`

Then run `source ~/.profile` to load the new variables

## Checking version

On the terminal, run `lsb_release -d`

## Adding a share in a VirtualBox Guest

1. Install the _guest additions_ 
    1. In the VirtualBox guest window click on _Devices_ menu and then on _Insert Guest Additions CD Image_
    2. Log into the guest machine
    3. Mount the _guest additions_ cdrom
        1. Create a cdrom folder in `/media`, e.g. `$sudo mkdir /media/cdrom`
        2. Mount the cdrom, e.g. `$sudo mount /dev/cdrom /media/cdrom`
    4. Install the _guest additions_
        1. `$cd /media/cdrom`
        2. `$sudo ./VBoxLinuxAdditions.run`
2. Configure the user
    2. Go to the guest machine
    3. Add the current user to the group vboxsf, e.g. `$sudo usermod -aG vboxsf $USER`
3. Create the share folder on the VirtualBox guest
    1. In the VirtualBox guest window click on _Devices_ menu, then on _Share Folders_, then on _Share Folder Settings_
    2. Add a new share folder
        1. Select the folder path
        2. Set the share name
        3. Check the `Mount Automatically` box
        4. Set the mount point path in the guest machine
4. Configure for mounting the share folder automatically
    1. Go to the guest machine
    2. Open the fstab file, e.g. `$sudo nano /etc/fstab`
    3. Configure the share folder mount point, by appending the following line to the fstab file
        1. `shared_named_in_virtual_box /home/user/point_mount_name vboxsf defaults,dmode=755,fmode=644,gid=1000,uid=1000 0 0`
    4. Save the file
    5. Reboot the guest machine

