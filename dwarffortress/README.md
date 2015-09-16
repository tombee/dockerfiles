# Dwarf Fortress in a Container

```
$ xhost +
$ export DISPLAY=:0.0
$ docker run --name df --rm -it \
    -e DISPLAY \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -v /dev/snd:/dev/snd \
    -v $HOME/df/data/save:/df_linux/data/save \
    tombee/dwarffortress
```
