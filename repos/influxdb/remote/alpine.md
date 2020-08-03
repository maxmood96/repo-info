## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:32dbb22a7a1f0d3be2a034cc7aac0bd43d68066b4375d0d2c8f745072df9f438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:39d0ca6f1278d2e38eb40f92fff6111b181dfa3d07e98181249113350e005974
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68430025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a3d14e43adecbd4ae14a5ab30bf9b0ab7edfeaa1ddb6b94224cdad972b8d98`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:35 GMT
ADD file:a0afd0b0db7f9ee9496186ead087ec00edd1386ea8c018557d15720053f7308e in / 
# Fri, 24 Apr 2020 01:05:35 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 14:15:54 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 24 Apr 2020 15:28:09 GMT
RUN apk add --no-cache tzdata bash ca-certificates &&     update-ca-certificates
# Wed, 15 Jul 2020 00:20:41 GMT
ENV INFLUXDB_VERSION=1.8.1
# Mon, 03 Aug 2020 22:34:28 GMT
RUN set -ex &&     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz.asc influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf influxdb-${INFLUXDB_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/influxdb-*/influxdb.conf &&     chmod +x /usr/src/influxdb-*/* &&     cp -a /usr/src/influxdb-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:3d8a606d61e1fc0042cf34d036eda4550a18d140c47376dacc02d96ee6f2dd8b in /etc/influxdb/influxdb.conf 
# Mon, 03 Aug 2020 22:34:29 GMT
EXPOSE 8086
# Mon, 03 Aug 2020 22:34:29 GMT
VOLUME [/var/lib/influxdb]
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:61c4af7a0e637328374ec46266ed6dde40adf7d14ac6c5081100924991beb7f3 in /entrypoint.sh 
# Mon, 03 Aug 2020 22:34:29 GMT
COPY file:e7af69cde81ffb6eddc175488941183d1244772c36c27b74751d54389fb71701 in /init-influxdb.sh 
# Mon, 03 Aug 2020 22:34:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Aug 2020 22:34:30 GMT
CMD ["influxd"]
```

-	Layers:
	-	`sha256:31603596830fc7e56753139f9c2c6bd3759e48a850659506ebfb885d1cf3aef5`  
		Last Modified: Fri, 24 Apr 2020 01:06:12 GMT  
		Size: 2.8 MB (2773413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321996f3080d1a7516b5914e27460b495eb04950d0190554844f395e7be9c793`  
		Last Modified: Fri, 24 Apr 2020 14:16:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9984b0a697389d40ad58252364c9cbb4e4a5258602767230a8f149134746718`  
		Last Modified: Fri, 24 Apr 2020 15:30:04 GMT  
		Size: 1.9 MB (1863602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac116993ab18e3e4368870163f4aa9a16213584178dca11b2f8176feb7e0f88`  
		Last Modified: Mon, 03 Aug 2020 22:35:31 GMT  
		Size: 63.8 MB (63791146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a5fc5379a9b5202ac0c9eb6cecb4989f866ab37ed15fb0fe720dbd241d6286`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f48eac3660df184b7a56993e71edd267a8538148b294500bcd92d8021db376`  
		Last Modified: Mon, 03 Aug 2020 22:35:21 GMT  
		Size: 208.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e23b94f7fd3e8b623c5b780e09385cd870cfb847c31db816af592e9738463e9`  
		Last Modified: Mon, 03 Aug 2020 22:35:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
