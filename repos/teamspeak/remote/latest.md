## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:12b89d83f86068c0e9486afc10335db26297b87c7029022bdcaaaa479e9127c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:1621140e799071e70f32638aedd9d60a63d1dad7ff51ce98eb700654f15c3b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13998191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d681884cf002dc49bdee2c2f42eeaaf6c7ea64ee7215f7539e7432f3dcd5b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 18 Sep 2023 06:58:15 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
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
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247a0bb0fd023232a812150773a9216a7a3c9c79ce09ec1cc0a6dae41fede648`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 1.3 MB (1328077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c51778cba8a57ab7b5b0893b93f706b3fa0124bb656682274d41f8ccffc345`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5ac08d27ac93137ac5333b7b401b8fb78af3b2cc3d74f8e774bcb7273de077`  
		Last Modified: Wed, 08 Jan 2025 18:12:49 GMT  
		Size: 9.2 MB (9249269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74140cadac51e68cbba5f7a1cea6d9d7d6187634fd6e02709e06e94f2876557a`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:latest` - unknown; unknown

```console
$ docker pull teamspeak@sha256:02c63afa535a93b4a77d2f30b60c526e784dbd366ad64982034a0a96f090b03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02602b9c3f14b2dc8496f1edce6996f4f975b9e0094be1c770f6ea84fd1349d`

```dockerfile
```

-	Layers:
	-	`sha256:c4ef94ed0b530acdc00c4eee7d4a3b7f26974ceb00a57c173d8b08fa7f007b5b`  
		Last Modified: Wed, 08 Jan 2025 18:12:48 GMT  
		Size: 14.2 KB (14219 bytes)  
		MIME: application/vnd.in-toto+json
