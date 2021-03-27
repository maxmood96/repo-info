## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:640fcb3179a784f1f67dedd46b5dd62c8b4d68a3ffe0adbac60545414ec115ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:7d2dea407734534bcadb3dff06e7a45a22d94c98e03aa13a4a15d11ea3ba5f86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51785790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3abdeb8d7c066e6b7cd52a39f7b1fe93893b25db80f3cb4f901dbcfb5ed09889`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 09:09:58 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:01 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 27 Mar 2021 09:10:01 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Sat, 27 Mar 2021 09:10:08 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 09:10:09 GMT
VOLUME [/data]
# Sat, 27 Mar 2021 09:10:09 GMT
WORKDIR /data
# Sat, 27 Mar 2021 09:10:09 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 27 Mar 2021 09:10:09 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52897da0e7cb3d0cd73c7d8f210289fd21b69a0a915dd468cb8b5822f2a5a182`  
		Last Modified: Sat, 27 Mar 2021 09:10:58 GMT  
		Size: 6.7 MB (6690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47aad8c1069a1f3d4880682544c679be36ac115fffea611dfd42b2ba3106b1e9`  
		Last Modified: Sat, 27 Mar 2021 09:10:56 GMT  
		Size: 2.6 KB (2617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c856427df50e83000162f91c7fadd4ba0227e8d5aa73bdc1043695e7ae9d55`  
		Last Modified: Sat, 27 Mar 2021 09:10:59 GMT  
		Size: 18.0 MB (17991759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b1e2260a7e1bd8da16aadf32854144aea98733220d3e995c0d64c38eb2de7`  
		Last Modified: Sat, 27 Mar 2021 09:10:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
