## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:6afc518104ab051ab072757c3a32385b699be1216b27c9e14c8ba013746c1285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:090287e9f32020effffc566206d63722691fc54af6406cd7aaf6531886fdbb19
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.7 MB (410737391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffb9253c80470edaf516e8f1e9c99ebe24287a1e111d5e4d9f42ac87d3a35c6`
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
# Wed, 10 Aug 2022 18:22:58 GMT
ENV MONGO_VERSION=5.0.10
# Wed, 10 Aug 2022 18:23:29 GMT
COPY dir:df5a20c766b4f2e5091ee0297302276ffd6ab5dcd6ee60951a0bb3d59ed41b5f in C:\mongodb 
# Wed, 10 Aug 2022 18:23:40 GMT
RUN mongo --version && mongod --version
# Wed, 10 Aug 2022 18:23:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Aug 2022 18:23:42 GMT
EXPOSE 27017
# Wed, 10 Aug 2022 18:23:42 GMT
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
	-	`sha256:2ab0ce74c35408b4d8f3ae27d4075c6758d6157e984206ccf740ad384c4e06ac`  
		Last Modified: Wed, 10 Aug 2022 18:55:15 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003bdf0d5f2694240ecf228129c296d41892568f27cfa2f6344f8527371fb42c`  
		Last Modified: Wed, 10 Aug 2022 18:56:08 GMT  
		Size: 307.1 MB (307094713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20da4afb1f9208b31e01580cdf3bc80ed50840bf2f2273cbc411d728c29e64b`  
		Last Modified: Wed, 10 Aug 2022 18:55:13 GMT  
		Size: 89.1 KB (89127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ae86661238cf8fe1e5b891d1c509b3fd4e9eb634fb53c23dd857e65bb85789`  
		Last Modified: Wed, 10 Aug 2022 18:55:12 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b6517ac990ba97b57fae18a61b7e2d6b4f1a5cae9097bee019a331da766635`  
		Last Modified: Wed, 10 Aug 2022 18:55:12 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2996fab9f4c65c8d684379cc154372d5826daf066c153322b823f769e006c3aa`  
		Last Modified: Wed, 10 Aug 2022 18:55:12 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
