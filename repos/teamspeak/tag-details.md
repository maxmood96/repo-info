<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `teamspeak`

-	[`teamspeak:3.13`](#teamspeak313)
-	[`teamspeak:3.13.8`](#teamspeak3138)
-	[`teamspeak:latest`](#teamspeaklatest)

## `teamspeak:3.13`

```console
$ docker pull teamspeak@sha256:4d3fa1c0db9a5a4ac69a2d07d6f0478539e464b15e7186c243a9f194bc1141fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:3.13` - linux; amd64

```console
$ docker pull teamspeak@sha256:c1f32b157d1b5cb922bb64656b416f09fb5e854723a45be04635485a4e8e56a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f6ac3a35cbea9a9649363f93cdf6f629f28667980012d7d6d02e846297e681`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:22:15 GMT
RUN set -eux;     apk add --no-cache ca-certificates libstdc++ su-exec libpq;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Wed, 15 Apr 2026 20:22:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server TS3SERVER_FILETRANSFER_PORT=30033
# Wed, 15 Apr 2026 20:22:17 GMT
LABEL com.teamspeak.title=TeamSpeak 3 Server
# Wed, 15 Apr 2026 20:22:17 GMT
LABEL com.teamspeak.version=3.13.7
# Wed, 15 Apr 2026 20:22:17 GMT
LABEL com.teamspeak.description=TeamSpeak 3 Server on Alpine Linux
# Wed, 15 Apr 2026 20:22:17 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Wed, 15 Apr 2026 20:22:17 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 15 Apr 2026 20:22:17 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib;     rm -rf /opt/ts3server/redist # buildkit
# Wed, 15 Apr 2026 20:22:17 GMT
VOLUME [/var/ts3server/]
# Wed, 15 Apr 2026 20:22:17 GMT
WORKDIR /var/ts3server/
# Wed, 15 Apr 2026 20:22:17 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Wed, 15 Apr 2026 20:22:17 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Wed, 15 Apr 2026 20:22:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 15 Apr 2026 20:22:17 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec93caac8a804a9c30b0457a8b0ecf08834e96f8688f3e9e1da18aa656087a82`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 1.5 MB (1538797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02758a1cd5f8c10b6717d861c2c1eb9a51e7c07b6f310b8126b9f8ff387b380`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 9.3 MB (9250596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1745cdd1a9f4ce3a955c259c7a6de2eaaf85e0445b37f00ccb50e8b4bb58855`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:3.13` - unknown; unknown

```console
$ docker pull teamspeak@sha256:8924584e01eba59de6a0dcdebfed5338183073b724c1bfb70596bd74eb1f086b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af12e3a838ebf77a1135675a4bb301f173f8240edc4ef33cf9af4b5ae1b630`

```dockerfile
```

-	Layers:
	-	`sha256:965af222baca04799a0300239e401250966c233f41bb5ef95fb5786f91fd95f7`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 13.2 KB (13210 bytes)  
		MIME: application/vnd.in-toto+json

## `teamspeak:3.13.8`

**does not exist** (yet?)

## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:4d3fa1c0db9a5a4ac69a2d07d6f0478539e464b15e7186c243a9f194bc1141fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:c1f32b157d1b5cb922bb64656b416f09fb5e854723a45be04635485a4e8e56a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f6ac3a35cbea9a9649363f93cdf6f629f28667980012d7d6d02e846297e681`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:22:15 GMT
RUN set -eux;     apk add --no-cache ca-certificates libstdc++ su-exec libpq;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Wed, 15 Apr 2026 20:22:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server TS3SERVER_FILETRANSFER_PORT=30033
# Wed, 15 Apr 2026 20:22:17 GMT
LABEL com.teamspeak.title=TeamSpeak 3 Server
# Wed, 15 Apr 2026 20:22:17 GMT
LABEL com.teamspeak.version=3.13.7
# Wed, 15 Apr 2026 20:22:17 GMT
LABEL com.teamspeak.description=TeamSpeak 3 Server on Alpine Linux
# Wed, 15 Apr 2026 20:22:17 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Wed, 15 Apr 2026 20:22:17 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 15 Apr 2026 20:22:17 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib;     rm -rf /opt/ts3server/redist # buildkit
# Wed, 15 Apr 2026 20:22:17 GMT
VOLUME [/var/ts3server/]
# Wed, 15 Apr 2026 20:22:17 GMT
WORKDIR /var/ts3server/
# Wed, 15 Apr 2026 20:22:17 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Wed, 15 Apr 2026 20:22:17 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Wed, 15 Apr 2026 20:22:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 15 Apr 2026 20:22:17 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec93caac8a804a9c30b0457a8b0ecf08834e96f8688f3e9e1da18aa656087a82`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 1.5 MB (1538797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02758a1cd5f8c10b6717d861c2c1eb9a51e7c07b6f310b8126b9f8ff387b380`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 9.3 MB (9250596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1745cdd1a9f4ce3a955c259c7a6de2eaaf85e0445b37f00ccb50e8b4bb58855`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:latest` - unknown; unknown

```console
$ docker pull teamspeak@sha256:8924584e01eba59de6a0dcdebfed5338183073b724c1bfb70596bd74eb1f086b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af12e3a838ebf77a1135675a4bb301f173f8240edc4ef33cf9af4b5ae1b630`

```dockerfile
```

-	Layers:
	-	`sha256:965af222baca04799a0300239e401250966c233f41bb5ef95fb5786f91fd95f7`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 13.2 KB (13210 bytes)  
		MIME: application/vnd.in-toto+json
