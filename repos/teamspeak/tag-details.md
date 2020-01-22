<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `teamspeak`

-	[`teamspeak:3.11`](#teamspeak311)
-	[`teamspeak:3.11.0`](#teamspeak3110)
-	[`teamspeak:latest`](#teamspeaklatest)

## `teamspeak:3.11`

```console
$ docker pull teamspeak@sha256:f3e22772e6c76051e3eb6ecb5ecee3269f1b76cbf3fa4367416f064770fc56d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `teamspeak:3.11` - linux; amd64

```console
$ docker pull teamspeak@sha256:ace78226aa651ec02d0ca2298f14bfa704559e8adb2e3deb1580ab7651833216
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85aeeaf7686929b3ababb7d6bf5a7c74274e62b0185ffd90e1c2787cf894e15`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2019 23:24:05 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec
# Wed, 22 Jan 2020 04:59:22 GMT
RUN set -eux;  addgroup -g 9987 ts3server;  adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;  install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Wed, 22 Jan 2020 04:59:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Wed, 22 Jan 2020 04:59:23 GMT
ARG TEAMSPEAK_CHECKSUM=f93e96b556e11fc7b520416b6a22cde902ae12ef14a7f99b0107cde97ce48fc6
# Wed, 22 Jan 2020 04:59:23 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_alpine-3.11.0.tar.bz2
# Wed, 22 Jan 2020 04:59:27 GMT
# ARGS: TEAMSPEAK_CHECKSUM=f93e96b556e11fc7b520416b6a22cde902ae12ef14a7f99b0107cde97ce48fc6 TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_alpine-3.11.0.tar.bz2
RUN set -eux;  apk add --no-cache --virtual .fetch-deps tar;  wget "${TEAMSPEAK_URL}" -O server.tar.bz2;  echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;  mkdir -p /opt/ts3server;  tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;  rm server.tar.bz2;  apk del .fetch-deps;  mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;  ldconfig /usr/local/lib
# Wed, 22 Jan 2020 04:59:27 GMT
VOLUME [/var/ts3server/]
# Wed, 22 Jan 2020 04:59:28 GMT
WORKDIR /var/ts3server/
# Wed, 22 Jan 2020 04:59:28 GMT
EXPOSE 10011 30033 9987/udp
# Wed, 22 Jan 2020 04:59:28 GMT
COPY file:6d1cf26aa3141617a27d9a975d3a4ef216e03df89fc20159d5734f178aab0e88 in /opt/ts3server 
# Wed, 22 Jan 2020 04:59:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 22 Jan 2020 04:59:29 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7ed9f66ae44d575a13f839b900f53b39138cea0eee9b80098bf458e108f3f8`  
		Last Modified: Mon, 11 Nov 2019 23:24:20 GMT  
		Size: 763.2 KB (763196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ec2bcd5b6b55e2f92bf706522780e37aef8b5476e4d352e23ac1f7d75d3bbe`  
		Last Modified: Wed, 22 Jan 2020 04:59:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec277e70bdcbc20dd2bc2c69035afd50793b6eb255c2a48267e4624326706268`  
		Last Modified: Wed, 22 Jan 2020 04:59:37 GMT  
		Size: 8.7 MB (8745605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1d851b342328e9f9ffe0a42a93514640eec05fce9525b00fddb41f619f209f`  
		Last Modified: Wed, 22 Jan 2020 04:59:35 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `teamspeak:3.11.0`

```console
$ docker pull teamspeak@sha256:f3e22772e6c76051e3eb6ecb5ecee3269f1b76cbf3fa4367416f064770fc56d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `teamspeak:3.11.0` - linux; amd64

```console
$ docker pull teamspeak@sha256:ace78226aa651ec02d0ca2298f14bfa704559e8adb2e3deb1580ab7651833216
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85aeeaf7686929b3ababb7d6bf5a7c74274e62b0185ffd90e1c2787cf894e15`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2019 23:24:05 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec
# Wed, 22 Jan 2020 04:59:22 GMT
RUN set -eux;  addgroup -g 9987 ts3server;  adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;  install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Wed, 22 Jan 2020 04:59:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Wed, 22 Jan 2020 04:59:23 GMT
ARG TEAMSPEAK_CHECKSUM=f93e96b556e11fc7b520416b6a22cde902ae12ef14a7f99b0107cde97ce48fc6
# Wed, 22 Jan 2020 04:59:23 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_alpine-3.11.0.tar.bz2
# Wed, 22 Jan 2020 04:59:27 GMT
# ARGS: TEAMSPEAK_CHECKSUM=f93e96b556e11fc7b520416b6a22cde902ae12ef14a7f99b0107cde97ce48fc6 TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_alpine-3.11.0.tar.bz2
RUN set -eux;  apk add --no-cache --virtual .fetch-deps tar;  wget "${TEAMSPEAK_URL}" -O server.tar.bz2;  echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;  mkdir -p /opt/ts3server;  tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;  rm server.tar.bz2;  apk del .fetch-deps;  mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;  ldconfig /usr/local/lib
# Wed, 22 Jan 2020 04:59:27 GMT
VOLUME [/var/ts3server/]
# Wed, 22 Jan 2020 04:59:28 GMT
WORKDIR /var/ts3server/
# Wed, 22 Jan 2020 04:59:28 GMT
EXPOSE 10011 30033 9987/udp
# Wed, 22 Jan 2020 04:59:28 GMT
COPY file:6d1cf26aa3141617a27d9a975d3a4ef216e03df89fc20159d5734f178aab0e88 in /opt/ts3server 
# Wed, 22 Jan 2020 04:59:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 22 Jan 2020 04:59:29 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7ed9f66ae44d575a13f839b900f53b39138cea0eee9b80098bf458e108f3f8`  
		Last Modified: Mon, 11 Nov 2019 23:24:20 GMT  
		Size: 763.2 KB (763196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ec2bcd5b6b55e2f92bf706522780e37aef8b5476e4d352e23ac1f7d75d3bbe`  
		Last Modified: Wed, 22 Jan 2020 04:59:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec277e70bdcbc20dd2bc2c69035afd50793b6eb255c2a48267e4624326706268`  
		Last Modified: Wed, 22 Jan 2020 04:59:37 GMT  
		Size: 8.7 MB (8745605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1d851b342328e9f9ffe0a42a93514640eec05fce9525b00fddb41f619f209f`  
		Last Modified: Wed, 22 Jan 2020 04:59:35 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `teamspeak:latest`

```console
$ docker pull teamspeak@sha256:f3e22772e6c76051e3eb6ecb5ecee3269f1b76cbf3fa4367416f064770fc56d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `teamspeak:latest` - linux; amd64

```console
$ docker pull teamspeak@sha256:ace78226aa651ec02d0ca2298f14bfa704559e8adb2e3deb1580ab7651833216
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.3 MB (12298797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85aeeaf7686929b3ababb7d6bf5a7c74274e62b0185ffd90e1c2787cf894e15`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["ts3server"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Mon, 11 Nov 2019 23:24:05 GMT
RUN apk add --no-cache ca-certificates libstdc++ su-exec
# Wed, 22 Jan 2020 04:59:22 GMT
RUN set -eux;  addgroup -g 9987 ts3server;  adduser -u 9987 -Hh /var/ts3server -G ts3server -s /sbin/nologin -D ts3server;  install -d -o ts3server -g ts3server -m 775 /var/ts3server /var/run/ts3server /opt/ts3server
# Wed, 22 Jan 2020 04:59:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/ts3server
# Wed, 22 Jan 2020 04:59:23 GMT
ARG TEAMSPEAK_CHECKSUM=f93e96b556e11fc7b520416b6a22cde902ae12ef14a7f99b0107cde97ce48fc6
# Wed, 22 Jan 2020 04:59:23 GMT
ARG TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_alpine-3.11.0.tar.bz2
# Wed, 22 Jan 2020 04:59:27 GMT
# ARGS: TEAMSPEAK_CHECKSUM=f93e96b556e11fc7b520416b6a22cde902ae12ef14a7f99b0107cde97ce48fc6 TEAMSPEAK_URL=https://files.teamspeak-services.com/releases/server/3.11.0/teamspeak3-server_linux_alpine-3.11.0.tar.bz2
RUN set -eux;  apk add --no-cache --virtual .fetch-deps tar;  wget "${TEAMSPEAK_URL}" -O server.tar.bz2;  echo "${TEAMSPEAK_CHECKSUM} *server.tar.bz2" | sha256sum -c -;  mkdir -p /opt/ts3server;  tar -xf server.tar.bz2 --strip-components=1 -C /opt/ts3server;  rm server.tar.bz2;  apk del .fetch-deps;  mv /opt/ts3server/*.so /opt/ts3server/redist/* /usr/local/lib;  ldconfig /usr/local/lib
# Wed, 22 Jan 2020 04:59:27 GMT
VOLUME [/var/ts3server/]
# Wed, 22 Jan 2020 04:59:28 GMT
WORKDIR /var/ts3server/
# Wed, 22 Jan 2020 04:59:28 GMT
EXPOSE 10011 30033 9987/udp
# Wed, 22 Jan 2020 04:59:28 GMT
COPY file:6d1cf26aa3141617a27d9a975d3a4ef216e03df89fc20159d5734f178aab0e88 in /opt/ts3server 
# Wed, 22 Jan 2020 04:59:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 22 Jan 2020 04:59:29 GMT
CMD ["ts3server"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7ed9f66ae44d575a13f839b900f53b39138cea0eee9b80098bf458e108f3f8`  
		Last Modified: Mon, 11 Nov 2019 23:24:20 GMT  
		Size: 763.2 KB (763196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ec2bcd5b6b55e2f92bf706522780e37aef8b5476e4d352e23ac1f7d75d3bbe`  
		Last Modified: Wed, 22 Jan 2020 04:59:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec277e70bdcbc20dd2bc2c69035afd50793b6eb255c2a48267e4624326706268`  
		Last Modified: Wed, 22 Jan 2020 04:59:37 GMT  
		Size: 8.7 MB (8745605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1d851b342328e9f9ffe0a42a93514640eec05fce9525b00fddb41f619f209f`  
		Last Modified: Wed, 22 Jan 2020 04:59:35 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
