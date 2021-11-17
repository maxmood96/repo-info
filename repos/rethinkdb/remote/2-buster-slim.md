## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:bf0b74da846cf30f1c422573b6faaba09d3354657e71473312fe90a83f77f9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:a6a58a5ca7e87210999ae543d5adc67b635f925f7aa32b79cee9ecc7c203059f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51838989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caab5fcad254c52b72bf9ad2c3ab94eea05a7f4a6f039c8dad2ba5cc9d0e8d27`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:02 GMT
ADD file:3c54ad257f2e04f7294ce879b884820cf4726c8e93ec548172825963e40c79ad in / 
# Wed, 17 Nov 2021 02:21:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 22:24:51 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:25:02 GMT
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Wed, 17 Nov 2021 22:25:02 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Wed, 17 Nov 2021 22:25:10 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 22:25:10 GMT
VOLUME [/data]
# Wed, 17 Nov 2021 22:25:11 GMT
WORKDIR /data
# Wed, 17 Nov 2021 22:25:11 GMT
CMD ["rethinkdb" "--bind" "all"]
# Wed, 17 Nov 2021 22:25:11 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:a10c77af261312e7c92bcc184f2d1726175ff7f142e44b01c5779cd79348b9fd`  
		Last Modified: Wed, 17 Nov 2021 02:26:31 GMT  
		Size: 27.2 MB (27153675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fb6b02a9a0ade6df258d7064777b68071482b115c8902e01a27194bdf15940`  
		Last Modified: Wed, 17 Nov 2021 22:25:33 GMT  
		Size: 6.7 MB (6691116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de316cb2988512400f1cb24315615f7d9c61e4cc781ce4b78a1a6797a2bd58dc`  
		Last Modified: Wed, 17 Nov 2021 22:25:31 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6dfcaddf3c553eb8300f607eee1151bedccf8957248f60b590a2a3a720a26c`  
		Last Modified: Wed, 17 Nov 2021 22:25:34 GMT  
		Size: 18.0 MB (17991459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276ce5b4b66351bef0957b0c61e6d0eb8e4f8a00fef8581f63e8a5d61f01c416`  
		Last Modified: Wed, 17 Nov 2021 22:25:31 GMT  
		Size: 127.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
