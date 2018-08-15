# Plex for RaspberryPi

```
docker run -d --name plex --net=host \
	-v /where/you/want/to/have/plex/tmp/data:/tmp/plex \
	-v /where/you/want/to/store/plex/data:/config \
	-v /path/to/your/media:/data \
	mrtrustor/plex:latest
```

If Plex crashed, you need to remove the PID file for it to start again.
It's located in:

```
/where/you/want/to/store/plex/data/Plex Media Server/plexmediaserver.pid
```
