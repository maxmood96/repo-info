<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-jammy`](#mariadb10-jammy)
-	[`mariadb:10.11`](#mariadb1011)
-	[`mariadb:10.11-jammy`](#mariadb1011-jammy)
-	[`mariadb:10.11.7`](#mariadb10117)
-	[`mariadb:10.11.7-jammy`](#mariadb10117-jammy)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.33`](#mariadb10433)
-	[`mariadb:10.4.33-focal`](#mariadb10433-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.24`](#mariadb10524)
-	[`mariadb:10.5.24-focal`](#mariadb10524-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.17`](#mariadb10617)
-	[`mariadb:10.6.17-focal`](#mariadb10617-focal)
-	[`mariadb:11`](#mariadb11)
-	[`mariadb:11-jammy`](#mariadb11-jammy)
-	[`mariadb:11.0`](#mariadb110)
-	[`mariadb:11.0-jammy`](#mariadb110-jammy)
-	[`mariadb:11.0.5`](#mariadb1105)
-	[`mariadb:11.0.5-jammy`](#mariadb1105-jammy)
-	[`mariadb:11.1`](#mariadb111)
-	[`mariadb:11.1-jammy`](#mariadb111-jammy)
-	[`mariadb:11.1.4`](#mariadb1114)
-	[`mariadb:11.1.4-jammy`](#mariadb1114-jammy)
-	[`mariadb:11.2`](#mariadb112)
-	[`mariadb:11.2-jammy`](#mariadb112-jammy)
-	[`mariadb:11.2.3`](#mariadb1123)
-	[`mariadb:11.2.3-jammy`](#mariadb1123-jammy)
-	[`mariadb:11.3-rc`](#mariadb113-rc)
-	[`mariadb:11.3-rc-jammy`](#mariadb113-rc-jammy)
-	[`mariadb:11.3.1-rc`](#mariadb1131-rc)
-	[`mariadb:11.3.1-rc-jammy`](#mariadb1131-rc-jammy)
-	[`mariadb:jammy`](#mariadbjammy)
-	[`mariadb:latest`](#mariadblatest)
-	[`mariadb:lts`](#mariadblts)
-	[`mariadb:lts-jammy`](#mariadblts-jammy)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:d1a4db6dd5fcf9f568037d1b9cdd405bd8148d56d1e36a7f06c9b993e9476d9e
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

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:9b9b57e1318bb5db999e060403c67bdebf50e90af64acab4b5d6ad658bcfcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122480108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde847aae62ff6f5b603d43e9504e27f822fd3949bfab1528e050b705b8b1b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2817c62f6d6843a9de3b3ff2e04505d12d83ded65a1625e0a9e6499235ad8f59`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec2a6bfc166d790b63e5354ffd8401676ef049f1ce56b2356306c77195dd49`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 5.6 MB (5649824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe20e272a77a01dc91791831b1a6d9d87b7d2e139f29df52f00c3f50d6726ee`  
		Last Modified: Mon, 12 Feb 2024 21:55:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fafbc37c58a7def18ed59a47552a68b382855a952b3d80e61c4cf706e1b9f`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e16823318490326752cff30bb17c5fe0c46c99e9199ff002a198ef0caf20e`  
		Last Modified: Mon, 12 Feb 2024 21:55:03 GMT  
		Size: 87.3 MB (87267323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a2b3981523db2a0c7c4c09f29512ee412b8ca004f175a3d56ba3ef762fda74`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d439c920270a39584dc7a8189308dd08f233e46c6a781bb72a1057729d51a`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10` - unknown; unknown

```console
$ docker pull mariadb@sha256:aa4d4e0c2aa48755320330d77beb5dcee3a1cd363533291a5828939cbd2add30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb888e8d249b104b1fb66253f85ce65eab94c3dfbe5f08e88fd1c0fe460384bf`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e1fac19a0148fc80b3395aa858539a11dd03f1336caefe7a24a65fea33067`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 4.0 MB (3979664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339e1b2bf18e127d310c767bd69c43e48f86fcfc46cf89449100d47850f2a422`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:86b60a8f3a6ac54c6482fee881cdd091ec89c1764127dc3e324fb7bcbbcba2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ce5f5ad4c0b6026f8b44d3f63a85c885a5585ee0d61a30f65e99b4ab8e2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94215bb141ed659a2e78ce05835cab755771f37c91ce21db4157554bad74c5e2`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce804ebe7c9c5ecfa62c662c85795d68311c6310ea45d0976900a7da948dd4e`  
		Last Modified: Tue, 13 Feb 2024 00:26:09 GMT  
		Size: 84.0 MB (84031849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b00d871e8a003f35a7f72737616127ea45b0e2493fbfd6bdc88a5f3a305006`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536c082b82dc51df7bea3d0464fd33781a5b5b76eaf822eb0d859d5512f9c77`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10` - unknown; unknown

```console
$ docker pull mariadb@sha256:9debb8593c7a672e9a123f544c63ba4d2fedb8305ad4eec883ca5f34a03bb8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4f4b565f196a65120a0eac6f1cea66e6ebfae0a8dc1b1d6b5754f9580d875d`

```dockerfile
```

-	Layers:
	-	`sha256:6df64df298f5f4dccffcb18affdd6a9313692f336839a0dd190372418e62b728`  
		Last Modified: Tue, 13 Feb 2024 00:26:06 GMT  
		Size: 4.0 MB (3983667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff7e6e627eb1f86a7410304df28f307d471b8f7b45e5904a198f582cdfc9e3e`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 31.0 KB (30991 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e1b0af6c871be8eec5791e452aecc79a2d5a0864f6438fdbd170c5212bac7c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130578641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f7a396d93f9eb3a81461dc343fda50d5ac1c2d6b06115759bccfc2f3ecdc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255eff2f62075d64e932eb7182c831b214973f2f0f581d47d40f22ea3d7059a`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18409da1bec295a582a56d8ae2e5631b2b7f1a17a481a882368cda7dc24af2`  
		Last Modified: Mon, 12 Feb 2024 22:48:04 GMT  
		Size: 90.0 MB (89960675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2bb5ba30db4af537487f1517e800b929315a77213ae40880c783dc50b300f5`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3408bf50bfd2907b72641fc363a51db6355030eb3525848813f699500b8a2`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10` - unknown; unknown

```console
$ docker pull mariadb@sha256:3499ea7308e67876f907e771f46b4db10c5437b9a0a1321a8f6ec9303f24d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178e1a68d2466747f4788141535703d0d7312d0ccbf1d45592bc5e7e49661f77`

```dockerfile
```

-	Layers:
	-	`sha256:a2c3038914ebe4ee069ff611291476b20c98a5ce5a1628c97d0b236077f4cbb1`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 4.0 MB (3985590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922cd5ba14809d63b032ea5744a85f5188c53ea269f121924553b5d088d28492`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:1313a2db308ac99e5064c01e087f2bb089c30ad83618ff8b5de911f3d20d1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121205840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aab662bedd776d651e8052f73f97908b6332c32a7a9e48dab890639f58c3e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5489c06038c18e372c7b90b22b2cf47db1467e7f1189c88ad6bca777d5190`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c533f93841b9cb3e974ae1f4f58b4fb381e31ad1403187c39eb6deecf920e`  
		Last Modified: Thu, 08 Feb 2024 17:43:50 GMT  
		Size: 87.6 MB (87628410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce941ad314a8efd36aa3955c69f7ac3e61b8d0398e5aa255e0e64d39ef9baf`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135db96191d18d5787d9cf2d1290b7663f0ca4451a16a004cf36bceac9c0b22`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10` - unknown; unknown

```console
$ docker pull mariadb@sha256:b8b8d9498b0036746728c78da1f3b06ee89659013890a8fb2a5f3eef3d78565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6677f1f9f2c40259478a71fedd8871a756a602f6555170a296e537c4ec841db0`

```dockerfile
```

-	Layers:
	-	`sha256:42c37c1a3494118265f54fe8f5fc8f337772d21ec612d32c4dbd8f0a0d62bbfa`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 4.0 MB (3957804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce20a145c0cb372b118c3f2e525403518aa76ee3880a1e1327e6a9ed867fe19`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:d1a4db6dd5fcf9f568037d1b9cdd405bd8148d56d1e36a7f06c9b993e9476d9e
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

### `mariadb:10-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:9b9b57e1318bb5db999e060403c67bdebf50e90af64acab4b5d6ad658bcfcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122480108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde847aae62ff6f5b603d43e9504e27f822fd3949bfab1528e050b705b8b1b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2817c62f6d6843a9de3b3ff2e04505d12d83ded65a1625e0a9e6499235ad8f59`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec2a6bfc166d790b63e5354ffd8401676ef049f1ce56b2356306c77195dd49`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 5.6 MB (5649824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe20e272a77a01dc91791831b1a6d9d87b7d2e139f29df52f00c3f50d6726ee`  
		Last Modified: Mon, 12 Feb 2024 21:55:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fafbc37c58a7def18ed59a47552a68b382855a952b3d80e61c4cf706e1b9f`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e16823318490326752cff30bb17c5fe0c46c99e9199ff002a198ef0caf20e`  
		Last Modified: Mon, 12 Feb 2024 21:55:03 GMT  
		Size: 87.3 MB (87267323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a2b3981523db2a0c7c4c09f29512ee412b8ca004f175a3d56ba3ef762fda74`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d439c920270a39584dc7a8189308dd08f233e46c6a781bb72a1057729d51a`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:aa4d4e0c2aa48755320330d77beb5dcee3a1cd363533291a5828939cbd2add30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb888e8d249b104b1fb66253f85ce65eab94c3dfbe5f08e88fd1c0fe460384bf`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e1fac19a0148fc80b3395aa858539a11dd03f1336caefe7a24a65fea33067`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 4.0 MB (3979664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339e1b2bf18e127d310c767bd69c43e48f86fcfc46cf89449100d47850f2a422`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:86b60a8f3a6ac54c6482fee881cdd091ec89c1764127dc3e324fb7bcbbcba2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ce5f5ad4c0b6026f8b44d3f63a85c885a5585ee0d61a30f65e99b4ab8e2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94215bb141ed659a2e78ce05835cab755771f37c91ce21db4157554bad74c5e2`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce804ebe7c9c5ecfa62c662c85795d68311c6310ea45d0976900a7da948dd4e`  
		Last Modified: Tue, 13 Feb 2024 00:26:09 GMT  
		Size: 84.0 MB (84031849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b00d871e8a003f35a7f72737616127ea45b0e2493fbfd6bdc88a5f3a305006`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536c082b82dc51df7bea3d0464fd33781a5b5b76eaf822eb0d859d5512f9c77`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:9debb8593c7a672e9a123f544c63ba4d2fedb8305ad4eec883ca5f34a03bb8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4f4b565f196a65120a0eac6f1cea66e6ebfae0a8dc1b1d6b5754f9580d875d`

```dockerfile
```

-	Layers:
	-	`sha256:6df64df298f5f4dccffcb18affdd6a9313692f336839a0dd190372418e62b728`  
		Last Modified: Tue, 13 Feb 2024 00:26:06 GMT  
		Size: 4.0 MB (3983667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff7e6e627eb1f86a7410304df28f307d471b8f7b45e5904a198f582cdfc9e3e`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 31.0 KB (30991 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e1b0af6c871be8eec5791e452aecc79a2d5a0864f6438fdbd170c5212bac7c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130578641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f7a396d93f9eb3a81461dc343fda50d5ac1c2d6b06115759bccfc2f3ecdc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255eff2f62075d64e932eb7182c831b214973f2f0f581d47d40f22ea3d7059a`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18409da1bec295a582a56d8ae2e5631b2b7f1a17a481a882368cda7dc24af2`  
		Last Modified: Mon, 12 Feb 2024 22:48:04 GMT  
		Size: 90.0 MB (89960675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2bb5ba30db4af537487f1517e800b929315a77213ae40880c783dc50b300f5`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3408bf50bfd2907b72641fc363a51db6355030eb3525848813f699500b8a2`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3499ea7308e67876f907e771f46b4db10c5437b9a0a1321a8f6ec9303f24d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178e1a68d2466747f4788141535703d0d7312d0ccbf1d45592bc5e7e49661f77`

```dockerfile
```

-	Layers:
	-	`sha256:a2c3038914ebe4ee069ff611291476b20c98a5ce5a1628c97d0b236077f4cbb1`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 4.0 MB (3985590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922cd5ba14809d63b032ea5744a85f5188c53ea269f121924553b5d088d28492`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:1313a2db308ac99e5064c01e087f2bb089c30ad83618ff8b5de911f3d20d1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121205840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aab662bedd776d651e8052f73f97908b6332c32a7a9e48dab890639f58c3e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5489c06038c18e372c7b90b22b2cf47db1467e7f1189c88ad6bca777d5190`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c533f93841b9cb3e974ae1f4f58b4fb381e31ad1403187c39eb6deecf920e`  
		Last Modified: Thu, 08 Feb 2024 17:43:50 GMT  
		Size: 87.6 MB (87628410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce941ad314a8efd36aa3955c69f7ac3e61b8d0398e5aa255e0e64d39ef9baf`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135db96191d18d5787d9cf2d1290b7663f0ca4451a16a004cf36bceac9c0b22`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:b8b8d9498b0036746728c78da1f3b06ee89659013890a8fb2a5f3eef3d78565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6677f1f9f2c40259478a71fedd8871a756a602f6555170a296e537c4ec841db0`

```dockerfile
```

-	Layers:
	-	`sha256:42c37c1a3494118265f54fe8f5fc8f337772d21ec612d32c4dbd8f0a0d62bbfa`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 4.0 MB (3957804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce20a145c0cb372b118c3f2e525403518aa76ee3880a1e1327e6a9ed867fe19`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.11`

```console
$ docker pull mariadb@sha256:d1a4db6dd5fcf9f568037d1b9cdd405bd8148d56d1e36a7f06c9b993e9476d9e
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

### `mariadb:10.11` - linux; amd64

```console
$ docker pull mariadb@sha256:9b9b57e1318bb5db999e060403c67bdebf50e90af64acab4b5d6ad658bcfcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122480108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde847aae62ff6f5b603d43e9504e27f822fd3949bfab1528e050b705b8b1b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2817c62f6d6843a9de3b3ff2e04505d12d83ded65a1625e0a9e6499235ad8f59`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec2a6bfc166d790b63e5354ffd8401676ef049f1ce56b2356306c77195dd49`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 5.6 MB (5649824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe20e272a77a01dc91791831b1a6d9d87b7d2e139f29df52f00c3f50d6726ee`  
		Last Modified: Mon, 12 Feb 2024 21:55:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fafbc37c58a7def18ed59a47552a68b382855a952b3d80e61c4cf706e1b9f`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e16823318490326752cff30bb17c5fe0c46c99e9199ff002a198ef0caf20e`  
		Last Modified: Mon, 12 Feb 2024 21:55:03 GMT  
		Size: 87.3 MB (87267323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a2b3981523db2a0c7c4c09f29512ee412b8ca004f175a3d56ba3ef762fda74`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d439c920270a39584dc7a8189308dd08f233e46c6a781bb72a1057729d51a`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11` - unknown; unknown

```console
$ docker pull mariadb@sha256:aa4d4e0c2aa48755320330d77beb5dcee3a1cd363533291a5828939cbd2add30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb888e8d249b104b1fb66253f85ce65eab94c3dfbe5f08e88fd1c0fe460384bf`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e1fac19a0148fc80b3395aa858539a11dd03f1336caefe7a24a65fea33067`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 4.0 MB (3979664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339e1b2bf18e127d310c767bd69c43e48f86fcfc46cf89449100d47850f2a422`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:86b60a8f3a6ac54c6482fee881cdd091ec89c1764127dc3e324fb7bcbbcba2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ce5f5ad4c0b6026f8b44d3f63a85c885a5585ee0d61a30f65e99b4ab8e2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94215bb141ed659a2e78ce05835cab755771f37c91ce21db4157554bad74c5e2`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce804ebe7c9c5ecfa62c662c85795d68311c6310ea45d0976900a7da948dd4e`  
		Last Modified: Tue, 13 Feb 2024 00:26:09 GMT  
		Size: 84.0 MB (84031849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b00d871e8a003f35a7f72737616127ea45b0e2493fbfd6bdc88a5f3a305006`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536c082b82dc51df7bea3d0464fd33781a5b5b76eaf822eb0d859d5512f9c77`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11` - unknown; unknown

```console
$ docker pull mariadb@sha256:9debb8593c7a672e9a123f544c63ba4d2fedb8305ad4eec883ca5f34a03bb8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4f4b565f196a65120a0eac6f1cea66e6ebfae0a8dc1b1d6b5754f9580d875d`

```dockerfile
```

-	Layers:
	-	`sha256:6df64df298f5f4dccffcb18affdd6a9313692f336839a0dd190372418e62b728`  
		Last Modified: Tue, 13 Feb 2024 00:26:06 GMT  
		Size: 4.0 MB (3983667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff7e6e627eb1f86a7410304df28f307d471b8f7b45e5904a198f582cdfc9e3e`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 31.0 KB (30991 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e1b0af6c871be8eec5791e452aecc79a2d5a0864f6438fdbd170c5212bac7c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130578641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f7a396d93f9eb3a81461dc343fda50d5ac1c2d6b06115759bccfc2f3ecdc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255eff2f62075d64e932eb7182c831b214973f2f0f581d47d40f22ea3d7059a`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18409da1bec295a582a56d8ae2e5631b2b7f1a17a481a882368cda7dc24af2`  
		Last Modified: Mon, 12 Feb 2024 22:48:04 GMT  
		Size: 90.0 MB (89960675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2bb5ba30db4af537487f1517e800b929315a77213ae40880c783dc50b300f5`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3408bf50bfd2907b72641fc363a51db6355030eb3525848813f699500b8a2`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11` - unknown; unknown

```console
$ docker pull mariadb@sha256:3499ea7308e67876f907e771f46b4db10c5437b9a0a1321a8f6ec9303f24d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178e1a68d2466747f4788141535703d0d7312d0ccbf1d45592bc5e7e49661f77`

```dockerfile
```

-	Layers:
	-	`sha256:a2c3038914ebe4ee069ff611291476b20c98a5ce5a1628c97d0b236077f4cbb1`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 4.0 MB (3985590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922cd5ba14809d63b032ea5744a85f5188c53ea269f121924553b5d088d28492`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11` - linux; s390x

```console
$ docker pull mariadb@sha256:1313a2db308ac99e5064c01e087f2bb089c30ad83618ff8b5de911f3d20d1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121205840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aab662bedd776d651e8052f73f97908b6332c32a7a9e48dab890639f58c3e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5489c06038c18e372c7b90b22b2cf47db1467e7f1189c88ad6bca777d5190`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c533f93841b9cb3e974ae1f4f58b4fb381e31ad1403187c39eb6deecf920e`  
		Last Modified: Thu, 08 Feb 2024 17:43:50 GMT  
		Size: 87.6 MB (87628410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce941ad314a8efd36aa3955c69f7ac3e61b8d0398e5aa255e0e64d39ef9baf`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135db96191d18d5787d9cf2d1290b7663f0ca4451a16a004cf36bceac9c0b22`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11` - unknown; unknown

```console
$ docker pull mariadb@sha256:b8b8d9498b0036746728c78da1f3b06ee89659013890a8fb2a5f3eef3d78565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6677f1f9f2c40259478a71fedd8871a756a602f6555170a296e537c4ec841db0`

```dockerfile
```

-	Layers:
	-	`sha256:42c37c1a3494118265f54fe8f5fc8f337772d21ec612d32c4dbd8f0a0d62bbfa`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 4.0 MB (3957804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce20a145c0cb372b118c3f2e525403518aa76ee3880a1e1327e6a9ed867fe19`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.11-jammy`

```console
$ docker pull mariadb@sha256:d1a4db6dd5fcf9f568037d1b9cdd405bd8148d56d1e36a7f06c9b993e9476d9e
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

### `mariadb:10.11-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:9b9b57e1318bb5db999e060403c67bdebf50e90af64acab4b5d6ad658bcfcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122480108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde847aae62ff6f5b603d43e9504e27f822fd3949bfab1528e050b705b8b1b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2817c62f6d6843a9de3b3ff2e04505d12d83ded65a1625e0a9e6499235ad8f59`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec2a6bfc166d790b63e5354ffd8401676ef049f1ce56b2356306c77195dd49`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 5.6 MB (5649824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe20e272a77a01dc91791831b1a6d9d87b7d2e139f29df52f00c3f50d6726ee`  
		Last Modified: Mon, 12 Feb 2024 21:55:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fafbc37c58a7def18ed59a47552a68b382855a952b3d80e61c4cf706e1b9f`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e16823318490326752cff30bb17c5fe0c46c99e9199ff002a198ef0caf20e`  
		Last Modified: Mon, 12 Feb 2024 21:55:03 GMT  
		Size: 87.3 MB (87267323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a2b3981523db2a0c7c4c09f29512ee412b8ca004f175a3d56ba3ef762fda74`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d439c920270a39584dc7a8189308dd08f233e46c6a781bb72a1057729d51a`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:aa4d4e0c2aa48755320330d77beb5dcee3a1cd363533291a5828939cbd2add30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb888e8d249b104b1fb66253f85ce65eab94c3dfbe5f08e88fd1c0fe460384bf`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e1fac19a0148fc80b3395aa858539a11dd03f1336caefe7a24a65fea33067`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 4.0 MB (3979664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339e1b2bf18e127d310c767bd69c43e48f86fcfc46cf89449100d47850f2a422`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:86b60a8f3a6ac54c6482fee881cdd091ec89c1764127dc3e324fb7bcbbcba2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ce5f5ad4c0b6026f8b44d3f63a85c885a5585ee0d61a30f65e99b4ab8e2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94215bb141ed659a2e78ce05835cab755771f37c91ce21db4157554bad74c5e2`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce804ebe7c9c5ecfa62c662c85795d68311c6310ea45d0976900a7da948dd4e`  
		Last Modified: Tue, 13 Feb 2024 00:26:09 GMT  
		Size: 84.0 MB (84031849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b00d871e8a003f35a7f72737616127ea45b0e2493fbfd6bdc88a5f3a305006`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536c082b82dc51df7bea3d0464fd33781a5b5b76eaf822eb0d859d5512f9c77`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:9debb8593c7a672e9a123f544c63ba4d2fedb8305ad4eec883ca5f34a03bb8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4f4b565f196a65120a0eac6f1cea66e6ebfae0a8dc1b1d6b5754f9580d875d`

```dockerfile
```

-	Layers:
	-	`sha256:6df64df298f5f4dccffcb18affdd6a9313692f336839a0dd190372418e62b728`  
		Last Modified: Tue, 13 Feb 2024 00:26:06 GMT  
		Size: 4.0 MB (3983667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff7e6e627eb1f86a7410304df28f307d471b8f7b45e5904a198f582cdfc9e3e`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 31.0 KB (30991 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e1b0af6c871be8eec5791e452aecc79a2d5a0864f6438fdbd170c5212bac7c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130578641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f7a396d93f9eb3a81461dc343fda50d5ac1c2d6b06115759bccfc2f3ecdc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255eff2f62075d64e932eb7182c831b214973f2f0f581d47d40f22ea3d7059a`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18409da1bec295a582a56d8ae2e5631b2b7f1a17a481a882368cda7dc24af2`  
		Last Modified: Mon, 12 Feb 2024 22:48:04 GMT  
		Size: 90.0 MB (89960675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2bb5ba30db4af537487f1517e800b929315a77213ae40880c783dc50b300f5`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3408bf50bfd2907b72641fc363a51db6355030eb3525848813f699500b8a2`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3499ea7308e67876f907e771f46b4db10c5437b9a0a1321a8f6ec9303f24d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178e1a68d2466747f4788141535703d0d7312d0ccbf1d45592bc5e7e49661f77`

```dockerfile
```

-	Layers:
	-	`sha256:a2c3038914ebe4ee069ff611291476b20c98a5ce5a1628c97d0b236077f4cbb1`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 4.0 MB (3985590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922cd5ba14809d63b032ea5744a85f5188c53ea269f121924553b5d088d28492`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:1313a2db308ac99e5064c01e087f2bb089c30ad83618ff8b5de911f3d20d1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121205840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aab662bedd776d651e8052f73f97908b6332c32a7a9e48dab890639f58c3e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5489c06038c18e372c7b90b22b2cf47db1467e7f1189c88ad6bca777d5190`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c533f93841b9cb3e974ae1f4f58b4fb381e31ad1403187c39eb6deecf920e`  
		Last Modified: Thu, 08 Feb 2024 17:43:50 GMT  
		Size: 87.6 MB (87628410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce941ad314a8efd36aa3955c69f7ac3e61b8d0398e5aa255e0e64d39ef9baf`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135db96191d18d5787d9cf2d1290b7663f0ca4451a16a004cf36bceac9c0b22`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:b8b8d9498b0036746728c78da1f3b06ee89659013890a8fb2a5f3eef3d78565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6677f1f9f2c40259478a71fedd8871a756a602f6555170a296e537c4ec841db0`

```dockerfile
```

-	Layers:
	-	`sha256:42c37c1a3494118265f54fe8f5fc8f337772d21ec612d32c4dbd8f0a0d62bbfa`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 4.0 MB (3957804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce20a145c0cb372b118c3f2e525403518aa76ee3880a1e1327e6a9ed867fe19`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.11.7`

```console
$ docker pull mariadb@sha256:200281eae78cabfad8661a39fa231358f3c3fbf0d510b4faf7c32b544cb3c2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `mariadb:10.11.7` - linux; amd64

```console
$ docker pull mariadb@sha256:9b9b57e1318bb5db999e060403c67bdebf50e90af64acab4b5d6ad658bcfcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122480108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde847aae62ff6f5b603d43e9504e27f822fd3949bfab1528e050b705b8b1b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2817c62f6d6843a9de3b3ff2e04505d12d83ded65a1625e0a9e6499235ad8f59`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec2a6bfc166d790b63e5354ffd8401676ef049f1ce56b2356306c77195dd49`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 5.6 MB (5649824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe20e272a77a01dc91791831b1a6d9d87b7d2e139f29df52f00c3f50d6726ee`  
		Last Modified: Mon, 12 Feb 2024 21:55:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fafbc37c58a7def18ed59a47552a68b382855a952b3d80e61c4cf706e1b9f`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e16823318490326752cff30bb17c5fe0c46c99e9199ff002a198ef0caf20e`  
		Last Modified: Mon, 12 Feb 2024 21:55:03 GMT  
		Size: 87.3 MB (87267323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a2b3981523db2a0c7c4c09f29512ee412b8ca004f175a3d56ba3ef762fda74`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d439c920270a39584dc7a8189308dd08f233e46c6a781bb72a1057729d51a`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11.7` - unknown; unknown

```console
$ docker pull mariadb@sha256:aa4d4e0c2aa48755320330d77beb5dcee3a1cd363533291a5828939cbd2add30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb888e8d249b104b1fb66253f85ce65eab94c3dfbe5f08e88fd1c0fe460384bf`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e1fac19a0148fc80b3395aa858539a11dd03f1336caefe7a24a65fea33067`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 4.0 MB (3979664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339e1b2bf18e127d310c767bd69c43e48f86fcfc46cf89449100d47850f2a422`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:86b60a8f3a6ac54c6482fee881cdd091ec89c1764127dc3e324fb7bcbbcba2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ce5f5ad4c0b6026f8b44d3f63a85c885a5585ee0d61a30f65e99b4ab8e2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94215bb141ed659a2e78ce05835cab755771f37c91ce21db4157554bad74c5e2`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce804ebe7c9c5ecfa62c662c85795d68311c6310ea45d0976900a7da948dd4e`  
		Last Modified: Tue, 13 Feb 2024 00:26:09 GMT  
		Size: 84.0 MB (84031849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b00d871e8a003f35a7f72737616127ea45b0e2493fbfd6bdc88a5f3a305006`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536c082b82dc51df7bea3d0464fd33781a5b5b76eaf822eb0d859d5512f9c77`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11.7` - unknown; unknown

```console
$ docker pull mariadb@sha256:9debb8593c7a672e9a123f544c63ba4d2fedb8305ad4eec883ca5f34a03bb8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4f4b565f196a65120a0eac6f1cea66e6ebfae0a8dc1b1d6b5754f9580d875d`

```dockerfile
```

-	Layers:
	-	`sha256:6df64df298f5f4dccffcb18affdd6a9313692f336839a0dd190372418e62b728`  
		Last Modified: Tue, 13 Feb 2024 00:26:06 GMT  
		Size: 4.0 MB (3983667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff7e6e627eb1f86a7410304df28f307d471b8f7b45e5904a198f582cdfc9e3e`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 31.0 KB (30991 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e1b0af6c871be8eec5791e452aecc79a2d5a0864f6438fdbd170c5212bac7c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130578641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f7a396d93f9eb3a81461dc343fda50d5ac1c2d6b06115759bccfc2f3ecdc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255eff2f62075d64e932eb7182c831b214973f2f0f581d47d40f22ea3d7059a`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18409da1bec295a582a56d8ae2e5631b2b7f1a17a481a882368cda7dc24af2`  
		Last Modified: Mon, 12 Feb 2024 22:48:04 GMT  
		Size: 90.0 MB (89960675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2bb5ba30db4af537487f1517e800b929315a77213ae40880c783dc50b300f5`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3408bf50bfd2907b72641fc363a51db6355030eb3525848813f699500b8a2`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11.7` - unknown; unknown

```console
$ docker pull mariadb@sha256:3499ea7308e67876f907e771f46b4db10c5437b9a0a1321a8f6ec9303f24d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178e1a68d2466747f4788141535703d0d7312d0ccbf1d45592bc5e7e49661f77`

```dockerfile
```

-	Layers:
	-	`sha256:a2c3038914ebe4ee069ff611291476b20c98a5ce5a1628c97d0b236077f4cbb1`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 4.0 MB (3985590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922cd5ba14809d63b032ea5744a85f5188c53ea269f121924553b5d088d28492`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.11.7-jammy`

```console
$ docker pull mariadb@sha256:200281eae78cabfad8661a39fa231358f3c3fbf0d510b4faf7c32b544cb3c2a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `mariadb:10.11.7-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:9b9b57e1318bb5db999e060403c67bdebf50e90af64acab4b5d6ad658bcfcf6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122480108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde847aae62ff6f5b603d43e9504e27f822fd3949bfab1528e050b705b8b1b84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2817c62f6d6843a9de3b3ff2e04505d12d83ded65a1625e0a9e6499235ad8f59`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec2a6bfc166d790b63e5354ffd8401676ef049f1ce56b2356306c77195dd49`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 5.6 MB (5649824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe20e272a77a01dc91791831b1a6d9d87b7d2e139f29df52f00c3f50d6726ee`  
		Last Modified: Mon, 12 Feb 2024 21:55:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0fafbc37c58a7def18ed59a47552a68b382855a952b3d80e61c4cf706e1b9f`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479e16823318490326752cff30bb17c5fe0c46c99e9199ff002a198ef0caf20e`  
		Last Modified: Mon, 12 Feb 2024 21:55:03 GMT  
		Size: 87.3 MB (87267323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a2b3981523db2a0c7c4c09f29512ee412b8ca004f175a3d56ba3ef762fda74`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d439c920270a39584dc7a8189308dd08f233e46c6a781bb72a1057729d51a`  
		Last Modified: Mon, 12 Feb 2024 21:55:02 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11.7-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:aa4d4e0c2aa48755320330d77beb5dcee3a1cd363533291a5828939cbd2add30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4010799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb888e8d249b104b1fb66253f85ce65eab94c3dfbe5f08e88fd1c0fe460384bf`

```dockerfile
```

-	Layers:
	-	`sha256:5a5e1fac19a0148fc80b3395aa858539a11dd03f1336caefe7a24a65fea33067`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 4.0 MB (3979664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:339e1b2bf18e127d310c767bd69c43e48f86fcfc46cf89449100d47850f2a422`  
		Last Modified: Mon, 12 Feb 2024 21:55:01 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11.7-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:86b60a8f3a6ac54c6482fee881cdd091ec89c1764127dc3e324fb7bcbbcba2be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116865624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5ce5f5ad4c0b6026f8b44d3f63a85c885a5585ee0d61a30f65e99b4ab8e2c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94215bb141ed659a2e78ce05835cab755771f37c91ce21db4157554bad74c5e2`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce804ebe7c9c5ecfa62c662c85795d68311c6310ea45d0976900a7da948dd4e`  
		Last Modified: Tue, 13 Feb 2024 00:26:09 GMT  
		Size: 84.0 MB (84031849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b00d871e8a003f35a7f72737616127ea45b0e2493fbfd6bdc88a5f3a305006`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0536c082b82dc51df7bea3d0464fd33781a5b5b76eaf822eb0d859d5512f9c77`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 8.3 KB (8251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11.7-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:9debb8593c7a672e9a123f544c63ba4d2fedb8305ad4eec883ca5f34a03bb8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4f4b565f196a65120a0eac6f1cea66e6ebfae0a8dc1b1d6b5754f9580d875d`

```dockerfile
```

-	Layers:
	-	`sha256:6df64df298f5f4dccffcb18affdd6a9313692f336839a0dd190372418e62b728`  
		Last Modified: Tue, 13 Feb 2024 00:26:06 GMT  
		Size: 4.0 MB (3983667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ff7e6e627eb1f86a7410304df28f307d471b8f7b45e5904a198f582cdfc9e3e`  
		Last Modified: Tue, 13 Feb 2024 00:26:05 GMT  
		Size: 31.0 KB (30991 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.11.7-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e1b0af6c871be8eec5791e452aecc79a2d5a0864f6438fdbd170c5212bac7c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130578641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f7a396d93f9eb3a81461dc343fda50d5ac1c2d6b06115759bccfc2f3ecdc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 25 Jan 2024 17:56:59 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:56:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:56:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:57:02 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Thu, 25 Jan 2024 17:57:02 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.11.7+maria~ubu2204
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.7+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.7/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255eff2f62075d64e932eb7182c831b214973f2f0f581d47d40f22ea3d7059a`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18409da1bec295a582a56d8ae2e5631b2b7f1a17a481a882368cda7dc24af2`  
		Last Modified: Mon, 12 Feb 2024 22:48:04 GMT  
		Size: 90.0 MB (89960675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2bb5ba30db4af537487f1517e800b929315a77213ae40880c783dc50b300f5`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3408bf50bfd2907b72641fc363a51db6355030eb3525848813f699500b8a2`  
		Last Modified: Mon, 12 Feb 2024 22:48:00 GMT  
		Size: 8.2 KB (8250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.11.7-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3499ea7308e67876f907e771f46b4db10c5437b9a0a1321a8f6ec9303f24d234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178e1a68d2466747f4788141535703d0d7312d0ccbf1d45592bc5e7e49661f77`

```dockerfile
```

-	Layers:
	-	`sha256:a2c3038914ebe4ee069ff611291476b20c98a5ce5a1628c97d0b236077f4cbb1`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 4.0 MB (3985590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922cd5ba14809d63b032ea5744a85f5188c53ea269f121924553b5d088d28492`  
		Last Modified: Mon, 12 Feb 2024 22:48:01 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:e39757f29ada2a84beb9cd14a4960b39b9f8502b144c16d3aef56676663eed30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:0511d6b7f68bf62306120736d30d9d69920aa3836a47bc7719d85f9d4c14f5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa4daaa733ad2a149594935695e886297defe7ee16b368c1368bbb8821df148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ee913a99cdb375debcf6c3b8d2cd5f63cf3d47502ebcd6dcb167c4f21d851b`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0b91afa4cea59b45c9d3b64155cda0e36526f3817b6e521b57dadc5467346b`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 7.2 MB (7179106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9c4e5788d20b42c56bdfa693472ee201ac59f86c591780ef60666ae5a3c4e`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41292064b99f2f802a73c442452c9803f22d1c0a7dca21fa7eec820d7aa4c4a4`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7814150c29684e8cc6ccec3338673f677e8fe63f7d3cf172f41ebdbf5bc47c`  
		Last Modified: Mon, 12 Feb 2024 21:55:18 GMT  
		Size: 83.5 MB (83485891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfe31688361f9a05bad63fa5628cf57ea80afe00e50c596a27cf91aa4670a99`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d8adbbc65edb5b4b9a3ac7adf914cade3200405a2e89d54fb293d82582f517`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 8.1 KB (8095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d349383082528d306d41eb3d05e730218b2f29d1833733578c9fb0be39ea7821`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4` - unknown; unknown

```console
$ docker pull mariadb@sha256:8b8650c735dcbc30698cc54b45f33cdce07f71a4e29f2f83c1023fc0b34115c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3861384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a50bc979f50dfc6723a22007142ca6c0d543d5c5e41a6bb861b6b63cae84395`

```dockerfile
```

-	Layers:
	-	`sha256:21c29e8e0e8ac6e5ba45aba1d9bf8a94ff194e09549725c40b60de159d53f252`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.8 MB (3828942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2647ab6b9a5428f90df5aae486e5ceeadfc66d8cc62f9214569d14aa821d3c`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 32.4 KB (32442 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de268d98e11f9c726c871b479e82e0f57f74f8976a85e3c0f3653cda391178e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115557821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed661318c2e8ab762cc6065f0f741f78444b9bbea2af11822344f87477b940de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1db8757f198d433b94d7f89edf19df1badbfe70058c411690d354c384b9d7c`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33a19ef7dcf0aa2550a0a82632e3d1f3dc88e3d466334da571fc83ca2563e8`  
		Last Modified: Tue, 13 Feb 2024 00:29:00 GMT  
		Size: 82.7 MB (82662001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a2800c12af38135cd6f0507491957a40601a78ab3437459101d539dc536dff`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2f35ea230f971a2a8f2fe9af166c6f62c276409a9d85e00533cb512103f1af`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20116907e06e9b0eb2cb0e537a572845c1c9876713b6a276ea5b00bab70c4f8`  
		Last Modified: Tue, 13 Feb 2024 00:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4` - unknown; unknown

```console
$ docker pull mariadb@sha256:73d184d6123d64b57bddf5d01d45c8ddf1b82182a470915c55cd3853203a8d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3866919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d309fc61223364e6e6e47ba4c6aa766cf1d2cb96d41cc42d6514f3d16bfbc0a`

```dockerfile
```

-	Layers:
	-	`sha256:470d4bb823933f06bb48e2ddb14f83c3f4cd1fa60e674c9cc5efb522d9e471da`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.8 MB (3834628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad78f327db78c5cb13814e68d4b84660cbc80623d759223ae173d8574a047c5`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 32.3 KB (32291 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1334b15991e5ea2f5c270ed1cffc5e15cc808a61f8d995c50e02a2defc59dcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127935389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f16b9197eb0f7d352d90d8b750eaa8b0a37b0a9059ca1b79bcc20fa770c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e264f1d18ce361e721890632532d327931ad7e59da3104c081afd3bd68ad1`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44449e21f6ab4e91ffb92771366b5bcc32e85df0720ab84517ffbc4f4a91d9a2`  
		Last Modified: Mon, 12 Feb 2024 22:53:02 GMT  
		Size: 87.9 MB (87937752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c34f659b84bc2eb0a6c3feb69e848b66474a4919c1eb6ea97480034158d278`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0598f1a9e153d4ff85477c1c237704f5c01704721c5864ad3ccc3f51cfa6c3`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a72f49d8e1fde94e6458bf81471bf36a676c6213c69fb4343639ba7fadd420`  
		Last Modified: Mon, 12 Feb 2024 22:53:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4` - unknown; unknown

```console
$ docker pull mariadb@sha256:f5de46116d34498f5c16ff0ac56cfbab77e23d5aafb1b7a676dff70e82246203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44577be4c07ee263ceabaa03bebf738eb905b393c096b359cde227557a82c8d1`

```dockerfile
```

-	Layers:
	-	`sha256:c5344bac892b25f11b67e1d8e9b20f05fa9012d69f519a170e4ecd76c572bbca`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 3.8 MB (3836321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455bef82fc2d54ed8873f265de44435b19fff93498b05b7340b3ec6ca3dfb98c`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 32.3 KB (32329 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:e39757f29ada2a84beb9cd14a4960b39b9f8502b144c16d3aef56676663eed30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:0511d6b7f68bf62306120736d30d9d69920aa3836a47bc7719d85f9d4c14f5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa4daaa733ad2a149594935695e886297defe7ee16b368c1368bbb8821df148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ee913a99cdb375debcf6c3b8d2cd5f63cf3d47502ebcd6dcb167c4f21d851b`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0b91afa4cea59b45c9d3b64155cda0e36526f3817b6e521b57dadc5467346b`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 7.2 MB (7179106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9c4e5788d20b42c56bdfa693472ee201ac59f86c591780ef60666ae5a3c4e`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41292064b99f2f802a73c442452c9803f22d1c0a7dca21fa7eec820d7aa4c4a4`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7814150c29684e8cc6ccec3338673f677e8fe63f7d3cf172f41ebdbf5bc47c`  
		Last Modified: Mon, 12 Feb 2024 21:55:18 GMT  
		Size: 83.5 MB (83485891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfe31688361f9a05bad63fa5628cf57ea80afe00e50c596a27cf91aa4670a99`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d8adbbc65edb5b4b9a3ac7adf914cade3200405a2e89d54fb293d82582f517`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 8.1 KB (8095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d349383082528d306d41eb3d05e730218b2f29d1833733578c9fb0be39ea7821`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:8b8650c735dcbc30698cc54b45f33cdce07f71a4e29f2f83c1023fc0b34115c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3861384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a50bc979f50dfc6723a22007142ca6c0d543d5c5e41a6bb861b6b63cae84395`

```dockerfile
```

-	Layers:
	-	`sha256:21c29e8e0e8ac6e5ba45aba1d9bf8a94ff194e09549725c40b60de159d53f252`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.8 MB (3828942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2647ab6b9a5428f90df5aae486e5ceeadfc66d8cc62f9214569d14aa821d3c`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 32.4 KB (32442 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de268d98e11f9c726c871b479e82e0f57f74f8976a85e3c0f3653cda391178e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115557821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed661318c2e8ab762cc6065f0f741f78444b9bbea2af11822344f87477b940de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1db8757f198d433b94d7f89edf19df1badbfe70058c411690d354c384b9d7c`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33a19ef7dcf0aa2550a0a82632e3d1f3dc88e3d466334da571fc83ca2563e8`  
		Last Modified: Tue, 13 Feb 2024 00:29:00 GMT  
		Size: 82.7 MB (82662001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a2800c12af38135cd6f0507491957a40601a78ab3437459101d539dc536dff`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2f35ea230f971a2a8f2fe9af166c6f62c276409a9d85e00533cb512103f1af`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20116907e06e9b0eb2cb0e537a572845c1c9876713b6a276ea5b00bab70c4f8`  
		Last Modified: Tue, 13 Feb 2024 00:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:73d184d6123d64b57bddf5d01d45c8ddf1b82182a470915c55cd3853203a8d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3866919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d309fc61223364e6e6e47ba4c6aa766cf1d2cb96d41cc42d6514f3d16bfbc0a`

```dockerfile
```

-	Layers:
	-	`sha256:470d4bb823933f06bb48e2ddb14f83c3f4cd1fa60e674c9cc5efb522d9e471da`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.8 MB (3834628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad78f327db78c5cb13814e68d4b84660cbc80623d759223ae173d8574a047c5`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 32.3 KB (32291 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1334b15991e5ea2f5c270ed1cffc5e15cc808a61f8d995c50e02a2defc59dcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127935389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f16b9197eb0f7d352d90d8b750eaa8b0a37b0a9059ca1b79bcc20fa770c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e264f1d18ce361e721890632532d327931ad7e59da3104c081afd3bd68ad1`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44449e21f6ab4e91ffb92771366b5bcc32e85df0720ab84517ffbc4f4a91d9a2`  
		Last Modified: Mon, 12 Feb 2024 22:53:02 GMT  
		Size: 87.9 MB (87937752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c34f659b84bc2eb0a6c3feb69e848b66474a4919c1eb6ea97480034158d278`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0598f1a9e153d4ff85477c1c237704f5c01704721c5864ad3ccc3f51cfa6c3`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a72f49d8e1fde94e6458bf81471bf36a676c6213c69fb4343639ba7fadd420`  
		Last Modified: Mon, 12 Feb 2024 22:53:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:f5de46116d34498f5c16ff0ac56cfbab77e23d5aafb1b7a676dff70e82246203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44577be4c07ee263ceabaa03bebf738eb905b393c096b359cde227557a82c8d1`

```dockerfile
```

-	Layers:
	-	`sha256:c5344bac892b25f11b67e1d8e9b20f05fa9012d69f519a170e4ecd76c572bbca`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 3.8 MB (3836321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455bef82fc2d54ed8873f265de44435b19fff93498b05b7340b3ec6ca3dfb98c`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 32.3 KB (32329 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.4.33`

```console
$ docker pull mariadb@sha256:e39757f29ada2a84beb9cd14a4960b39b9f8502b144c16d3aef56676663eed30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `mariadb:10.4.33` - linux; amd64

```console
$ docker pull mariadb@sha256:0511d6b7f68bf62306120736d30d9d69920aa3836a47bc7719d85f9d4c14f5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa4daaa733ad2a149594935695e886297defe7ee16b368c1368bbb8821df148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ee913a99cdb375debcf6c3b8d2cd5f63cf3d47502ebcd6dcb167c4f21d851b`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0b91afa4cea59b45c9d3b64155cda0e36526f3817b6e521b57dadc5467346b`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 7.2 MB (7179106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9c4e5788d20b42c56bdfa693472ee201ac59f86c591780ef60666ae5a3c4e`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41292064b99f2f802a73c442452c9803f22d1c0a7dca21fa7eec820d7aa4c4a4`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7814150c29684e8cc6ccec3338673f677e8fe63f7d3cf172f41ebdbf5bc47c`  
		Last Modified: Mon, 12 Feb 2024 21:55:18 GMT  
		Size: 83.5 MB (83485891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfe31688361f9a05bad63fa5628cf57ea80afe00e50c596a27cf91aa4670a99`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d8adbbc65edb5b4b9a3ac7adf914cade3200405a2e89d54fb293d82582f517`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 8.1 KB (8095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d349383082528d306d41eb3d05e730218b2f29d1833733578c9fb0be39ea7821`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4.33` - unknown; unknown

```console
$ docker pull mariadb@sha256:8b8650c735dcbc30698cc54b45f33cdce07f71a4e29f2f83c1023fc0b34115c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3861384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a50bc979f50dfc6723a22007142ca6c0d543d5c5e41a6bb861b6b63cae84395`

```dockerfile
```

-	Layers:
	-	`sha256:21c29e8e0e8ac6e5ba45aba1d9bf8a94ff194e09549725c40b60de159d53f252`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.8 MB (3828942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2647ab6b9a5428f90df5aae486e5ceeadfc66d8cc62f9214569d14aa821d3c`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 32.4 KB (32442 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4.33` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de268d98e11f9c726c871b479e82e0f57f74f8976a85e3c0f3653cda391178e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115557821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed661318c2e8ab762cc6065f0f741f78444b9bbea2af11822344f87477b940de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1db8757f198d433b94d7f89edf19df1badbfe70058c411690d354c384b9d7c`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33a19ef7dcf0aa2550a0a82632e3d1f3dc88e3d466334da571fc83ca2563e8`  
		Last Modified: Tue, 13 Feb 2024 00:29:00 GMT  
		Size: 82.7 MB (82662001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a2800c12af38135cd6f0507491957a40601a78ab3437459101d539dc536dff`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2f35ea230f971a2a8f2fe9af166c6f62c276409a9d85e00533cb512103f1af`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20116907e06e9b0eb2cb0e537a572845c1c9876713b6a276ea5b00bab70c4f8`  
		Last Modified: Tue, 13 Feb 2024 00:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4.33` - unknown; unknown

```console
$ docker pull mariadb@sha256:73d184d6123d64b57bddf5d01d45c8ddf1b82182a470915c55cd3853203a8d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3866919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d309fc61223364e6e6e47ba4c6aa766cf1d2cb96d41cc42d6514f3d16bfbc0a`

```dockerfile
```

-	Layers:
	-	`sha256:470d4bb823933f06bb48e2ddb14f83c3f4cd1fa60e674c9cc5efb522d9e471da`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.8 MB (3834628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad78f327db78c5cb13814e68d4b84660cbc80623d759223ae173d8574a047c5`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 32.3 KB (32291 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4.33` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1334b15991e5ea2f5c270ed1cffc5e15cc808a61f8d995c50e02a2defc59dcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127935389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f16b9197eb0f7d352d90d8b750eaa8b0a37b0a9059ca1b79bcc20fa770c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e264f1d18ce361e721890632532d327931ad7e59da3104c081afd3bd68ad1`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44449e21f6ab4e91ffb92771366b5bcc32e85df0720ab84517ffbc4f4a91d9a2`  
		Last Modified: Mon, 12 Feb 2024 22:53:02 GMT  
		Size: 87.9 MB (87937752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c34f659b84bc2eb0a6c3feb69e848b66474a4919c1eb6ea97480034158d278`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0598f1a9e153d4ff85477c1c237704f5c01704721c5864ad3ccc3f51cfa6c3`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a72f49d8e1fde94e6458bf81471bf36a676c6213c69fb4343639ba7fadd420`  
		Last Modified: Mon, 12 Feb 2024 22:53:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4.33` - unknown; unknown

```console
$ docker pull mariadb@sha256:f5de46116d34498f5c16ff0ac56cfbab77e23d5aafb1b7a676dff70e82246203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44577be4c07ee263ceabaa03bebf738eb905b393c096b359cde227557a82c8d1`

```dockerfile
```

-	Layers:
	-	`sha256:c5344bac892b25f11b67e1d8e9b20f05fa9012d69f519a170e4ecd76c572bbca`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 3.8 MB (3836321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455bef82fc2d54ed8873f265de44435b19fff93498b05b7340b3ec6ca3dfb98c`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 32.3 KB (32329 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.4.33-focal`

```console
$ docker pull mariadb@sha256:e39757f29ada2a84beb9cd14a4960b39b9f8502b144c16d3aef56676663eed30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `mariadb:10.4.33-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:0511d6b7f68bf62306120736d30d9d69920aa3836a47bc7719d85f9d4c14f5c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.2 MB (118193934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa4daaa733ad2a149594935695e886297defe7ee16b368c1368bbb8821df148`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ee913a99cdb375debcf6c3b8d2cd5f63cf3d47502ebcd6dcb167c4f21d851b`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0b91afa4cea59b45c9d3b64155cda0e36526f3817b6e521b57dadc5467346b`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 7.2 MB (7179106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f9c4e5788d20b42c56bdfa693472ee201ac59f86c591780ef60666ae5a3c4e`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41292064b99f2f802a73c442452c9803f22d1c0a7dca21fa7eec820d7aa4c4a4`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7814150c29684e8cc6ccec3338673f677e8fe63f7d3cf172f41ebdbf5bc47c`  
		Last Modified: Mon, 12 Feb 2024 21:55:18 GMT  
		Size: 83.5 MB (83485891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dfe31688361f9a05bad63fa5628cf57ea80afe00e50c596a27cf91aa4670a99`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.6 KB (3619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d8adbbc65edb5b4b9a3ac7adf914cade3200405a2e89d54fb293d82582f517`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 8.1 KB (8095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d349383082528d306d41eb3d05e730218b2f29d1833733578c9fb0be39ea7821`  
		Last Modified: Mon, 12 Feb 2024 21:55:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4.33-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:8b8650c735dcbc30698cc54b45f33cdce07f71a4e29f2f83c1023fc0b34115c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3861384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a50bc979f50dfc6723a22007142ca6c0d543d5c5e41a6bb861b6b63cae84395`

```dockerfile
```

-	Layers:
	-	`sha256:21c29e8e0e8ac6e5ba45aba1d9bf8a94ff194e09549725c40b60de159d53f252`  
		Last Modified: Mon, 12 Feb 2024 21:55:15 GMT  
		Size: 3.8 MB (3828942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2647ab6b9a5428f90df5aae486e5ceeadfc66d8cc62f9214569d14aa821d3c`  
		Last Modified: Mon, 12 Feb 2024 21:55:14 GMT  
		Size: 32.4 KB (32442 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4.33-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de268d98e11f9c726c871b479e82e0f57f74f8976a85e3c0f3653cda391178e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.6 MB (115557821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed661318c2e8ab762cc6065f0f741f78444b9bbea2af11822344f87477b940de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 13:04:26 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:04:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:04:26 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:04:27 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 23 Jan 2024 13:04:27 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1db8757f198d433b94d7f89edf19df1badbfe70058c411690d354c384b9d7c`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33a19ef7dcf0aa2550a0a82632e3d1f3dc88e3d466334da571fc83ca2563e8`  
		Last Modified: Tue, 13 Feb 2024 00:29:00 GMT  
		Size: 82.7 MB (82662001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a2800c12af38135cd6f0507491957a40601a78ab3437459101d539dc536dff`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2f35ea230f971a2a8f2fe9af166c6f62c276409a9d85e00533cb512103f1af`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20116907e06e9b0eb2cb0e537a572845c1c9876713b6a276ea5b00bab70c4f8`  
		Last Modified: Tue, 13 Feb 2024 00:28:58 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4.33-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:73d184d6123d64b57bddf5d01d45c8ddf1b82182a470915c55cd3853203a8d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3866919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d309fc61223364e6e6e47ba4c6aa766cf1d2cb96d41cc42d6514f3d16bfbc0a`

```dockerfile
```

-	Layers:
	-	`sha256:470d4bb823933f06bb48e2ddb14f83c3f4cd1fa60e674c9cc5efb522d9e471da`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 3.8 MB (3834628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dad78f327db78c5cb13814e68d4b84660cbc80623d759223ae173d8574a047c5`  
		Last Modified: Tue, 13 Feb 2024 00:28:57 GMT  
		Size: 32.3 KB (32291 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.4.33-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1334b15991e5ea2f5c270ed1cffc5e15cc808a61f8d995c50e02a2defc59dcd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127935389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de6f16b9197eb0f7d352d90d8b750eaa8b0a37b0a9059ca1b79bcc20fa770c29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 23 Jan 2024 12:54:35 GMT
ARG RELEASE
# Tue, 23 Jan 2024 12:54:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 12:54:35 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 12:54:38 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 23 Jan 2024 12:54:39 GMT
CMD ["/bin/bash"]
# Sun, 11 Feb 2024 23:03:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV GOSU_VERSION=1.17
# Sun, 11 Feb 2024 23:03:42 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENV LANG=C.UTF-8
# Sun, 11 Feb 2024 23:03:42 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.33 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_MAJOR=10.4
# Sun, 11 Feb 2024 23:03:42 GMT
ARG MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ENV MARIADB_VERSION=1:10.4.33+maria~ubu2004
# Sun, 11 Feb 2024 23:03:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run//mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run//mysqld; 	chmod 1777 /var/run//mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
VOLUME [/var/lib/mysql]
# Sun, 11 Feb 2024 23:03:42 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.4 MARIADB_VERSION=1:10.4.33+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.33/repo/ubuntu/ focal main main/debug
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat # buildkit
# Sun, 11 Feb 2024 23:03:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 11 Feb 2024 23:03:42 GMT
EXPOSE map[3306/tcp:{}]
# Sun, 11 Feb 2024 23:03:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257e264f1d18ce361e721890632532d327931ad7e59da3104c081afd3bd68ad1`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44449e21f6ab4e91ffb92771366b5bcc32e85df0720ab84517ffbc4f4a91d9a2`  
		Last Modified: Mon, 12 Feb 2024 22:53:02 GMT  
		Size: 87.9 MB (87937752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c34f659b84bc2eb0a6c3feb69e848b66474a4919c1eb6ea97480034158d278`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 3.6 KB (3617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0598f1a9e153d4ff85477c1c237704f5c01704721c5864ad3ccc3f51cfa6c3`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 8.1 KB (8093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a72f49d8e1fde94e6458bf81471bf36a676c6213c69fb4343639ba7fadd420`  
		Last Modified: Mon, 12 Feb 2024 22:53:01 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.4.33-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:f5de46116d34498f5c16ff0ac56cfbab77e23d5aafb1b7a676dff70e82246203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3868650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44577be4c07ee263ceabaa03bebf738eb905b393c096b359cde227557a82c8d1`

```dockerfile
```

-	Layers:
	-	`sha256:c5344bac892b25f11b67e1d8e9b20f05fa9012d69f519a170e4ecd76c572bbca`  
		Last Modified: Mon, 12 Feb 2024 22:53:00 GMT  
		Size: 3.8 MB (3836321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:455bef82fc2d54ed8873f265de44435b19fff93498b05b7340b3ec6ca3dfb98c`  
		Last Modified: Mon, 12 Feb 2024 22:52:59 GMT  
		Size: 32.3 KB (32329 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:6122f729893e286a3cfc789fb546dd041cf244e4de84272ab5727028ca107730
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

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:44b025abf54f798e7a9ac95d543b1f1d3dc80af1769237f6d5f72d807bdb61aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120457080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc3807752990d5e6f85c7f4eed70f53cea3523985d58dfdb761eba2c5720ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ce84e449118f88e0ddd38f8b6fd0d855d0ab2f08b34a7a81347fac8fe19f29`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6663e8686f0a932a93d852a4b401e50c7318c4d86d40e9cc3b55dc896cbcdb`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 7.2 MB (7179046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4ed2974b5cda9f7ca6150129676130f01f5e096903b207ca3e8d9eb5ecc616`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37cccd2cd8ec5d0229c304416a55ef48808f6396f6a4e918a9c4af2fe441aba`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f7ecfc90a594d28f7477caabe0ea0ba78b1aa79f19838bc5ea1c86631050df`  
		Last Modified: Fri, 02 Feb 2024 00:55:55 GMT  
		Size: 85.7 MB (85749495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34018581dae4c4db7e4c62a3fbf652c8c72429c8d88f689a7eb79db7805278f`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fcf1e0fdf4fa145ad4c170f2a17c231b64416c6894173e7394cc23ae440935`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 7.8 KB (7828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5` - unknown; unknown

```console
$ docker pull mariadb@sha256:41a68d6d6843364a8ec5856f0bc9c71e72c3723b309438210c14e7e0af8d2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3864109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685c0e666156371d45e300309af7f86e796f6a492439cf33d32e86e2821e5d53`

```dockerfile
```

-	Layers:
	-	`sha256:31ce1e16c0f3d7abae8bc0efe43af72972bbd0ad16996cf8d2391f3b156f3157`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 3.8 MB (3833993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed60376235a19d21a3bc7539e491b7b2cc161cd5be8779f7bc4f164f89dfcb66`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 30.1 KB (30116 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0746802702a74ec5aff3d42b147bf79009930f9fe302008b196e6913611d72a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117747432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac246e9fee30242e9029dc5403edbf47bd307f757d029c250fa982852e4f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1f56bda2c885d9f1e31d259816bc9f820e00480b474983310e505ff222d1d5`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f9b7dd88b413f261ccabd88d0f60d76c59a2ccff27c91e73bceff3e6a1096`  
		Last Modified: Sat, 03 Feb 2024 08:39:33 GMT  
		Size: 84.9 MB (84852008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d5faa0696f2842d59a27b1e48950260cbd936e7bdb64e05c1752240bfbb347`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c38821881ee98a1d77f74b9f6586a33b7396fb8eb4d935d2b7427a177f46ed9`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 7.8 KB (7827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5` - unknown; unknown

```console
$ docker pull mariadb@sha256:7aa4aefc37f9588c672ca720115da4f9859263f33e581feecd3bf3e965a4ecda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3869700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e7c406dbf0b084dba5fc128f2443a697e44bad17b583c769ac694713940326`

```dockerfile
```

-	Layers:
	-	`sha256:1bba7c0f7171c4a2386545e6eb3fd94146731dd3ec48ee17c248988d3191874b`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 3.8 MB (3839735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4b17cb189697aa2367a74d4db0d2d6c5e5d50fe69763b23a0ef01d401d7854`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 30.0 KB (29965 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:21583837164e1cf7d2e712dac5d000145b2112b9d9036a29eb939f184b24bff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130219532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b54f5dae406fd12fecd15968972c8b8beb2fedb5ac890617bf26ad6125c4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5473a32ba2cdac3805cec8f8b94092533874ae8b71e7059994fb9b0d0a0dbc66`  
		Last Modified: Fri, 02 Feb 2024 20:28:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83fcc60eac60e57da2ef78153783dc15193618480e1fb8dcdb16941bd9330c3`  
		Last Modified: Fri, 02 Feb 2024 20:28:35 GMT  
		Size: 90.2 MB (90222288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb3c2a906ddab7297f492916e2643220ad727c749486e1e59f5cf632a1d4426`  
		Last Modified: Fri, 02 Feb 2024 20:28:32 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d36e260fe80138a3bb7e1d85fcd8405999dba1df13c7106d43f29cd9f10ed6`  
		Last Modified: Fri, 02 Feb 2024 20:28:33 GMT  
		Size: 7.8 KB (7828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5` - unknown; unknown

```console
$ docker pull mariadb@sha256:b1bbc902bca3122aa8840f9500f982f2d347f9f26d7f96a8eb3023cb9367492e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3871449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512311cd5f8c4de7a6c4d750249924fe3f29974f1d22dde94e49529bf873a82c`

```dockerfile
```

-	Layers:
	-	`sha256:6314615ba1e0c50db15eafadb58d0b8b03c5b27f0c73d78de818f0ee4fa83646`  
		Last Modified: Fri, 02 Feb 2024 20:28:32 GMT  
		Size: 3.8 MB (3841448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68371d51bc3949268380a9fc21a5b74593b29acb17bdbcc9ccd360739285c96b`  
		Last Modified: Fri, 02 Feb 2024 20:28:32 GMT  
		Size: 30.0 KB (30001 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:9e31d22be09db688f72de1aae3400112655a326ecee41bba12121dbdf0445857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118832808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab7dcdf36d19977d83e6640cd6ea07a321b3ec3b094501c994d3881c3f8e91b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5c9202eb73d17302f2cc366ebffe022abacde01c41e47c6d408a29334a481207`  
		Last Modified: Tue, 23 Jan 2024 13:11:03 GMT  
		Size: 26.4 MB (26362871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed9217481ad5b0e6b234febae22dae05f21c67694d46dd0814b05c025a277c9`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0386a00da775a17d229fd684d3ccdc2d6e1301c4c5b4473d6a9982862a3f75`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 6.7 MB (6731600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5be0c831f9a1faa69481048daca5554c5da1d0d53c3bbad83de80999dfaf81`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c991e4808ef177192ae7507d9323675d3ee0a7ade8b23f015def43b81a51aa`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ce20b93185c191d142d6aab9df1e8cd4e02728aa2c0a755a936dad7ee51926`  
		Last Modified: Thu, 08 Feb 2024 18:47:44 GMT  
		Size: 85.7 MB (85724716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d936623a39b7945de6d96796c57fe7cfb59433c260e46073b7de8b93fa73e617`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a468e22320c0ce8b4d725815840a66fb785650470c6fa86d7fd9ebe0d5ce1f`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 7.8 KB (7827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5` - unknown; unknown

```console
$ docker pull mariadb@sha256:6c25056fc9fce0c3bde5853440a96e50e11869c4816f8ed53b0fe7e719028c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3863446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f3ff8edb4ff41d56594117270fcfe9fd957abd194d4abe8c6900fe202aa7a`

```dockerfile
```

-	Layers:
	-	`sha256:eca081b1a43f5409745cc69b216994371516494031a6a2d201ad5bb1f9786873`  
		Last Modified: Thu, 08 Feb 2024 18:47:43 GMT  
		Size: 3.8 MB (3833491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33103960b4782382f2516a32cb2359be18e42f49509f027cd613aa5c0d51502f`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 30.0 KB (29955 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:6122f729893e286a3cfc789fb546dd041cf244e4de84272ab5727028ca107730
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

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:44b025abf54f798e7a9ac95d543b1f1d3dc80af1769237f6d5f72d807bdb61aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.5 MB (120457080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52fc3807752990d5e6f85c7f4eed70f53cea3523985d58dfdb761eba2c5720ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ce84e449118f88e0ddd38f8b6fd0d855d0ab2f08b34a7a81347fac8fe19f29`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6663e8686f0a932a93d852a4b401e50c7318c4d86d40e9cc3b55dc896cbcdb`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 7.2 MB (7179046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4ed2974b5cda9f7ca6150129676130f01f5e096903b207ca3e8d9eb5ecc616`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37cccd2cd8ec5d0229c304416a55ef48808f6396f6a4e918a9c4af2fe441aba`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f7ecfc90a594d28f7477caabe0ea0ba78b1aa79f19838bc5ea1c86631050df`  
		Last Modified: Fri, 02 Feb 2024 00:55:55 GMT  
		Size: 85.7 MB (85749495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34018581dae4c4db7e4c62a3fbf652c8c72429c8d88f689a7eb79db7805278f`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fcf1e0fdf4fa145ad4c170f2a17c231b64416c6894173e7394cc23ae440935`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 7.8 KB (7828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:41a68d6d6843364a8ec5856f0bc9c71e72c3723b309438210c14e7e0af8d2ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3864109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685c0e666156371d45e300309af7f86e796f6a492439cf33d32e86e2821e5d53`

```dockerfile
```

-	Layers:
	-	`sha256:31ce1e16c0f3d7abae8bc0efe43af72972bbd0ad16996cf8d2391f3b156f3157`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 3.8 MB (3833993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed60376235a19d21a3bc7539e491b7b2cc161cd5be8779f7bc4f164f89dfcb66`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 30.1 KB (30116 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0746802702a74ec5aff3d42b147bf79009930f9fe302008b196e6913611d72a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117747432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ac246e9fee30242e9029dc5403edbf47bd307f757d029c250fa982852e4f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1f56bda2c885d9f1e31d259816bc9f820e00480b474983310e505ff222d1d5`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3f9b7dd88b413f261ccabd88d0f60d76c59a2ccff27c91e73bceff3e6a1096`  
		Last Modified: Sat, 03 Feb 2024 08:39:33 GMT  
		Size: 84.9 MB (84852008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d5faa0696f2842d59a27b1e48950260cbd936e7bdb64e05c1752240bfbb347`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c38821881ee98a1d77f74b9f6586a33b7396fb8eb4d935d2b7427a177f46ed9`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 7.8 KB (7827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:7aa4aefc37f9588c672ca720115da4f9859263f33e581feecd3bf3e965a4ecda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3869700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e7c406dbf0b084dba5fc128f2443a697e44bad17b583c769ac694713940326`

```dockerfile
```

-	Layers:
	-	`sha256:1bba7c0f7171c4a2386545e6eb3fd94146731dd3ec48ee17c248988d3191874b`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 3.8 MB (3839735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f4b17cb189697aa2367a74d4db0d2d6c5e5d50fe69763b23a0ef01d401d7854`  
		Last Modified: Sat, 03 Feb 2024 08:39:30 GMT  
		Size: 30.0 KB (29965 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:21583837164e1cf7d2e712dac5d000145b2112b9d9036a29eb939f184b24bff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130219532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b54f5dae406fd12fecd15968972c8b8beb2fedb5ac890617bf26ad6125c4d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5473a32ba2cdac3805cec8f8b94092533874ae8b71e7059994fb9b0d0a0dbc66`  
		Last Modified: Fri, 02 Feb 2024 20:28:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83fcc60eac60e57da2ef78153783dc15193618480e1fb8dcdb16941bd9330c3`  
		Last Modified: Fri, 02 Feb 2024 20:28:35 GMT  
		Size: 90.2 MB (90222288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb3c2a906ddab7297f492916e2643220ad727c749486e1e59f5cf632a1d4426`  
		Last Modified: Fri, 02 Feb 2024 20:28:32 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d36e260fe80138a3bb7e1d85fcd8405999dba1df13c7106d43f29cd9f10ed6`  
		Last Modified: Fri, 02 Feb 2024 20:28:33 GMT  
		Size: 7.8 KB (7828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:b1bbc902bca3122aa8840f9500f982f2d347f9f26d7f96a8eb3023cb9367492e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3871449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512311cd5f8c4de7a6c4d750249924fe3f29974f1d22dde94e49529bf873a82c`

```dockerfile
```

-	Layers:
	-	`sha256:6314615ba1e0c50db15eafadb58d0b8b03c5b27f0c73d78de818f0ee4fa83646`  
		Last Modified: Fri, 02 Feb 2024 20:28:32 GMT  
		Size: 3.8 MB (3841448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68371d51bc3949268380a9fc21a5b74593b29acb17bdbcc9ccd360739285c96b`  
		Last Modified: Fri, 02 Feb 2024 20:28:32 GMT  
		Size: 30.0 KB (30001 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:9e31d22be09db688f72de1aae3400112655a326ecee41bba12121dbdf0445857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118832808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab7dcdf36d19977d83e6640cd6ea07a321b3ec3b094501c994d3881c3f8e91b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.23 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.5.23+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.5 MARIADB_VERSION=1:10.5.23+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.23/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5c9202eb73d17302f2cc366ebffe022abacde01c41e47c6d408a29334a481207`  
		Last Modified: Tue, 23 Jan 2024 13:11:03 GMT  
		Size: 26.4 MB (26362871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed9217481ad5b0e6b234febae22dae05f21c67694d46dd0814b05c025a277c9`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0386a00da775a17d229fd684d3ccdc2d6e1301c4c5b4473d6a9982862a3f75`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 6.7 MB (6731600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5be0c831f9a1faa69481048daca5554c5da1d0d53c3bbad83de80999dfaf81`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c991e4808ef177192ae7507d9323675d3ee0a7ade8b23f015def43b81a51aa`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ce20b93185c191d142d6aab9df1e8cd4e02728aa2c0a755a936dad7ee51926`  
		Last Modified: Thu, 08 Feb 2024 18:47:44 GMT  
		Size: 85.7 MB (85724716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d936623a39b7945de6d96796c57fe7cfb59433c260e46073b7de8b93fa73e617`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a468e22320c0ce8b4d725815840a66fb785650470c6fa86d7fd9ebe0d5ce1f`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 7.8 KB (7827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.5-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:6c25056fc9fce0c3bde5853440a96e50e11869c4816f8ed53b0fe7e719028c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3863446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f3ff8edb4ff41d56594117270fcfe9fd957abd194d4abe8c6900fe202aa7a`

```dockerfile
```

-	Layers:
	-	`sha256:eca081b1a43f5409745cc69b216994371516494031a6a2d201ad5bb1f9786873`  
		Last Modified: Thu, 08 Feb 2024 18:47:43 GMT  
		Size: 3.8 MB (3833491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33103960b4782382f2516a32cb2359be18e42f49509f027cd613aa5c0d51502f`  
		Last Modified: Thu, 08 Feb 2024 18:47:42 GMT  
		Size: 30.0 KB (29955 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.5.24`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:10.5.24-focal`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:cd2d6086da91f818b197b7c9abff87131b6b19dd401203191c10934091aaf41f
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

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:00d41c8b5d61c1c1904896fcf98029c5d5f7deaf21d4adb03e0d00d955fc1bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120797399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fbb70b8165849c093d7dfae33673a4ea4397cfd03ac26a733fd0118c76c8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51589605430e66e3b5fd9380ed027882b39737b51eb22e481cc16aac3adad4b`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb7b492b7f37f3124bd5419320aad67c048189a87e0d6d2234a1b8046fd67fe`  
		Last Modified: Fri, 02 Feb 2024 00:56:32 GMT  
		Size: 7.2 MB (7179068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc81bb9b5369af07109453d808885b63c33561b7092904c49bafd4490fb17ec`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39d74f2bf878b0b92f4383eaddd65e6ae50314610a7e8fb8aecab9527423c5`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb78610af4c419a86e6b33cdc86b25507cdffb50054c0b904750087d20465b`  
		Last Modified: Fri, 02 Feb 2024 00:56:36 GMT  
		Size: 86.1 MB (86089766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845e15a8b24e0c6644c5e2b30fd832997b671d22a684c5f2d99ae7772d9af681`  
		Last Modified: Fri, 02 Feb 2024 00:56:32 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6a85711210dec051fa5617920458373f9cc588e961616d5b1efcb4c31e4d26`  
		Last Modified: Fri, 02 Feb 2024 00:56:32 GMT  
		Size: 7.9 KB (7854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6` - unknown; unknown

```console
$ docker pull mariadb@sha256:a1bfdaf894885817149005c6ca06f38b7fed329a4e274c58d50fc8dec2cc01e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3874254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d845aeb711c6d0b094b14208f852fa3f85ddddf4461f371893b35f942d92c3a`

```dockerfile
```

-	Layers:
	-	`sha256:07d6d5b56bcb8d35cde533e7dcb2c3396fcc94bd756b71c1213fffccd5135d72`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 3.8 MB (3844139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d337cf4ab25212e9e272799de7c3cde7865758bbd6e5fc843e643580d9ab6eca`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 30.1 KB (30115 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0b18d9dea5b9cbaa11c5ede8836fb4dca6115005de8c5a4a026082b4b9baf313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117966229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edee1a5d6675f93d9cdc2b153b09e01e544625586c714b8d5042a1de60a8722a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d345fcfa15b2d2d569854ebaaa373b4fc9a4e09aed502d02b61244a0758e6ab`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9f008870dd15551117bfa82e3fbdabd053d6672cde1bfaccb3401f30862fe2`  
		Last Modified: Sat, 03 Feb 2024 08:38:43 GMT  
		Size: 85.1 MB (85070780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc5dad2c352ca17b99f1fd98ec30f4f063db4bb148f0ea94c5c5fd737508b6d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114a94044d354bf8fe2736c0d16dd1c5f2aef360d955923fe9c62c01e6a2a1c0`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6` - unknown; unknown

```console
$ docker pull mariadb@sha256:4d30e85d201665baa2dcc9b5b68b267cb87786e95fb6c60e46193e60820d8a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3879847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769bf02e98160ad65425d1f8b336200bab4b9a0842bc5e8d5788ed5442cf249d`

```dockerfile
```

-	Layers:
	-	`sha256:d29e83ffbc11846e14d6cc6440424cc6e9558e3c826fd07ae35314ffc26ee629`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 3.8 MB (3849882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69fb10134ed8f6941a8d2b2591a94279b89d3d79588b5c77aa85d2158bda87a9`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 30.0 KB (29965 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b0f8f7c52b2706adeaf09cab8540074c91e4e1a4308bcb7b0966f458bf142da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130384217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb70cff4c0ea67399688254f9ea4cf384da69e4faf95e974bd9ec784fea65a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cda1e88568eb5427aa68804053b1f6ba5ffab41a79025d08fa2577223212cd`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05942b3b1d61439d30fd273e34a0ade64d055d8a22ef04bf2265207182c0400a`  
		Last Modified: Fri, 02 Feb 2024 20:26:44 GMT  
		Size: 90.4 MB (90386944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23bd512688135e396809f42eb826e8207df1a35d60cd8d513dd6e8746cc0c7b`  
		Last Modified: Fri, 02 Feb 2024 20:26:42 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc670c946ab0fbe5e2fb20b536dbc026af998adc6e37b8261fed5e7a7765d7`  
		Last Modified: Fri, 02 Feb 2024 20:26:42 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6` - unknown; unknown

```console
$ docker pull mariadb@sha256:f511e6f916a2434c109b5db62fdd6b5a04236a814f26e1b9a8989028da8eceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3881763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503018c6ddd67416b811f3a714b9b441b653cf38da69f8044be48b0531b5e139`

```dockerfile
```

-	Layers:
	-	`sha256:a499b94491376e38f613a10f2528f02b69a8ca4acae409d004ea790132a2ac87`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 3.9 MB (3851601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b369ac102c0b4b5bc5405097c3b300bb2e2ecd45e9a2846e9609c55f80ddb404`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 30.2 KB (30162 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:0456e9c9beb2a49e9216b09772047412ded72f90ff0068b94a9f5e14334f59c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118995427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc0bb91aa060af37a9f9629583e332b9b3c50e400732648d5b83560b87e9878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5c9202eb73d17302f2cc366ebffe022abacde01c41e47c6d408a29334a481207`  
		Last Modified: Tue, 23 Jan 2024 13:11:03 GMT  
		Size: 26.4 MB (26362871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed9217481ad5b0e6b234febae22dae05f21c67694d46dd0814b05c025a277c9`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0386a00da775a17d229fd684d3ccdc2d6e1301c4c5b4473d6a9982862a3f75`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 6.7 MB (6731600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5be0c831f9a1faa69481048daca5554c5da1d0d53c3bbad83de80999dfaf81`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486c6ebb8923e12a47ed8f0d409677abf58d3a6ea4bd34ab1cb04b08ec0950a`  
		Last Modified: Thu, 08 Feb 2024 18:38:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54af88263ea60ee0c6c90aeb5e64cb7b6b8793df3d4f59d2cc98d97f5d54a27`  
		Last Modified: Thu, 08 Feb 2024 18:38:59 GMT  
		Size: 85.9 MB (85887308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85612fb92f0fdfe44b148d4a11895c6b71665709cb8e9cac214749616128fa08`  
		Last Modified: Thu, 08 Feb 2024 18:38:59 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ece91a010bc15264d1d186e06aa1514f207b4347ae7a6b3832d626751e865b`  
		Last Modified: Thu, 08 Feb 2024 18:38:58 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6` - unknown; unknown

```console
$ docker pull mariadb@sha256:233ff0c5d5b98f278a2f224422e524adc1bbb5e4160e58fa6fcba546ebd28bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3866889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4cd70f93dcbfd9464660f4216c28226ca4152805845cc3251c7f3b3f1d754`

```dockerfile
```

-	Layers:
	-	`sha256:e1fc9d32b45ccc5808e61824e2afd7b6417593d98a8d2055e95af2496a9649f9`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 3.8 MB (3836934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a106be96a698931731779f3bf895141ff5e17ce92399d588176192f596ebc1`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 30.0 KB (29955 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:cd2d6086da91f818b197b7c9abff87131b6b19dd401203191c10934091aaf41f
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

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:00d41c8b5d61c1c1904896fcf98029c5d5f7deaf21d4adb03e0d00d955fc1bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120797399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fbb70b8165849c093d7dfae33673a4ea4397cfd03ac26a733fd0118c76c8e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8ee0874247356ecb5ea92128219660506b139dcb6cc45dcab84d98b3c6485061`  
		Last Modified: Tue, 23 Jan 2024 13:10:37 GMT  
		Size: 27.5 MB (27514928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51589605430e66e3b5fd9380ed027882b39737b51eb22e481cc16aac3adad4b`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb7b492b7f37f3124bd5419320aad67c048189a87e0d6d2234a1b8046fd67fe`  
		Last Modified: Fri, 02 Feb 2024 00:56:32 GMT  
		Size: 7.2 MB (7179068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc81bb9b5369af07109453d808885b63c33561b7092904c49bafd4490fb17ec`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc39d74f2bf878b0b92f4383eaddd65e6ae50314610a7e8fb8aecab9527423c5`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccb78610af4c419a86e6b33cdc86b25507cdffb50054c0b904750087d20465b`  
		Last Modified: Fri, 02 Feb 2024 00:56:36 GMT  
		Size: 86.1 MB (86089766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845e15a8b24e0c6644c5e2b30fd832997b671d22a684c5f2d99ae7772d9af681`  
		Last Modified: Fri, 02 Feb 2024 00:56:32 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6a85711210dec051fa5617920458373f9cc588e961616d5b1efcb4c31e4d26`  
		Last Modified: Fri, 02 Feb 2024 00:56:32 GMT  
		Size: 7.9 KB (7854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:a1bfdaf894885817149005c6ca06f38b7fed329a4e274c58d50fc8dec2cc01e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3874254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d845aeb711c6d0b094b14208f852fa3f85ddddf4461f371893b35f942d92c3a`

```dockerfile
```

-	Layers:
	-	`sha256:07d6d5b56bcb8d35cde533e7dcb2c3396fcc94bd756b71c1213fffccd5135d72`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 3.8 MB (3844139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d337cf4ab25212e9e272799de7c3cde7865758bbd6e5fc843e643580d9ab6eca`  
		Last Modified: Fri, 02 Feb 2024 00:56:31 GMT  
		Size: 30.1 KB (30115 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0b18d9dea5b9cbaa11c5ede8836fb4dca6115005de8c5a4a026082b4b9baf313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.0 MB (117966229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edee1a5d6675f93d9cdc2b153b09e01e544625586c714b8d5042a1de60a8722a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9497e9dbcde9a04e764625c77c975cfced1dd0bb3bb7717572ea47621f3c12a7 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bc5b5b7ccd1e19c62fdfc4688b98b69619822aab7431a47a392d5795347d854f`  
		Last Modified: Tue, 23 Jan 2024 13:10:43 GMT  
		Size: 26.0 MB (25975597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cf7962aa45fb27b0ee385e0055d511f417519d36598b4cfdcd08b66e97d40`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06186067ba21672592cc2ed56831e6c8762373c8a22fdbf1f8257071d9f0f50d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 6.9 MB (6906207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78439c680642d51b23e0011a26a3adc8b3e24f67d0f80dec754cb136305e3dc4`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d345fcfa15b2d2d569854ebaaa373b4fc9a4e09aed502d02b61244a0758e6ab`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9f008870dd15551117bfa82e3fbdabd053d6672cde1bfaccb3401f30862fe2`  
		Last Modified: Sat, 03 Feb 2024 08:38:43 GMT  
		Size: 85.1 MB (85070780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc5dad2c352ca17b99f1fd98ec30f4f063db4bb148f0ea94c5c5fd737508b6d`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114a94044d354bf8fe2736c0d16dd1c5f2aef360d955923fe9c62c01e6a2a1c0`  
		Last Modified: Sat, 03 Feb 2024 08:38:41 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:4d30e85d201665baa2dcc9b5b68b267cb87786e95fb6c60e46193e60820d8a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3879847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769bf02e98160ad65425d1f8b336200bab4b9a0842bc5e8d5788ed5442cf249d`

```dockerfile
```

-	Layers:
	-	`sha256:d29e83ffbc11846e14d6cc6440424cc6e9558e3c826fd07ae35314ffc26ee629`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 3.8 MB (3849882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69fb10134ed8f6941a8d2b2591a94279b89d3d79588b5c77aa85d2158bda87a9`  
		Last Modified: Sat, 03 Feb 2024 08:38:40 GMT  
		Size: 30.0 KB (29965 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b0f8f7c52b2706adeaf09cab8540074c91e4e1a4308bcb7b0966f458bf142da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130384217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb70cff4c0ea67399688254f9ea4cf384da69e4faf95e974bd9ec784fea65a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:96f44a86185939ee5de23552dc064d300ba16f7f31dc2d5ea1081d99cb0ecc9f in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:487202f3bdb365605d5ba731764af67c0bdaf9e0aaf27d8fcc97ea51b6c8e624`  
		Last Modified: Tue, 23 Jan 2024 13:10:56 GMT  
		Size: 32.1 MB (32076570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5a0061493d8daf5bed561527ac1e5a20198bf4a26a277abd0f69f186a53bd5`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d9b09c03e5de434fdc1e27d12b1f205eceaaeb610a57b966dcb45602fb6dc`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 7.9 MB (7907044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264cd88eb2159584ed6077df4e3484d04445db9be40cab944e8ea20e9b4ee12`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cda1e88568eb5427aa68804053b1f6ba5ffab41a79025d08fa2577223212cd`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05942b3b1d61439d30fd273e34a0ade64d055d8a22ef04bf2265207182c0400a`  
		Last Modified: Fri, 02 Feb 2024 20:26:44 GMT  
		Size: 90.4 MB (90386944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23bd512688135e396809f42eb826e8207df1a35d60cd8d513dd6e8746cc0c7b`  
		Last Modified: Fri, 02 Feb 2024 20:26:42 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc670c946ab0fbe5e2fb20b536dbc026af998adc6e37b8261fed5e7a7765d7`  
		Last Modified: Fri, 02 Feb 2024 20:26:42 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:f511e6f916a2434c109b5db62fdd6b5a04236a814f26e1b9a8989028da8eceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3881763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503018c6ddd67416b811f3a714b9b441b653cf38da69f8044be48b0531b5e139`

```dockerfile
```

-	Layers:
	-	`sha256:a499b94491376e38f613a10f2528f02b69a8ca4acae409d004ea790132a2ac87`  
		Last Modified: Fri, 02 Feb 2024 20:26:41 GMT  
		Size: 3.9 MB (3851601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b369ac102c0b4b5bc5405097c3b300bb2e2ecd45e9a2846e9609c55f80ddb404`  
		Last Modified: Fri, 02 Feb 2024 20:26:40 GMT  
		Size: 30.2 KB (30162 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:0456e9c9beb2a49e9216b09772047412ded72f90ff0068b94a9f5e14334f59c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.0 MB (118995427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc0bb91aa060af37a9f9629583e332b9b3c50e400732648d5b83560b87e9878`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:9688c7fb864a2f858b61b1962f9c2236540bc2d74ee75df78412ca5655b0c9da in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.16 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.6.16+maria~ubu2004
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_MAJOR=10.6 MARIADB_VERSION=1:10.6.16+maria~ubu2004 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.16/repo/ubuntu/ focal main main/debug
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5c9202eb73d17302f2cc366ebffe022abacde01c41e47c6d408a29334a481207`  
		Last Modified: Tue, 23 Jan 2024 13:11:03 GMT  
		Size: 26.4 MB (26362871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed9217481ad5b0e6b234febae22dae05f21c67694d46dd0814b05c025a277c9`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0386a00da775a17d229fd684d3ccdc2d6e1301c4c5b4473d6a9982862a3f75`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 6.7 MB (6731600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5be0c831f9a1faa69481048daca5554c5da1d0d53c3bbad83de80999dfaf81`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3486c6ebb8923e12a47ed8f0d409677abf58d3a6ea4bd34ab1cb04b08ec0950a`  
		Last Modified: Thu, 08 Feb 2024 18:38:57 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54af88263ea60ee0c6c90aeb5e64cb7b6b8793df3d4f59d2cc98d97f5d54a27`  
		Last Modified: Thu, 08 Feb 2024 18:38:59 GMT  
		Size: 85.9 MB (85887308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85612fb92f0fdfe44b148d4a11895c6b71665709cb8e9cac214749616128fa08`  
		Last Modified: Thu, 08 Feb 2024 18:38:59 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ece91a010bc15264d1d186e06aa1514f207b4347ae7a6b3832d626751e865b`  
		Last Modified: Thu, 08 Feb 2024 18:38:58 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10.6-focal` - unknown; unknown

```console
$ docker pull mariadb@sha256:233ff0c5d5b98f278a2f224422e524adc1bbb5e4160e58fa6fcba546ebd28bf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3866889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee4cd70f93dcbfd9464660f4216c28226ca4152805845cc3251c7f3b3f1d754`

```dockerfile
```

-	Layers:
	-	`sha256:e1fc9d32b45ccc5808e61824e2afd7b6417593d98a8d2055e95af2496a9649f9`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 3.8 MB (3836934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a106be96a698931731779f3bf895141ff5e17ce92399d588176192f596ebc1`  
		Last Modified: Thu, 08 Feb 2024 18:38:56 GMT  
		Size: 30.0 KB (29955 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:10.6.17`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:10.6.17-focal`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:11`

```console
$ docker pull mariadb@sha256:c5077bb44d13a3f34dadb5a15861149e29b3251d1e24036d2dad9611dc9d940b
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

### `mariadb:11` - linux; amd64

```console
$ docker pull mariadb@sha256:ac933f87a5fc8b743a3c522179116ee63aec31105795dc28dea8b80bb74cdd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122624938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2b86cbac506ee1dca87b9bc6bddd0afb59d14e97e111ff6579887121fedae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955af01184c592f12e5de240eda533477b01b4c0777c18fd24a03b1027b0d42`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4a36e9424429bf1441f3e646a19537016e33041f6f9cfbbcc269ffaeb0edf4`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 5.6 MB (5649815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2686694394f7ef8c31877573326b23ef14b6296a9f0307a36906267cd6526151`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8f6cdd86a74f5434d00cd45b1b1d8463cb578f0557d598be18026c41aee1ad`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1987b8fb40a553948f232cf04ef5f07b9f2cc930c3508e6250f4808c136cb4`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 87.4 MB (87412562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3122371054c90da6f4fc7b594a04d0e04d4d099119109f0a01bc791e9e7caa6`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff77ae47b7a7200a5aa62e38bd09ad59780d3c0b5d0ed51ab853b9d16534334c`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11` - unknown; unknown

```console
$ docker pull mariadb@sha256:574ad766d2c05c746e51cb7480bd17a84efb527f23403a821bfa648edfc79b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a8ffb4f8e2e8b08c3da707c0f2742eb6ac7c97e8d890a74f4123e824ab12f2`

```dockerfile
```

-	Layers:
	-	`sha256:66d53cfa8206f30e5a14160a685b1abf4b11cf01b9aaae8d14c05e24afe04b27`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 4.0 MB (3978817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975066aa3e53f5b6a6771f1c9e98dd40ac87ffa8d49a721df50cf82c5a41773c`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 31.1 KB (31110 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1d79400a715fa30c94a868100b90fd506a4eaa3c71e3ec35532c01adb956e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84779845dabc7aab31a204bd342786607ac7775eb65546a5cbc25795b9ffc167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373253c883a50b984c3ec0963a10754b26a79cf1acb5c823b7887723def0c735`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd7a3de467e91c07faa63725d43071ae72b24c75808d7007bf3a82384dc29f`  
		Last Modified: Mon, 05 Feb 2024 18:47:41 GMT  
		Size: 84.2 MB (84156653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126032fa9029463cd45e55881785774400725bdc658ccca50c927006201f534`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023d35d07ffebe8de7c713efb8a820740580a41efcd4aed3e49e653732834d2`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11` - unknown; unknown

```console
$ docker pull mariadb@sha256:515dda71994fdf0341a0432a835d212028c2bd5957610b967463f18ba4147f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a4c105771440be6fcb741da79bb9d48509e18a3799ba7c72d8f9458fdf9ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7e557dadc2d887dd8103ec45d14d7a98bc7bfb8b6cadc0e0832cff809d28621`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 4.0 MB (3984616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9ead628910db6f24ad7466fdc27798a49d613f9ea7b5d7468592a039b07562`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0ea8b05a78b3022edfe6dfd751459e4e3421500f19a56659ee3ad809e04bffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018e025309f0dbafaf79c818396f2bdd8999f44ff37bd1e695efd1c8893ed6b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49d44709db7912001f09e0851400b84f45d2382a60947871faf61b621b954a`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0be29236241cb2e0d6f222a69247de5509f6975e381255246127e3a9159a7fc`  
		Last Modified: Mon, 05 Feb 2024 18:38:07 GMT  
		Size: 90.1 MB (90104472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b5878949260cb24b8cbda0d02b8a8a266b06bd1bda88ab2ca3767f5cd41430`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd71d10a10e1e14bbfb9925e4c72610e7a3e98ef09272fbe48a61b04b780e7`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11` - unknown; unknown

```console
$ docker pull mariadb@sha256:8ba9476b7f3d90af42f5d36d8cfb3dd6eb9321ea6d4044e2c0f693d9058a1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4017562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caf27e11fe0cf4c7a6d1722627a4e599a97cf10cffa700a5d0155588067b196`

```dockerfile
```

-	Layers:
	-	`sha256:4725353045ba396686ce028810c882db371b7724ef165abbe39774e9ee46a9a5`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 4.0 MB (3986539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafab714de3738e756f7ed85afd7fcbcf669b6659307f370fbb24e854aae1eb4`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11` - linux; s390x

```console
$ docker pull mariadb@sha256:f9f49c9f007f7fd8311fa7647304065fddbdf672d1289b9c0ae12fcb06c8acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121424496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda69562b8c1ec49d8016058008cdf3963c8b7d6696fcf72121ca58586d3f0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f731715baa6e5b84de0afe5f601fa9008239b9a718d57d192b61d1baf87f7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c1253f7574b4c5f1b783cda9d5c15de7ab7c3671280ef7250ccd741bb4076`  
		Last Modified: Fri, 09 Feb 2024 00:15:22 GMT  
		Size: 87.8 MB (87847070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8b242b513bdb295d302e08b64e750979618323ac189232cee8f94000ff482`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f0ce0e7fa2138054a778a2e918545fa710c88721def8252a7b641e87c3cc7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11` - unknown; unknown

```console
$ docker pull mariadb@sha256:a170e1c48a26273490451ee23c952f7a8493039f476e10e96ad8ea2bebc65241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83514bf7822a4ed17bfbbf112388889516b2344efb6a274383c866f2f6993d9`

```dockerfile
```

-	Layers:
	-	`sha256:a82cd0ed0851eaf1b0da0a124f628956048c9dbda792d06901aa7d61ca4acd63`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 4.0 MB (3958609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b15641747d419d74d8a0b7e217a3368151a425fb99117c2580a8b4dc4508f8`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11-jammy`

```console
$ docker pull mariadb@sha256:c5077bb44d13a3f34dadb5a15861149e29b3251d1e24036d2dad9611dc9d940b
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

### `mariadb:11-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:ac933f87a5fc8b743a3c522179116ee63aec31105795dc28dea8b80bb74cdd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122624938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2b86cbac506ee1dca87b9bc6bddd0afb59d14e97e111ff6579887121fedae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955af01184c592f12e5de240eda533477b01b4c0777c18fd24a03b1027b0d42`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4a36e9424429bf1441f3e646a19537016e33041f6f9cfbbcc269ffaeb0edf4`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 5.6 MB (5649815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2686694394f7ef8c31877573326b23ef14b6296a9f0307a36906267cd6526151`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8f6cdd86a74f5434d00cd45b1b1d8463cb578f0557d598be18026c41aee1ad`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1987b8fb40a553948f232cf04ef5f07b9f2cc930c3508e6250f4808c136cb4`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 87.4 MB (87412562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3122371054c90da6f4fc7b594a04d0e04d4d099119109f0a01bc791e9e7caa6`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff77ae47b7a7200a5aa62e38bd09ad59780d3c0b5d0ed51ab853b9d16534334c`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:574ad766d2c05c746e51cb7480bd17a84efb527f23403a821bfa648edfc79b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a8ffb4f8e2e8b08c3da707c0f2742eb6ac7c97e8d890a74f4123e824ab12f2`

```dockerfile
```

-	Layers:
	-	`sha256:66d53cfa8206f30e5a14160a685b1abf4b11cf01b9aaae8d14c05e24afe04b27`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 4.0 MB (3978817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975066aa3e53f5b6a6771f1c9e98dd40ac87ffa8d49a721df50cf82c5a41773c`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 31.1 KB (31110 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1d79400a715fa30c94a868100b90fd506a4eaa3c71e3ec35532c01adb956e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84779845dabc7aab31a204bd342786607ac7775eb65546a5cbc25795b9ffc167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373253c883a50b984c3ec0963a10754b26a79cf1acb5c823b7887723def0c735`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd7a3de467e91c07faa63725d43071ae72b24c75808d7007bf3a82384dc29f`  
		Last Modified: Mon, 05 Feb 2024 18:47:41 GMT  
		Size: 84.2 MB (84156653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126032fa9029463cd45e55881785774400725bdc658ccca50c927006201f534`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023d35d07ffebe8de7c713efb8a820740580a41efcd4aed3e49e653732834d2`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:515dda71994fdf0341a0432a835d212028c2bd5957610b967463f18ba4147f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a4c105771440be6fcb741da79bb9d48509e18a3799ba7c72d8f9458fdf9ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7e557dadc2d887dd8103ec45d14d7a98bc7bfb8b6cadc0e0832cff809d28621`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 4.0 MB (3984616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9ead628910db6f24ad7466fdc27798a49d613f9ea7b5d7468592a039b07562`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0ea8b05a78b3022edfe6dfd751459e4e3421500f19a56659ee3ad809e04bffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018e025309f0dbafaf79c818396f2bdd8999f44ff37bd1e695efd1c8893ed6b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49d44709db7912001f09e0851400b84f45d2382a60947871faf61b621b954a`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0be29236241cb2e0d6f222a69247de5509f6975e381255246127e3a9159a7fc`  
		Last Modified: Mon, 05 Feb 2024 18:38:07 GMT  
		Size: 90.1 MB (90104472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b5878949260cb24b8cbda0d02b8a8a266b06bd1bda88ab2ca3767f5cd41430`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd71d10a10e1e14bbfb9925e4c72610e7a3e98ef09272fbe48a61b04b780e7`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:8ba9476b7f3d90af42f5d36d8cfb3dd6eb9321ea6d4044e2c0f693d9058a1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4017562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caf27e11fe0cf4c7a6d1722627a4e599a97cf10cffa700a5d0155588067b196`

```dockerfile
```

-	Layers:
	-	`sha256:4725353045ba396686ce028810c882db371b7724ef165abbe39774e9ee46a9a5`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 4.0 MB (3986539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafab714de3738e756f7ed85afd7fcbcf669b6659307f370fbb24e854aae1eb4`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:f9f49c9f007f7fd8311fa7647304065fddbdf672d1289b9c0ae12fcb06c8acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121424496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda69562b8c1ec49d8016058008cdf3963c8b7d6696fcf72121ca58586d3f0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f731715baa6e5b84de0afe5f601fa9008239b9a718d57d192b61d1baf87f7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c1253f7574b4c5f1b783cda9d5c15de7ab7c3671280ef7250ccd741bb4076`  
		Last Modified: Fri, 09 Feb 2024 00:15:22 GMT  
		Size: 87.8 MB (87847070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8b242b513bdb295d302e08b64e750979618323ac189232cee8f94000ff482`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f0ce0e7fa2138054a778a2e918545fa710c88721def8252a7b641e87c3cc7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a170e1c48a26273490451ee23c952f7a8493039f476e10e96ad8ea2bebc65241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83514bf7822a4ed17bfbbf112388889516b2344efb6a274383c866f2f6993d9`

```dockerfile
```

-	Layers:
	-	`sha256:a82cd0ed0851eaf1b0da0a124f628956048c9dbda792d06901aa7d61ca4acd63`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 4.0 MB (3958609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b15641747d419d74d8a0b7e217a3368151a425fb99117c2580a8b4dc4508f8`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.0`

```console
$ docker pull mariadb@sha256:33efe0652f553a4cfe81907a6510efcebc125c34def0167e7cc33f7e504d7608
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

### `mariadb:11.0` - linux; amd64

```console
$ docker pull mariadb@sha256:79dafddcfb7f8d85a1ffdf16ce761e81caaf963459060e34a1b12595eb6a9a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122375405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32413f4eb345c7ab1c75a3b9861c7347c18ddfc05a0e633873c2dbf33b05a6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14495432812618041db928192ddfb00ac40aec33e6f6b40186aff831468268cc`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f18f74619a2052cce68ca62ec8683f60e384f3cf284c38ef20ec906917be01`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 5.6 MB (5649772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5bacd0f7147199d140b0a05fdf0689548e17b2fb09842bc452a95ee865c764`  
		Last Modified: Fri, 02 Feb 2024 00:55:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3944449acc9e784cbe65adeced60bccd2017c8897ce81e9425cead70f1567b2e`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078ee6ee3b931b0bf527b4db362805fb50022f9ebc10a29afdbeceef23e5625`  
		Last Modified: Fri, 02 Feb 2024 00:55:55 GMT  
		Size: 87.2 MB (87163067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4921482d47afaf3d348aa202a65a349d3f298adc10a68775856ecb7e646b30b`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426ae17e1b0d2b91968205f023796ae3a5f9efe6f40cf264e6c6242b6b8b55bc`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0` - unknown; unknown

```console
$ docker pull mariadb@sha256:4df1aa1c37a9bc697aca8a66cdb0f8343b6ce65f31f207bfebbdc611f998ea21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d0a100a5a00ea356db5bf83b337d02f1d5e16297771f3a2e96071acd110758`

```dockerfile
```

-	Layers:
	-	`sha256:cdf4e71a4af3f0bc8dc6cfe248beeccccaeb8318b4e99211d799756fbe8fd184`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 4.0 MB (3976792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7d6cf5cbcf9c6cd8a0669d9a25203c422bfbd3dfb34ffc10546b65238e33c0`  
		Last Modified: Fri, 02 Feb 2024 00:55:51 GMT  
		Size: 29.9 KB (29920 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.0` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8cae7756795c7c92d0703f12cee75b0fc4393d0d516e19fb2145337ccb2457df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116762978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b3d411d8a46256dd94cab3c4e228627f51b519997db37dbcd13ab6532888b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5981169ab52d8861e0db279907a72b177cbe80b73b6c8b329af3d5b86752cc`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b9ecc65d1ff8fb079668a4b7efc3a69914b635179ec018e193fe4dfa33fad6`  
		Last Modified: Mon, 05 Feb 2024 18:48:22 GMT  
		Size: 83.9 MB (83929610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d386209b99c5cee28e6356033039a88b7f8b6da79b4c85448714e7d09f50656`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189e89b5eb1da55a60f6d9342ea478163f21bbebb2906e3e17eaf0405c2333d8`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0` - unknown; unknown

```console
$ docker pull mariadb@sha256:cf11f7adb73fa5ecbb34d3215ba0d46a086377c81ee30cf98017e149dda9b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4012353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2853bc8005c918183af19dbcdd0c982ff930175acb790f9e16d4f23db9a3ea2f`

```dockerfile
```

-	Layers:
	-	`sha256:f5dde9c8605c91f54416f05f9d95ef7f4bc241cb08c74f32f32ae5935c870314`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 4.0 MB (3982583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81e67581b5ef95ee1a01f6538cba8119635917f7ba0fbb19b4bd6ed48b024138`  
		Last Modified: Mon, 05 Feb 2024 18:48:18 GMT  
		Size: 29.8 KB (29770 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.0` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6df2f3330b22ae95ff67081faee2161e59a9e66f5207f5c02c08c572ed21462c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130467680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9475225e84656a1ca9d9a70d8a6ef1e5d948d8eb7b637e6e77d0adeb5a77c532`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ae90806861a551474a083784b3b84e4ad984cd94c4eaff8e2d7cca30a42ea`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0f46542a832d27086c409ecfde1e0cbc738ea487b568b624660c4427ed38c`  
		Last Modified: Mon, 05 Feb 2024 18:39:04 GMT  
		Size: 89.9 MB (89850109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49836b4a60df628bc47306cb2becc83bfca3e0630e1976e91c5c10731726c198`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330789808ecc0a64261f65bf4aecda8d4bc10ee6da811bfa5b61b3f91edcc135`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0` - unknown; unknown

```console
$ docker pull mariadb@sha256:3b889bd08ef2feaf104442fa8636f23444c5099fdbfdd3b32b853a639ba06e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d10850fbbce253a160cb78f3c87a14945cc15c7a2649c88e5e2af9a85dc535`

```dockerfile
```

-	Layers:
	-	`sha256:7f6fada290f6cd33885e9cc18d63b9fe73bef4112f1877508a279b0821598bd4`  
		Last Modified: Mon, 05 Feb 2024 18:39:02 GMT  
		Size: 4.0 MB (3984490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c074867612244f339477504e64375c7c6a0155e657ba5562b929206260a9fe94`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 29.8 KB (29806 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.0` - linux; s390x

```console
$ docker pull mariadb@sha256:d2110bc5397579eb3163a64a15a947b359f845fb6d59f0de79e0a486b905459b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121166350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a138795ac668de5f3c0cb651a24215e5fd8715aa28da37538ad3722d0867a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbb373ddcd5cd2d9e16112bb754ee30040a82d038ce4d2f9639de63c8d2c29`  
		Last Modified: Fri, 09 Feb 2024 00:16:44 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a87650d6850ad135b2d3562ed1687ba1828b1ef9c50403ac5cc2a688c45a08`  
		Last Modified: Fri, 09 Feb 2024 00:16:46 GMT  
		Size: 87.6 MB (87588919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4397400371f5f691afc08bb2ec738056c7c38e56b87107d8657989b0b8bce970`  
		Last Modified: Fri, 09 Feb 2024 00:16:45 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d874b8f1c8013c321a4538a55dfef4de92dd1d5e98ceaa883a58f7f4bbed5b29`  
		Last Modified: Fri, 09 Feb 2024 00:16:44 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0` - unknown; unknown

```console
$ docker pull mariadb@sha256:c1086733133f9081f871f86cc71c07f40786d1fa23111f386e4f671d9064de4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3986343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f859d790e801b8a83db68f809732b4d9dcd1ecabd914a3a17bf0ee4c5d0fc0`

```dockerfile
```

-	Layers:
	-	`sha256:a03e23922f63cadadd7a27cd683da9ec9b2349cfaf496efc115c3938e8ac4599`  
		Last Modified: Fri, 09 Feb 2024 00:16:45 GMT  
		Size: 4.0 MB (3956584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76dcbefa1db609b9f8f9122d3c68d3ebc0010159b043b3e1e183499f51dfbae`  
		Last Modified: Fri, 09 Feb 2024 00:16:45 GMT  
		Size: 29.8 KB (29759 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.0-jammy`

```console
$ docker pull mariadb@sha256:33efe0652f553a4cfe81907a6510efcebc125c34def0167e7cc33f7e504d7608
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

### `mariadb:11.0-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:79dafddcfb7f8d85a1ffdf16ce761e81caaf963459060e34a1b12595eb6a9a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122375405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c32413f4eb345c7ab1c75a3b9861c7347c18ddfc05a0e633873c2dbf33b05a6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14495432812618041db928192ddfb00ac40aec33e6f6b40186aff831468268cc`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f18f74619a2052cce68ca62ec8683f60e384f3cf284c38ef20ec906917be01`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 5.6 MB (5649772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5bacd0f7147199d140b0a05fdf0689548e17b2fb09842bc452a95ee865c764`  
		Last Modified: Fri, 02 Feb 2024 00:55:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3944449acc9e784cbe65adeced60bccd2017c8897ce81e9425cead70f1567b2e`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b078ee6ee3b931b0bf527b4db362805fb50022f9ebc10a29afdbeceef23e5625`  
		Last Modified: Fri, 02 Feb 2024 00:55:55 GMT  
		Size: 87.2 MB (87163067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4921482d47afaf3d348aa202a65a349d3f298adc10a68775856ecb7e646b30b`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426ae17e1b0d2b91968205f023796ae3a5f9efe6f40cf264e6c6242b6b8b55bc`  
		Last Modified: Fri, 02 Feb 2024 00:55:53 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:4df1aa1c37a9bc697aca8a66cdb0f8343b6ce65f31f207bfebbdc611f998ea21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4006712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d0a100a5a00ea356db5bf83b337d02f1d5e16297771f3a2e96071acd110758`

```dockerfile
```

-	Layers:
	-	`sha256:cdf4e71a4af3f0bc8dc6cfe248beeccccaeb8318b4e99211d799756fbe8fd184`  
		Last Modified: Fri, 02 Feb 2024 00:55:52 GMT  
		Size: 4.0 MB (3976792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d7d6cf5cbcf9c6cd8a0669d9a25203c422bfbd3dfb34ffc10546b65238e33c0`  
		Last Modified: Fri, 02 Feb 2024 00:55:51 GMT  
		Size: 29.9 KB (29920 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.0-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8cae7756795c7c92d0703f12cee75b0fc4393d0d516e19fb2145337ccb2457df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116762978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b3d411d8a46256dd94cab3c4e228627f51b519997db37dbcd13ab6532888b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5981169ab52d8861e0db279907a72b177cbe80b73b6c8b329af3d5b86752cc`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b9ecc65d1ff8fb079668a4b7efc3a69914b635179ec018e193fe4dfa33fad6`  
		Last Modified: Mon, 05 Feb 2024 18:48:22 GMT  
		Size: 83.9 MB (83929610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d386209b99c5cee28e6356033039a88b7f8b6da79b4c85448714e7d09f50656`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:189e89b5eb1da55a60f6d9342ea478163f21bbebb2906e3e17eaf0405c2333d8`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:cf11f7adb73fa5ecbb34d3215ba0d46a086377c81ee30cf98017e149dda9b6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4012353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2853bc8005c918183af19dbcdd0c982ff930175acb790f9e16d4f23db9a3ea2f`

```dockerfile
```

-	Layers:
	-	`sha256:f5dde9c8605c91f54416f05f9d95ef7f4bc241cb08c74f32f32ae5935c870314`  
		Last Modified: Mon, 05 Feb 2024 18:48:19 GMT  
		Size: 4.0 MB (3982583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81e67581b5ef95ee1a01f6538cba8119635917f7ba0fbb19b4bd6ed48b024138`  
		Last Modified: Mon, 05 Feb 2024 18:48:18 GMT  
		Size: 29.8 KB (29770 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.0-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6df2f3330b22ae95ff67081faee2161e59a9e66f5207f5c02c08c572ed21462c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130467680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9475225e84656a1ca9d9a70d8a6ef1e5d948d8eb7b637e6e77d0adeb5a77c532`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1ae90806861a551474a083784b3b84e4ad984cd94c4eaff8e2d7cca30a42ea`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68e0f46542a832d27086c409ecfde1e0cbc738ea487b568b624660c4427ed38c`  
		Last Modified: Mon, 05 Feb 2024 18:39:04 GMT  
		Size: 89.9 MB (89850109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49836b4a60df628bc47306cb2becc83bfca3e0630e1976e91c5c10731726c198`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330789808ecc0a64261f65bf4aecda8d4bc10ee6da811bfa5b61b3f91edcc135`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3b889bd08ef2feaf104442fa8636f23444c5099fdbfdd3b32b853a639ba06e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d10850fbbce253a160cb78f3c87a14945cc15c7a2649c88e5e2af9a85dc535`

```dockerfile
```

-	Layers:
	-	`sha256:7f6fada290f6cd33885e9cc18d63b9fe73bef4112f1877508a279b0821598bd4`  
		Last Modified: Mon, 05 Feb 2024 18:39:02 GMT  
		Size: 4.0 MB (3984490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c074867612244f339477504e64375c7c6a0155e657ba5562b929206260a9fe94`  
		Last Modified: Mon, 05 Feb 2024 18:39:01 GMT  
		Size: 29.8 KB (29806 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.0-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:d2110bc5397579eb3163a64a15a947b359f845fb6d59f0de79e0a486b905459b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121166350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a138795ac668de5f3c0cb651a24215e5fd8715aa28da37538ad3722d0867a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.0.4+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.0.4+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.4/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbb373ddcd5cd2d9e16112bb754ee30040a82d038ce4d2f9639de63c8d2c29`  
		Last Modified: Fri, 09 Feb 2024 00:16:44 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a87650d6850ad135b2d3562ed1687ba1828b1ef9c50403ac5cc2a688c45a08`  
		Last Modified: Fri, 09 Feb 2024 00:16:46 GMT  
		Size: 87.6 MB (87588919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4397400371f5f691afc08bb2ec738056c7c38e56b87107d8657989b0b8bce970`  
		Last Modified: Fri, 09 Feb 2024 00:16:45 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d874b8f1c8013c321a4538a55dfef4de92dd1d5e98ceaa883a58f7f4bbed5b29`  
		Last Modified: Fri, 09 Feb 2024 00:16:44 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.0-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:c1086733133f9081f871f86cc71c07f40786d1fa23111f386e4f671d9064de4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3986343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f859d790e801b8a83db68f809732b4d9dcd1ecabd914a3a17bf0ee4c5d0fc0`

```dockerfile
```

-	Layers:
	-	`sha256:a03e23922f63cadadd7a27cd683da9ec9b2349cfaf496efc115c3938e8ac4599`  
		Last Modified: Fri, 09 Feb 2024 00:16:45 GMT  
		Size: 4.0 MB (3956584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d76dcbefa1db609b9f8f9122d3c68d3ebc0010159b043b3e1e183499f51dfbae`  
		Last Modified: Fri, 09 Feb 2024 00:16:45 GMT  
		Size: 29.8 KB (29759 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.0.5`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:11.0.5-jammy`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:11.1`

```console
$ docker pull mariadb@sha256:9d85ee635c90f14bbd83bd8b508aa978230a6eff17f02b0639e80cc1f14c53a7
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

### `mariadb:11.1` - linux; amd64

```console
$ docker pull mariadb@sha256:287c6de2af0b08fbdf0f2ef7084e30c2ceb942593e0b948b6a0b05ab7c47023e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122541695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8221b60509c257f5c584a6ca999d0173c9002039ca1799abb893dd9a7bdfbd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6af74db82a81d6a19b73e7e7474024bd530a968d48d51330e83adf6e2c44c`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11733c93cbafa95dee029f90e23892563c02f466e639e46254d1f7739c679f46`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 5.6 MB (5649763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbada1f007a3dc14215b22331717716d81821dfb5d2a1e82b0a90a220edf53b8`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf24d4c2f7de1cd34fc396253eae6abdef55afd95565d75f8a4e9c770e8c87`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b1e14aafb29b1c55b50ffcdc76dd10babb04e1f56f5523005d9f23cbcbb31`  
		Last Modified: Fri, 02 Feb 2024 00:55:42 GMT  
		Size: 87.3 MB (87329371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9744c80586b95b3a959d72fe5d22e284b6a3f1c989e14cc675c30f99f1b2a58`  
		Last Modified: Fri, 02 Feb 2024 00:55:40 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b990cc35b31f103de52886a7730e0d212855deb128d5df0c99731515358d6`  
		Last Modified: Fri, 02 Feb 2024 00:55:40 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1` - unknown; unknown

```console
$ docker pull mariadb@sha256:fb49196ed27af904085b237a0c1bff07a279ed7a68f408b153ebe1f4e4fb90a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4562af9e8951b5f545e78e07262c0da2ab9873d851abd2785110ad33748d3ea1`

```dockerfile
```

-	Layers:
	-	`sha256:e4ddd326f9116619ccb396dd7d8869e207d74c1643a668137e986c102a071155`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 4.0 MB (3977623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0ea005206bd4578a840742a2ac7a12da3d345166bf961f06f85c92768339fd`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 29.9 KB (29921 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f991f28e54f2b64d9c79cadccf4776da679a386752b3e2d377805da49e310806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116878340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6a8a4c24dd680adbebd6a0c8bddf8640c2ca749d9b48f8becac5b7013ff0c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18009db60e5c7ef202bb7d696c200b155e075d46a2273378d20afa27ba937ce`  
		Last Modified: Mon, 05 Feb 2024 18:47:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15899d4379b00718f5371aaa6a7a585bdca13718c32027d1ec2f8d5107c15f2a`  
		Last Modified: Mon, 05 Feb 2024 18:48:02 GMT  
		Size: 84.0 MB (84044975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8b7a817d938201d2268c8028988a82d593cd1ac8c40daaef460a98b4ffff70`  
		Last Modified: Mon, 05 Feb 2024 18:47:59 GMT  
		Size: 3.6 KB (3604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829a50281f8d82827dd16beaf523a48531cf3133f690b1488afc0e66e716afb9`  
		Last Modified: Mon, 05 Feb 2024 18:47:59 GMT  
		Size: 7.9 KB (7854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1` - unknown; unknown

```console
$ docker pull mariadb@sha256:1e26f0d8fcb7a6f111a39d5f0f155cac6aa0fab7f498e0a74163726b1a43cc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f814abacf284be3e785d37229b2618e31366a4b37f725dcdccf09c9b8170513d`

```dockerfile
```

-	Layers:
	-	`sha256:e4c50072076c070b420d3a8f906ff88780cba7984568b5ec15b2bae0ee518449`  
		Last Modified: Mon, 05 Feb 2024 18:48:00 GMT  
		Size: 4.0 MB (3983414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db3df735a2c3bc62a58911a033601615e0981559f9588d54abb02450878e88d`  
		Last Modified: Mon, 05 Feb 2024 18:48:00 GMT  
		Size: 29.8 KB (29770 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:72dc02393fe6e85432706ba3eca44b67a5c545d306e3cb2df5dc6cb0948cfe50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130616733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d683e6039ecdc40f9c07429f571a5783e0a46662eeeaf12e0ca460a094be60d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9259c38be3c8309a3b570d5f723a35d094bd3af3ae15bb90614a1413b572ddf2`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9174b656ca99b39301a817b5e57b407e3bede744067800563f8bdc3b4e13e29e`  
		Last Modified: Mon, 05 Feb 2024 18:38:34 GMT  
		Size: 90.0 MB (89999159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd5d93fe39de2eb02f78da744e7fbe1dce9c4fa6b913c1f49c1d2312b84a919`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683e6a2960c56fc9ef050bf89416748e978ca5b967a6cb21e71cc56f4c575a6`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1` - unknown; unknown

```console
$ docker pull mariadb@sha256:f626f0faff7eade5c310387a2c7c87200711494ee41015c739fa28e6ddf990c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b14945a7094d7f4ce2add5657985fda18b8a169f5470a549dd045991694c335`

```dockerfile
```

-	Layers:
	-	`sha256:114a4b09837782a6b69ca4a556b864adfd74f5864a782170ae17b695b5382781`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 4.0 MB (3985321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171a95d6c4097cd51ac5d457ba0b96829cf32fca00e185baa0f255ac40b37752`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 29.8 KB (29805 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.1` - linux; s390x

```console
$ docker pull mariadb@sha256:cbd707002dcca1faef530daa238c271c02d7597eefa14e9901039cad494e5528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121324818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60096748906071b9f5159b2c6ce248ec79b4e429d2bca3ce0ceb2d384cce79a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98dbc2c60902e6d00d821b6b87c9f7eba9024aa6dea710f242d4454b4d10d24`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f4ff6caedb70d2b3ca25cd2e89968026e5b37dabd772510f0df803caa40f89`  
		Last Modified: Fri, 09 Feb 2024 00:16:05 GMT  
		Size: 87.7 MB (87747387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39cca83fb1eaa15529823d4011650eb591796ccb25cc2af8527397f03471ee8`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d65f57ec16d3ae78ee2fcc7e385848b58bd053456f9ab7ca7eb495d99c0674`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1` - unknown; unknown

```console
$ docker pull mariadb@sha256:ef3188b4b585237879379b9653e984a34739a9b23014110b16c8883be45f551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b21810c51643c7059e4a0b50fbd7d19d2211c2fd534e216f7289c934ca93b5`

```dockerfile
```

-	Layers:
	-	`sha256:dcb5baa68fcda95f424c6b49e9161b79fe9a829c7c771fa8c3c4a2df4685c860`  
		Last Modified: Fri, 09 Feb 2024 00:16:04 GMT  
		Size: 4.0 MB (3957415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ed2c9ee24eb95231ea4b0459693f0252bdc26e2a60c0b0e21c590b3de47f65`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 29.8 KB (29760 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.1-jammy`

```console
$ docker pull mariadb@sha256:9d85ee635c90f14bbd83bd8b508aa978230a6eff17f02b0639e80cc1f14c53a7
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

### `mariadb:11.1-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:287c6de2af0b08fbdf0f2ef7084e30c2ceb942593e0b948b6a0b05ab7c47023e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.5 MB (122541695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8221b60509c257f5c584a6ca999d0173c9002039ca1799abb893dd9a7bdfbd04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d6af74db82a81d6a19b73e7e7474024bd530a968d48d51330e83adf6e2c44c`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11733c93cbafa95dee029f90e23892563c02f466e639e46254d1f7739c679f46`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 5.6 MB (5649763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbada1f007a3dc14215b22331717716d81821dfb5d2a1e82b0a90a220edf53b8`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bf24d4c2f7de1cd34fc396253eae6abdef55afd95565d75f8a4e9c770e8c87`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608b1e14aafb29b1c55b50ffcdc76dd10babb04e1f56f5523005d9f23cbcbb31`  
		Last Modified: Fri, 02 Feb 2024 00:55:42 GMT  
		Size: 87.3 MB (87329371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9744c80586b95b3a959d72fe5d22e284b6a3f1c989e14cc675c30f99f1b2a58`  
		Last Modified: Fri, 02 Feb 2024 00:55:40 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b990cc35b31f103de52886a7730e0d212855deb128d5df0c99731515358d6`  
		Last Modified: Fri, 02 Feb 2024 00:55:40 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:fb49196ed27af904085b237a0c1bff07a279ed7a68f408b153ebe1f4e4fb90a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4562af9e8951b5f545e78e07262c0da2ab9873d851abd2785110ad33748d3ea1`

```dockerfile
```

-	Layers:
	-	`sha256:e4ddd326f9116619ccb396dd7d8869e207d74c1643a668137e986c102a071155`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 4.0 MB (3977623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0ea005206bd4578a840742a2ac7a12da3d345166bf961f06f85c92768339fd`  
		Last Modified: Fri, 02 Feb 2024 00:55:39 GMT  
		Size: 29.9 KB (29921 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.1-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f991f28e54f2b64d9c79cadccf4776da679a386752b3e2d377805da49e310806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116878340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6a8a4c24dd680adbebd6a0c8bddf8640c2ca749d9b48f8becac5b7013ff0c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18009db60e5c7ef202bb7d696c200b155e075d46a2273378d20afa27ba937ce`  
		Last Modified: Mon, 05 Feb 2024 18:47:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15899d4379b00718f5371aaa6a7a585bdca13718c32027d1ec2f8d5107c15f2a`  
		Last Modified: Mon, 05 Feb 2024 18:48:02 GMT  
		Size: 84.0 MB (84044975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e8b7a817d938201d2268c8028988a82d593cd1ac8c40daaef460a98b4ffff70`  
		Last Modified: Mon, 05 Feb 2024 18:47:59 GMT  
		Size: 3.6 KB (3604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829a50281f8d82827dd16beaf523a48531cf3133f690b1488afc0e66e716afb9`  
		Last Modified: Mon, 05 Feb 2024 18:47:59 GMT  
		Size: 7.9 KB (7854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:1e26f0d8fcb7a6f111a39d5f0f155cac6aa0fab7f498e0a74163726b1a43cc8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f814abacf284be3e785d37229b2618e31366a4b37f725dcdccf09c9b8170513d`

```dockerfile
```

-	Layers:
	-	`sha256:e4c50072076c070b420d3a8f906ff88780cba7984568b5ec15b2bae0ee518449`  
		Last Modified: Mon, 05 Feb 2024 18:48:00 GMT  
		Size: 4.0 MB (3983414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db3df735a2c3bc62a58911a033601615e0981559f9588d54abb02450878e88d`  
		Last Modified: Mon, 05 Feb 2024 18:48:00 GMT  
		Size: 29.8 KB (29770 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.1-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:72dc02393fe6e85432706ba3eca44b67a5c545d306e3cb2df5dc6cb0948cfe50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130616733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d683e6039ecdc40f9c07429f571a5783e0a46662eeeaf12e0ca460a094be60d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9259c38be3c8309a3b570d5f723a35d094bd3af3ae15bb90614a1413b572ddf2`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9174b656ca99b39301a817b5e57b407e3bede744067800563f8bdc3b4e13e29e`  
		Last Modified: Mon, 05 Feb 2024 18:38:34 GMT  
		Size: 90.0 MB (89999159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd5d93fe39de2eb02f78da744e7fbe1dce9c4fa6b913c1f49c1d2312b84a919`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683e6a2960c56fc9ef050bf89416748e978ca5b967a6cb21e71cc56f4c575a6`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:f626f0faff7eade5c310387a2c7c87200711494ee41015c739fa28e6ddf990c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b14945a7094d7f4ce2add5657985fda18b8a169f5470a549dd045991694c335`

```dockerfile
```

-	Layers:
	-	`sha256:114a4b09837782a6b69ca4a556b864adfd74f5864a782170ae17b695b5382781`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 4.0 MB (3985321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:171a95d6c4097cd51ac5d457ba0b96829cf32fca00e185baa0f255ac40b37752`  
		Last Modified: Mon, 05 Feb 2024 18:38:31 GMT  
		Size: 29.8 KB (29805 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.1-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:cbd707002dcca1faef530daa238c271c02d7597eefa14e9901039cad494e5528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121324818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60096748906071b9f5159b2c6ce248ec79b4e429d2bca3ce0ceb2d384cce79a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.1.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:11.1.3+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.1.3+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.1.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98dbc2c60902e6d00d821b6b87c9f7eba9024aa6dea710f242d4454b4d10d24`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f4ff6caedb70d2b3ca25cd2e89968026e5b37dabd772510f0df803caa40f89`  
		Last Modified: Fri, 09 Feb 2024 00:16:05 GMT  
		Size: 87.7 MB (87747387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39cca83fb1eaa15529823d4011650eb591796ccb25cc2af8527397f03471ee8`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d65f57ec16d3ae78ee2fcc7e385848b58bd053456f9ab7ca7eb495d99c0674`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 7.9 KB (7857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.1-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:ef3188b4b585237879379b9653e984a34739a9b23014110b16c8883be45f551e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b21810c51643c7059e4a0b50fbd7d19d2211c2fd534e216f7289c934ca93b5`

```dockerfile
```

-	Layers:
	-	`sha256:dcb5baa68fcda95f424c6b49e9161b79fe9a829c7c771fa8c3c4a2df4685c860`  
		Last Modified: Fri, 09 Feb 2024 00:16:04 GMT  
		Size: 4.0 MB (3957415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94ed2c9ee24eb95231ea4b0459693f0252bdc26e2a60c0b0e21c590b3de47f65`  
		Last Modified: Fri, 09 Feb 2024 00:16:03 GMT  
		Size: 29.8 KB (29760 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.1.4`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:11.1.4-jammy`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:11.2`

```console
$ docker pull mariadb@sha256:c5077bb44d13a3f34dadb5a15861149e29b3251d1e24036d2dad9611dc9d940b
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

### `mariadb:11.2` - linux; amd64

```console
$ docker pull mariadb@sha256:ac933f87a5fc8b743a3c522179116ee63aec31105795dc28dea8b80bb74cdd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122624938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2b86cbac506ee1dca87b9bc6bddd0afb59d14e97e111ff6579887121fedae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955af01184c592f12e5de240eda533477b01b4c0777c18fd24a03b1027b0d42`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4a36e9424429bf1441f3e646a19537016e33041f6f9cfbbcc269ffaeb0edf4`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 5.6 MB (5649815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2686694394f7ef8c31877573326b23ef14b6296a9f0307a36906267cd6526151`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8f6cdd86a74f5434d00cd45b1b1d8463cb578f0557d598be18026c41aee1ad`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1987b8fb40a553948f232cf04ef5f07b9f2cc930c3508e6250f4808c136cb4`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 87.4 MB (87412562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3122371054c90da6f4fc7b594a04d0e04d4d099119109f0a01bc791e9e7caa6`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff77ae47b7a7200a5aa62e38bd09ad59780d3c0b5d0ed51ab853b9d16534334c`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2` - unknown; unknown

```console
$ docker pull mariadb@sha256:574ad766d2c05c746e51cb7480bd17a84efb527f23403a821bfa648edfc79b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a8ffb4f8e2e8b08c3da707c0f2742eb6ac7c97e8d890a74f4123e824ab12f2`

```dockerfile
```

-	Layers:
	-	`sha256:66d53cfa8206f30e5a14160a685b1abf4b11cf01b9aaae8d14c05e24afe04b27`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 4.0 MB (3978817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975066aa3e53f5b6a6771f1c9e98dd40ac87ffa8d49a721df50cf82c5a41773c`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 31.1 KB (31110 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1d79400a715fa30c94a868100b90fd506a4eaa3c71e3ec35532c01adb956e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84779845dabc7aab31a204bd342786607ac7775eb65546a5cbc25795b9ffc167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373253c883a50b984c3ec0963a10754b26a79cf1acb5c823b7887723def0c735`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd7a3de467e91c07faa63725d43071ae72b24c75808d7007bf3a82384dc29f`  
		Last Modified: Mon, 05 Feb 2024 18:47:41 GMT  
		Size: 84.2 MB (84156653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126032fa9029463cd45e55881785774400725bdc658ccca50c927006201f534`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023d35d07ffebe8de7c713efb8a820740580a41efcd4aed3e49e653732834d2`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2` - unknown; unknown

```console
$ docker pull mariadb@sha256:515dda71994fdf0341a0432a835d212028c2bd5957610b967463f18ba4147f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a4c105771440be6fcb741da79bb9d48509e18a3799ba7c72d8f9458fdf9ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7e557dadc2d887dd8103ec45d14d7a98bc7bfb8b6cadc0e0832cff809d28621`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 4.0 MB (3984616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9ead628910db6f24ad7466fdc27798a49d613f9ea7b5d7468592a039b07562`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0ea8b05a78b3022edfe6dfd751459e4e3421500f19a56659ee3ad809e04bffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018e025309f0dbafaf79c818396f2bdd8999f44ff37bd1e695efd1c8893ed6b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49d44709db7912001f09e0851400b84f45d2382a60947871faf61b621b954a`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0be29236241cb2e0d6f222a69247de5509f6975e381255246127e3a9159a7fc`  
		Last Modified: Mon, 05 Feb 2024 18:38:07 GMT  
		Size: 90.1 MB (90104472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b5878949260cb24b8cbda0d02b8a8a266b06bd1bda88ab2ca3767f5cd41430`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd71d10a10e1e14bbfb9925e4c72610e7a3e98ef09272fbe48a61b04b780e7`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2` - unknown; unknown

```console
$ docker pull mariadb@sha256:8ba9476b7f3d90af42f5d36d8cfb3dd6eb9321ea6d4044e2c0f693d9058a1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4017562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caf27e11fe0cf4c7a6d1722627a4e599a97cf10cffa700a5d0155588067b196`

```dockerfile
```

-	Layers:
	-	`sha256:4725353045ba396686ce028810c882db371b7724ef165abbe39774e9ee46a9a5`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 4.0 MB (3986539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafab714de3738e756f7ed85afd7fcbcf669b6659307f370fbb24e854aae1eb4`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.2` - linux; s390x

```console
$ docker pull mariadb@sha256:f9f49c9f007f7fd8311fa7647304065fddbdf672d1289b9c0ae12fcb06c8acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121424496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda69562b8c1ec49d8016058008cdf3963c8b7d6696fcf72121ca58586d3f0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f731715baa6e5b84de0afe5f601fa9008239b9a718d57d192b61d1baf87f7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c1253f7574b4c5f1b783cda9d5c15de7ab7c3671280ef7250ccd741bb4076`  
		Last Modified: Fri, 09 Feb 2024 00:15:22 GMT  
		Size: 87.8 MB (87847070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8b242b513bdb295d302e08b64e750979618323ac189232cee8f94000ff482`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f0ce0e7fa2138054a778a2e918545fa710c88721def8252a7b641e87c3cc7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2` - unknown; unknown

```console
$ docker pull mariadb@sha256:a170e1c48a26273490451ee23c952f7a8493039f476e10e96ad8ea2bebc65241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83514bf7822a4ed17bfbbf112388889516b2344efb6a274383c866f2f6993d9`

```dockerfile
```

-	Layers:
	-	`sha256:a82cd0ed0851eaf1b0da0a124f628956048c9dbda792d06901aa7d61ca4acd63`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 4.0 MB (3958609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b15641747d419d74d8a0b7e217a3368151a425fb99117c2580a8b4dc4508f8`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.2-jammy`

```console
$ docker pull mariadb@sha256:c5077bb44d13a3f34dadb5a15861149e29b3251d1e24036d2dad9611dc9d940b
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

### `mariadb:11.2-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:ac933f87a5fc8b743a3c522179116ee63aec31105795dc28dea8b80bb74cdd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122624938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2b86cbac506ee1dca87b9bc6bddd0afb59d14e97e111ff6579887121fedae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955af01184c592f12e5de240eda533477b01b4c0777c18fd24a03b1027b0d42`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4a36e9424429bf1441f3e646a19537016e33041f6f9cfbbcc269ffaeb0edf4`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 5.6 MB (5649815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2686694394f7ef8c31877573326b23ef14b6296a9f0307a36906267cd6526151`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8f6cdd86a74f5434d00cd45b1b1d8463cb578f0557d598be18026c41aee1ad`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1987b8fb40a553948f232cf04ef5f07b9f2cc930c3508e6250f4808c136cb4`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 87.4 MB (87412562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3122371054c90da6f4fc7b594a04d0e04d4d099119109f0a01bc791e9e7caa6`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff77ae47b7a7200a5aa62e38bd09ad59780d3c0b5d0ed51ab853b9d16534334c`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:574ad766d2c05c746e51cb7480bd17a84efb527f23403a821bfa648edfc79b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a8ffb4f8e2e8b08c3da707c0f2742eb6ac7c97e8d890a74f4123e824ab12f2`

```dockerfile
```

-	Layers:
	-	`sha256:66d53cfa8206f30e5a14160a685b1abf4b11cf01b9aaae8d14c05e24afe04b27`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 4.0 MB (3978817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975066aa3e53f5b6a6771f1c9e98dd40ac87ffa8d49a721df50cf82c5a41773c`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 31.1 KB (31110 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.2-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1d79400a715fa30c94a868100b90fd506a4eaa3c71e3ec35532c01adb956e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84779845dabc7aab31a204bd342786607ac7775eb65546a5cbc25795b9ffc167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373253c883a50b984c3ec0963a10754b26a79cf1acb5c823b7887723def0c735`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd7a3de467e91c07faa63725d43071ae72b24c75808d7007bf3a82384dc29f`  
		Last Modified: Mon, 05 Feb 2024 18:47:41 GMT  
		Size: 84.2 MB (84156653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126032fa9029463cd45e55881785774400725bdc658ccca50c927006201f534`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023d35d07ffebe8de7c713efb8a820740580a41efcd4aed3e49e653732834d2`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:515dda71994fdf0341a0432a835d212028c2bd5957610b967463f18ba4147f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a4c105771440be6fcb741da79bb9d48509e18a3799ba7c72d8f9458fdf9ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7e557dadc2d887dd8103ec45d14d7a98bc7bfb8b6cadc0e0832cff809d28621`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 4.0 MB (3984616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9ead628910db6f24ad7466fdc27798a49d613f9ea7b5d7468592a039b07562`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.2-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0ea8b05a78b3022edfe6dfd751459e4e3421500f19a56659ee3ad809e04bffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018e025309f0dbafaf79c818396f2bdd8999f44ff37bd1e695efd1c8893ed6b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49d44709db7912001f09e0851400b84f45d2382a60947871faf61b621b954a`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0be29236241cb2e0d6f222a69247de5509f6975e381255246127e3a9159a7fc`  
		Last Modified: Mon, 05 Feb 2024 18:38:07 GMT  
		Size: 90.1 MB (90104472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b5878949260cb24b8cbda0d02b8a8a266b06bd1bda88ab2ca3767f5cd41430`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd71d10a10e1e14bbfb9925e4c72610e7a3e98ef09272fbe48a61b04b780e7`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:8ba9476b7f3d90af42f5d36d8cfb3dd6eb9321ea6d4044e2c0f693d9058a1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4017562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caf27e11fe0cf4c7a6d1722627a4e599a97cf10cffa700a5d0155588067b196`

```dockerfile
```

-	Layers:
	-	`sha256:4725353045ba396686ce028810c882db371b7724ef165abbe39774e9ee46a9a5`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 4.0 MB (3986539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafab714de3738e756f7ed85afd7fcbcf669b6659307f370fbb24e854aae1eb4`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.2-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:f9f49c9f007f7fd8311fa7647304065fddbdf672d1289b9c0ae12fcb06c8acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121424496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda69562b8c1ec49d8016058008cdf3963c8b7d6696fcf72121ca58586d3f0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f731715baa6e5b84de0afe5f601fa9008239b9a718d57d192b61d1baf87f7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c1253f7574b4c5f1b783cda9d5c15de7ab7c3671280ef7250ccd741bb4076`  
		Last Modified: Fri, 09 Feb 2024 00:15:22 GMT  
		Size: 87.8 MB (87847070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8b242b513bdb295d302e08b64e750979618323ac189232cee8f94000ff482`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f0ce0e7fa2138054a778a2e918545fa710c88721def8252a7b641e87c3cc7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.2-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a170e1c48a26273490451ee23c952f7a8493039f476e10e96ad8ea2bebc65241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83514bf7822a4ed17bfbbf112388889516b2344efb6a274383c866f2f6993d9`

```dockerfile
```

-	Layers:
	-	`sha256:a82cd0ed0851eaf1b0da0a124f628956048c9dbda792d06901aa7d61ca4acd63`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 4.0 MB (3958609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b15641747d419d74d8a0b7e217a3368151a425fb99117c2580a8b4dc4508f8`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.2.3`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:11.2.3-jammy`

```console
$ docker pull mariadb@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mariadb:11.3-rc`

```console
$ docker pull mariadb@sha256:36c160ba1c0d4cae0805cc3f5c28fde5b46400c70b7da806f1334cc1d517423f
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

### `mariadb:11.3-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:332e0f8981745f30340e1cbf9cd976923102d9fffb3b37b316ead0bbb32dc159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf5db6ad549950ff8b82550d8d5cbaa68f7a8d0b384c6d223b3adb61968ade3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74f64d7b4d132907452b9e1a19d68a04591eb83a97a38da977208dc43d06f5`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec6e0b2913a686c03911f1112f3cdbf085e17305ec4a5bc1895dc76fb04f789`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 5.6 MB (5649775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dac607f4be047838f47e4d7da54f1d4d61c6e0731f983623dee3dc7c38f74d2`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b714bec26853291a4584a03661c52b09aa385004e68285bea1a71e4c45b3f32`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a870a9d0295c754fd3b2aea0b0dda6587053a86236eb587c476fe0c80352a6e`  
		Last Modified: Fri, 02 Feb 2024 00:55:36 GMT  
		Size: 87.4 MB (87429697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff6f1d18a445c343943984bdc9833e7cab573d8be6ac3016e872a69bb879e6`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4cffd710a5d8bb18b3db3d9e953de6006197e7727c0e136fd44e38c784ae3c`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:374e47f167bac959bc686a18e6f253e5ca23ca3d0d9d0354eeeaf6c4f633baa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1ad3c668c87c990646b765346829f612f8133a34be96d33a89a3cec5ca288`

```dockerfile
```

-	Layers:
	-	`sha256:d135341c236caca8e3a04ea0c8b3b27df9369822e8fd6f88fffbf6abc7be7eec`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 4.0 MB (3977647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aec8f72fb8448282e96d2bb0641aef0de162f0c54d4853deda4b67f93f873b0`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 29.9 KB (29940 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d1ad8374a92921640b8543ea583eb2fcf8f6bacc227542f39c4f7367b9f9f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116999162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54db74e7561ecc4c3f842a9ca45d92cd2c4b91a2824ac676f5a0dcb570692f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd674190839afb6bc0a5e88a7527b803ec9f8de9d4f04a3b43e1b911957b143`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d20329371fec13b03e6cdfb0f54c6613667bd8140307fb3b6793483d7d809c`  
		Last Modified: Mon, 05 Feb 2024 18:47:23 GMT  
		Size: 84.2 MB (84165792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67f1d0d10c198e3b070c92bc5a1bfb2b68aa53412a8dde5c32fae8f53b37b44`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2837457af4abf5498092b01935812e6c002a9737782c967a09c1b175502a9d4f`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:531a855ec0311fb43e67f0c24a59b0692a35575220184ddb8fbef49387079bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ebb42503c06e14f639319c410401d476ffe9c5f8c548c0febbbd235db28313`

```dockerfile
```

-	Layers:
	-	`sha256:b8126668093de506c67200db97cbb5e1c40e9d2533213f526dc47853e8d12d1b`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 4.0 MB (3983438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac65880360e2a3f6eb212b56de0762b27b6cabd2453b4886885369a745441221`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 29.8 KB (29788 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eaaee1ac75c75b8104129dba271452f1fcb301d2b7b7c8a96529e738e5c579f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130737909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8411eddd2c4e42159978430d86e04ed09bedabc84c915e51e41c319f7c83dcf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e283e52d05285c8ada27d1d2a00480598a3f4a020aad2a6e08ada53ebfdcb860`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d4196df52219b6044a8263283d0baf322dba803f86b2d6bf017074288aec2d`  
		Last Modified: Mon, 05 Feb 2024 18:37:39 GMT  
		Size: 90.1 MB (90120338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80f0af7ca188004a195bbb310ed4da7df1ed78644b631aeb60157af3a56f78`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4d2395e43c753e475cbe1cf2818198cc885c9535cd8d57713dbd1cd48da25`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:c6f3100bb0ed761f272f83748f99764d172f36a49cb999d97fa0d484b0864338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f67baa3dcfe39a05723db7018251ca4e09e043bcd6794ed5343de21047292`

```dockerfile
```

-	Layers:
	-	`sha256:850d211abe6ad9b70cb933e9953e0f96d1473858b9ba09dbe4773227d66ca9a6`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 4.0 MB (3985345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bedb363d19ec5ae9cfb4f687ff6f267654fbda40fc86b9d22a82806eca5ffb0d`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 29.8 KB (29825 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:1f69db0e71f43a4b02f97077c22a51962bf9cfee9a787e1c5845f6743e85f5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121421040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd60fdb30625d0acea1f21cb5612e7875c217f45dee2bd082e4fc8977a7167c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910844cfc24ca382d794ae664d7c5eb9e86838e59a51548c283acfa4fe0586`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b29ace7b3860531e2df7027c2c5c7f7764fb548085b3b41509352e8fc47b2d`  
		Last Modified: Thu, 08 Feb 2024 23:57:03 GMT  
		Size: 87.8 MB (87843615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec3bf1b0539a2377ddb716c1693047d0c287485f68ff1932e194e68f8c480ed`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4799e4b5f399d1ffeaadd2aa6087b8212791fdb11e486ce3af0a579fe90513`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:a35d5699bb4d23f3e89582d53b239152f9f0cdce5d34fa39a890d40116c09f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024493704ba9cb4685acfaba8d303f2a638b146ae0ee12134d6776736ac90fba`

```dockerfile
```

-	Layers:
	-	`sha256:8aa7c8d53fe8347b22edc2239890ee2a1e455329e2cd19794abac6c9e0fa8cd6`  
		Last Modified: Thu, 08 Feb 2024 23:57:02 GMT  
		Size: 4.0 MB (3957439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4cfe9313fa1231a431562e297d0edc1064c3e0164b6a6fe92a7d21c94f8437`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 29.8 KB (29779 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.3-rc-jammy`

```console
$ docker pull mariadb@sha256:36c160ba1c0d4cae0805cc3f5c28fde5b46400c70b7da806f1334cc1d517423f
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

### `mariadb:11.3-rc-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:332e0f8981745f30340e1cbf9cd976923102d9fffb3b37b316ead0bbb32dc159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf5db6ad549950ff8b82550d8d5cbaa68f7a8d0b384c6d223b3adb61968ade3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74f64d7b4d132907452b9e1a19d68a04591eb83a97a38da977208dc43d06f5`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec6e0b2913a686c03911f1112f3cdbf085e17305ec4a5bc1895dc76fb04f789`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 5.6 MB (5649775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dac607f4be047838f47e4d7da54f1d4d61c6e0731f983623dee3dc7c38f74d2`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b714bec26853291a4584a03661c52b09aa385004e68285bea1a71e4c45b3f32`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a870a9d0295c754fd3b2aea0b0dda6587053a86236eb587c476fe0c80352a6e`  
		Last Modified: Fri, 02 Feb 2024 00:55:36 GMT  
		Size: 87.4 MB (87429697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff6f1d18a445c343943984bdc9833e7cab573d8be6ac3016e872a69bb879e6`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4cffd710a5d8bb18b3db3d9e953de6006197e7727c0e136fd44e38c784ae3c`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:374e47f167bac959bc686a18e6f253e5ca23ca3d0d9d0354eeeaf6c4f633baa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1ad3c668c87c990646b765346829f612f8133a34be96d33a89a3cec5ca288`

```dockerfile
```

-	Layers:
	-	`sha256:d135341c236caca8e3a04ea0c8b3b27df9369822e8fd6f88fffbf6abc7be7eec`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 4.0 MB (3977647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aec8f72fb8448282e96d2bb0641aef0de162f0c54d4853deda4b67f93f873b0`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 29.9 KB (29940 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3-rc-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d1ad8374a92921640b8543ea583eb2fcf8f6bacc227542f39c4f7367b9f9f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116999162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54db74e7561ecc4c3f842a9ca45d92cd2c4b91a2824ac676f5a0dcb570692f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd674190839afb6bc0a5e88a7527b803ec9f8de9d4f04a3b43e1b911957b143`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d20329371fec13b03e6cdfb0f54c6613667bd8140307fb3b6793483d7d809c`  
		Last Modified: Mon, 05 Feb 2024 18:47:23 GMT  
		Size: 84.2 MB (84165792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67f1d0d10c198e3b070c92bc5a1bfb2b68aa53412a8dde5c32fae8f53b37b44`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2837457af4abf5498092b01935812e6c002a9737782c967a09c1b175502a9d4f`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:531a855ec0311fb43e67f0c24a59b0692a35575220184ddb8fbef49387079bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ebb42503c06e14f639319c410401d476ffe9c5f8c548c0febbbd235db28313`

```dockerfile
```

-	Layers:
	-	`sha256:b8126668093de506c67200db97cbb5e1c40e9d2533213f526dc47853e8d12d1b`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 4.0 MB (3983438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac65880360e2a3f6eb212b56de0762b27b6cabd2453b4886885369a745441221`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 29.8 KB (29788 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3-rc-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eaaee1ac75c75b8104129dba271452f1fcb301d2b7b7c8a96529e738e5c579f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130737909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8411eddd2c4e42159978430d86e04ed09bedabc84c915e51e41c319f7c83dcf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e283e52d05285c8ada27d1d2a00480598a3f4a020aad2a6e08ada53ebfdcb860`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d4196df52219b6044a8263283d0baf322dba803f86b2d6bf017074288aec2d`  
		Last Modified: Mon, 05 Feb 2024 18:37:39 GMT  
		Size: 90.1 MB (90120338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80f0af7ca188004a195bbb310ed4da7df1ed78644b631aeb60157af3a56f78`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4d2395e43c753e475cbe1cf2818198cc885c9535cd8d57713dbd1cd48da25`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:c6f3100bb0ed761f272f83748f99764d172f36a49cb999d97fa0d484b0864338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f67baa3dcfe39a05723db7018251ca4e09e043bcd6794ed5343de21047292`

```dockerfile
```

-	Layers:
	-	`sha256:850d211abe6ad9b70cb933e9953e0f96d1473858b9ba09dbe4773227d66ca9a6`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 4.0 MB (3985345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bedb363d19ec5ae9cfb4f687ff6f267654fbda40fc86b9d22a82806eca5ffb0d`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 29.8 KB (29825 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3-rc-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:1f69db0e71f43a4b02f97077c22a51962bf9cfee9a787e1c5845f6743e85f5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121421040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd60fdb30625d0acea1f21cb5612e7875c217f45dee2bd082e4fc8977a7167c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910844cfc24ca382d794ae664d7c5eb9e86838e59a51548c283acfa4fe0586`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b29ace7b3860531e2df7027c2c5c7f7764fb548085b3b41509352e8fc47b2d`  
		Last Modified: Thu, 08 Feb 2024 23:57:03 GMT  
		Size: 87.8 MB (87843615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec3bf1b0539a2377ddb716c1693047d0c287485f68ff1932e194e68f8c480ed`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4799e4b5f399d1ffeaadd2aa6087b8212791fdb11e486ce3af0a579fe90513`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a35d5699bb4d23f3e89582d53b239152f9f0cdce5d34fa39a890d40116c09f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024493704ba9cb4685acfaba8d303f2a638b146ae0ee12134d6776736ac90fba`

```dockerfile
```

-	Layers:
	-	`sha256:8aa7c8d53fe8347b22edc2239890ee2a1e455329e2cd19794abac6c9e0fa8cd6`  
		Last Modified: Thu, 08 Feb 2024 23:57:02 GMT  
		Size: 4.0 MB (3957439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4cfe9313fa1231a431562e297d0edc1064c3e0164b6a6fe92a7d21c94f8437`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 29.8 KB (29779 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.3.1-rc`

```console
$ docker pull mariadb@sha256:36c160ba1c0d4cae0805cc3f5c28fde5b46400c70b7da806f1334cc1d517423f
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

### `mariadb:11.3.1-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:332e0f8981745f30340e1cbf9cd976923102d9fffb3b37b316ead0bbb32dc159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf5db6ad549950ff8b82550d8d5cbaa68f7a8d0b384c6d223b3adb61968ade3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74f64d7b4d132907452b9e1a19d68a04591eb83a97a38da977208dc43d06f5`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec6e0b2913a686c03911f1112f3cdbf085e17305ec4a5bc1895dc76fb04f789`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 5.6 MB (5649775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dac607f4be047838f47e4d7da54f1d4d61c6e0731f983623dee3dc7c38f74d2`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b714bec26853291a4584a03661c52b09aa385004e68285bea1a71e4c45b3f32`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a870a9d0295c754fd3b2aea0b0dda6587053a86236eb587c476fe0c80352a6e`  
		Last Modified: Fri, 02 Feb 2024 00:55:36 GMT  
		Size: 87.4 MB (87429697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff6f1d18a445c343943984bdc9833e7cab573d8be6ac3016e872a69bb879e6`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4cffd710a5d8bb18b3db3d9e953de6006197e7727c0e136fd44e38c784ae3c`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:374e47f167bac959bc686a18e6f253e5ca23ca3d0d9d0354eeeaf6c4f633baa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1ad3c668c87c990646b765346829f612f8133a34be96d33a89a3cec5ca288`

```dockerfile
```

-	Layers:
	-	`sha256:d135341c236caca8e3a04ea0c8b3b27df9369822e8fd6f88fffbf6abc7be7eec`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 4.0 MB (3977647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aec8f72fb8448282e96d2bb0641aef0de162f0c54d4853deda4b67f93f873b0`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 29.9 KB (29940 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3.1-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d1ad8374a92921640b8543ea583eb2fcf8f6bacc227542f39c4f7367b9f9f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116999162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54db74e7561ecc4c3f842a9ca45d92cd2c4b91a2824ac676f5a0dcb570692f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd674190839afb6bc0a5e88a7527b803ec9f8de9d4f04a3b43e1b911957b143`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d20329371fec13b03e6cdfb0f54c6613667bd8140307fb3b6793483d7d809c`  
		Last Modified: Mon, 05 Feb 2024 18:47:23 GMT  
		Size: 84.2 MB (84165792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67f1d0d10c198e3b070c92bc5a1bfb2b68aa53412a8dde5c32fae8f53b37b44`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2837457af4abf5498092b01935812e6c002a9737782c967a09c1b175502a9d4f`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:531a855ec0311fb43e67f0c24a59b0692a35575220184ddb8fbef49387079bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ebb42503c06e14f639319c410401d476ffe9c5f8c548c0febbbd235db28313`

```dockerfile
```

-	Layers:
	-	`sha256:b8126668093de506c67200db97cbb5e1c40e9d2533213f526dc47853e8d12d1b`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 4.0 MB (3983438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac65880360e2a3f6eb212b56de0762b27b6cabd2453b4886885369a745441221`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 29.8 KB (29788 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3.1-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eaaee1ac75c75b8104129dba271452f1fcb301d2b7b7c8a96529e738e5c579f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130737909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8411eddd2c4e42159978430d86e04ed09bedabc84c915e51e41c319f7c83dcf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e283e52d05285c8ada27d1d2a00480598a3f4a020aad2a6e08ada53ebfdcb860`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d4196df52219b6044a8263283d0baf322dba803f86b2d6bf017074288aec2d`  
		Last Modified: Mon, 05 Feb 2024 18:37:39 GMT  
		Size: 90.1 MB (90120338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80f0af7ca188004a195bbb310ed4da7df1ed78644b631aeb60157af3a56f78`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4d2395e43c753e475cbe1cf2818198cc885c9535cd8d57713dbd1cd48da25`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:c6f3100bb0ed761f272f83748f99764d172f36a49cb999d97fa0d484b0864338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f67baa3dcfe39a05723db7018251ca4e09e043bcd6794ed5343de21047292`

```dockerfile
```

-	Layers:
	-	`sha256:850d211abe6ad9b70cb933e9953e0f96d1473858b9ba09dbe4773227d66ca9a6`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 4.0 MB (3985345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bedb363d19ec5ae9cfb4f687ff6f267654fbda40fc86b9d22a82806eca5ffb0d`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 29.8 KB (29825 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3.1-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:1f69db0e71f43a4b02f97077c22a51962bf9cfee9a787e1c5845f6743e85f5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121421040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd60fdb30625d0acea1f21cb5612e7875c217f45dee2bd082e4fc8977a7167c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910844cfc24ca382d794ae664d7c5eb9e86838e59a51548c283acfa4fe0586`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b29ace7b3860531e2df7027c2c5c7f7764fb548085b3b41509352e8fc47b2d`  
		Last Modified: Thu, 08 Feb 2024 23:57:03 GMT  
		Size: 87.8 MB (87843615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec3bf1b0539a2377ddb716c1693047d0c287485f68ff1932e194e68f8c480ed`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4799e4b5f399d1ffeaadd2aa6087b8212791fdb11e486ce3af0a579fe90513`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc` - unknown; unknown

```console
$ docker pull mariadb@sha256:a35d5699bb4d23f3e89582d53b239152f9f0cdce5d34fa39a890d40116c09f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024493704ba9cb4685acfaba8d303f2a638b146ae0ee12134d6776736ac90fba`

```dockerfile
```

-	Layers:
	-	`sha256:8aa7c8d53fe8347b22edc2239890ee2a1e455329e2cd19794abac6c9e0fa8cd6`  
		Last Modified: Thu, 08 Feb 2024 23:57:02 GMT  
		Size: 4.0 MB (3957439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4cfe9313fa1231a431562e297d0edc1064c3e0164b6a6fe92a7d21c94f8437`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 29.8 KB (29779 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:11.3.1-rc-jammy`

```console
$ docker pull mariadb@sha256:36c160ba1c0d4cae0805cc3f5c28fde5b46400c70b7da806f1334cc1d517423f
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

### `mariadb:11.3.1-rc-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:332e0f8981745f30340e1cbf9cd976923102d9fffb3b37b316ead0bbb32dc159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122642031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf5db6ad549950ff8b82550d8d5cbaa68f7a8d0b384c6d223b3adb61968ade3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f74f64d7b4d132907452b9e1a19d68a04591eb83a97a38da977208dc43d06f5`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec6e0b2913a686c03911f1112f3cdbf085e17305ec4a5bc1895dc76fb04f789`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 5.6 MB (5649775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dac607f4be047838f47e4d7da54f1d4d61c6e0731f983623dee3dc7c38f74d2`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b714bec26853291a4584a03661c52b09aa385004e68285bea1a71e4c45b3f32`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a870a9d0295c754fd3b2aea0b0dda6587053a86236eb587c476fe0c80352a6e`  
		Last Modified: Fri, 02 Feb 2024 00:55:36 GMT  
		Size: 87.4 MB (87429697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ff6f1d18a445c343943984bdc9833e7cab573d8be6ac3016e872a69bb879e6`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4cffd710a5d8bb18b3db3d9e953de6006197e7727c0e136fd44e38c784ae3c`  
		Last Modified: Fri, 02 Feb 2024 00:55:35 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:374e47f167bac959bc686a18e6f253e5ca23ca3d0d9d0354eeeaf6c4f633baa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4007587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a1ad3c668c87c990646b765346829f612f8133a34be96d33a89a3cec5ca288`

```dockerfile
```

-	Layers:
	-	`sha256:d135341c236caca8e3a04ea0c8b3b27df9369822e8fd6f88fffbf6abc7be7eec`  
		Last Modified: Fri, 02 Feb 2024 00:55:34 GMT  
		Size: 4.0 MB (3977647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aec8f72fb8448282e96d2bb0641aef0de162f0c54d4853deda4b67f93f873b0`  
		Last Modified: Fri, 02 Feb 2024 00:55:33 GMT  
		Size: 29.9 KB (29940 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3.1-rc-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d1ad8374a92921640b8543ea583eb2fcf8f6bacc227542f39c4f7367b9f9f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116999162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54db74e7561ecc4c3f842a9ca45d92cd2c4b91a2824ac676f5a0dcb570692f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd674190839afb6bc0a5e88a7527b803ec9f8de9d4f04a3b43e1b911957b143`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d20329371fec13b03e6cdfb0f54c6613667bd8140307fb3b6793483d7d809c`  
		Last Modified: Mon, 05 Feb 2024 18:47:23 GMT  
		Size: 84.2 MB (84165792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b67f1d0d10c198e3b070c92bc5a1bfb2b68aa53412a8dde5c32fae8f53b37b44`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2837457af4abf5498092b01935812e6c002a9737782c967a09c1b175502a9d4f`  
		Last Modified: Mon, 05 Feb 2024 18:47:21 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:531a855ec0311fb43e67f0c24a59b0692a35575220184ddb8fbef49387079bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74ebb42503c06e14f639319c410401d476ffe9c5f8c548c0febbbd235db28313`

```dockerfile
```

-	Layers:
	-	`sha256:b8126668093de506c67200db97cbb5e1c40e9d2533213f526dc47853e8d12d1b`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 4.0 MB (3983438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac65880360e2a3f6eb212b56de0762b27b6cabd2453b4886885369a745441221`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 29.8 KB (29788 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3.1-rc-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:eaaee1ac75c75b8104129dba271452f1fcb301d2b7b7c8a96529e738e5c579f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130737909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8411eddd2c4e42159978430d86e04ed09bedabc84c915e51e41c319f7c83dcf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e283e52d05285c8ada27d1d2a00480598a3f4a020aad2a6e08ada53ebfdcb860`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d4196df52219b6044a8263283d0baf322dba803f86b2d6bf017074288aec2d`  
		Last Modified: Mon, 05 Feb 2024 18:37:39 GMT  
		Size: 90.1 MB (90120338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b80f0af7ca188004a195bbb310ed4da7df1ed78644b631aeb60157af3a56f78`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4d2395e43c753e475cbe1cf2818198cc885c9535cd8d57713dbd1cd48da25`  
		Last Modified: Mon, 05 Feb 2024 18:37:37 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:c6f3100bb0ed761f272f83748f99764d172f36a49cb999d97fa0d484b0864338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f67baa3dcfe39a05723db7018251ca4e09e043bcd6794ed5343de21047292`

```dockerfile
```

-	Layers:
	-	`sha256:850d211abe6ad9b70cb933e9953e0f96d1473858b9ba09dbe4773227d66ca9a6`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 4.0 MB (3985345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bedb363d19ec5ae9cfb4f687ff6f267654fbda40fc86b9d22a82806eca5ffb0d`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 29.8 KB (29825 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11.3.1-rc-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:1f69db0e71f43a4b02f97077c22a51962bf9cfee9a787e1c5845f6743e85f5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121421040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd60fdb30625d0acea1f21cb5612e7875c217f45dee2bd082e4fc8977a7167c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.3.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.3.1+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.3.1+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.3.1/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4910844cfc24ca382d794ae664d7c5eb9e86838e59a51548c283acfa4fe0586`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b29ace7b3860531e2df7027c2c5c7f7764fb548085b3b41509352e8fc47b2d`  
		Last Modified: Thu, 08 Feb 2024 23:57:03 GMT  
		Size: 87.8 MB (87843615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec3bf1b0539a2377ddb716c1693047d0c287485f68ff1932e194e68f8c480ed`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4799e4b5f399d1ffeaadd2aa6087b8212791fdb11e486ce3af0a579fe90513`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11.3.1-rc-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a35d5699bb4d23f3e89582d53b239152f9f0cdce5d34fa39a890d40116c09f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:024493704ba9cb4685acfaba8d303f2a638b146ae0ee12134d6776736ac90fba`

```dockerfile
```

-	Layers:
	-	`sha256:8aa7c8d53fe8347b22edc2239890ee2a1e455329e2cd19794abac6c9e0fa8cd6`  
		Last Modified: Thu, 08 Feb 2024 23:57:02 GMT  
		Size: 4.0 MB (3957439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b4cfe9313fa1231a431562e297d0edc1064c3e0164b6a6fe92a7d21c94f8437`  
		Last Modified: Thu, 08 Feb 2024 23:57:01 GMT  
		Size: 29.8 KB (29779 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:jammy`

```console
$ docker pull mariadb@sha256:c5077bb44d13a3f34dadb5a15861149e29b3251d1e24036d2dad9611dc9d940b
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

### `mariadb:jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:ac933f87a5fc8b743a3c522179116ee63aec31105795dc28dea8b80bb74cdd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122624938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2b86cbac506ee1dca87b9bc6bddd0afb59d14e97e111ff6579887121fedae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955af01184c592f12e5de240eda533477b01b4c0777c18fd24a03b1027b0d42`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4a36e9424429bf1441f3e646a19537016e33041f6f9cfbbcc269ffaeb0edf4`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 5.6 MB (5649815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2686694394f7ef8c31877573326b23ef14b6296a9f0307a36906267cd6526151`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8f6cdd86a74f5434d00cd45b1b1d8463cb578f0557d598be18026c41aee1ad`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1987b8fb40a553948f232cf04ef5f07b9f2cc930c3508e6250f4808c136cb4`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 87.4 MB (87412562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3122371054c90da6f4fc7b594a04d0e04d4d099119109f0a01bc791e9e7caa6`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff77ae47b7a7200a5aa62e38bd09ad59780d3c0b5d0ed51ab853b9d16534334c`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:574ad766d2c05c746e51cb7480bd17a84efb527f23403a821bfa648edfc79b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a8ffb4f8e2e8b08c3da707c0f2742eb6ac7c97e8d890a74f4123e824ab12f2`

```dockerfile
```

-	Layers:
	-	`sha256:66d53cfa8206f30e5a14160a685b1abf4b11cf01b9aaae8d14c05e24afe04b27`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 4.0 MB (3978817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975066aa3e53f5b6a6771f1c9e98dd40ac87ffa8d49a721df50cf82c5a41773c`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 31.1 KB (31110 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1d79400a715fa30c94a868100b90fd506a4eaa3c71e3ec35532c01adb956e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84779845dabc7aab31a204bd342786607ac7775eb65546a5cbc25795b9ffc167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373253c883a50b984c3ec0963a10754b26a79cf1acb5c823b7887723def0c735`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd7a3de467e91c07faa63725d43071ae72b24c75808d7007bf3a82384dc29f`  
		Last Modified: Mon, 05 Feb 2024 18:47:41 GMT  
		Size: 84.2 MB (84156653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126032fa9029463cd45e55881785774400725bdc658ccca50c927006201f534`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023d35d07ffebe8de7c713efb8a820740580a41efcd4aed3e49e653732834d2`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:515dda71994fdf0341a0432a835d212028c2bd5957610b967463f18ba4147f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a4c105771440be6fcb741da79bb9d48509e18a3799ba7c72d8f9458fdf9ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7e557dadc2d887dd8103ec45d14d7a98bc7bfb8b6cadc0e0832cff809d28621`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 4.0 MB (3984616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9ead628910db6f24ad7466fdc27798a49d613f9ea7b5d7468592a039b07562`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0ea8b05a78b3022edfe6dfd751459e4e3421500f19a56659ee3ad809e04bffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018e025309f0dbafaf79c818396f2bdd8999f44ff37bd1e695efd1c8893ed6b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49d44709db7912001f09e0851400b84f45d2382a60947871faf61b621b954a`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0be29236241cb2e0d6f222a69247de5509f6975e381255246127e3a9159a7fc`  
		Last Modified: Mon, 05 Feb 2024 18:38:07 GMT  
		Size: 90.1 MB (90104472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b5878949260cb24b8cbda0d02b8a8a266b06bd1bda88ab2ca3767f5cd41430`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd71d10a10e1e14bbfb9925e4c72610e7a3e98ef09272fbe48a61b04b780e7`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:8ba9476b7f3d90af42f5d36d8cfb3dd6eb9321ea6d4044e2c0f693d9058a1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4017562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caf27e11fe0cf4c7a6d1722627a4e599a97cf10cffa700a5d0155588067b196`

```dockerfile
```

-	Layers:
	-	`sha256:4725353045ba396686ce028810c882db371b7724ef165abbe39774e9ee46a9a5`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 4.0 MB (3986539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafab714de3738e756f7ed85afd7fcbcf669b6659307f370fbb24e854aae1eb4`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:f9f49c9f007f7fd8311fa7647304065fddbdf672d1289b9c0ae12fcb06c8acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121424496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda69562b8c1ec49d8016058008cdf3963c8b7d6696fcf72121ca58586d3f0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f731715baa6e5b84de0afe5f601fa9008239b9a718d57d192b61d1baf87f7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c1253f7574b4c5f1b783cda9d5c15de7ab7c3671280ef7250ccd741bb4076`  
		Last Modified: Fri, 09 Feb 2024 00:15:22 GMT  
		Size: 87.8 MB (87847070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8b242b513bdb295d302e08b64e750979618323ac189232cee8f94000ff482`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f0ce0e7fa2138054a778a2e918545fa710c88721def8252a7b641e87c3cc7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:a170e1c48a26273490451ee23c952f7a8493039f476e10e96ad8ea2bebc65241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83514bf7822a4ed17bfbbf112388889516b2344efb6a274383c866f2f6993d9`

```dockerfile
```

-	Layers:
	-	`sha256:a82cd0ed0851eaf1b0da0a124f628956048c9dbda792d06901aa7d61ca4acd63`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 4.0 MB (3958609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b15641747d419d74d8a0b7e217a3368151a425fb99117c2580a8b4dc4508f8`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:c5077bb44d13a3f34dadb5a15861149e29b3251d1e24036d2dad9611dc9d940b
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

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:ac933f87a5fc8b743a3c522179116ee63aec31105795dc28dea8b80bb74cdd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122624938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf2b86cbac506ee1dca87b9bc6bddd0afb59d14e97e111ff6579887121fedae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d955af01184c592f12e5de240eda533477b01b4c0777c18fd24a03b1027b0d42`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4a36e9424429bf1441f3e646a19537016e33041f6f9cfbbcc269ffaeb0edf4`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 5.6 MB (5649815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2686694394f7ef8c31877573326b23ef14b6296a9f0307a36906267cd6526151`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8f6cdd86a74f5434d00cd45b1b1d8463cb578f0557d598be18026c41aee1ad`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1987b8fb40a553948f232cf04ef5f07b9f2cc930c3508e6250f4808c136cb4`  
		Last Modified: Fri, 02 Feb 2024 00:56:01 GMT  
		Size: 87.4 MB (87412562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3122371054c90da6f4fc7b594a04d0e04d4d099119109f0a01bc791e9e7caa6`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff77ae47b7a7200a5aa62e38bd09ad59780d3c0b5d0ed51ab853b9d16534334c`  
		Last Modified: Fri, 02 Feb 2024 00:56:00 GMT  
		Size: 7.9 KB (7858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:574ad766d2c05c746e51cb7480bd17a84efb527f23403a821bfa648edfc79b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a8ffb4f8e2e8b08c3da707c0f2742eb6ac7c97e8d890a74f4123e824ab12f2`

```dockerfile
```

-	Layers:
	-	`sha256:66d53cfa8206f30e5a14160a685b1abf4b11cf01b9aaae8d14c05e24afe04b27`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 4.0 MB (3978817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:975066aa3e53f5b6a6771f1c9e98dd40ac87ffa8d49a721df50cf82c5a41773c`  
		Last Modified: Fri, 02 Feb 2024 00:55:59 GMT  
		Size: 31.1 KB (31110 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1d79400a715fa30c94a868100b90fd506a4eaa3c71e3ec35532c01adb956e117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (116990022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84779845dabc7aab31a204bd342786607ac7775eb65546a5cbc25795b9ffc167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373253c883a50b984c3ec0963a10754b26a79cf1acb5c823b7887723def0c735`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd7a3de467e91c07faa63725d43071ae72b24c75808d7007bf3a82384dc29f`  
		Last Modified: Mon, 05 Feb 2024 18:47:41 GMT  
		Size: 84.2 MB (84156653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126032fa9029463cd45e55881785774400725bdc658ccca50c927006201f534`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d023d35d07ffebe8de7c713efb8a820740580a41efcd4aed3e49e653732834d2`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 7.9 KB (7855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:515dda71994fdf0341a0432a835d212028c2bd5957610b967463f18ba4147f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a4c105771440be6fcb741da79bb9d48509e18a3799ba7c72d8f9458fdf9ac5`

```dockerfile
```

-	Layers:
	-	`sha256:e7e557dadc2d887dd8103ec45d14d7a98bc7bfb8b6cadc0e0832cff809d28621`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 4.0 MB (3984616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a9ead628910db6f24ad7466fdc27798a49d613f9ea7b5d7468592a039b07562`  
		Last Modified: Mon, 05 Feb 2024 18:47:39 GMT  
		Size: 31.0 KB (30971 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0ea8b05a78b3022edfe6dfd751459e4e3421500f19a56659ee3ad809e04bffa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130722045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018e025309f0dbafaf79c818396f2bdd8999f44ff37bd1e695efd1c8893ed6b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e49d44709db7912001f09e0851400b84f45d2382a60947871faf61b621b954a`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0be29236241cb2e0d6f222a69247de5509f6975e381255246127e3a9159a7fc`  
		Last Modified: Mon, 05 Feb 2024 18:38:07 GMT  
		Size: 90.1 MB (90104472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b5878949260cb24b8cbda0d02b8a8a266b06bd1bda88ab2ca3767f5cd41430`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabd71d10a10e1e14bbfb9925e4c72610e7a3e98ef09272fbe48a61b04b780e7`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 7.9 KB (7860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:8ba9476b7f3d90af42f5d36d8cfb3dd6eb9321ea6d4044e2c0f693d9058a1fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4017562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4caf27e11fe0cf4c7a6d1722627a4e599a97cf10cffa700a5d0155588067b196`

```dockerfile
```

-	Layers:
	-	`sha256:4725353045ba396686ce028810c882db371b7724ef165abbe39774e9ee46a9a5`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 4.0 MB (3986539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cafab714de3738e756f7ed85afd7fcbcf669b6659307f370fbb24e854aae1eb4`  
		Last Modified: Mon, 05 Feb 2024 18:38:03 GMT  
		Size: 31.0 KB (31023 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:f9f49c9f007f7fd8311fa7647304065fddbdf672d1289b9c0ae12fcb06c8acab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.4 MB (121424496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda69562b8c1ec49d8016058008cdf3963c8b7d6696fcf72121ca58586d3f0ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 21 Nov 2023 20:35:25 GMT
ARG RELEASE
# Tue, 21 Nov 2023 20:35:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 21 Nov 2023 20:35:25 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["/bin/bash"]
# Tue, 21 Nov 2023 20:35:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Nov 2023 20:35:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENV LANG=C.UTF-8
# Tue, 21 Nov 2023 20:35:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 21 Nov 2023 20:35:25 GMT
ARG MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ENV MARIADB_VERSION=1:11.2.2+maria~ubu2204
# Tue, 21 Nov 2023 20:35:25 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.2.2+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-11.2.2/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Nov 2023 20:35:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Nov 2023 20:35:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Nov 2023 20:35:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 21 Nov 2023 20:35:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f731715baa6e5b84de0afe5f601fa9008239b9a718d57d192b61d1baf87f7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c1253f7574b4c5f1b783cda9d5c15de7ab7c3671280ef7250ccd741bb4076`  
		Last Modified: Fri, 09 Feb 2024 00:15:22 GMT  
		Size: 87.8 MB (87847070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd8b242b513bdb295d302e08b64e750979618323ac189232cee8f94000ff482`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 3.6 KB (3607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571f0ce0e7fa2138054a778a2e918545fa710c88721def8252a7b641e87c3cc7`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:latest` - unknown; unknown

```console
$ docker pull mariadb@sha256:a170e1c48a26273490451ee23c952f7a8493039f476e10e96ad8ea2bebc65241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83514bf7822a4ed17bfbbf112388889516b2344efb6a274383c866f2f6993d9`

```dockerfile
```

-	Layers:
	-	`sha256:a82cd0ed0851eaf1b0da0a124f628956048c9dbda792d06901aa7d61ca4acd63`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 4.0 MB (3958609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b15641747d419d74d8a0b7e217a3368151a425fb99117c2580a8b4dc4508f8`  
		Last Modified: Fri, 09 Feb 2024 00:15:20 GMT  
		Size: 31.0 KB (30953 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:lts`

```console
$ docker pull mariadb@sha256:e846701e66dcc95a3f90d161cc3dfc2e4ff96f0699ee4fb93b0bfdab94158570
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

### `mariadb:lts` - linux; amd64

```console
$ docker pull mariadb@sha256:0a2c136bd7f771adcefe93b8cc828dcb9a451d93b305492fcc463f882f96b97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122395734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2af619908a56210a704427edea5839fba25c251122ca86271237062d897c1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e214e6737d8fb8119eb73eae3a8a55490b4c07e064ec530b1bed3fe736594f6f`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f0c6ea1b52a52ab6e042dd36ea7bf8a0c1826037654587893a868a854777`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 5.6 MB (5649827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b26a2f888b920916b631650e255030a0494c2e3c6ef060632fa240f6030cadc`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edc50b97c9b432709bd588e9f59fedaf1a60d45eec041a0192beb9deec14f15`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c975760206132ac66e98815e4323904597653188888a5e4a3da026030f6097`  
		Last Modified: Fri, 02 Feb 2024 00:55:44 GMT  
		Size: 87.2 MB (87183335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259c8eda6426e8ce56810e1d485c1da7991bd7ec6c900c18cbf0c19515afe13b`  
		Last Modified: Fri, 02 Feb 2024 00:55:42 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5ed3fd578b20ea5386d4be91e760920cf9991ae5efc053fae8cf9d063f58a5`  
		Last Modified: Fri, 02 Feb 2024 00:55:43 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:9b17ce98f87e2c9c5f52e6177212d72cecdaefeb32a42e13d5b528de20b4d2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0404cfd9352cc0e9af40f9f69e7985146377bed4e5a77b5021da95690c9245`

```dockerfile
```

-	Layers:
	-	`sha256:56011a0ab0ed0d64db1bcdd3b9d4712da39e07b84d7a479a6d61660fe513b567`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 4.0 MB (3978012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5aa8c9707979b58d1f13363b1741a6942a77801965ae30484e07487e2705c1b`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8d8ad390991307f339d27efd7758a72ce341141ed4f15de6a7db830c804278a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116767777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72247e4f4e004912b60f31958d2f81c3a078d57c89ff083e9e9c06e1b1d9f23e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365b92ace3793f0f4866adfec3489c0cea407aeb634855349e47065e91d4fd2e`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84abd8f0444f7c22644c3e04048f2825fc559130187470d64c3c6f9dedca9f30`  
		Last Modified: Mon, 05 Feb 2024 18:48:47 GMT  
		Size: 83.9 MB (83934404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e281a2c2bfe3b777b13c4259f37339b4a32093caf1c249638514136dd8595407`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce32ed88d7c667f6c49a294c905e6c253b2ad293bc1de2d74341ddec621f5c8d`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:22d87b66cad7e1d7fa241e20e94a3718b1f6dbc31573e2a40b6d3aff5f43ba50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4513a269427ed8c1efbaa1bfd3698aa9b37c71e4fb34dcf6d14122023c77cb17`

```dockerfile
```

-	Layers:
	-	`sha256:ea81eff742933d3a5ab08c0e54f55d3f5eacff8a17c9198933f6fc8d89d9227f`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 4.0 MB (3983811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9102af544a235121e2cb799452c0ee14691573b0253311b83d1df076a2c7695e`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 31.0 KB (30992 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:01bcacc2aa40042682a3a5d3413fd1a9d17c0cefd408884453157b345ca922eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130493872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fa1289158a6e8c0cbeaf39abb3c3c4311a98f0fe8c0e6b2728ceb4119fe89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562917155b8699e9edb268af81b9adff9da719522a737fdad7b898b80dce226`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d884a7e8a1a8f8bff42660029e457b0e2c9abb60b57fa687633210360fdc7e8b`  
		Last Modified: Mon, 05 Feb 2024 18:39:34 GMT  
		Size: 89.9 MB (89876303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1272f171b2af0ce8bfb62e6d143fca8fc15bf50ee236be5d4800cbfab9090`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13080409e7f6da4e0661987dc383e465fae9c4c552c9c9bd604c96545383773a`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:54d09e046e01b90abef395abd7ffc193f5799e397074c61efa0bc7c4b1361846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8703b6b075a14bf135706d51fc276e2669a2cdaa8b60d47f2f2c6c328ad8b443`

```dockerfile
```

-	Layers:
	-	`sha256:d3abb785ecde37d3b122c72488e32f12d9ae8caae4e014c177cc3b53a1c87385`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 4.0 MB (3985734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330a26f0c55ae29012af09504a1add3f2614a69ab65ff8963a6312e826a6687b`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:1313a2db308ac99e5064c01e087f2bb089c30ad83618ff8b5de911f3d20d1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121205840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aab662bedd776d651e8052f73f97908b6332c32a7a9e48dab890639f58c3e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5489c06038c18e372c7b90b22b2cf47db1467e7f1189c88ad6bca777d5190`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c533f93841b9cb3e974ae1f4f58b4fb381e31ad1403187c39eb6deecf920e`  
		Last Modified: Thu, 08 Feb 2024 17:43:50 GMT  
		Size: 87.6 MB (87628410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce941ad314a8efd36aa3955c69f7ac3e61b8d0398e5aa255e0e64d39ef9baf`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135db96191d18d5787d9cf2d1290b7663f0ca4451a16a004cf36bceac9c0b22`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:b8b8d9498b0036746728c78da1f3b06ee89659013890a8fb2a5f3eef3d78565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6677f1f9f2c40259478a71fedd8871a756a602f6555170a296e537c4ec841db0`

```dockerfile
```

-	Layers:
	-	`sha256:42c37c1a3494118265f54fe8f5fc8f337772d21ec612d32c4dbd8f0a0d62bbfa`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 4.0 MB (3957804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce20a145c0cb372b118c3f2e525403518aa76ee3880a1e1327e6a9ed867fe19`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json

## `mariadb:lts-jammy`

```console
$ docker pull mariadb@sha256:e846701e66dcc95a3f90d161cc3dfc2e4ff96f0699ee4fb93b0bfdab94158570
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

### `mariadb:lts-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:0a2c136bd7f771adcefe93b8cc828dcb9a451d93b305492fcc463f882f96b97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122395734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb2af619908a56210a704427edea5839fba25c251122ca86271237062d897c1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:57c139bbda7eb92a286d974aa8fef81acf1a8cbc742242619252c13b196ab499`  
		Last Modified: Thu, 25 Jan 2024 18:12:48 GMT  
		Size: 29.5 MB (29548926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e214e6737d8fb8119eb73eae3a8a55490b4c07e064ec530b1bed3fe736594f6f`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a9f0c6ea1b52a52ab6e042dd36ea7bf8a0c1826037654587893a868a854777`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 5.6 MB (5649827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b26a2f888b920916b631650e255030a0494c2e3c6ef060632fa240f6030cadc`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edc50b97c9b432709bd588e9f59fedaf1a60d45eec041a0192beb9deec14f15`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c975760206132ac66e98815e4323904597653188888a5e4a3da026030f6097`  
		Last Modified: Fri, 02 Feb 2024 00:55:44 GMT  
		Size: 87.2 MB (87183335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259c8eda6426e8ce56810e1d485c1da7991bd7ec6c900c18cbf0c19515afe13b`  
		Last Modified: Fri, 02 Feb 2024 00:55:42 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5ed3fd578b20ea5386d4be91e760920cf9991ae5efc053fae8cf9d063f58a5`  
		Last Modified: Fri, 02 Feb 2024 00:55:43 GMT  
		Size: 7.9 KB (7859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:9b17ce98f87e2c9c5f52e6177212d72cecdaefeb32a42e13d5b528de20b4d2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4009147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0404cfd9352cc0e9af40f9f69e7985146377bed4e5a77b5021da95690c9245`

```dockerfile
```

-	Layers:
	-	`sha256:56011a0ab0ed0d64db1bcdd3b9d4712da39e07b84d7a479a6d61660fe513b567`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 4.0 MB (3978012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5aa8c9707979b58d1f13363b1741a6942a77801965ae30484e07487e2705c1b`  
		Last Modified: Fri, 02 Feb 2024 00:55:41 GMT  
		Size: 31.1 KB (31135 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:8d8ad390991307f339d27efd7758a72ce341141ed4f15de6a7db830c804278a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116767777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72247e4f4e004912b60f31958d2f81c3a078d57c89ff083e9e9c06e1b1d9f23e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b91d8878f844c327b4ff924d4973661a399f10256ed50ac7c640b30c5894166b`  
		Last Modified: Thu, 25 Jan 2024 18:12:54 GMT  
		Size: 27.4 MB (27356544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6a0ce2d31630b201edc8f983314323a9cc34011191f169e7221345c3d30f8b`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f14a0603c1633bcb88c074ec92a24dbaec5969a9f27550c606fc89ae888e7`  
		Last Modified: Mon, 05 Feb 2024 18:47:20 GMT  
		Size: 5.5 MB (5463192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7babb41e5cc9c406872d0dc17d32bcecb58f433819c66722c8228da85762dac0`  
		Last Modified: Mon, 05 Feb 2024 18:47:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365b92ace3793f0f4866adfec3489c0cea407aeb634855349e47065e91d4fd2e`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84abd8f0444f7c22644c3e04048f2825fc559130187470d64c3c6f9dedca9f30`  
		Last Modified: Mon, 05 Feb 2024 18:48:47 GMT  
		Size: 83.9 MB (83934404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e281a2c2bfe3b777b13c4259f37339b4a32093caf1c249638514136dd8595407`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce32ed88d7c667f6c49a294c905e6c253b2ad293bc1de2d74341ddec621f5c8d`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:22d87b66cad7e1d7fa241e20e94a3718b1f6dbc31573e2a40b6d3aff5f43ba50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4014803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4513a269427ed8c1efbaa1bfd3698aa9b37c71e4fb34dcf6d14122023c77cb17`

```dockerfile
```

-	Layers:
	-	`sha256:ea81eff742933d3a5ab08c0e54f55d3f5eacff8a17c9198933f6fc8d89d9227f`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 4.0 MB (3983811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9102af544a235121e2cb799452c0ee14691573b0253311b83d1df076a2c7695e`  
		Last Modified: Mon, 05 Feb 2024 18:48:44 GMT  
		Size: 31.0 KB (30992 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:01bcacc2aa40042682a3a5d3413fd1a9d17c0cefd408884453157b345ca922eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130493872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7fa1289158a6e8c0cbeaf39abb3c3c4311a98f0fe8c0e6b2728ceb4119fe89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:516de9c24f8fb95b9521e039ca0709347304eaf18821af0546eb4f3e9da81a19 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f0afb1ddc42ac38d6ab6be33bdf9c04cc7528ff9311bcd35190909db8e7948e`  
		Last Modified: Thu, 25 Jan 2024 18:13:08 GMT  
		Size: 34.5 MB (34521631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f40b57701b307a8f7731b4af88c0810150af23223743aec617c43cbd72c6b2`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9f4639b172457925b32672fe9939d74cfdd86dabfb4fe6c47b4b51b8b056d`  
		Last Modified: Mon, 05 Feb 2024 18:37:36 GMT  
		Size: 6.1 MB (6082293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc95e724635b96eb8f46dca260d07a483586d3d617d73724af831555f2f1328`  
		Last Modified: Mon, 05 Feb 2024 18:37:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9562917155b8699e9edb268af81b9adff9da719522a737fdad7b898b80dce226`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d884a7e8a1a8f8bff42660029e457b0e2c9abb60b57fa687633210360fdc7e8b`  
		Last Modified: Mon, 05 Feb 2024 18:39:34 GMT  
		Size: 89.9 MB (89876303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c1272f171b2af0ce8bfb62e6d143fca8fc15bf50ee236be5d4800cbfab9090`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13080409e7f6da4e0661987dc383e465fae9c4c552c9c9bd604c96545383773a`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:54d09e046e01b90abef395abd7ffc193f5799e397074c61efa0bc7c4b1361846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4016778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8703b6b075a14bf135706d51fc276e2669a2cdaa8b60d47f2f2c6c328ad8b443`

```dockerfile
```

-	Layers:
	-	`sha256:d3abb785ecde37d3b122c72488e32f12d9ae8caae4e014c177cc3b53a1c87385`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 4.0 MB (3985734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330a26f0c55ae29012af09504a1add3f2614a69ab65ff8963a6312e826a6687b`  
		Last Modified: Mon, 05 Feb 2024 18:39:31 GMT  
		Size: 31.0 KB (31044 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:1313a2db308ac99e5064c01e087f2bb089c30ad83618ff8b5de911f3d20d1c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.2 MB (121205840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aab662bedd776d651e8052f73f97908b6332c32a7a9e48dab890639f58c3e2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 14 Nov 2023 23:22:11 GMT
ARG RELEASE
# Tue, 14 Nov 2023 23:22:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 14 Nov 2023 23:22:11 GMT
ADD file:f52d272f26110df8fef7d7ed8cbe853f5189a538fa0a3be48b322affd1b3ba76 in / 
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["/bin/bash"]
# Tue, 14 Nov 2023 23:22:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV GOSU_VERSION=1.17
# Tue, 14 Nov 2023 23:22:11 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENV LANG=C.UTF-8
# Tue, 14 Nov 2023 23:22:11 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 14 Nov 2023 23:22:11 GMT
ARG MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ENV MARIADB_VERSION=1:10.11.6+maria~ubu2204
# Tue, 14 Nov 2023 23:22:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.6+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.6/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Nov 2023 23:22:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 14 Nov 2023 23:22:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Nov 2023 23:22:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 14 Nov 2023 23:22:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b2afc8f0dccbc5496c814ae03ac3fff7e86393abd18b2d2910a9c489bfe64311`  
		Last Modified: Thu, 25 Jan 2024 18:13:16 GMT  
		Size: 28.0 MB (28028344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445a666f33e7f0e6a25abd40d7c5a5baf2e588deb750318f91e62894a99ad3ff`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d70fcf28e16d9369683e102c0cc036e07da358a76e20b7a3b56339acdd301e7`  
		Last Modified: Thu, 08 Feb 2024 17:43:48 GMT  
		Size: 5.5 MB (5535444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab06343adfdae01291f1bd454ad71e7274d03d5cffa1e0479679537454f87f5`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e5489c06038c18e372c7b90b22b2cf47db1467e7f1189c88ad6bca777d5190`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1c533f93841b9cb3e974ae1f4f58b4fb381e31ad1403187c39eb6deecf920e`  
		Last Modified: Thu, 08 Feb 2024 17:43:50 GMT  
		Size: 87.6 MB (87628410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fce941ad314a8efd36aa3955c69f7ac3e61b8d0398e5aa255e0e64d39ef9baf`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6135db96191d18d5787d9cf2d1290b7663f0ca4451a16a004cf36bceac9c0b22`  
		Last Modified: Thu, 08 Feb 2024 17:43:49 GMT  
		Size: 7.9 KB (7856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:b8b8d9498b0036746728c78da1f3b06ee89659013890a8fb2a5f3eef3d78565c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3988778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6677f1f9f2c40259478a71fedd8871a756a602f6555170a296e537c4ec841db0`

```dockerfile
```

-	Layers:
	-	`sha256:42c37c1a3494118265f54fe8f5fc8f337772d21ec612d32c4dbd8f0a0d62bbfa`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 4.0 MB (3957804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce20a145c0cb372b118c3f2e525403518aa76ee3880a1e1327e6a9ed867fe19`  
		Last Modified: Thu, 08 Feb 2024 17:43:47 GMT  
		Size: 31.0 KB (30974 bytes)  
		MIME: application/vnd.in-toto+json
