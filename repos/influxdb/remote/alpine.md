## `influxdb:alpine`

```console
$ docker pull influxdb@sha256:7cdfd116b08d0858766446468612a7d1b508f6eedda09167372c37e8b0abed29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:alpine` - linux; amd64

```console
$ docker pull influxdb@sha256:6f0508f1834cc0eeeba394618b9e3fac6c279cd83b46ef80f3c6569989a03851
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.6 MB (204556947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a00fe993fbb4c3a647e8a8d605112e71bf4ebcd9dd42ed3902ece5e5877a5cea`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:17:07 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:23:24 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:23:25 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:24:17 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:24 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:24:25 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:24:27 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:24:28 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:24:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:24:28 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:24:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:24:28 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:24:28 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:24:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:24:29 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b667f667e0d162df357cbdea46ee3457fd45395b451ccad50381f4665f8149`  
		Last Modified: Tue, 09 Aug 2022 18:18:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6402af9050b861838e26160dfa36debcd6dd6475ea0fd83bca7456ce75a5b625`  
		Last Modified: Mon, 22 Aug 2022 20:26:43 GMT  
		Size: 9.8 MB (9849332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25e48e1ebaf1c86c438b7e1a5c14b907d4df63562a822fbdc21e2463a6d2dbf`  
		Last Modified: Mon, 22 Aug 2022 20:26:41 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6090bd6322587c0389ad7e821fc1b220abaa84fea246f6fc17b8da6536b75e06`  
		Last Modified: Mon, 22 Aug 2022 20:28:02 GMT  
		Size: 185.8 MB (185802071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f074e0862a2ae8b98660ed0eab954a18e20ab7244bbad52291249de2dbbd21`  
		Last Modified: Mon, 22 Aug 2022 20:27:49 GMT  
		Size: 6.1 MB (6071078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d0edd1fdfd0ad366e3d01eca9ac9ddcde5cdbcc27823f5735bfbc7ab26dd39`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0ad10eabd449a6d520dd27ebeac3f5db06e0ec3b5ad83cbf321efbc3b663a0`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248077695501b84babac21af1f23c1fc9e595b111dffbb8657f9b00f90d95897`  
		Last Modified: Mon, 22 Aug 2022 20:27:48 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:alpine` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:aec00d1d3bdd04865834b2ce5efbf9eb0087dd974fbfda851c9edf17bcd86ca1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200461612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9316463e8a256e525078cb0fd4cc1f9a559a00caf6276cc33dbef40a980a9068`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:37:19 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 22 Aug 2022 20:40:08 GMT
RUN apk add --no-cache tzdata bash ca-certificates gnupg run-parts su-exec &&     update-ca-certificates
# Mon, 22 Aug 2022 20:40:09 GMT
RUN addgroup -S -g 1000 influxdb &&     adduser -S -G influxdb -u 1000 -h /home/influxdb -s /bin/sh influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Mon, 22 Aug 2022 20:42:00 GMT
ENV INFLUXDB_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:07 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2_linux_${ARCH}/influxd /usr/local/bin/influxd &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Mon, 22 Aug 2022 20:42:07 GMT
ENV INFLUX_CLI_VERSION=2.4.0
# Mon, 22 Aug 2022 20:42:10 GMT
RUN set -eux &&     ARCH="$(apk --print-arch)" &&     if [ ${ARCH} = x86_64 ]; then         ARCH=amd64;     elif [ ${ARCH} = aarch64 ]; then         ARCH=arm64;     else         echo "Unsupported architecture: ${ARCH}" && exit 1;     fi &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Mon, 22 Aug 2022 20:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Mon, 22 Aug 2022 20:42:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Mon, 22 Aug 2022 20:42:14 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 22 Aug 2022 20:42:15 GMT
COPY file:a6a402694185d5f58fa629116844ddbbc1c391c2cafad4c8077c27ee45de05a8 in /entrypoint.sh 
# Mon, 22 Aug 2022 20:42:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Aug 2022 20:42:16 GMT
CMD ["influxd"]
# Mon, 22 Aug 2022 20:42:17 GMT
EXPOSE 8086
# Mon, 22 Aug 2022 20:42:18 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 22 Aug 2022 20:42:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 22 Aug 2022 20:42:20 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 22 Aug 2022 20:42:21 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d115c2e84067616c51d32a9aa355071965e141dcaab8f8a8b3d26939dab269`  
		Last Modified: Tue, 09 Aug 2022 20:39:47 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c43c4a50852ded4220bf7f48c74a648463f1cbaa41d1e64945009b0ab04ab97c`  
		Last Modified: Mon, 22 Aug 2022 20:43:04 GMT  
		Size: 9.7 MB (9686496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8279c4c64bc9372a4413cb0c0b4a8fcec42038f48bceba1672521f1cf362a277`  
		Last Modified: Mon, 22 Aug 2022 20:43:02 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7297eb6832b83766a5181e62614f8bcb8e572cef2eaab4b32ea5164aff056eb9`  
		Last Modified: Mon, 22 Aug 2022 20:44:31 GMT  
		Size: 182.4 MB (182445450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a937fb0ab9fb1127943c02b2132570f00067589a6e9ad4f88e12b0f897227b`  
		Last Modified: Mon, 22 Aug 2022 20:44:17 GMT  
		Size: 5.6 MB (5600655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25361e1233670c2910e01baa942181c9bcecef679384f6176ef71c9052e1dde`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d265faea80360c2fc8079279fe00a752e7ca06dd60c3ccc9d9bb05e59dc1dd`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b117a445a9fe39c2069cc8b0d5818dc0a8f82a977ae2a05740bee4e09460cb`  
		Last Modified: Mon, 22 Aug 2022 20:44:16 GMT  
		Size: 5.0 KB (5018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
