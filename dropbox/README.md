```
$ docker run -d --name dropbox -it -v /home/tom/Dropbox:/root/Dropbox tombee/dropbox
$ docker logs -f dropbox
This computer isn't linked to any Dropbox account...
Please visit https://www.dropbox.com/cli_link_nonce?nonce=************************* to link this device.
```

