```
docker run -d -it \
	--name keepass \
	-v /home/tombee/Dropbox/keys/tomwbarlow.kdb:/root/tomwbarlow.kdb \
	-v /tmp/.X11-unix:/tmp/.X11-unix \
	-e DISPLAY=unix$DISPLAY \
	tombee/keepass
```
