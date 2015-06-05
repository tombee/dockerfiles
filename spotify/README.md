```
docker run -d \
	-v /etc/localtime:/etc/localtime:ro \
	-v /tmp/.X11-unix:/tmp/.X11-unix \
	-e DISPLAY=unix$DISPLAY \
	--device /dev/snd:/dev/snd \
	-v $HOME/.spotify/config:/root/.config/spotify \
	-v $HOME/.spotify/cache:/root/.cache/spotify \
	--name spotify \
	tombee/spotify
```

