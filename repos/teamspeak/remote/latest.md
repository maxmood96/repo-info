## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:10499180e88f24170812e12b34083332a7573ae35a4becba5d7a85d9761050e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:ea9ea3efb3f340bb57d72190a3e59eb6df00a5cba42a5efcd20c0170fc1166de
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13992466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a55cbd47c33124de53529cbd03012613bc84996891e61507c95417ada0a8f5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:36:28 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec libpq
# Fri, 21 Jun 2024 02:36:29 GMT
RUN set -eux;     addgroup -g 9987 ts3server;     adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;     install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Fri, 21 Jun 2024 02:36:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Fri, 21 Jun 2024 02:36:29 GMT
ARG TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e
# Fri, 21 Jun 2024 02:36:29 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
# Fri, 21 Jun 2024 02:36:32 GMT
# ARGS: TEAMSPEAK_CHECKSUM=359aac972679cfd98d62af51ddaf80e674cab166e13c6a835e81759097f9ba2e TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.13.7/teamspeak3-server_linux_alpine-3.13.7.tar.bz2
RUN set -eux;     apk add --no-cache --virtual .fetch-deps tar;     wget "${TEAMSPEAK_URL}" -O server.tar.bz2;     echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;     mkdir -p /opt/ts3server;     tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;     rm server.tar.bz2;     apk del .fetch-deps;     mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;     ldconfig /usr/local/lib
# Fri, 21 Jun 2024 02:36:33 GMT
VOLUME [/var/ts3server/]
# Fri, 21 Jun 2024 02:36:33 GMT
WORKDIR /var/ts3server/
# Fri, 21 Jun 2024 02:36:33 GMT
EXPOSE 10011 30033 9987/udp
# Fri, 21 Jun 2024 02:36:33 GMT
COPY file:d9f653f53e40ea33be02ca61f8194eb1a4147066050f721a3172007f06bb834c in /opt/ts3server 
# Fri, 21 Jun 2024 02:36:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 21 Jun 2024 02:36:33 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c71af0382830e5af9f52219002f81fd453e0e7730bc084545c2fbca7ac39c8c`  
		Last Modified: Fri, 21 Jun 2024 02:36:42 GMT  
		Size: 1.3 MB (1326483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e431479bf5cb0766b10e52742903bcd19ee366c8b421c5ad68eb8afc2eb3e0ab`  
		Last Modified: Fri, 21 Jun 2024 02:36:41 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec099790e5d566b1050f65bdd899b46bbc12c8bbbfb9a2d8a3b82420362396ba`  
		Last Modified: Fri, 21 Jun 2024 02:36:43 GMT  
		Size: 9.2 MB (9249248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1015e208cc3d355565eea16ea72c2bb6bd33d11666b9bd4b67ac95cd856153`  
		Last Modified: Fri, 21 Jun 2024 02:36:42 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
