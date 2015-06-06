```
docker run -d -it \
	--name keepass \
	-v /home/tom/Dropbox/keys/tombarlow.kdb:/root/tombarlow.kdb \
	-v /tmp/.X11-unix:/tmp/.X11-unix \
	-e DISPLAY=unix$DISPLAY \
	tombee/keepass
```
