## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:15acbc64c92f57ef1fd8dd203791fa7f70a14707e60ee494132f26b5ca265c6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:15ff29970f209b3c639162382130ac925035e57cffe22dba8e53f86189fb80e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.6 MB (14588824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcd763fd1adf802a0d21b87b0d5353ce00075786c9fd015c0f25b5aa430a9bb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:05 GMT
RUN set -eux;     apk add --no-cache ca-certificates libstdc++ su-exec libpq;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server TS3SERVER_FILETRANSFER_PORT=30033
# Mon, 22 Jun 2026 19:53:07 GMT
LABEL com.teamspeak.title=TeamSpeak 3 Server
# Mon, 22 Jun 2026 19:53:07 GMT
LABEL com.teamspeak.version=3.13.8
# Mon, 22 Jun 2026 19:53:07 GMT
LABEL com.teamspeak.description=TeamSpeak 3 Server on Alpine Linux
# Mon, 22 Jun 2026 19:53:07 GMT
ARG TEAMSPEAK_CHECKSUM=b04af5fbcbca3e847336389569eca3bff6339cba6f13f0151d6b012360e038ae
# Mon, 22 Jun 2026 19:53:07 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.8/teamspeak3-server_linux_alpine-3.13.8.tar.bz2
# Mon, 22 Jun 2026 19:53:07 GMT
# ARGS: TEAMSPEAK_CHECKSUM=b04af5fbcbca3e847336389569eca3bff6339cba6f13f0151d6b012360e038ae TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.8/teamspeak3-server_linux_alpine-3.13.8.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib;     rm -rf /opt/ts3server/redist # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
VOLUME [/var/ts3server/]
# Mon, 22 Jun 2026 19:53:07 GMT
WORKDIR /var/ts3server/
# Mon, 22 Jun 2026 19:53:07 GMT
EXPOSE map[10011/tcp:{} 30033/tcp:{} 9987/udp:{}]
# Mon, 22 Jun 2026 19:53:07 GMT
COPY entrypoint.sh /opt/ts3server # buildkit
# Mon, 22 Jun 2026 19:53:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Mon, 22 Jun 2026 19:53:07 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20450458b311eeea24386a9e674f7c9b792dc95ea3122e772cb66d8b9b7705b2`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 1.5 MB (1491119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9401b7d25013e1fe97735c3bbb4525ec55fc945ca13c3ac5b7e2cf3cc89566b`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 9.3 MB (9251700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa113739bb53453d412e3fdfdb21950fc2791258d9a129f3c60d331ec8ca1e4`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 1.6 KB (1552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `teamspeak:latest` - unknown; unknown

```console
$ docker pull teamspeak@sha256:d497ef473384fac18b54855c10fd4366afe9cf8dfb0efba7e72e54ad820f7957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.2 KB (13210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c630cf36fdb35df4140c4ab4038cbc256e8a81851cf4b3a51360895934e900`

```dockerfile
```

-	Layers:
	-	`sha256:00934ab82ad6f6ff5b1426368a98dcd8fc205025f1e301fe512d1ec4ea74a722`  
		Last Modified: Mon, 22 Jun 2026 19:53:12 GMT  
		Size: 13.2 KB (13210 bytes)  
		MIME: application/vnd.in-toto+json
