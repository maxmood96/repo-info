## `nats-streaming:windowsservercore`

```console
$ docker pull nats-streaming@sha256:0954b1fd6d70cfb78baae82704cf9ea559d545b07d5badf44f17fc513e5487f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64

### `nats-streaming:windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull nats-streaming@sha256:f9e4f055730264ed54cecfdc4121cf1d5eaf3e0004293010825f6e191c017cfc
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 GB (5728218879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86c2ae9f93291ca241e4d52261c6d67d40832ff0291b6e59f7fb4af7523b82c`
-	Default Command: `["nats-streaming-server","-m","8222"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 22:51:26 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 Dec 2019 22:51:28 GMT
RUN cmd /S /C #(nop) WORKDIR C:\nats-streaming-server
# Wed, 11 Dec 2019 22:51:30 GMT
RUN cmd /S /C #(nop) COPY file:d333dfb9aa0fca02ce2e2300447082af645803b49703ee1671951f7dba266042 in nats-streaming-server.exe 
# Wed, 11 Dec 2019 22:51:33 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 8222
# Wed, 11 Dec 2019 22:51:34 GMT
RUN cmd /S /C #(nop)  CMD ["nats-streaming-server" "-m" "8222"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd6ba5629456c8603c7314360c958c835db45df5657a12408c0ef6415c30207c`  
		Last Modified: Wed, 11 Dec 2019 22:52:49 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dadd2a214c252be891fb485f082b59673928793e06958f742ca3982773ed34`  
		Last Modified: Wed, 11 Dec 2019 22:52:49 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dc9620a32f58813caf0e9876186fb219bffdf7714f9592f718b195ec8a456a`  
		Last Modified: Wed, 11 Dec 2019 22:52:51 GMT  
		Size: 5.5 MB (5510085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32295285a2becde7956eecc1b3fa8430ef17a54af08124fbb824062d25502ca7`  
		Last Modified: Wed, 11 Dec 2019 22:52:49 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9720713411029a58b3bcd152fa61b79ac974b586d8d89b2990b8fa5f26a6a5a`  
		Last Modified: Wed, 11 Dec 2019 22:52:49 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
