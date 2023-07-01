## `mongo:6-nanoserver-1809`

```console
$ docker pull mongo@sha256:1f675230f8f40c335f85774c4e5577f73f1a043bcda371a8993c22e2eba79e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `mongo:6-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:411f9ad2a82206711fc1429d6e2e14f275ffdcff6bc5c146384349691b8f3a84
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.4 MB (621413255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a80be13a867db801afd6115801ad1213ca5f19ae101f9c559ae69c7965c0862`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 01:50:24 GMT
SHELL [cmd /S /C]
# Sat, 24 Jun 2023 02:33:09 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 02:33:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 24 Jun 2023 02:33:24 GMT
USER ContainerUser
# Sat, 24 Jun 2023 02:33:25 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Fri, 30 Jun 2023 23:35:35 GMT
ENV MONGO_VERSION=6.0.7
# Fri, 30 Jun 2023 23:36:11 GMT
COPY dir:6115b874c812adb9a4e4da58fe85482084095a26c49827ac1513416f28ff99f9 in C:\mongodb 
# Fri, 30 Jun 2023 23:36:25 GMT
RUN mongod --version
# Fri, 30 Jun 2023 23:36:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 30 Jun 2023 23:36:27 GMT
EXPOSE 27017
# Fri, 30 Jun 2023 23:36:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0712dde7e721d063ebcbe80a9968c96e3b3af1f54a33928786e0d37335da4cd`  
		Last Modified: Sat, 24 Jun 2023 02:18:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a638f113f886e54e8e494347981d25a36f28873f1b9e0905cef7ef9ef0227`  
		Last Modified: Sat, 24 Jun 2023 06:33:56 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4deb983b7c23277ea52231f8a02797b91fd72aad7b9b8234cceb857505961`  
		Last Modified: Sat, 24 Jun 2023 06:33:54 GMT  
		Size: 69.6 KB (69575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3592f8eaf22ebd67118459d39e793af2168190561abf11f80b1f570fb5a468f9`  
		Last Modified: Sat, 24 Jun 2023 06:33:54 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96471f034d4e67736ba12bcd5d8242ea5e6eb15532c4a6b23bb1f6876802c8f8`  
		Last Modified: Sat, 24 Jun 2023 06:33:54 GMT  
		Size: 267.2 KB (267152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7a9e80eccf5bad85d09f85a31b25c4f258e709925352bcea8afd6ccd2aebbe`  
		Last Modified: Sat, 01 Jul 2023 00:36:14 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bb7592820e5d0c9b3398045d12a449929336b821cfd6687085561f2aefca292`  
		Last Modified: Sat, 01 Jul 2023 00:37:29 GMT  
		Size: 516.6 MB (516590167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad09cd831de1f37693cb475ca9c6fa7fe69c25ed42e5d46b4b266f53cfd2c4`  
		Last Modified: Sat, 01 Jul 2023 00:36:12 GMT  
		Size: 77.5 KB (77535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d008d0a02ae646fb66799a65b0b83a73182322c83e750a9bb387f57cfaf2c6cd`  
		Last Modified: Sat, 01 Jul 2023 00:36:12 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3d2c45f80ba998e287221918e8ecab3ab76dbb3dd82fdd518a19126b126677`  
		Last Modified: Sat, 01 Jul 2023 00:36:12 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f740b222a8b0072aa54ba6523429d86c9f9ba086c40e73c831a9b8e88f9ec1ed`  
		Last Modified: Sat, 01 Jul 2023 00:36:12 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
