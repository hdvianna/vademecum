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
    1. On the VirtualBox guest window click on _Devices_ menu and then on _Insert Guest Additions CD Image_
    2. Log into the guest
    3. Mount the _guest additions_ cdrom
        1. Create a cdrom folder o `/media`, e.g. `$sudo mkdir /media/cdrom`
        2. Mount the cdrom, e.g. `sudo mount /dev/cdrom /media/cdrom`
    4. Install the _guest additions_ cd rom

