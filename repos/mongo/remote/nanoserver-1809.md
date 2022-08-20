## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:ab2f4a05f9f17bf917a179e080dee40f497a4aa40407bf1121b50f44b311ee5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:30265e856fd19c553e5f9b7335d1feaf62b8e37a26af7221f246125f6e8446bb
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.9 MB (411880344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d6c0bde3beb818576b681c9a52ddf2e5955c6cd275a7f3234e0d4154c2facf3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Aug 2022 18:08:38 GMT
RUN Apply image 10.0.17763.3287
# Wed, 10 Aug 2022 13:04:30 GMT
SHELL [cmd /S /C]
# Wed, 10 Aug 2022 18:22:41 GMT
USER ContainerAdministrator
# Wed, 10 Aug 2022 18:22:55 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 10 Aug 2022 18:22:56 GMT
USER ContainerUser
# Wed, 10 Aug 2022 18:22:57 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Sat, 20 Aug 2022 01:21:43 GMT
ENV MONGO_VERSION=5.0.11
# Sat, 20 Aug 2022 01:22:14 GMT
COPY dir:945135105d32f315ec4cb75022847d1be3478ca04a5556c21f2f97bea0709e14 in C:\mongodb 
# Sat, 20 Aug 2022 01:22:29 GMT
RUN mongo --version && mongod --version
# Sat, 20 Aug 2022 01:22:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 20 Aug 2022 01:22:31 GMT
EXPOSE 27017
# Sat, 20 Aug 2022 01:22:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5c9d6483dab113d2d9b50fdf3156622aa2ec3d6faaed5664d15a5568032d1714`  
		Size: 103.2 MB (103204200 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:9982991b820814ad737b2a161e973194e66b8d7b0a9890bee49cd158d7e77dec`  
		Last Modified: Wed, 10 Aug 2022 13:27:27 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7180e2213de155098394f0dbf886f68478c49bc5ef2c0977d6e28da9593090df`  
		Last Modified: Wed, 10 Aug 2022 18:55:17 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0b5eb91e7b8da02b963c0e45697ecd1e88fdea8a134974bf17366b2dc3a68e`  
		Last Modified: Wed, 10 Aug 2022 18:55:15 GMT  
		Size: 77.8 KB (77802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c59fe6b6f7e47222898a3f00c7f02b87dcb9f4480cf874d6f00b55cbcede826`  
		Last Modified: Wed, 10 Aug 2022 18:55:14 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9ccf06a99cd0032feb37c8d5a167ba6372e41687f302366e20b947fe83bafe`  
		Last Modified: Wed, 10 Aug 2022 18:55:14 GMT  
		Size: 263.5 KB (263523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e43338ea71d1f4d5637684c76e55dd8931d65f968ccc0abaa487d65610f6139`  
		Last Modified: Sat, 20 Aug 2022 01:41:44 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0798c36165bb7f08124dc86888503395d9e02ecae8230a487bbcab2832e3589`  
		Last Modified: Sat, 20 Aug 2022 01:42:39 GMT  
		Size: 308.2 MB (308238374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb7de0731974937e22cfed451f1d2a22c7831fd3c95920c6078cfba50498de5`  
		Last Modified: Sat, 20 Aug 2022 01:41:42 GMT  
		Size: 88.4 KB (88449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ad01aa21f2dca0d6655b55716378d50f595b8c8face46ebac1e6b41b490bc0`  
		Last Modified: Sat, 20 Aug 2022 01:41:41 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e073c0d5981967eb903c10bee4ffac3beaf05b5f4d1b71c382877c30b41d251b`  
		Last Modified: Sat, 20 Aug 2022 01:41:41 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb13c35f59870c303ae248d581151b64755545f4a95bf0caebe99864fab3f47`  
		Last Modified: Sat, 20 Aug 2022 01:41:41 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
