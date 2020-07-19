# Apache2

---

Cek Status

```
sudo systemctl status apache2
```

Restart

```
sudo systemctl restart apache2

127.0.0.1   localhost
127.0.1.1   guest-desktop
your_server_IP example.com
your_server_IP test.com
```

## Reinstall Apache2

```
sudo apt-get -o DPkg::Options::="--force-confmiss" --reinstall install apache2
sudo apt-get purge apache2
sudo apt-get install apache2
```

https://qastack.id/ubuntu/26228/how-can-i-reinstall-apache-httpd-after-deleting-some-of-the-configuration-files
