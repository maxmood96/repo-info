## `influxdb:latest`

```console
$ docker pull influxdb@sha256:799aace0d410205ee8f37041acc6072ca4d5fff643119727a140d213f8ae44c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:a29e5df3e1cca465176376e64ee2e6ed0120f10ab04b330b5324faa22eed6daf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.9 MB (182886325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d67ab18943c7df0b5d0da16348608c3aa8eb6a5d54d21ac2a3c236a74927189`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:10 GMT
ADD file:28eba36c2d43c343d9dfd5ace80db0043e1f92aa3afb4aa95d6cbb54d7e6efef in / 
# Thu, 17 Mar 2022 04:04:11 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:32:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 08:55:58 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 19 Mar 2022 08:55:58 GMT
ENV GOSU_VER=1.12
# Sat, 19 Mar 2022 08:56:03 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Sat, 19 Mar 2022 08:56:34 GMT
ENV INFLUXDB_VERSION=2.1.1
# Sat, 19 Mar 2022 08:56:40 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Sat, 19 Mar 2022 08:56:40 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Sat, 19 Mar 2022 08:56:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Sat, 19 Mar 2022 08:56:45 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 19 Mar 2022 08:56:45 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 19 Mar 2022 08:56:45 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 19 Mar 2022 08:56:45 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Sat, 19 Mar 2022 08:56:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 08:56:45 GMT
CMD ["influxd"]
# Sat, 19 Mar 2022 08:56:45 GMT
EXPOSE 8086
# Sat, 19 Mar 2022 08:56:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 19 Mar 2022 08:56:45 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 19 Mar 2022 08:56:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 19 Mar 2022 08:56:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:7d66b83ec869a899bc8364af9c9eb0f1a5ba6907f699ef52f3182e19e2598924`  
		Last Modified: Thu, 17 Mar 2022 04:10:29 GMT  
		Size: 50.4 MB (50437294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88439e7b50a5f3923f67f432b6863c1e11adf4e45bf9740515d2cc01fd8e155`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 7.8 MB (7834140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22360a9558f73f04bb5e4dbe6dbe1584cb913040ae66388a8db66fc2ed131002`  
		Last Modified: Fri, 18 Mar 2022 07:04:47 GMT  
		Size: 10.0 MB (9997260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9d2c016e5c17deb8126e44153c5ba641cfc920a91ed6a5e11a669c544e02fe`  
		Last Modified: Sat, 19 Mar 2022 09:02:05 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f676b1914da4ce851ebca49deca0e782ff75c061dd08f73c41961196b6ac03f8`  
		Last Modified: Sat, 19 Mar 2022 09:02:03 GMT  
		Size: 961.0 KB (960964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fec6e1b6230576c5a7ba164c88e323a9c9a31a35b2b1dc32a469aa3e0836106`  
		Last Modified: Sat, 19 Mar 2022 09:02:48 GMT  
		Size: 108.3 MB (108324841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d103a21252e57304f7629ada34a8fa20a029aa543d776fb2441ed008a32da6b2`  
		Last Modified: Sat, 19 Mar 2022 09:02:41 GMT  
		Size: 5.3 MB (5324471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c306a07eeb6fd70d1ff7c64b17285949364b8134a40c1d1ef7bb4f07e8631f0e`  
		Last Modified: Sat, 19 Mar 2022 09:02:40 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c1726c8842101f5068807f0e578eb641c94902a76ac0955589c3ccef36b32d`  
		Last Modified: Sat, 19 Mar 2022 09:02:40 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f588dc4b1425218e636903757e933d54958e5166579505d6a00fe9d72712dc46`  
		Last Modified: Sat, 19 Mar 2022 09:02:40 GMT  
		Size: 5.0 KB (5012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:1de096d85e07563fde58e70656b71785f95932cc934b2f76e2b07d5192a4d840
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183387337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa46e52834181a5c7409d6cf0496f7a8bf7f54a936ad2eb29c8adc606f3a4621`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:08 GMT
ADD file:37cabd1fec04269c22fc158f62ce5bc655934f2e58fb1ff3a1e366a33ba9bc18 in / 
# Thu, 17 Mar 2022 03:22:09 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:12:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:10:41 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Sat, 19 Mar 2022 04:10:42 GMT
ENV GOSU_VER=1.12
# Sat, 19 Mar 2022 04:10:46 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Sat, 19 Mar 2022 04:11:16 GMT
ENV INFLUXDB_VERSION=2.1.1
# Sat, 19 Mar 2022 04:11:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influxd /usr/local/bin/influxd &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version
# Sat, 19 Mar 2022 04:11:29 GMT
ENV INFLUX_CLI_VERSION=2.2.1
# Sat, 19 Mar 2022 04:11:33 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}/influx /usr/local/bin/influx &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-client-${INFLUX_CLI_VERSION}-linux-${ARCH}* &&     influx version
# Sat, 19 Mar 2022 04:11:34 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Sat, 19 Mar 2022 04:11:35 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Sat, 19 Mar 2022 04:11:37 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Sat, 19 Mar 2022 04:11:38 GMT
COPY file:a64302f264563d538089431198a37bdc67423165f65d702bc1fe865140128cf1 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:11:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:11:39 GMT
CMD ["influxd"]
# Sat, 19 Mar 2022 04:11:40 GMT
EXPOSE 8086
# Sat, 19 Mar 2022 04:11:41 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Sat, 19 Mar 2022 04:11:42 GMT
ENV INFLUXD_INIT_PORT=9999
# Sat, 19 Mar 2022 04:11:43 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Sat, 19 Mar 2022 04:11:44 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:3996f04b7c6c17d8b25c04c7287353b896b4a0b10ab440f47d00573a7d5c3e17`  
		Last Modified: Thu, 17 Mar 2022 03:28:59 GMT  
		Size: 49.2 MB (49222993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80907b498681187ef4aa817ec6f39ba351e376afbb4fcf4415841ab9015cfc59`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 7.7 MB (7695349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8327dc7899c1a628cf11f95bb594fca3c86e45d1f4f0eb73d2ba9058eba5927`  
		Last Modified: Thu, 17 Mar 2022 22:22:15 GMT  
		Size: 9.8 MB (9767203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444eeb277652a3ac4ff0d84540a509c644cdf53587304b3cf527e6f63ad3af4d`  
		Last Modified: Sat, 19 Mar 2022 04:13:06 GMT  
		Size: 1.7 KB (1663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159d0fc7c44655b4f54d98daf50549faa19be0ae99d7b70b04906ca9262d4d8e`  
		Last Modified: Sat, 19 Mar 2022 04:13:04 GMT  
		Size: 896.3 KB (896338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ac9bfc5c9efe3c16232111ecb45ddbce1a26a960c87244ca416a1a08566426`  
		Last Modified: Sat, 19 Mar 2022 04:13:38 GMT  
		Size: 110.9 MB (110891609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745c2245c9f8827d2cae66e3c93ac8a5e69bfe5a533d4cb5f342ec87219ae468`  
		Last Modified: Sat, 19 Mar 2022 04:13:29 GMT  
		Size: 4.9 MB (4906725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eb5f55c031ecf1698fa52d24bcc7293768ec4b8354a9fcb027d7df82bcd29c`  
		Last Modified: Sat, 19 Mar 2022 04:13:28 GMT  
		Size: 209.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7c33b81b950f8a1a9022072b612f4c23fbe50467f65c51033c2e831bcd3b0f`  
		Last Modified: Sat, 19 Mar 2022 04:13:28 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721d2dd815280a880f5d95bd85e9bb025a5e6a013fed0c0872d3b93c362f0634`  
		Last Modified: Sat, 19 Mar 2022 04:13:28 GMT  
		Size: 5.0 KB (5014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
