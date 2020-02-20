## `nats-streaming:nanoserver-1809`

```console
$ docker pull nats-streaming@sha256:68e5ae8b5a32058eb3aee66c66d24dd6910c8e0d3a40ab3cb591c4a21048d21b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `nats-streaming:nanoserver-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull nats-streaming@sha256:3e115c17687fa0e483c87ed931406cb2c9e41106fc90a3bd33837a3054962a6e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107201932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789aa174349fbec8acb48a68f39a48690451ff152aab31da24f2c40cc6fc97ad`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sun, 16 Feb 2020 01:25:57 GMT
RUN Apply image 1809-amd64
# Thu, 20 Feb 2020 05:07:58 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Thu, 20 Feb 2020 05:08:00 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Thu, 20 Feb 2020 05:08:02 GMT
RUN cmd /S /C #(nop) COPY file:d30725f7225d14fba35e88513adf63da18fc9fef9c4f6c817dff8f784f19a7c1 in nats-streaming-server.exe 
# Thu, 20 Feb 2020 05:08:04 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Thu, 20 Feb 2020 05:08:05 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:a35da61c356213336e646756218539950461ff2bf096badf307a23add6e70053`  
		Size: 101.1 MB (101145811 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cf376b4a5e6deb66a4640f1d8d0c8c40ca949673b388cd17070f88095406acca`  
		Last Modified: Thu, 20 Feb 2020 05:08:49 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb508987e8aa0ee95e77b700be9e46c315eb2224172dd11e29082acb63755caa`  
		Last Modified: Thu, 20 Feb 2020 05:08:58 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3c46cb9191e30fe34da955036a3e147af5c2ac12a2c1704f6fb0dc0eb96762`  
		Last Modified: Thu, 20 Feb 2020 05:08:51 GMT  
		Size: 6.1 MB (6052185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9a22e3298563822192d0c36af7de72e8723d4a04338f1dfe7d40221743cdac`  
		Last Modified: Thu, 20 Feb 2020 05:08:49 GMT  
		Size: 920.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110ea2b61b8f7e5b826feed77d9a4e981ee84b95d47052aee2492dffba086721`  
		Last Modified: Thu, 20 Feb 2020 05:08:49 GMT  
		Size: 923.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
