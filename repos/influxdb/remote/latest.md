## `influxdb:latest`

```console
$ docker pull influxdb@sha256:d20893f055bb937d2071a40f1fe4b8b9cdcc6376763d5d1d1e9ca54f1bff8aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:194407d7191e84a6c69f9edc16e1493179241bf1600d366d4975229fee3e038f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172325295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e63af069cd6e36536b6451ce0675104e5a5ec4c5e7fd176297e185bf37a686`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 01:51:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 01:51:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 29 Sep 2021 06:27:51 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Wed, 29 Sep 2021 06:27:51 GMT
ENV GOSU_VER=1.12
# Wed, 29 Sep 2021 06:27:55 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Tue, 05 Oct 2021 17:39:16 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 05 Oct 2021 17:39:26 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 05 Oct 2021 17:39:27 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Oct 2021 17:39:28 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Oct 2021 17:39:28 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Oct 2021 17:39:28 GMT
COPY file:d7feb20b951141d711981be8e82cc1301ac374a4bdcd763025f350ecad4e1f75 in /entrypoint.sh 
# Tue, 05 Oct 2021 17:39:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Oct 2021 17:39:29 GMT
CMD ["influxd"]
# Tue, 05 Oct 2021 17:39:29 GMT
EXPOSE 8086
# Tue, 05 Oct 2021 17:39:29 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Oct 2021 17:39:29 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Oct 2021 17:39:29 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Oct 2021 17:39:30 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd67d668d6911bf21ad4701522e1ed3af416837433fdba3f88cff06a23e23861`  
		Last Modified: Tue, 28 Sep 2021 01:59:09 GMT  
		Size: 7.8 MB (7833602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae016bc26876abbd5e952133b02b04d4c1dae1bc75a3d9386250e4797ccd87a`  
		Last Modified: Tue, 28 Sep 2021 01:59:09 GMT  
		Size: 10.0 MB (9997190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c929756af316d40810a0b10a60961acc9de8d603ed050710a7e894689a1e17a`  
		Last Modified: Wed, 29 Sep 2021 06:31:25 GMT  
		Size: 1.8 KB (1806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9186926ca7015fa3f6b798752ddfc1a42db9763e43500bc8e5de9fff7b92522d`  
		Last Modified: Wed, 29 Sep 2021 06:31:22 GMT  
		Size: 961.0 KB (960989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe55f2d8f25daf887add134b4dea1131e5920cd052ab48276ac168b61024a75b`  
		Last Modified: Tue, 05 Oct 2021 17:40:58 GMT  
		Size: 103.1 MB (103090642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c79ed64c23c171a2a780be71df757f8d1c8be1392c4fd5f408bc130bfeb2aae`  
		Last Modified: Tue, 05 Oct 2021 17:40:49 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad642110b70ade9dce6fb304dfaae9419b9ecaf713be4e2088a683d3f79bb10`  
		Last Modified: Tue, 05 Oct 2021 17:40:49 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086844e7c60e63f32c18b42782910fbb25b11cfb88365b78838a8835cc0cabfe`  
		Last Modified: Tue, 05 Oct 2021 17:40:49 GMT  
		Size: 4.3 KB (4323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:4e56d7ae7e306c8d54463b43bd0cc0603a97295a5987309dd6b8d576ddaa083e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174332651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048ac864884959d98cc21955b72b2005681becdabbbc0b9a386ebf1b665d4155`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Tue, 28 Sep 2021 01:40:56 GMT
ADD file:51975e5f400da759b2cd8f7eba13ad61dd4edbbee0d0fac09b697bfa039d1515 in / 
# Tue, 28 Sep 2021 01:40:57 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 02:17:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 02:17:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 28 Sep 2021 21:58:31 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Tue, 28 Sep 2021 21:58:31 GMT
ENV GOSU_VER=1.12
# Tue, 28 Sep 2021 21:58:34 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Tue, 05 Oct 2021 00:39:59 GMT
ENV INFLUXDB_VERSION=2.0.9
# Tue, 05 Oct 2021 00:40:11 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Tue, 05 Oct 2021 00:40:12 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Tue, 05 Oct 2021 00:40:12 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Tue, 05 Oct 2021 00:40:12 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Tue, 05 Oct 2021 00:40:12 GMT
COPY file:d7feb20b951141d711981be8e82cc1301ac374a4bdcd763025f350ecad4e1f75 in /entrypoint.sh 
# Tue, 05 Oct 2021 00:40:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 05 Oct 2021 00:40:13 GMT
CMD ["influxd"]
# Tue, 05 Oct 2021 00:40:13 GMT
EXPOSE 8086
# Tue, 05 Oct 2021 00:40:13 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Tue, 05 Oct 2021 00:40:13 GMT
ENV INFLUXD_INIT_PORT=9999
# Tue, 05 Oct 2021 00:40:13 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Tue, 05 Oct 2021 00:40:14 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:70fe10514d0290bd1e8986c0fd63a67204813d37fc5863cf9bf8bf61b2031537`  
		Last Modified: Tue, 28 Sep 2021 01:48:53 GMT  
		Size: 49.2 MB (49222381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9679d540d5f2659fa72eaa9fa11dc318510dc1e7795eab1bc39295855a03d1d0`  
		Last Modified: Tue, 28 Sep 2021 02:26:00 GMT  
		Size: 7.7 MB (7695855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052683e57413fa9352045785beb2e5728edac5063c3b899145698f812b5fb903`  
		Last Modified: Tue, 28 Sep 2021 02:26:00 GMT  
		Size: 10.0 MB (9984315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fbdf4c46d6c97c0f3af3092d2060290dad9a1fd542b91c4e8790cad0c7381d`  
		Last Modified: Tue, 28 Sep 2021 22:00:03 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a8253f6adc5ce3b687e412c769d37cdd7576a45eb3a86e8950210ab1d4d427`  
		Last Modified: Tue, 28 Sep 2021 22:00:00 GMT  
		Size: 896.4 KB (896379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f6e5daeeb4f0987916be588e5df6b582e80a7d588af38c081c9fd0ff753afb`  
		Last Modified: Tue, 05 Oct 2021 00:41:16 GMT  
		Size: 106.5 MB (106527052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2dd575eea52432344d4ed259dc5512ae195bd265cad024ed206aad92977438`  
		Last Modified: Tue, 05 Oct 2021 00:41:04 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072eea4819167ce610a410f2c1add4ecc36c5b4ebb5b2aed99ca18ee0ab6f295`  
		Last Modified: Tue, 05 Oct 2021 00:41:04 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3a246b2dc644132f7b437f032890b29f733117925801c763a1813eac8a65c3`  
		Last Modified: Tue, 05 Oct 2021 00:41:04 GMT  
		Size: 4.3 KB (4324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
