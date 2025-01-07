<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `teamspeak`

-	[`teamspeak:3.13`](#teamspeak313)
-	[`teamspeak:3.13.7`](#teamspeak3137)
-	[`teamspeak:latest`](#teamspeaklatest)

## `teamspeak:3.13`

```console
$ docker pull teamspeak@sha256:18ccbec6813ee925034491867a4ab2a1c578974dfc763981fd5c50ddc17ee789
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:3.13` - linux; amd64

```console
$ docker pull teamspeak@sha256:3ea032a19afc91b6fbb1a4eae28315a5f1b9aabb35e63c7925ebf6ced720f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13972200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd8c9f69ecbe975e23e99abdb809807473a66db371fdaacb1c4379bfbf0b5f2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 18 Sep 2023 06:58:15 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 06:58:15 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Mon, 18 Sep 2023 06:58:15 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Mon, 18 Sep 2023 06:58:15 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Mon, 18 Sep 2023 06:58:15 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
VOLUME [/var/ts3server/]
# Mon, 18 Sep 2023 06:58:15 GMT
WORKDIR /var/ts3server/
# Mon, 18 Sep 2023 06:58:15 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Mon, 18 Sep 2023 06:58:15 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 18 Sep 2023 06:58:15 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbeb1ec3d6629b680cb8b736025933c5dd4f715ee5ec6b3dd17054b5fd9f973`  
		Size: 1.3 MB (1312438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa1cb886aa4c29542231932f6a9c6e170b00fd0d30ff741e6231114914e15dd`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc208237990d2630bb38691c1b4df1c5810c723a737f702f9a1e48bd4854176e`  
		Size: 9.2 MB (9249258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96017aa274b81290fa9a660fbc755031607f1f3e87444a259f80fb9ce4363b42`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:3.13` - unknown; unknown

```console
$ docker pull teamspeak@sha256:69638f9777242dc16b421d9df6c9912492f85aa9b9de8081668c4c841f6ae2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b88fa9fd2710ea322b55e201c1330654c30d171d205e635d0bee11629645a`

```dockerfile
```

-	Layers:
	-	`sha256:000e49d6e1c0649b42aee346dfecc3790907bcdf7f5f57ef70c20642792b686a`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `teamspeak:3.13.7`

```console
$ docker pull teamspeak@sha256:18ccbec6813ee925034491867a4ab2a1c578974dfc763981fd5c50ddc17ee789
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:3.13.7` - linux; amd64

```console
$ docker pull teamspeak@sha256:3ea032a19afc91b6fbb1a4eae28315a5f1b9aabb35e63c7925ebf6ced720f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13972200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd8c9f69ecbe975e23e99abdb809807473a66db371fdaacb1c4379bfbf0b5f2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 18 Sep 2023 06:58:15 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 06:58:15 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Mon, 18 Sep 2023 06:58:15 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Mon, 18 Sep 2023 06:58:15 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Mon, 18 Sep 2023 06:58:15 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
VOLUME [/var/ts3server/]
# Mon, 18 Sep 2023 06:58:15 GMT
WORKDIR /var/ts3server/
# Mon, 18 Sep 2023 06:58:15 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Mon, 18 Sep 2023 06:58:15 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 18 Sep 2023 06:58:15 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbeb1ec3d6629b680cb8b736025933c5dd4f715ee5ec6b3dd17054b5fd9f973`  
		Size: 1.3 MB (1312438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa1cb886aa4c29542231932f6a9c6e170b00fd0d30ff741e6231114914e15dd`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc208237990d2630bb38691c1b4df1c5810c723a737f702f9a1e48bd4854176e`  
		Size: 9.2 MB (9249258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96017aa274b81290fa9a660fbc755031607f1f3e87444a259f80fb9ce4363b42`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:3.13.7` - unknown; unknown

```console
$ docker pull teamspeak@sha256:69638f9777242dc16b421d9df6c9912492f85aa9b9de8081668c4c841f6ae2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b88fa9fd2710ea322b55e201c1330654c30d171d205e635d0bee11629645a`

```dockerfile
```

-	Layers:
	-	`sha256:000e49d6e1c0649b42aee346dfecc3790907bcdf7f5f57ef70c20642792b686a`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json

## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:18ccbec6813ee925034491867a4ab2a1c578974dfc763981fd5c50ddc17ee789
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:3ea032a19afc91b6fbb1a4eae28315a5f1b9aabb35e63c7925ebf6ced720f2a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13972200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd8c9f69ecbe975e23e99abdb809807473a66db371fdaacb1c4379bfbf0b5f2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 18 Sep 2023 06:58:15 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Sep 2023 06:58:15 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Mon, 18 Sep 2023 06:58:15 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Mon, 18 Sep 2023 06:58:15 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Mon, 18 Sep 2023 06:58:15 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
VOLUME [/var/ts3server/]
# Mon, 18 Sep 2023 06:58:15 GMT
WORKDIR /var/ts3server/
# Mon, 18 Sep 2023 06:58:15 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Mon, 18 Sep 2023 06:58:15 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Mon, 18 Sep 2023 06:58:15 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 18 Sep 2023 06:58:15 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbeb1ec3d6629b680cb8b736025933c5dd4f715ee5ec6b3dd17054b5fd9f973`  
		Size: 1.3 MB (1312438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa1cb886aa4c29542231932f6a9c6e170b00fd0d30ff741e6231114914e15dd`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc208237990d2630bb38691c1b4df1c5810c723a737f702f9a1e48bd4854176e`  
		Size: 9.2 MB (9249258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96017aa274b81290fa9a660fbc755031607f1f3e87444a259f80fb9ce4363b42`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:latest` - unknown; unknown

```console
$ docker pull teamspeak@sha256:69638f9777242dc16b421d9df6c9912492f85aa9b9de8081668c4c841f6ae2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b88fa9fd2710ea322b55e201c1330654c30d171d205e635d0bee11629645a`

```dockerfile
```

-	Layers:
	-	`sha256:000e49d6e1c0649b42aee346dfecc3790907bcdf7f5f57ef70c20642792b686a`  
		Last Modified: Tue, 07 Jan 2025 03:15:24 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
