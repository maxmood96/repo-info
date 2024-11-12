<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `teamspeak`

-	[`teamspeak:3.13`](#teamspeak313)
-	[`teamspeak:3.13.7`](#teamspeak3137)
-	[`teamspeak:latest`](#teamspeaklatest)

## `teamspeak:3.13`

```console
$ docker pull teamspeak@sha256:ddbeb29446ca423498692bd9f3ae67ff109121f80a95c7d405b1083c02c80087
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:3.13` - linux; amd64

```console
$ docker pull teamspeak@sha256:499eb628148dcb232bdac5585e992c0cb41517dec048cc8ad9e6b560c8e49045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13994945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08997aaffffb23422f1f503c6363445a48b10f24e8ebdc885e331315ac9a9c7d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 18 Sep 2023 06:58:15 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbfae5d7726322ce7d8ceb4acf505399c4ee07753d30b1a9a82cfc68c4b6998`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.3 MB (1326431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ca4c319bd08b8f1f91efcfc841da25b2c95f084c14178a5399a6cee1181243`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e51cf33e07cedd023719312464a609b8b3fe1ca0a3964a89b01dbcb5612d03f`  
		Last Modified: Tue, 12 Nov 2024 02:10:55 GMT  
		Size: 9.2 MB (9249237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45425e14a2e5fb90b826c58692701eae2f447fe29bb885a0cf36f55629cd66a`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:3.13` - unknown; unknown

```console
$ docker pull teamspeak@sha256:ac71967814068ae5d67c50e02ea52595972e6df55a314eff85c86e8ce9bf831a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282aaf9e9129583286d558d0eece5c911aafcf99055231a24e8add737ba75903`

```dockerfile
```

-	Layers:
	-	`sha256:b45d463ffa087b2431756a8523abc5687445bd9ae67f28b0b75fab3dc013d109`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 14.2 KB (14219 bytes)  
		MIME: application/vnd.in-toto+json

## `teamspeak:3.13.7`

```console
$ docker pull teamspeak@sha256:ddbeb29446ca423498692bd9f3ae67ff109121f80a95c7d405b1083c02c80087
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:3.13.7` - linux; amd64

```console
$ docker pull teamspeak@sha256:499eb628148dcb232bdac5585e992c0cb41517dec048cc8ad9e6b560c8e49045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13994945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08997aaffffb23422f1f503c6363445a48b10f24e8ebdc885e331315ac9a9c7d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 18 Sep 2023 06:58:15 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbfae5d7726322ce7d8ceb4acf505399c4ee07753d30b1a9a82cfc68c4b6998`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.3 MB (1326431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ca4c319bd08b8f1f91efcfc841da25b2c95f084c14178a5399a6cee1181243`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e51cf33e07cedd023719312464a609b8b3fe1ca0a3964a89b01dbcb5612d03f`  
		Last Modified: Tue, 12 Nov 2024 02:10:55 GMT  
		Size: 9.2 MB (9249237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45425e14a2e5fb90b826c58692701eae2f447fe29bb885a0cf36f55629cd66a`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:3.13.7` - unknown; unknown

```console
$ docker pull teamspeak@sha256:ac71967814068ae5d67c50e02ea52595972e6df55a314eff85c86e8ce9bf831a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282aaf9e9129583286d558d0eece5c911aafcf99055231a24e8add737ba75903`

```dockerfile
```

-	Layers:
	-	`sha256:b45d463ffa087b2431756a8523abc5687445bd9ae67f28b0b75fab3dc013d109`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 14.2 KB (14219 bytes)  
		MIME: application/vnd.in-toto+json

## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:ddbeb29446ca423498692bd9f3ae67ff109121f80a95c7d405b1083c02c80087
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:499eb628148dcb232bdac5585e992c0cb41517dec048cc8ad9e6b560c8e49045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13994945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08997aaffffb23422f1f503c6363445a48b10f24e8ebdc885e331315ac9a9c7d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 18 Sep 2023 06:58:15 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbfae5d7726322ce7d8ceb4acf505399c4ee07753d30b1a9a82cfc68c4b6998`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.3 MB (1326431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ca4c319bd08b8f1f91efcfc841da25b2c95f084c14178a5399a6cee1181243`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e51cf33e07cedd023719312464a609b8b3fe1ca0a3964a89b01dbcb5612d03f`  
		Last Modified: Tue, 12 Nov 2024 02:10:55 GMT  
		Size: 9.2 MB (9249237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45425e14a2e5fb90b826c58692701eae2f447fe29bb885a0cf36f55629cd66a`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 1.6 KB (1559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:latest` - unknown; unknown

```console
$ docker pull teamspeak@sha256:ac71967814068ae5d67c50e02ea52595972e6df55a314eff85c86e8ce9bf831a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282aaf9e9129583286d558d0eece5c911aafcf99055231a24e8add737ba75903`

```dockerfile
```

-	Layers:
	-	`sha256:b45d463ffa087b2431756a8523abc5687445bd9ae67f28b0b75fab3dc013d109`  
		Last Modified: Tue, 12 Nov 2024 02:10:54 GMT  
		Size: 14.2 KB (14219 bytes)  
		MIME: application/vnd.in-toto+json
