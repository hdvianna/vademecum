# Ubuntu

## Proxy setup
1. Create a proxy.conf file
```
sudo /etc/apt/apt.conf.d/proxy.conf
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
