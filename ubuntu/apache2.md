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

```
sudo apt install apache2
systemctl start apache2
systemctl enable apache2
```

## Reinstall Apache2

```
sudo apt-get -o DPkg::Options::="--force-confmiss" --reinstall install apache2
sudo apt-get purge apache2
sudo apt-get install apache2
```

## References

- https://qastack.id/ubuntu/26228/how-can-i-reinstall-apache-httpd-after-deleting-some-of-the-configuration-files
- https://www.liquidweb.com/kb/install-apache-2-ubuntu-18-04/
- https://unix.stackexchange.com/questions/367338/re-install-apache2-after-purge-apt-get-says-its-already-the-newest-version
