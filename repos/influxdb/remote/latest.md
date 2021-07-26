## `influxdb:latest`

```console
$ docker pull influxdb@sha256:085d0a0f2a627ac22586305772e20e4c390cd1e4dd95daa7923f5144638c3f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `influxdb:latest` - linux; amd64

```console
$ docker pull influxdb@sha256:e838ddbcc17920f8694d33c014d26208e30e18c77548e11fb1e6157eeaf746c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178699675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d636ad7ee210123228a7815b07cac9bfa682fba8e2baa59ceefbcf36cae7a0b7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:12:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:12:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 23 Jul 2021 02:11:48 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Fri, 23 Jul 2021 02:11:48 GMT
ENV GOSU_VER=1.12
# Fri, 23 Jul 2021 02:11:52 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Fri, 23 Jul 2021 02:11:52 GMT
ENV INFLUXDB_VERSION=2.0.7
# Fri, 23 Jul 2021 02:12:04 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Fri, 23 Jul 2021 02:12:05 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Fri, 23 Jul 2021 02:12:06 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Fri, 23 Jul 2021 02:12:06 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 26 Jul 2021 18:38:18 GMT
COPY file:d7feb20b951141d711981be8e82cc1301ac374a4bdcd763025f350ecad4e1f75 in /entrypoint.sh 
# Mon, 26 Jul 2021 18:38:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Jul 2021 18:38:18 GMT
CMD ["influxd"]
# Mon, 26 Jul 2021 18:38:19 GMT
EXPOSE 8086
# Mon, 26 Jul 2021 18:38:19 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 26 Jul 2021 18:38:19 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 26 Jul 2021 18:38:19 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 26 Jul 2021 18:38:19 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c040670e5e559fd936db175530ad4c1dd014bd25b2bf25ea19fa20554fe2d736`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:073a180f4992853fa3dd8da604e7b041bc8ea92157749d042c0853312f178f6a`  
		Last Modified: Thu, 22 Jul 2021 01:19:54 GMT  
		Size: 10.0 MB (9997222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5dd72bb5822c84767458713b69fb93494a51e0f356be877980108a66b5edb4`  
		Last Modified: Fri, 23 Jul 2021 02:15:55 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43d73623c47956e65cca3ea8e1026b64b571a193a561279f59aec4161aaabe`  
		Last Modified: Fri, 23 Jul 2021 02:15:52 GMT  
		Size: 961.0 KB (960993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228da6afce0c88cf244531ea9865dcdca910ac701fec49cca3e18065cdf3b23c`  
		Last Modified: Fri, 23 Jul 2021 02:16:04 GMT  
		Size: 109.5 MB (109466222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87372622f1cae336a495dc753b4dc4c32a032e4dc6f6b0b50d52b9976ebfb155`  
		Last Modified: Fri, 23 Jul 2021 02:15:52 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c702d2aa14b6d7e01a8839c634c18c42ad26a8e7f6c5ba2e7527dc148f95db`  
		Last Modified: Fri, 23 Jul 2021 02:15:52 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a4dbf9bcd62203c3ae84d2eb1ba21d75314fd0891c7fd715880440716a7ae8`  
		Last Modified: Mon, 26 Jul 2021 18:39:29 GMT  
		Size: 4.3 KB (4324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `influxdb:latest` - linux; arm64 variant v8

```console
$ docker pull influxdb@sha256:3803e388276670ef3309e4bf628a7ac1f6ccc653c5097dc21be7b5fcdea92242
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180628903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6278f2ebb5f13314938ae066bd408a55c0a18d747ff135144ff4d1e2823888a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["influxd"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:59 GMT
ADD file:3e8e075f08a6b727602af05c539f43648a48663cbb3a88eeba310cfc32c01d78 in / 
# Thu, 22 Jul 2021 00:40:00 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 01:15:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 01:16:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 22 Jul 2021 13:29:57 GMT
RUN groupadd -r influxdb --gid=1000 &&     useradd -r -g influxdb --uid=1000 --home-dir=/home/influxdb --shell=/bin/bash influxdb &&     mkdir -p /home/influxdb &&     chown -R influxdb:influxdb /home/influxdb
# Thu, 22 Jul 2021 13:29:58 GMT
ENV GOSU_VER=1.12
# Thu, 22 Jul 2021 13:30:00 GMT
RUN set -eux; 	dpkgArch="$(dpkg --print-architecture)" && 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch" && 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VER/gosu-$dpkgArch.asc" && 	export GNUPGHOME="$(mktemp -d)" && 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 && 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu && 	gpgconf --kill all && 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc && 	chmod +x /usr/local/bin/gosu && 	gosu --version && 	gosu nobody true
# Thu, 22 Jul 2021 13:30:01 GMT
ENV INFLUXDB_VERSION=2.0.7
# Thu, 22 Jul 2021 13:30:07 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/influxdb/releases/influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver keys.openpgp.org --recv-keys 8C2D403D3C3BDB81A4C27C883C3E4B7317FFE40A &&     gpg --batch --verify influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz.asc influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     tar xzf influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}.tar.gz &&     cp influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}/influx* /usr/local/bin/ &&     rm -rf "$GNUPGHOME" influxdb2.key influxdb2-${INFLUXDB_VERSION}-linux-${ARCH}* &&     influxd version &&     influx version
# Thu, 22 Jul 2021 13:30:08 GMT
RUN mkdir /docker-entrypoint-initdb.d &&     mkdir -p /var/lib/influxdb2 &&     chown -R influxdb:influxdb /var/lib/influxdb2 &&     mkdir -p /etc/influxdb2 &&     chown -R influxdb:influxdb /etc/influxdb2
# Thu, 22 Jul 2021 13:30:09 GMT
VOLUME [/var/lib/influxdb2 /etc/influxdb2]
# Thu, 22 Jul 2021 13:30:09 GMT
COPY file:77129326da9464dfa98aab4911582df608de5d5bf6a6f6ed89619b704cac95bc in /etc/defaults/influxdb2/config.yml 
# Mon, 26 Jul 2021 18:39:45 GMT
COPY file:d7feb20b951141d711981be8e82cc1301ac374a4bdcd763025f350ecad4e1f75 in /entrypoint.sh 
# Mon, 26 Jul 2021 18:39:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 26 Jul 2021 18:39:45 GMT
CMD ["influxd"]
# Mon, 26 Jul 2021 18:39:45 GMT
EXPOSE 8086
# Mon, 26 Jul 2021 18:39:45 GMT
ENV INFLUX_CONFIGS_PATH=/etc/influxdb2/influx-configs
# Mon, 26 Jul 2021 18:39:46 GMT
ENV INFLUXD_INIT_PORT=9999
# Mon, 26 Jul 2021 18:39:46 GMT
ENV INFLUXD_INIT_PING_ATTEMPTS=600
# Mon, 26 Jul 2021 18:39:46 GMT
ENV DOCKER_INFLUXDB_INIT_CLI_CONFIG_NAME=default
```

-	Layers:
	-	`sha256:d272b0d8f7c4fd0caf0ef022ce544cfe3800e349a73b585f82837e6526a4247e`  
		Last Modified: Thu, 22 Jul 2021 00:45:18 GMT  
		Size: 49.2 MB (49222109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fabd82f026fa10e0e0341fa3d6d3112de04413ea6c46e72bcc1dca40d924aa`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 7.7 MB (7694906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0193c0cdceae23cd0e13721651d74f409440171fe8a1c8b521616b6ed29db6e1`  
		Last Modified: Thu, 22 Jul 2021 01:25:00 GMT  
		Size: 10.0 MB (9984335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72025b507cdae151c0b6a15a41fc8edf704ecb19e502485346c7efeeb73aea4`  
		Last Modified: Thu, 22 Jul 2021 13:31:29 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1240e5da131e2c54a018863ff5eb49a86e2b22437b0d25b035be16fa8a59526e`  
		Last Modified: Thu, 22 Jul 2021 13:31:27 GMT  
		Size: 896.4 KB (896377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97aadc627e70699960e6ebed86dd1809bd50b303034c2ade33dbcd582940808b`  
		Last Modified: Thu, 22 Jul 2021 13:31:38 GMT  
		Size: 112.8 MB (112824502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7781af78b62eafae4d636eb5636556c7d66b78778ae728b8652db9f66bc6e5af`  
		Last Modified: Thu, 22 Jul 2021 13:31:26 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9660237b9a4fb416294ffd8e4bd29d9e2b573799f503d2f7ec30aeeeaf40933`  
		Last Modified: Thu, 22 Jul 2021 13:31:26 GMT  
		Size: 260.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9f4dae3922518234a011458f3fcf435eb7d8a9d91ac8b9477e4aaa6de23bc25`  
		Last Modified: Mon, 26 Jul 2021 18:40:28 GMT  
		Size: 4.3 KB (4325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
