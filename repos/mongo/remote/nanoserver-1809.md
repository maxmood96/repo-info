## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:133e4119b593f1a759319fe41b182dd1d6aef456ea21456a67c0f8580e8822a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:1b45b1bac48c500ef38c899cba7a05f5cf160c9391430925c70301b427e1ad9f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **763.2 MB (763242292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4a4abfde491880ebcd69706d5bc77d90de6d2fd816d9528992fb5ac60ced004`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Tue, 13 Aug 2024 21:13:04 GMT
SHELL [cmd /S /C]
# Tue, 13 Aug 2024 21:13:07 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 21:13:10 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 13 Aug 2024 21:13:11 GMT
USER ContainerUser
# Tue, 13 Aug 2024 21:13:13 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 13 Aug 2024 21:13:14 GMT
ENV MONGO_VERSION=7.0.12
# Tue, 13 Aug 2024 21:13:45 GMT
COPY dir:f0b5fa50aabc110faf03295e6346b9d39d589dd155d9a16877c392688d63cd36 in C:\mongodb 
# Tue, 13 Aug 2024 21:13:54 GMT
RUN mongod --version
# Tue, 13 Aug 2024 21:13:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 21:13:55 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 21:13:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177d01c193368af6a655c381f37f6f010b7919995c34a8e54a0cae671635dd7f`  
		Last Modified: Tue, 13 Aug 2024 21:14:00 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec3f7ed786063a720022d3e1fed260d13ba87a5707a53f5719817d0b738e6d6`  
		Last Modified: Tue, 13 Aug 2024 21:14:00 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2575810bd3321f48260f62e00ff47cc96582420cd757678f8f44e61207af7df0`  
		Last Modified: Tue, 13 Aug 2024 21:13:59 GMT  
		Size: 72.5 KB (72492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5caff9020da00950b1d42dc869e304394230640f32daf4261ee577cad5d0ca1`  
		Last Modified: Tue, 13 Aug 2024 21:13:59 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd46bea9d8fecb3cf990d9b113065bbb69043905ef4b456956290fa3353beb6`  
		Last Modified: Tue, 13 Aug 2024 21:13:59 GMT  
		Size: 275.2 KB (275171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0073141fe988d686d051da233144ea6906468472d9b19117cece7f58a0f607ab`  
		Last Modified: Tue, 13 Aug 2024 21:13:59 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bfbd029bdd743294ac88079b36e4e2af3f3ebe80ec56ee61e8f42e2ed26c92`  
		Last Modified: Tue, 13 Aug 2024 21:14:45 GMT  
		Size: 607.7 MB (607714612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e88b5d73574abcb6056aa0535b405d968b74328b45cad76798c44fea91ff3c`  
		Last Modified: Tue, 13 Aug 2024 21:13:58 GMT  
		Size: 89.7 KB (89651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a377e64fbfeb2dc3bbaa1f06cf830270398143e580d1b4db37d29dd31b5f0d`  
		Last Modified: Tue, 13 Aug 2024 21:13:58 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fb2f4b7707388aa75b58958b67786b6af6518735d65df070e6c77ea506e1a1`  
		Last Modified: Tue, 13 Aug 2024 21:13:58 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b33fac56b85b9f2e6ec7c1fbf4cb15b1c8a7080b888ce2631fe668bad3f6c0b`  
		Last Modified: Tue, 13 Aug 2024 21:13:58 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
