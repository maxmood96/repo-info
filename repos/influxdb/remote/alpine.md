## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:037b9c0755493886bbc2638f1e1c7760fb82534c92731d6f0389a7af7933c52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:06308c0090faf779227b2a0057b48021cdf5b979bc675fb7e70d5ddf793f7c2e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127269412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3c34e321d28240dcdc466f99d27eaa497de4868fa297bd5b0d1b4d4c33ad63`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 18:05:42 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 19 Mar 2022 08:56:19 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Sat, 19 Mar 2022 08:56:20 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 19 Mar 2022 08:56:20 GMT
ENV GOSU_VER=1.12
# Sat, 19 Mar 2022 08:56:23 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 08:56:50 GMT
ENV INFLUXDB_VERSION=2.1.1
# Sat, 19 Mar 2022 08:56:56 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Sat, 19 Mar 2022 08:56:56 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Sat, 19 Mar 2022 08:56:59 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Sat, 19 Mar 2022 08:57:00 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 19 Mar 2022 08:57:00 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 19 Mar 2022 08:57:00 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 19 Mar 2022 08:57:00 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Sat, 19 Mar 2022 08:57:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 08:57:00 GMT
CMD ["influxd"]
# Sat, 19 Mar 2022 08:57:00 GMT
EXPOSE 8086
# Sat, 19 Mar 2022 08:57:00 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 19 Mar 2022 08:57:01 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 19 Mar 2022 08:57:01 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 19 Mar 2022 08:57:01 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa1326b35d047e371043a2411e65bd818c27909ab1ecf1ce37b55741744e890`  
		Last Modified: Thu, 17 Mar 2022 18:07:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d7448b2ddd8d77f4ff33830a3b6999154e9ad8524d87d2c68bd0b4d3b4a388`  
		Last Modified: Sat, 19 Mar 2022 09:02:26 GMT  
		Size: 9.8 MB (9836358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2c7a943976e02f6571ee342a1aa333db1e733ea9ba13bc2a9d4347c69c1b09`  
		Last Modified: Sat, 19 Mar 2022 09:02:24 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe0c4b4cfa9b6fe3d275579024680036078029c8c0e7c805cc5672657336a12`  
		Last Modified: Sat, 19 Mar 2022 09:02:22 GMT  
		Size: 960.6 KB (960606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8273224c835999f81b70b6478092ff8a5cf3c164b7cdc3c11e41a7a63c4c60`  
		Last Modified: Sat, 19 Mar 2022 09:03:09 GMT  
		Size: 108.3 MB (108324825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de22a8380e9706c9c21d9696ceac7bb845110af0da04c8ff382fcc5521e3387d`  
		Last Modified: Sat, 19 Mar 2022 09:03:02 GMT  
		Size: 5.3 MB (5324482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4121aab9803357f0d56cabfb46cc0597de95b01d0c3ce7e85db5324feea62c9`  
		Last Modified: Sat, 19 Mar 2022 09:03:01 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38e3f55ee8efeec4483ea2558aa6161b63726de238ca24403dda0aa85ec5242`  
		Last Modified: Sat, 19 Mar 2022 09:03:01 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66654efea0efd57f17a079e7845a2a8569f8b30d9ee124712e0cb9c6e30f9456`  
		Last Modified: Sat, 19 Mar 2022 09:03:01 GMT  
		Size: 5.0 KB (5014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4c877f8a2c150e13ebafd4dc5f23c3ff544dd3b27d3204d712ea970ba589253b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.1 MB (129088352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0f5e556eb1c21aa0769411d80b09b00a4aa94f5d4d356040b8f801e5cb23f36`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 18:43:12 GMT
ADD file:611998b78638b13e78919dd4635674032ab233f9b7aae6f62beaf6634cd18b9e in / 
# Thu, 17 Mar 2022 18:43:13 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 21:45:34 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 21:45:37 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts &&     update-ca-certificates
# Thu, 17 Mar 2022 21:45:38 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Thu, 17 Mar 2022 21:45:39 GMT
ENV GOSU_VER=1.12
# Thu, 17 Mar 2022 21:45:43 GMT
RUN set -eux;     ARCH="$(apk --print-arch)" &&     case "${ARCH}" in         x86_64)  ARCH=amd64;;         aarch64) ARCH=arm64;;         *)       echo "Unsupported architecture: ${ARCH}"; exit 1;;     esac && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$ARCH.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 17 Mar 2022 21:46:22 GMT
ENV INFLUXDB_VERSION=2.1.1
# Thu, 17 Mar 2022 21:46:31 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Thu, 17 Mar 2022 21:46:31 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Thu, 17 Mar 2022 21:46:35 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Thu, 17 Mar 2022 21:46:36 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 17 Mar 2022 21:46:37 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 17 Mar 2022 21:46:39 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Thu, 17 Mar 2022 21:46:40 GMT
COPY file:2bb0090d5bd94b26299db34eae2a7f9cc567840d43e1bba3e59b735fd488fc0d in /entrypoint.sh 
# Thu, 17 Mar 2022 21:46:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 21:46:41 GMT
CMD ["influxd"]
# Thu, 17 Mar 2022 21:46:42 GMT
EXPOSE 8086
# Thu, 17 Mar 2022 21:46:43 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Thu, 17 Mar 2022 21:46:44 GMT
ENV INFLUXD_INIT_PORT=9999
# Thu, 17 Mar 2022 21:46:45 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Thu, 17 Mar 2022 21:46:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:93a1719cf26168d3a85db2594d76b17ccc4b25996620bceed3c2a13eaa165325`  
		Last Modified: Thu, 17 Mar 2022 18:44:00 GMT  
		Size: 2.7 MB (2715888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d6f548bfb57cfbb8e8d5078c6c3547eb414eb279d6d3300aa72c08a98d1c1f`  
		Last Modified: Thu, 17 Mar 2022 21:47:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6088127ed14f76fbb1db6a94c3401b92985391d50ce952a595ee759532f1642`  
		Last Modified: Thu, 17 Mar 2022 21:47:31 GMT  
		Size: 9.7 MB (9671196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12b25f04973d7d96a4746853a0d99f81b48293a11bde2ef55bacdf141d2b263`  
		Last Modified: Thu, 17 Mar 2022 21:47:29 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb837ebacd1bd4d2fe6cf5d59bec128b95c872f0262aed1fc75a7b7cbd246311`  
		Last Modified: Thu, 17 Mar 2022 21:47:27 GMT  
		Size: 896.1 KB (896076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9889b1d4b2db737b8de23ad3d6a798a8b162c0c950ba0fdacd071a88c73db7c`  
		Last Modified: Thu, 17 Mar 2022 21:48:00 GMT  
		Size: 110.9 MB (110891612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd6abdcc677e87d85932c1077f05a7e46a30264f32c0165aab0fcc617ebe367`  
		Last Modified: Thu, 17 Mar 2022 21:47:51 GMT  
		Size: 4.9 MB (4906728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1a9da7f35fd510aee9f2cfe8ab4b54015b58e1ef8c50cc5886089a67503276`  
		Last Modified: Thu, 17 Mar 2022 21:47:50 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e6dc9aa2d0fcd0470d0eeecbf073985ad962003508931a174c77574b038bce`  
		Last Modified: Thu, 17 Mar 2022 21:47:50 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e996072f9a7d100d91d743e0d0a33e81df6c2629b43057d4dd4181cc98163443`  
		Last Modified: Thu, 17 Mar 2022 21:47:50 GMT  
		Size: 5.0 KB (5017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
