<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `teamspeak`

-	[`teamspeak:3.13`](#teamspeak313)
-	[`teamspeak:3.13.7`](#teamspeak3137)
-	[`teamspeak:latest`](#teamspeaklatest)

## `teamspeak:3.13`

```console
$ docker pull teamspeak@sha256:093b6754e2f5417bd5766658394e4ebe9da5d96a7740e66015e158dcd02893ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:3.13` - linux; amd64

```console
$ docker pull teamspeak@sha256:b8db19607db4cb1eebbb151bf126b103503dbc8225885d7a324cfdd0195e2a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14656472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ec2bdee711b64d63c9814504bff95c3962063a51d4ea0c35c0ffd4e37735c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 19:36:03 GMT
RUN set -eux;     apk add --no-cache ca-certificates libstdc++ su-exec libpq;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server TS3SERVER_FILETRANSFER_PORT=30033
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.title=TeamSpeak 3 Server
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.version=3.13.7
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.description=TeamSpeak 3 Server on Alpine Linux
# Wed, 11 Feb 2026 19:36:06 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Wed, 11 Feb 2026 19:36:06 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 11 Feb 2026 19:36:06 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib;     rm -rf /opt/ts3server/redist # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
VOLUME [/var/ts3server/]
# Wed, 11 Feb 2026 19:36:06 GMT
WORKDIR /var/ts3server/
# Wed, 11 Feb 2026 19:36:06 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Wed, 11 Feb 2026 19:36:06 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Feb 2026 19:36:06 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72180c624322f4b39e6d9d55c5360c429d709cefdea1a18e02e276bf55299573`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 1.5 MB (1542438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698fcefab67521565bd5855e1107066e3d075d10d7250c28f63df175e636bd1`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 9.3 MB (9250629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f07ee71e0d162785e4a212db935b9c0a65bf451654fb504139c72a745636684`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:3.13` - unknown; unknown

```console
$ docker pull teamspeak@sha256:64acb467050b1f639a22a012beb580c65be9dab90704d12346f9f428fcc3295e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7703525939de613cd7cc9176ceec1e1930b27a241abaec08510fe421d21c632`

```dockerfile
```

-	Layers:
	-	`sha256:b4fb82913fbacfb9c902a3003571bcf46645b26212be355cd14b5f222055a945`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 13.2 KB (13210 bytes)  
		MIME: application/vnd.in-toto+json

## `teamspeak:3.13.7`

```console
$ docker pull teamspeak@sha256:093b6754e2f5417bd5766658394e4ebe9da5d96a7740e66015e158dcd02893ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:3.13.7` - linux; amd64

```console
$ docker pull teamspeak@sha256:b8db19607db4cb1eebbb151bf126b103503dbc8225885d7a324cfdd0195e2a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14656472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ec2bdee711b64d63c9814504bff95c3962063a51d4ea0c35c0ffd4e37735c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 19:36:03 GMT
RUN set -eux;     apk add --no-cache ca-certificates libstdc++ su-exec libpq;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server TS3SERVER_FILETRANSFER_PORT=30033
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.title=TeamSpeak 3 Server
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.version=3.13.7
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.description=TeamSpeak 3 Server on Alpine Linux
# Wed, 11 Feb 2026 19:36:06 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Wed, 11 Feb 2026 19:36:06 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 11 Feb 2026 19:36:06 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib;     rm -rf /opt/ts3server/redist # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
VOLUME [/var/ts3server/]
# Wed, 11 Feb 2026 19:36:06 GMT
WORKDIR /var/ts3server/
# Wed, 11 Feb 2026 19:36:06 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Wed, 11 Feb 2026 19:36:06 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Feb 2026 19:36:06 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72180c624322f4b39e6d9d55c5360c429d709cefdea1a18e02e276bf55299573`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 1.5 MB (1542438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698fcefab67521565bd5855e1107066e3d075d10d7250c28f63df175e636bd1`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 9.3 MB (9250629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f07ee71e0d162785e4a212db935b9c0a65bf451654fb504139c72a745636684`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:3.13.7` - unknown; unknown

```console
$ docker pull teamspeak@sha256:64acb467050b1f639a22a012beb580c65be9dab90704d12346f9f428fcc3295e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7703525939de613cd7cc9176ceec1e1930b27a241abaec08510fe421d21c632`

```dockerfile
```

-	Layers:
	-	`sha256:b4fb82913fbacfb9c902a3003571bcf46645b26212be355cd14b5f222055a945`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 13.2 KB (13210 bytes)  
		MIME: application/vnd.in-toto+json

## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:093b6754e2f5417bd5766658394e4ebe9da5d96a7740e66015e158dcd02893ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:b8db19607db4cb1eebbb151bf126b103503dbc8225885d7a324cfdd0195e2a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14656472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ec2bdee711b64d63c9814504bff95c3962063a51d4ea0c35c0ffd4e37735c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 11 Feb 2026 19:36:03 GMT
RUN set -eux;     apk add --no-cache ca-certificates libstdc++ su-exec libpq;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server TS3SERVER_FILETRANSFER_PORT=30033
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.title=TeamSpeak 3 Server
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.version=3.13.7
# Wed, 11 Feb 2026 19:36:06 GMT
LABEL com.teamspeak.description=TeamSpeak 3 Server on Alpine Linux
# Wed, 11 Feb 2026 19:36:06 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Wed, 11 Feb 2026 19:36:06 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Wed, 11 Feb 2026 19:36:06 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib;     rm -rf /opt/ts3server/redist # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
VOLUME [/var/ts3server/]
# Wed, 11 Feb 2026 19:36:06 GMT
WORKDIR /var/ts3server/
# Wed, 11 Feb 2026 19:36:06 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Wed, 11 Feb 2026 19:36:06 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Wed, 11 Feb 2026 19:36:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Feb 2026 19:36:06 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72180c624322f4b39e6d9d55c5360c429d709cefdea1a18e02e276bf55299573`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 1.5 MB (1542438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7698fcefab67521565bd5855e1107066e3d075d10d7250c28f63df175e636bd1`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 9.3 MB (9250629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f07ee71e0d162785e4a212db935b9c0a65bf451654fb504139c72a745636684`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:latest` - unknown; unknown

```console
$ docker pull teamspeak@sha256:64acb467050b1f639a22a012beb580c65be9dab90704d12346f9f428fcc3295e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7703525939de613cd7cc9176ceec1e1930b27a241abaec08510fe421d21c632`

```dockerfile
```

-	Layers:
	-	`sha256:b4fb82913fbacfb9c902a3003571bcf46645b26212be355cd14b5f222055a945`  
		Last Modified: Wed, 11 Feb 2026 19:36:10 GMT  
		Size: 13.2 KB (13210 bytes)  
		MIME: application/vnd.in-toto+json
