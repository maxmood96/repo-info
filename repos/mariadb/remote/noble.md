## `mariadb:noble`

```console
$ docker pull mariadb@sha256:11706a6fd276c2eada52d0d69b1a2aa1f1484cbe78137678e02cca8f7a0ae502
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `mariadb:noble` - linux; amd64

```console
$ docker pull mariadb@sha256:6169f1cdbd27219c6789f517930d5f0483d7bb879ef6b3398eb053e8640758b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104928091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4815a3e162ea782e860dc3085f1b8583165ab2fc40958e48c6cdb1843a9cf561`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbf45358826d4e4d00ae28b2c595322b1ebdf74473585cb3e0856774a7b0b6`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ed3e3fde04f30f2fabafc4f825094d0e2dee8eec40c1781523f396e463a2d6`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 5.3 MB (5349410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b381eed6c88677ae6533bffa51f7fc49c06ef8ed0b8c1ef044a2097f74290a2`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7547f36e49715c784bfdc07472a6a57e03bd095f7b3c3c1d33e94aa060ffe8f`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e33262a388454af4c34c2b5165a00e629483269534c6a2e54b593c82b2a3c3`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 69.8 MB (69846914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3984aae8ebb430d1d164d5935584344c498927e6add738fe0d9bc2ed0205b72e`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 4.0 KB (4043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9883ef72c7c9df44f2a514ea30bc4e6cc9f10448adc00143577fe8a76ccababe`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 8.4 KB (8404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:419ba76b1594e7ab31821d192fab994fe029b14866f8e36db2fbe50a6b50cd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f51b0236a152d3de57a2b336268ab6a1e18f9e38424c6d3523c4753b38735b1`

```dockerfile
```

-	Layers:
	-	`sha256:06ef9241ec7b7675743bdcfe0c547347ded53751d9d6b44adae516605849939c`  
		Last Modified: Thu, 08 May 2025 18:54:34 GMT  
		Size: 4.1 MB (4081415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aced8a21cae5d40e7bccb23d2dc38054abee28aa0d706db3167d73e78a1dd0e8`  
		Last Modified: Thu, 08 May 2025 18:54:19 GMT  
		Size: 31.2 KB (31228 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5cdb6a7dd02b58321fc8c5f4b8489a7ca3d046f0513bcb1dbf65e19fdfc3938c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102865348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3508175435164c6ea6b50dec7800e49df7181a1117e4d1b3d63aa48009ec1924`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:1bafcbb31dbbcfab5d15f474524e7fdd408a80128ddb9f1743e9f39cfa86ce33 in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:2f074dc76c5da961ce13817b02fa1e3c3070ad4b94970aa7f52f6c0d63b07696`  
		Last Modified: Thu, 08 May 2025 17:04:47 GMT  
		Size: 28.8 MB (28846876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd9d703b6042193fc457d3a67a57618927beb52e43680cee068b2ef89b41baa`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2105ee6d42b1160939129ba741c606b58a4711580fd83e98551f3d6581a4e42e`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 5.1 MB (5130220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543485a1def59668d076bbe16d76d823ca65c2360392b4fcb168c63e9a6f1b92`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e839560ee9e4edf40e5e51511e9ed898038a40fa5fc0cbad7fc1f08f22bbb651`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b51dd454910b150497b8a80c53f31b8dc0faa5997dd7e9a24b007205718f4dc`  
		Last Modified: Thu, 08 May 2025 17:05:28 GMT  
		Size: 68.9 MB (68874013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d726755f6d3303a3a92f356d1e659d7c497995457a511b460bdd008cf685833`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dacd430fdd3b2ccd7bb72080db77b631e50550630638db11a0257243ddcdc5`  
		Last Modified: Thu, 08 May 2025 17:05:24 GMT  
		Size: 8.4 KB (8403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:78c3116b57aa44e7e4427e3e45dc202df0bd1c74006ca30e9ad8282194d59818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d156d8ffdf8dbcc15cb5a5ee315911e3108d96de4cc098d6907fa1555364ecfd`

```dockerfile
```

-	Layers:
	-	`sha256:ac2421e4f90be92e050dbdb41f7d547c5a09e89026a42a02f8db7d2c4d3f135a`  
		Last Modified: Thu, 08 May 2025 18:54:44 GMT  
		Size: 4.1 MB (4088688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da36e10b318761d212091bd65a51eeee8b6aedac38c959a1a9a6ff370cbd5fd4`  
		Last Modified: Thu, 08 May 2025 18:54:43 GMT  
		Size: 31.4 KB (31440 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:9c0efe71121ef59aa9ff48879ed2a5d4e2dd4fd4bc79387b8fef59b62d046cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.0 MB (115048043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f6a5ddcda30a823b7be806a98a61f6f2f40db232d872a0e6dadb6286d1a74f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:d4d363297b0bc97147d6215ececd915564f3540c035d4c68fcdd781acaf0e4e7 in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:fd7ce82c353803b69e06046e91345d15e766766fa395e4fb8e9f652834cddb32`  
		Last Modified: Thu, 08 May 2025 17:06:29 GMT  
		Size: 34.3 MB (34340838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e3a1c0b30c5466488617de16a792bc59cfb4240533d4a9d0b2ee319cd157de`  
		Last Modified: Thu, 08 May 2025 18:54:47 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205daf0c2e056e894e613ccfc60a1603e9f0efe65ade4cf53c1a83c704c1f2af`  
		Last Modified: Thu, 08 May 2025 18:54:49 GMT  
		Size: 5.9 MB (5913407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9f13295ae49ac8b31d830619752324f9d4f2596a0c0c83d979c8926feadbdb`  
		Last Modified: Thu, 08 May 2025 18:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bd6995fb8a55d3575c7a4b070740c4f980e6fdba4f91973f8933c46b273169`  
		Last Modified: Thu, 08 May 2025 18:54:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0bdaf30b0c08a6c2c955e293957873ddea7b3f7a5a4a4f2e88b6b0eb66d93f`  
		Last Modified: Thu, 08 May 2025 18:55:08 GMT  
		Size: 74.8 MB (74779562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab2674a2cc5a3d40b6e4b0d3d6990c6a2bde5a1b53cc48cba21f17c40b5352e`  
		Last Modified: Thu, 08 May 2025 18:54:48 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26d8e339556b59c803aefc31bc609528a5fbad747055d24c198585ac3e7552c`  
		Last Modified: Thu, 08 May 2025 18:54:49 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:9a8a67d9cc05805836c5228e7c17e452c869e2c81655712fc4e202c1a66d37ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a7a0969636b5cf28c3d9ba06d2bbf9fb1083e503e3aa25f398f18c08fe402c`

```dockerfile
```

-	Layers:
	-	`sha256:50f4099f2e406d3bef12a4936d513560a4c24799535368bc6423232c95492530`  
		Last Modified: Thu, 08 May 2025 18:55:15 GMT  
		Size: 4.1 MB (4089168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551a3ac2adde786d4cbecfaf2ab9d80a69563f29943b90b5a64697285b1eef22`  
		Last Modified: Thu, 08 May 2025 18:55:14 GMT  
		Size: 31.3 KB (31303 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:4869e00af85a227989115c9f347b9748d18942aa3a7dbc1d05102a8ab23ec493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110276995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787c7e44f96c69117b61eaaa324dc81ace703d180782349fea37b4a0c9db4d71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 14 Feb 2025 06:55:09 GMT
ARG RELEASE
# Fri, 14 Feb 2025 06:55:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 14 Feb 2025 06:55:09 GMT
ADD file:486993225aeae656f8d559f5c296f6c3164966e35f4b628d26e1da1b75592143 in / 
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["/bin/bash"]
# Fri, 14 Feb 2025 06:55:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV GOSU_VERSION=1.17
# Fri, 14 Feb 2025 06:55:09 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENV LANG=C.UTF-8
# Fri, 14 Feb 2025 06:55:09 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.7.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Feb 2025 06:55:09 GMT
ARG MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ENV MARIADB_VERSION=1:11.7.2+maria~ubu2404
# Fri, 14 Feb 2025 06:55:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.7.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.7.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Feb 2025 06:55:09 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Feb 2025 06:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Feb 2025 06:55:09 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Feb 2025 06:55:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:52a1750d5fddc355cdc90a83890b7d582c7f145aa5d114d9582cd010b8ead145`  
		Last Modified: Thu, 08 May 2025 17:05:48 GMT  
		Size: 30.0 MB (29956186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958384073f53f82757de78f2fd2e895877e2da75d97d4f43ff3f40c25064f7e7`  
		Last Modified: Thu, 08 May 2025 18:55:19 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ce21cfc12bf72b395c951a3fba3e8eac54bb5f0a7c8218deec06656a50d78b`  
		Last Modified: Thu, 08 May 2025 18:55:20 GMT  
		Size: 5.5 MB (5482943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2bbf586c5dc75b674ec4918cf5d81dcf00c528e1862120a9a6d9b4cc4b90b3`  
		Last Modified: Thu, 08 May 2025 18:55:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae19426e2ac76b9f846755efb32bd3c3f76e4848cc49406c2bc1dc3e3da8f199`  
		Last Modified: Thu, 08 May 2025 18:55:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416e0268867bce16af8a1dafe13aa7061759a56ae7ed4f008b0b40d391a550d4`  
		Last Modified: Thu, 08 May 2025 18:55:37 GMT  
		Size: 74.8 MB (74823626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa3c340ae2cea5546c33c637d54cbc33f0ec51d7383f9570ff654a21a26ab15`  
		Last Modified: Thu, 08 May 2025 18:55:20 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa08d361d75ca25d4c4890c9111c0751ddf7585db39e3fcbba147d73155b318`  
		Last Modified: Thu, 08 May 2025 18:55:21 GMT  
		Size: 8.4 KB (8404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:819f0127418b91bbe36b167848e4018b5d1d52f8493da26a8c7a5e925ba09865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4114366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709e348dda97c6494e14743703cb4c6334d3fe7906568545a59ec9ae0cb2e17c`

```dockerfile
```

-	Layers:
	-	`sha256:092686c1df6ad858eb2e84065d5c547a0c98840ffacd5d18adddf8c5f860e71b`  
		Last Modified: Thu, 08 May 2025 18:55:44 GMT  
		Size: 4.1 MB (4083138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e5ac1a4257d4291e5da20d0cce96ae8d2a1b47a92fd9738916efe94c209c8ea`  
		Last Modified: Thu, 08 May 2025 18:55:43 GMT  
		Size: 31.2 KB (31228 bytes)  
		MIME: application/vnd.in-toto+json
