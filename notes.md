
```sh
docker start 089d1932d225
docker attach 089d1932d225
docker exec -it 089d1932d225  bash -c "source /root/labelfusion/docker/docker_startup.sh && /bin/bash"
docker exec -it --privileged 089d1932d225  bash -c "source /root/labelfusion/docker/docker_startup.sh && /bin/bash"
```

