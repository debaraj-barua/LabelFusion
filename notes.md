
```sh
docker start 089d1932d225
docker attach 089d1932d225
docker exec -it 089d1932d225  bash -c "source /root/labelfusion/docker/docker_startup.sh && /bin/bash"
```

To use GUI: [[source]](http://wiki.ros.org/docker/Tutorials/GUI)

First, 
```sh
export containerId=089d1932d225
xhost +local:`docker inspect --format='{{ .Config.Hostname }}' $containerId`
```
Now we can start the container, and attach to our terminals:

```sh
docker start 089d1932d225
docker attach 089d1932d225
docker exec -it 089d1932d225  bash -c "source /root/labelfusion/docker/docker_startup.sh && /bin/bash"\
    --env="DISPLAY" \
    --env="QT_X11_NO_MITSHM=1" \
    --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" 
```
