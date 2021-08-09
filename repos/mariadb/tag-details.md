<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.40`](#mariadb10240)
-	[`mariadb:10.2.40-bionic`](#mariadb10240-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.31`](#mariadb10331)
-	[`mariadb:10.3.31-focal`](#mariadb10331-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.21`](#mariadb10421)
-	[`mariadb:10.4.21-focal`](#mariadb10421-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.12`](#mariadb10512)
-	[`mariadb:10.5.12-focal`](#mariadb10512-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.4`](#mariadb1064)
-	[`mariadb:10.6.4-focal`](#mariadb1064-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:f269bf7dc93dba53745c424ea9064c690c1224604c73793fcea4019abb27f0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:abd7c7416fd1b62bb216504f43a33921516dd527b36664b62355588deca9117c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109277614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f276f080220ce22db6e607f464e042570515b1b3d3ae03361db1ccef08b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:08:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:08:23 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:08:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:08:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:08:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:08:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:08:46 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 00:08:46 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:26:39 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:26:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:27:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:27:25 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:27:25 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:27:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:27:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:27:26 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:27:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb140a0551352f5156c6a13b36727ad0aae313be276fab6bd318c2cba256a9f0`  
		Last Modified: Tue, 27 Jul 2021 00:12:20 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30512fa1a94cc2482eeaf059f79ce38aa4f603c2defe33998d85c2d2e956002b`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 4.8 MB (4813162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8fcc2d063d7408470485f3a8fbf38c139104bd68e1c5335c576764a8fc7ee2`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 3.5 MB (3547372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f11911c2ef7d32010088cdd2dc674473579ec4ee07fadbd86b3590a90f284d7`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322065849b37adce4f4b199b1fcba599346d0b3c11542c0e7e25755b25c60fbe`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 1.6 MB (1585615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2eef23ce3eea0a95b77bbc7682dadfc5fc39f6bcd71f22d9aba781c899b99`  
		Last Modified: Tue, 27 Jul 2021 00:12:14 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac773a01d910467cf70bb984e236ad126e708ec3519e4b586812293ae08d4ae6`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f8eed5d5b225f36a8055ea118e8e07196ea927073eaa6b1d60e528a2f449a`  
		Last Modified: Mon, 09 Aug 2021 19:30:21 GMT  
		Size: 72.6 MB (72609316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b998c0995447a11364efdaf1e75eeedb063453ebfcfa32bedbf59aa5cad5202`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a04801e8caea4413206f26fa6cf8b0e481fa927362eea3c834e025b36ef9fb`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:dbfb165fd148f34cd2e94edb6960b8569ecfe0112ef151e5ba49a389e0907b7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104314600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2459fe1d5c5b3aebc68825048062b98c73df956e8383d0c18e09f811e088959`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:52:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:53:02 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:53:02 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:53:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:53:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:53:25 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:53:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:53:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:53:27 GMT
ARG MARIADB_MAJOR=10.2
# Mon, 26 Jul 2021 22:53:27 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 26 Jul 2021 22:53:27 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Mon, 26 Jul 2021 22:53:27 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Mon, 26 Jul 2021 22:53:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Mon, 26 Jul 2021 22:53:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:53:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:53:54 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:53:54 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:53:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:53:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:53:55 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:53:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a25e4d9a236ab47600d579f7b8c9905ca430959a44f271735f446c02d17c44`  
		Last Modified: Mon, 26 Jul 2021 22:57:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce5417302bea90dcbe8518deedd4e3d8848df7c8c20795c5f0ccfcdb4ecb2bb`  
		Last Modified: Mon, 26 Jul 2021 22:57:39 GMT  
		Size: 4.4 MB (4395594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa29f54b225074541b6766b92e911c457b9321fd6227bd5049be10dc67c5288`  
		Last Modified: Mon, 26 Jul 2021 22:57:39 GMT  
		Size: 3.2 MB (3204675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1418a03d03f2954b52b7664df3333b9c3be69ecdc7fb36f7813d88ffca765b7a`  
		Last Modified: Mon, 26 Jul 2021 22:57:38 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a035a246a54f038f6617137a1fb706414e502327e464b5f7c956f7336a449`  
		Last Modified: Mon, 26 Jul 2021 22:57:39 GMT  
		Size: 1.5 MB (1532373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab32778a8e053b4250c42e07f914a482996b741329588568d11d86c0d061153`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7e71f37ed51e4859fb071b4497919cad040ef364bb8485414c43bd85d69864`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a763ccc78d96ffedf856be1b4b4b6eec5569806144f6b42a80c37baec1db95b3`  
		Last Modified: Mon, 26 Jul 2021 22:57:48 GMT  
		Size: 71.4 MB (71437119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93646094990804e21512f93f969054ed30c3df81b294a5ebc8f6acef6e4bee0`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c89f4db1ee1990bf20d0fea9f5cfb9f00f5f86fec1f92168e7898a73401a7b`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1542e68b1d26e59100b74755bff5e1f5605eb88d0315991d09906d883325aa27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117677946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c38b272f8f58ecaf1030ea8496fffec224ab8ee12dc2313de5c13497245459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:21:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:21:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:21:44 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:22:24 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:22:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:22:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:22:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:23:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:23:05 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 02:23:07 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:39:32 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:37 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:43:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:43:33 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:43:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:43:54 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:43:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369dd90b95d5e9e1f7299ee72bcc98c621a479bdd448995a21b7d2e18ca75c6f`  
		Last Modified: Tue, 27 Jul 2021 02:29:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250de9da182a63a714f54597dc6306ac894ef11aaf8df9201705a0fd59942b7f`  
		Last Modified: Tue, 27 Jul 2021 02:28:59 GMT  
		Size: 5.6 MB (5630466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317de8985ff8af48122ff1378537bc7fbf84fa3bcf6d458e6a75cea28d0a1e24`  
		Last Modified: Tue, 27 Jul 2021 02:28:58 GMT  
		Size: 3.5 MB (3528921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c5ce4ef345c6df4ad4307ef718016906f4b26c1acb7357ca63c501a730c5d7`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f397676522b618a417470f1aa2e15c07db16aa22c6c549e08841baec3bc25a`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 1.9 MB (1938720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a70d1088ca86bed51db4882db9013cc70c2d60f9008aa42e63347af965891f`  
		Last Modified: Tue, 27 Jul 2021 02:28:54 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb5820ea221765dc720a8619dc4aaf79b35eaf2861cca2a79ecb50f9d28fbbb`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2313bc2270fb370255337e749783b4a28f305644a4a387e28271ab6121b374`  
		Last Modified: Mon, 09 Aug 2021 19:48:01 GMT  
		Size: 76.1 MB (76128758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0546e8b3fb31277222b26c8a72f570f103b4a9a224b0df18fa18e0ecf0927ef`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c761f0aac1a9a03d5195b6aea2ccbb20186ef3fc51c6b88d534a48135be4d589`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:f269bf7dc93dba53745c424ea9064c690c1224604c73793fcea4019abb27f0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:abd7c7416fd1b62bb216504f43a33921516dd527b36664b62355588deca9117c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109277614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f276f080220ce22db6e607f464e042570515b1b3d3ae03361db1ccef08b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:08:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:08:23 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:08:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:08:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:08:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:08:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:08:46 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 00:08:46 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:26:39 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:26:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:27:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:27:25 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:27:25 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:27:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:27:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:27:26 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:27:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb140a0551352f5156c6a13b36727ad0aae313be276fab6bd318c2cba256a9f0`  
		Last Modified: Tue, 27 Jul 2021 00:12:20 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30512fa1a94cc2482eeaf059f79ce38aa4f603c2defe33998d85c2d2e956002b`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 4.8 MB (4813162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8fcc2d063d7408470485f3a8fbf38c139104bd68e1c5335c576764a8fc7ee2`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 3.5 MB (3547372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f11911c2ef7d32010088cdd2dc674473579ec4ee07fadbd86b3590a90f284d7`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322065849b37adce4f4b199b1fcba599346d0b3c11542c0e7e25755b25c60fbe`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 1.6 MB (1585615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2eef23ce3eea0a95b77bbc7682dadfc5fc39f6bcd71f22d9aba781c899b99`  
		Last Modified: Tue, 27 Jul 2021 00:12:14 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac773a01d910467cf70bb984e236ad126e708ec3519e4b586812293ae08d4ae6`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f8eed5d5b225f36a8055ea118e8e07196ea927073eaa6b1d60e528a2f449a`  
		Last Modified: Mon, 09 Aug 2021 19:30:21 GMT  
		Size: 72.6 MB (72609316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b998c0995447a11364efdaf1e75eeedb063453ebfcfa32bedbf59aa5cad5202`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a04801e8caea4413206f26fa6cf8b0e481fa927362eea3c834e025b36ef9fb`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:dbfb165fd148f34cd2e94edb6960b8569ecfe0112ef151e5ba49a389e0907b7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104314600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2459fe1d5c5b3aebc68825048062b98c73df956e8383d0c18e09f811e088959`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:49 GMT
ADD file:e87e065765ef99e8db25307f469c7481ab480ac5fe6353ae4caf402766f14045 in / 
# Mon, 26 Jul 2021 21:48:50 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:52:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:53:02 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:53:02 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:53:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:53:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:53:25 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:53:25 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:53:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:53:27 GMT
ARG MARIADB_MAJOR=10.2
# Mon, 26 Jul 2021 22:53:27 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 26 Jul 2021 22:53:27 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Mon, 26 Jul 2021 22:53:27 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Mon, 26 Jul 2021 22:53:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Mon, 26 Jul 2021 22:53:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:53:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:53:54 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:53:54 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:53:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:53:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:53:55 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:53:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fda1cca7a3cc2b66c161597f27e151a9b1cab79d73c7c0c2706606813a3e58cf`  
		Last Modified: Mon, 26 Jul 2021 21:50:37 GMT  
		Size: 23.7 MB (23731597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a25e4d9a236ab47600d579f7b8c9905ca430959a44f271735f446c02d17c44`  
		Last Modified: Mon, 26 Jul 2021 22:57:41 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce5417302bea90dcbe8518deedd4e3d8848df7c8c20795c5f0ccfcdb4ecb2bb`  
		Last Modified: Mon, 26 Jul 2021 22:57:39 GMT  
		Size: 4.4 MB (4395594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa29f54b225074541b6766b92e911c457b9321fd6227bd5049be10dc67c5288`  
		Last Modified: Mon, 26 Jul 2021 22:57:39 GMT  
		Size: 3.2 MB (3204675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1418a03d03f2954b52b7664df3333b9c3be69ecdc7fb36f7813d88ffca765b7a`  
		Last Modified: Mon, 26 Jul 2021 22:57:38 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78a035a246a54f038f6617137a1fb706414e502327e464b5f7c956f7336a449`  
		Last Modified: Mon, 26 Jul 2021 22:57:39 GMT  
		Size: 1.5 MB (1532373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab32778a8e053b4250c42e07f914a482996b741329588568d11d86c0d061153`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 5.2 KB (5170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7e71f37ed51e4859fb071b4497919cad040ef364bb8485414c43bd85d69864`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a763ccc78d96ffedf856be1b4b4b6eec5569806144f6b42a80c37baec1db95b3`  
		Last Modified: Mon, 26 Jul 2021 22:57:48 GMT  
		Size: 71.4 MB (71437119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93646094990804e21512f93f969054ed30c3df81b294a5ebc8f6acef6e4bee0`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c89f4db1ee1990bf20d0fea9f5cfb9f00f5f86fec1f92168e7898a73401a7b`  
		Last Modified: Mon, 26 Jul 2021 22:57:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1542e68b1d26e59100b74755bff5e1f5605eb88d0315991d09906d883325aa27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117677946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c38b272f8f58ecaf1030ea8496fffec224ab8ee12dc2313de5c13497245459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:21:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:21:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:21:44 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:22:24 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:22:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:22:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:22:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:23:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:23:05 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 02:23:07 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:39:32 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:37 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:43:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:43:33 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:43:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:43:54 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:43:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369dd90b95d5e9e1f7299ee72bcc98c621a479bdd448995a21b7d2e18ca75c6f`  
		Last Modified: Tue, 27 Jul 2021 02:29:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250de9da182a63a714f54597dc6306ac894ef11aaf8df9201705a0fd59942b7f`  
		Last Modified: Tue, 27 Jul 2021 02:28:59 GMT  
		Size: 5.6 MB (5630466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317de8985ff8af48122ff1378537bc7fbf84fa3bcf6d458e6a75cea28d0a1e24`  
		Last Modified: Tue, 27 Jul 2021 02:28:58 GMT  
		Size: 3.5 MB (3528921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c5ce4ef345c6df4ad4307ef718016906f4b26c1acb7357ca63c501a730c5d7`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f397676522b618a417470f1aa2e15c07db16aa22c6c549e08841baec3bc25a`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 1.9 MB (1938720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a70d1088ca86bed51db4882db9013cc70c2d60f9008aa42e63347af965891f`  
		Last Modified: Tue, 27 Jul 2021 02:28:54 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb5820ea221765dc720a8619dc4aaf79b35eaf2861cca2a79ecb50f9d28fbbb`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2313bc2270fb370255337e749783b4a28f305644a4a387e28271ab6121b374`  
		Last Modified: Mon, 09 Aug 2021 19:48:01 GMT  
		Size: 76.1 MB (76128758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0546e8b3fb31277222b26c8a72f570f103b4a9a224b0df18fa18e0ecf0927ef`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c761f0aac1a9a03d5195b6aea2ccbb20186ef3fc51c6b88d534a48135be4d589`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.40`

```console
$ docker pull mariadb@sha256:8a3f9daaafa945e4136bb078fc1a44ff8dd4608a2965f0b15f889816c5e7eb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.2.40` - linux; amd64

```console
$ docker pull mariadb@sha256:abd7c7416fd1b62bb216504f43a33921516dd527b36664b62355588deca9117c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109277614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f276f080220ce22db6e607f464e042570515b1b3d3ae03361db1ccef08b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:08:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:08:23 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:08:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:08:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:08:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:08:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:08:46 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 00:08:46 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:26:39 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:26:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:27:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:27:25 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:27:25 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:27:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:27:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:27:26 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:27:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb140a0551352f5156c6a13b36727ad0aae313be276fab6bd318c2cba256a9f0`  
		Last Modified: Tue, 27 Jul 2021 00:12:20 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30512fa1a94cc2482eeaf059f79ce38aa4f603c2defe33998d85c2d2e956002b`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 4.8 MB (4813162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8fcc2d063d7408470485f3a8fbf38c139104bd68e1c5335c576764a8fc7ee2`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 3.5 MB (3547372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f11911c2ef7d32010088cdd2dc674473579ec4ee07fadbd86b3590a90f284d7`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322065849b37adce4f4b199b1fcba599346d0b3c11542c0e7e25755b25c60fbe`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 1.6 MB (1585615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2eef23ce3eea0a95b77bbc7682dadfc5fc39f6bcd71f22d9aba781c899b99`  
		Last Modified: Tue, 27 Jul 2021 00:12:14 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac773a01d910467cf70bb984e236ad126e708ec3519e4b586812293ae08d4ae6`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f8eed5d5b225f36a8055ea118e8e07196ea927073eaa6b1d60e528a2f449a`  
		Last Modified: Mon, 09 Aug 2021 19:30:21 GMT  
		Size: 72.6 MB (72609316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b998c0995447a11364efdaf1e75eeedb063453ebfcfa32bedbf59aa5cad5202`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a04801e8caea4413206f26fa6cf8b0e481fa927362eea3c834e025b36ef9fb`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.40` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1542e68b1d26e59100b74755bff5e1f5605eb88d0315991d09906d883325aa27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117677946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c38b272f8f58ecaf1030ea8496fffec224ab8ee12dc2313de5c13497245459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:21:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:21:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:21:44 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:22:24 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:22:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:22:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:22:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:23:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:23:05 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 02:23:07 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:39:32 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:37 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:43:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:43:33 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:43:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:43:54 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:43:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369dd90b95d5e9e1f7299ee72bcc98c621a479bdd448995a21b7d2e18ca75c6f`  
		Last Modified: Tue, 27 Jul 2021 02:29:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250de9da182a63a714f54597dc6306ac894ef11aaf8df9201705a0fd59942b7f`  
		Last Modified: Tue, 27 Jul 2021 02:28:59 GMT  
		Size: 5.6 MB (5630466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317de8985ff8af48122ff1378537bc7fbf84fa3bcf6d458e6a75cea28d0a1e24`  
		Last Modified: Tue, 27 Jul 2021 02:28:58 GMT  
		Size: 3.5 MB (3528921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c5ce4ef345c6df4ad4307ef718016906f4b26c1acb7357ca63c501a730c5d7`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f397676522b618a417470f1aa2e15c07db16aa22c6c549e08841baec3bc25a`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 1.9 MB (1938720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a70d1088ca86bed51db4882db9013cc70c2d60f9008aa42e63347af965891f`  
		Last Modified: Tue, 27 Jul 2021 02:28:54 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb5820ea221765dc720a8619dc4aaf79b35eaf2861cca2a79ecb50f9d28fbbb`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2313bc2270fb370255337e749783b4a28f305644a4a387e28271ab6121b374`  
		Last Modified: Mon, 09 Aug 2021 19:48:01 GMT  
		Size: 76.1 MB (76128758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0546e8b3fb31277222b26c8a72f570f103b4a9a224b0df18fa18e0ecf0927ef`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c761f0aac1a9a03d5195b6aea2ccbb20186ef3fc51c6b88d534a48135be4d589`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.40-bionic`

```console
$ docker pull mariadb@sha256:8a3f9daaafa945e4136bb078fc1a44ff8dd4608a2965f0b15f889816c5e7eb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.2.40-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:abd7c7416fd1b62bb216504f43a33921516dd527b36664b62355588deca9117c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109277614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1f276f080220ce22db6e607f464e042570515b1b3d3ae03361db1ccef08b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:30 GMT
ADD file:e729fb032bd2f7cde20fb343da0cd358447e8b23028422c123944e8d0be660fa in / 
# Mon, 26 Jul 2021 21:21:31 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:08:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:08:23 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:23 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:08:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:08:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:08:44 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:08:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:08:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:08:46 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 00:08:46 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:26:39 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:26:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:26:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:27:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:27:25 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:27:25 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:27:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:27:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:27:26 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:27:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feac5306138255e28a9862d3f3d29025d0a4d0648855afe1acd6131af07138ac`  
		Last Modified: Mon, 26 Jul 2021 21:22:52 GMT  
		Size: 26.7 MB (26709039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb140a0551352f5156c6a13b36727ad0aae313be276fab6bd318c2cba256a9f0`  
		Last Modified: Tue, 27 Jul 2021 00:12:20 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30512fa1a94cc2482eeaf059f79ce38aa4f603c2defe33998d85c2d2e956002b`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 4.8 MB (4813162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e8fcc2d063d7408470485f3a8fbf38c139104bd68e1c5335c576764a8fc7ee2`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 3.5 MB (3547372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f11911c2ef7d32010088cdd2dc674473579ec4ee07fadbd86b3590a90f284d7`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322065849b37adce4f4b199b1fcba599346d0b3c11542c0e7e25755b25c60fbe`  
		Last Modified: Tue, 27 Jul 2021 00:12:18 GMT  
		Size: 1.6 MB (1585615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a2eef23ce3eea0a95b77bbc7682dadfc5fc39f6bcd71f22d9aba781c899b99`  
		Last Modified: Tue, 27 Jul 2021 00:12:14 GMT  
		Size: 5.0 KB (5029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac773a01d910467cf70bb984e236ad126e708ec3519e4b586812293ae08d4ae6`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65f8eed5d5b225f36a8055ea118e8e07196ea927073eaa6b1d60e528a2f449a`  
		Last Modified: Mon, 09 Aug 2021 19:30:21 GMT  
		Size: 72.6 MB (72609316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b998c0995447a11364efdaf1e75eeedb063453ebfcfa32bedbf59aa5cad5202`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a04801e8caea4413206f26fa6cf8b0e481fa927362eea3c834e025b36ef9fb`  
		Last Modified: Mon, 09 Aug 2021 19:30:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.40-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:1542e68b1d26e59100b74755bff5e1f5605eb88d0315991d09906d883325aa27
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117677946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c38b272f8f58ecaf1030ea8496fffec224ab8ee12dc2313de5c13497245459`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:21:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:21:42 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:21:44 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:22:24 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:22:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:22:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:22:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:23:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:23:05 GMT
ARG MARIADB_MAJOR=10.2
# Tue, 27 Jul 2021 02:23:07 GMT
ENV MARIADB_MAJOR=10.2
# Mon, 09 Aug 2021 19:39:32 GMT
ARG MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:37 GMT
ENV MARIADB_VERSION=1:10.2.40+maria~bionic
# Mon, 09 Aug 2021 19:39:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:43:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:43:33 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:43:36 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:43:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.40/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:43:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:43:54 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:43:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369dd90b95d5e9e1f7299ee72bcc98c621a479bdd448995a21b7d2e18ca75c6f`  
		Last Modified: Tue, 27 Jul 2021 02:29:00 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250de9da182a63a714f54597dc6306ac894ef11aaf8df9201705a0fd59942b7f`  
		Last Modified: Tue, 27 Jul 2021 02:28:59 GMT  
		Size: 5.6 MB (5630466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317de8985ff8af48122ff1378537bc7fbf84fa3bcf6d458e6a75cea28d0a1e24`  
		Last Modified: Tue, 27 Jul 2021 02:28:58 GMT  
		Size: 3.5 MB (3528921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c5ce4ef345c6df4ad4307ef718016906f4b26c1acb7357ca63c501a730c5d7`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f397676522b618a417470f1aa2e15c07db16aa22c6c549e08841baec3bc25a`  
		Last Modified: Tue, 27 Jul 2021 02:28:57 GMT  
		Size: 1.9 MB (1938720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a70d1088ca86bed51db4882db9013cc70c2d60f9008aa42e63347af965891f`  
		Last Modified: Tue, 27 Jul 2021 02:28:54 GMT  
		Size: 5.0 KB (5028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb5820ea221765dc720a8619dc4aaf79b35eaf2861cca2a79ecb50f9d28fbbb`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2313bc2270fb370255337e749783b4a28f305644a4a387e28271ab6121b374`  
		Last Modified: Mon, 09 Aug 2021 19:48:01 GMT  
		Size: 76.1 MB (76128758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0546e8b3fb31277222b26c8a72f570f103b4a9a224b0df18fa18e0ecf0927ef`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c761f0aac1a9a03d5195b6aea2ccbb20186ef3fc51c6b88d534a48135be4d589`  
		Last Modified: Mon, 09 Aug 2021 19:47:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:22b37b6f88d1bc277b87446e6d152d1ea29d286ec6fdd6bf36463419f47b6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:1ab45fcbf5231f9f3527e2c57e0c6a57e0ee0e12dc37373f2b57aece0d9e0807
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8dae1f6f5606d625fe0e3aaa1f8791e4d00674bf05c0cd907e7565d3c5403`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:07:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 00:07:32 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:26:04 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:26:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:26:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:26:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:26:31 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:26:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:26:32 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900c3d54d69bc9fab7b747feb0a470376a1a346e1ba78752ead65506d06f33f`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d3f780dd791eb10b78b4b0376c3afed298ac67dc52262a1278dabfc1d318f`  
		Last Modified: Mon, 09 Aug 2021 19:29:54 GMT  
		Size: 80.1 MB (80090705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77805c057f07ba4de9b922b741a8b078369c3e440e1fa4b80d1c645510e6df66`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fa47ecdca663b37feca04369ec700446cb994ecc1d7d09c6436613e0c34ce9`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de36ca68ca20c7db67cb1e67a1618131ddd4769d4b95d844ab52dda00622b6ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117619696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443048b1f79857a7ac5512e1b98fe1f4e7eafb4fb1b872d31ccc57324fc3aaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_MAJOR=10.3
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:41:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:58 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0316e9b461e7e70a5fddb9074b216b9a48b94be01e4fc15bfa3bb54e9940caa5`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dd2a135dbe6cb25a9e2df1f2af911d95d20d837d61d631181bb2f907c300e7`  
		Last Modified: Mon, 09 Aug 2021 19:45:25 GMT  
		Size: 79.4 MB (79413565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1cd915e2308e4eb2989de2ff0a335f05058dcbc9b0be3d0a07c15b2fec187e`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1278e70da9bbec91206dc1a2cdede2c7a582abccaaa9621602cb50af32f5305f`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee3e3a13e267f025f2f76988ac95eff3e8771e80bdd6a19a4dfe4191baaaa2f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee69d70a05d108b91f57174ad144788a86814c14f746ed448af3b789e11c55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:18:29 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 02:18:30 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:33:17 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:24 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:34:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:38:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:38:30 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:38:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:38:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:39:08 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:39:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c44c1594096752ada6ed92604830640dfb30532bb4bef9286d87106641171`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2768461faac96a25d8dda5bb9ca72d8f376094a119254fec9101de609a6b5d99`  
		Last Modified: Mon, 09 Aug 2021 19:47:27 GMT  
		Size: 84.7 MB (84668868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5921594fde1ae68d8eb7c9e67dc38772e2d8bb4afc3fade4f6dc4484146ffd`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdcee0fbec51cf829dd268049dbc5fbd6ff4b409fac5d1df8cfa0a3895787cd`  
		Last Modified: Mon, 09 Aug 2021 19:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:22b37b6f88d1bc277b87446e6d152d1ea29d286ec6fdd6bf36463419f47b6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1ab45fcbf5231f9f3527e2c57e0c6a57e0ee0e12dc37373f2b57aece0d9e0807
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8dae1f6f5606d625fe0e3aaa1f8791e4d00674bf05c0cd907e7565d3c5403`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:07:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 00:07:32 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:26:04 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:26:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:26:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:26:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:26:31 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:26:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:26:32 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900c3d54d69bc9fab7b747feb0a470376a1a346e1ba78752ead65506d06f33f`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d3f780dd791eb10b78b4b0376c3afed298ac67dc52262a1278dabfc1d318f`  
		Last Modified: Mon, 09 Aug 2021 19:29:54 GMT  
		Size: 80.1 MB (80090705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77805c057f07ba4de9b922b741a8b078369c3e440e1fa4b80d1c645510e6df66`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fa47ecdca663b37feca04369ec700446cb994ecc1d7d09c6436613e0c34ce9`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de36ca68ca20c7db67cb1e67a1618131ddd4769d4b95d844ab52dda00622b6ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117619696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443048b1f79857a7ac5512e1b98fe1f4e7eafb4fb1b872d31ccc57324fc3aaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_MAJOR=10.3
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:41:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:58 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0316e9b461e7e70a5fddb9074b216b9a48b94be01e4fc15bfa3bb54e9940caa5`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dd2a135dbe6cb25a9e2df1f2af911d95d20d837d61d631181bb2f907c300e7`  
		Last Modified: Mon, 09 Aug 2021 19:45:25 GMT  
		Size: 79.4 MB (79413565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1cd915e2308e4eb2989de2ff0a335f05058dcbc9b0be3d0a07c15b2fec187e`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1278e70da9bbec91206dc1a2cdede2c7a582abccaaa9621602cb50af32f5305f`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee3e3a13e267f025f2f76988ac95eff3e8771e80bdd6a19a4dfe4191baaaa2f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee69d70a05d108b91f57174ad144788a86814c14f746ed448af3b789e11c55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:18:29 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 02:18:30 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:33:17 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:24 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:34:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:38:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:38:30 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:38:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:38:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:39:08 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:39:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c44c1594096752ada6ed92604830640dfb30532bb4bef9286d87106641171`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2768461faac96a25d8dda5bb9ca72d8f376094a119254fec9101de609a6b5d99`  
		Last Modified: Mon, 09 Aug 2021 19:47:27 GMT  
		Size: 84.7 MB (84668868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5921594fde1ae68d8eb7c9e67dc38772e2d8bb4afc3fade4f6dc4484146ffd`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdcee0fbec51cf829dd268049dbc5fbd6ff4b409fac5d1df8cfa0a3895787cd`  
		Last Modified: Mon, 09 Aug 2021 19:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.31`

```console
$ docker pull mariadb@sha256:22b37b6f88d1bc277b87446e6d152d1ea29d286ec6fdd6bf36463419f47b6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.31` - linux; amd64

```console
$ docker pull mariadb@sha256:1ab45fcbf5231f9f3527e2c57e0c6a57e0ee0e12dc37373f2b57aece0d9e0807
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8dae1f6f5606d625fe0e3aaa1f8791e4d00674bf05c0cd907e7565d3c5403`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:07:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 00:07:32 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:26:04 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:26:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:26:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:26:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:26:31 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:26:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:26:32 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900c3d54d69bc9fab7b747feb0a470376a1a346e1ba78752ead65506d06f33f`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d3f780dd791eb10b78b4b0376c3afed298ac67dc52262a1278dabfc1d318f`  
		Last Modified: Mon, 09 Aug 2021 19:29:54 GMT  
		Size: 80.1 MB (80090705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77805c057f07ba4de9b922b741a8b078369c3e440e1fa4b80d1c645510e6df66`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fa47ecdca663b37feca04369ec700446cb994ecc1d7d09c6436613e0c34ce9`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de36ca68ca20c7db67cb1e67a1618131ddd4769d4b95d844ab52dda00622b6ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117619696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443048b1f79857a7ac5512e1b98fe1f4e7eafb4fb1b872d31ccc57324fc3aaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_MAJOR=10.3
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:41:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:58 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0316e9b461e7e70a5fddb9074b216b9a48b94be01e4fc15bfa3bb54e9940caa5`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dd2a135dbe6cb25a9e2df1f2af911d95d20d837d61d631181bb2f907c300e7`  
		Last Modified: Mon, 09 Aug 2021 19:45:25 GMT  
		Size: 79.4 MB (79413565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1cd915e2308e4eb2989de2ff0a335f05058dcbc9b0be3d0a07c15b2fec187e`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1278e70da9bbec91206dc1a2cdede2c7a582abccaaa9621602cb50af32f5305f`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee3e3a13e267f025f2f76988ac95eff3e8771e80bdd6a19a4dfe4191baaaa2f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee69d70a05d108b91f57174ad144788a86814c14f746ed448af3b789e11c55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:18:29 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 02:18:30 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:33:17 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:24 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:34:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:38:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:38:30 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:38:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:38:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:39:08 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:39:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c44c1594096752ada6ed92604830640dfb30532bb4bef9286d87106641171`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2768461faac96a25d8dda5bb9ca72d8f376094a119254fec9101de609a6b5d99`  
		Last Modified: Mon, 09 Aug 2021 19:47:27 GMT  
		Size: 84.7 MB (84668868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5921594fde1ae68d8eb7c9e67dc38772e2d8bb4afc3fade4f6dc4484146ffd`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdcee0fbec51cf829dd268049dbc5fbd6ff4b409fac5d1df8cfa0a3895787cd`  
		Last Modified: Mon, 09 Aug 2021 19:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.31-focal`

```console
$ docker pull mariadb@sha256:22b37b6f88d1bc277b87446e6d152d1ea29d286ec6fdd6bf36463419f47b6bda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.31-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1ab45fcbf5231f9f3527e2c57e0c6a57e0ee0e12dc37373f2b57aece0d9e0807
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120014376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c8dae1f6f5606d625fe0e3aaa1f8791e4d00674bf05c0cd907e7565d3c5403`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:07:32 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 00:07:32 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:26:04 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:26:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:26:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:26:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:26:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:26:31 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:26:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:26:32 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900c3d54d69bc9fab7b747feb0a470376a1a346e1ba78752ead65506d06f33f`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496d3f780dd791eb10b78b4b0376c3afed298ac67dc52262a1278dabfc1d318f`  
		Last Modified: Mon, 09 Aug 2021 19:29:54 GMT  
		Size: 80.1 MB (80090705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77805c057f07ba4de9b922b741a8b078369c3e440e1fa4b80d1c645510e6df66`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fa47ecdca663b37feca04369ec700446cb994ecc1d7d09c6436613e0c34ce9`  
		Last Modified: Mon, 09 Aug 2021 19:29:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:de36ca68ca20c7db67cb1e67a1618131ddd4769d4b95d844ab52dda00622b6ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117619696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:443048b1f79857a7ac5512e1b98fe1f4e7eafb4fb1b872d31ccc57324fc3aaf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_MAJOR=10.3
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:41:30 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:41:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:57 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:58 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0316e9b461e7e70a5fddb9074b216b9a48b94be01e4fc15bfa3bb54e9940caa5`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dd2a135dbe6cb25a9e2df1f2af911d95d20d837d61d631181bb2f907c300e7`  
		Last Modified: Mon, 09 Aug 2021 19:45:25 GMT  
		Size: 79.4 MB (79413565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1cd915e2308e4eb2989de2ff0a335f05058dcbc9b0be3d0a07c15b2fec187e`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1278e70da9bbec91206dc1a2cdede2c7a582abccaaa9621602cb50af32f5305f`  
		Last Modified: Mon, 09 Aug 2021 19:45:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.31-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:ee3e3a13e267f025f2f76988ac95eff3e8771e80bdd6a19a4dfe4191baaaa2f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130878367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee69d70a05d108b91f57174ad144788a86814c14f746ed448af3b789e11c55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:18:29 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 27 Jul 2021 02:18:30 GMT
ENV MARIADB_MAJOR=10.3
# Mon, 09 Aug 2021 19:33:17 GMT
ARG MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:24 GMT
ENV MARIADB_VERSION=1:10.3.31+maria~focal
# Mon, 09 Aug 2021 19:33:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:34:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:38:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:38:30 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:38:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:38:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.31/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:38:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:39:08 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:39:16 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4c44c1594096752ada6ed92604830640dfb30532bb4bef9286d87106641171`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2768461faac96a25d8dda5bb9ca72d8f376094a119254fec9101de609a6b5d99`  
		Last Modified: Mon, 09 Aug 2021 19:47:27 GMT  
		Size: 84.7 MB (84668868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5921594fde1ae68d8eb7c9e67dc38772e2d8bb4afc3fade4f6dc4484146ffd`  
		Last Modified: Mon, 09 Aug 2021 19:47:10 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bdcee0fbec51cf829dd268049dbc5fbd6ff4b409fac5d1df8cfa0a3895787cd`  
		Last Modified: Mon, 09 Aug 2021 19:47:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:41c3dc14927ea22fa7d5aac9832b389b817143a8cb256d97a126c83b001a7528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:f757259fb431216040a77292d79428710cdcc9f3c1db17811c2029e7131f9950
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124736934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f9f97d14cefa84e69d9df6e30855f8848c94ff3b52b1c80bb988bd60827682`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:56 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 00:06:56 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:25:34 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:59 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9b140ec558f045515897d54da2f1b097d349f88038b068e731417640c41c08`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eedef259b7b484e50a0cbf6f8ee8c2667b10d8bb9f321fa1f0aa88999912963`  
		Last Modified: Mon, 09 Aug 2021 19:29:25 GMT  
		Size: 84.8 MB (84813265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b94f4075293104c9899b2260662705f0b15e3f761324aacd2cc2db7d251fdf`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3699fac03dbbc7d3b70481b014e6954b4ef80a698aad277b545b6ea5f875e0fc`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:747ed7663f397b0c048d455ef04f7cb611372362b6397c039d24b7989fdf152f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122253459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33ac3510362ff22e3965c712f9e8fc5e451cb8c8fd57f84c1d800a73596fc74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:43 GMT
ARG MARIADB_MAJOR=10.4
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:40:58 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:23 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8cda980021ce8fd8f004ec96459fdb51b6c0fb1d911b91b328ec35e4694005`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de715d29ec0327803cbb424ab91c6176fc8f3d2c630544771a7df7a43feeb68`  
		Last Modified: Mon, 09 Aug 2021 19:44:53 GMT  
		Size: 84.0 MB (84047331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd44740a99ef5ba0da46cdfed86143a754c1ad1c0fac71e3b3e4b98b0b59ed`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075d5f3e273b337e29fb852d9a27352301f4a3efc708b9ceaed89d47c9ed332`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c6313d6768416158bb0c4b766d0c73e2b37599a3e57073adcbd2f20a3eb90436
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375c0548a54460915cdbdb18da2c09f8ee0740f29908f6fd430d24253ac55f79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:15:03 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 02:15:06 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:28:45 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:48 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:28:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:32:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:32:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:32:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:32:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:32:48 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:32:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd48726927856271f322485a6de75cece86f85c05479ff7e70e2e6d5ebbb424`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f067682d4150a7de01414baa115d5a6375406c67fabc09fa0e7652d396e00c`  
		Last Modified: Mon, 09 Aug 2021 19:46:50 GMT  
		Size: 89.3 MB (89254317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adb83fc0fd3a0ed26d72ceeaf19a3a310f541466d600710ce7e75e7522f3c09`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4523f2d5de9af7d4a2a77dfd0db6d8dd034f14df578bbfff3fcc6793ba0d352`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:41c3dc14927ea22fa7d5aac9832b389b817143a8cb256d97a126c83b001a7528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:f757259fb431216040a77292d79428710cdcc9f3c1db17811c2029e7131f9950
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124736934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f9f97d14cefa84e69d9df6e30855f8848c94ff3b52b1c80bb988bd60827682`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:56 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 00:06:56 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:25:34 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:59 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9b140ec558f045515897d54da2f1b097d349f88038b068e731417640c41c08`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eedef259b7b484e50a0cbf6f8ee8c2667b10d8bb9f321fa1f0aa88999912963`  
		Last Modified: Mon, 09 Aug 2021 19:29:25 GMT  
		Size: 84.8 MB (84813265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b94f4075293104c9899b2260662705f0b15e3f761324aacd2cc2db7d251fdf`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3699fac03dbbc7d3b70481b014e6954b4ef80a698aad277b545b6ea5f875e0fc`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:747ed7663f397b0c048d455ef04f7cb611372362b6397c039d24b7989fdf152f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122253459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33ac3510362ff22e3965c712f9e8fc5e451cb8c8fd57f84c1d800a73596fc74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:43 GMT
ARG MARIADB_MAJOR=10.4
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:40:58 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:23 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8cda980021ce8fd8f004ec96459fdb51b6c0fb1d911b91b328ec35e4694005`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de715d29ec0327803cbb424ab91c6176fc8f3d2c630544771a7df7a43feeb68`  
		Last Modified: Mon, 09 Aug 2021 19:44:53 GMT  
		Size: 84.0 MB (84047331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd44740a99ef5ba0da46cdfed86143a754c1ad1c0fac71e3b3e4b98b0b59ed`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075d5f3e273b337e29fb852d9a27352301f4a3efc708b9ceaed89d47c9ed332`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c6313d6768416158bb0c4b766d0c73e2b37599a3e57073adcbd2f20a3eb90436
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375c0548a54460915cdbdb18da2c09f8ee0740f29908f6fd430d24253ac55f79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:15:03 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 02:15:06 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:28:45 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:48 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:28:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:32:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:32:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:32:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:32:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:32:48 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:32:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd48726927856271f322485a6de75cece86f85c05479ff7e70e2e6d5ebbb424`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f067682d4150a7de01414baa115d5a6375406c67fabc09fa0e7652d396e00c`  
		Last Modified: Mon, 09 Aug 2021 19:46:50 GMT  
		Size: 89.3 MB (89254317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adb83fc0fd3a0ed26d72ceeaf19a3a310f541466d600710ce7e75e7522f3c09`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4523f2d5de9af7d4a2a77dfd0db6d8dd034f14df578bbfff3fcc6793ba0d352`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.21`

```console
$ docker pull mariadb@sha256:41c3dc14927ea22fa7d5aac9832b389b817143a8cb256d97a126c83b001a7528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.21` - linux; amd64

```console
$ docker pull mariadb@sha256:f757259fb431216040a77292d79428710cdcc9f3c1db17811c2029e7131f9950
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124736934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f9f97d14cefa84e69d9df6e30855f8848c94ff3b52b1c80bb988bd60827682`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:56 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 00:06:56 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:25:34 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:59 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9b140ec558f045515897d54da2f1b097d349f88038b068e731417640c41c08`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eedef259b7b484e50a0cbf6f8ee8c2667b10d8bb9f321fa1f0aa88999912963`  
		Last Modified: Mon, 09 Aug 2021 19:29:25 GMT  
		Size: 84.8 MB (84813265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b94f4075293104c9899b2260662705f0b15e3f761324aacd2cc2db7d251fdf`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3699fac03dbbc7d3b70481b014e6954b4ef80a698aad277b545b6ea5f875e0fc`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:747ed7663f397b0c048d455ef04f7cb611372362b6397c039d24b7989fdf152f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122253459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33ac3510362ff22e3965c712f9e8fc5e451cb8c8fd57f84c1d800a73596fc74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:43 GMT
ARG MARIADB_MAJOR=10.4
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:40:58 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:23 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8cda980021ce8fd8f004ec96459fdb51b6c0fb1d911b91b328ec35e4694005`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de715d29ec0327803cbb424ab91c6176fc8f3d2c630544771a7df7a43feeb68`  
		Last Modified: Mon, 09 Aug 2021 19:44:53 GMT  
		Size: 84.0 MB (84047331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd44740a99ef5ba0da46cdfed86143a754c1ad1c0fac71e3b3e4b98b0b59ed`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075d5f3e273b337e29fb852d9a27352301f4a3efc708b9ceaed89d47c9ed332`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c6313d6768416158bb0c4b766d0c73e2b37599a3e57073adcbd2f20a3eb90436
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375c0548a54460915cdbdb18da2c09f8ee0740f29908f6fd430d24253ac55f79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:15:03 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 02:15:06 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:28:45 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:48 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:28:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:32:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:32:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:32:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:32:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:32:48 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:32:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd48726927856271f322485a6de75cece86f85c05479ff7e70e2e6d5ebbb424`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f067682d4150a7de01414baa115d5a6375406c67fabc09fa0e7652d396e00c`  
		Last Modified: Mon, 09 Aug 2021 19:46:50 GMT  
		Size: 89.3 MB (89254317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adb83fc0fd3a0ed26d72ceeaf19a3a310f541466d600710ce7e75e7522f3c09`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4523f2d5de9af7d4a2a77dfd0db6d8dd034f14df578bbfff3fcc6793ba0d352`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.21-focal`

```console
$ docker pull mariadb@sha256:41c3dc14927ea22fa7d5aac9832b389b817143a8cb256d97a126c83b001a7528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.21-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:f757259fb431216040a77292d79428710cdcc9f3c1db17811c2029e7131f9950
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124736934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f9f97d14cefa84e69d9df6e30855f8848c94ff3b52b1c80bb988bd60827682`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:56 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 00:06:56 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:25:34 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:25:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:58 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:25:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:59 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9b140ec558f045515897d54da2f1b097d349f88038b068e731417640c41c08`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eedef259b7b484e50a0cbf6f8ee8c2667b10d8bb9f321fa1f0aa88999912963`  
		Last Modified: Mon, 09 Aug 2021 19:29:25 GMT  
		Size: 84.8 MB (84813265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b94f4075293104c9899b2260662705f0b15e3f761324aacd2cc2db7d251fdf`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3699fac03dbbc7d3b70481b014e6954b4ef80a698aad277b545b6ea5f875e0fc`  
		Last Modified: Mon, 09 Aug 2021 19:29:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:747ed7663f397b0c048d455ef04f7cb611372362b6397c039d24b7989fdf152f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122253459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b33ac3510362ff22e3965c712f9e8fc5e451cb8c8fd57f84c1d800a73596fc74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:43 GMT
ARG MARIADB_MAJOR=10.4
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:40:58 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:40:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:41:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:41:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:41:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:41:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:41:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:41:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:41:23 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:41:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8cda980021ce8fd8f004ec96459fdb51b6c0fb1d911b91b328ec35e4694005`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de715d29ec0327803cbb424ab91c6176fc8f3d2c630544771a7df7a43feeb68`  
		Last Modified: Mon, 09 Aug 2021 19:44:53 GMT  
		Size: 84.0 MB (84047331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd44740a99ef5ba0da46cdfed86143a754c1ad1c0fac71e3b3e4b98b0b59ed`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2075d5f3e273b337e29fb852d9a27352301f4a3efc708b9ceaed89d47c9ed332`  
		Last Modified: Mon, 09 Aug 2021 19:44:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.21-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c6313d6768416158bb0c4b766d0c73e2b37599a3e57073adcbd2f20a3eb90436
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135463813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375c0548a54460915cdbdb18da2c09f8ee0740f29908f6fd430d24253ac55f79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:15:03 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 27 Jul 2021 02:15:06 GMT
ENV MARIADB_MAJOR=10.4
# Mon, 09 Aug 2021 19:28:45 GMT
ARG MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:48 GMT
ENV MARIADB_VERSION=1:10.4.21+maria~focal
# Mon, 09 Aug 2021 19:28:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:28:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:32:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:32:31 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:32:33 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:32:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.21/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 09 Aug 2021 19:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:32:48 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:32:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd48726927856271f322485a6de75cece86f85c05479ff7e70e2e6d5ebbb424`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f067682d4150a7de01414baa115d5a6375406c67fabc09fa0e7652d396e00c`  
		Last Modified: Mon, 09 Aug 2021 19:46:50 GMT  
		Size: 89.3 MB (89254317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9adb83fc0fd3a0ed26d72ceeaf19a3a310f541466d600710ce7e75e7522f3c09`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4523f2d5de9af7d4a2a77dfd0db6d8dd034f14df578bbfff3fcc6793ba0d352`  
		Last Modified: Mon, 09 Aug 2021 19:46:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:59ffa5cb436450aa81cfaf694ab1405f98da9b923693374473503470296f9843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:714b7e3ed906a2d4a0c11ded8dcadc804dde593be5474ef88f911ce6b54dadad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126860537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9643f47b304c4a77314f35c725cf5dc7e63b29f9a0350e52b99d1e8ca6067276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:25 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 00:06:25 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:25:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:28 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd18312032de063877ef5ff92e06d0c5b2e33d2f09d4ebaca4062371d5919e2`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f5eb96adc50bc11b45b80d6c343b69bfa553f315a2d8a25e9f48221c720b17`  
		Last Modified: Mon, 09 Aug 2021 19:28:57 GMT  
		Size: 86.9 MB (86936993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7dacc2466ab5456742e63e09e203e507a8be337cc4f5bddd587740684f8f9`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ce9db83875c6eab39e3501bdead79302aaeed0d2e14ba1cb7cf949f1330c5f79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63160122130272c449a608a4854767dd9cbffc759fb415be47ff83e2c05edb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_MAJOR=10.5
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:40:30 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:52 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:52 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19f53b76b27a3d5dc6c211cf1c18cb2abc5718796150f603945de04beac187d`  
		Last Modified: Mon, 09 Aug 2021 19:44:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ef71f1ffe0f3f91183b5ccbb2edc474e49a539aca0ad5c84c9201a0d70482`  
		Last Modified: Mon, 09 Aug 2021 19:44:19 GMT  
		Size: 86.1 MB (86101124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b2f8fe9a028c85a303d7caca97e7ac83c15b49a77568ba7f5100c39f9f295c`  
		Last Modified: Mon, 09 Aug 2021 19:44:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a22827c392d5d8aa35de016791f7037b3a783257bc715118bdca87dbdc3f1623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6ffd715dfd27be255eb10756b6b1dddf856f016349451df5b3d3ca927a22eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:11:32 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 02:11:34 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:23:36 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:45 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:28:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:28:14 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:28:18 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:28:30 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:28:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e4a78feeb863bb4a36ec743301f11db8142e4252ab6db2dd94470d0ffb950`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96967b218a123706ee5fe6b9cf79c4124c016aa86825dec7ba7ddae281301f63`  
		Last Modified: Mon, 09 Aug 2021 19:46:14 GMT  
		Size: 91.4 MB (91371131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b234b373bbf599e2b861274d9dfe19b7b3a14f24555c4b292df94ca2cf425c5`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:59ffa5cb436450aa81cfaf694ab1405f98da9b923693374473503470296f9843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:714b7e3ed906a2d4a0c11ded8dcadc804dde593be5474ef88f911ce6b54dadad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126860537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9643f47b304c4a77314f35c725cf5dc7e63b29f9a0350e52b99d1e8ca6067276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:25 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 00:06:25 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:25:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:28 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd18312032de063877ef5ff92e06d0c5b2e33d2f09d4ebaca4062371d5919e2`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f5eb96adc50bc11b45b80d6c343b69bfa553f315a2d8a25e9f48221c720b17`  
		Last Modified: Mon, 09 Aug 2021 19:28:57 GMT  
		Size: 86.9 MB (86936993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7dacc2466ab5456742e63e09e203e507a8be337cc4f5bddd587740684f8f9`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ce9db83875c6eab39e3501bdead79302aaeed0d2e14ba1cb7cf949f1330c5f79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63160122130272c449a608a4854767dd9cbffc759fb415be47ff83e2c05edb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_MAJOR=10.5
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:40:30 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:52 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:52 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19f53b76b27a3d5dc6c211cf1c18cb2abc5718796150f603945de04beac187d`  
		Last Modified: Mon, 09 Aug 2021 19:44:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ef71f1ffe0f3f91183b5ccbb2edc474e49a539aca0ad5c84c9201a0d70482`  
		Last Modified: Mon, 09 Aug 2021 19:44:19 GMT  
		Size: 86.1 MB (86101124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b2f8fe9a028c85a303d7caca97e7ac83c15b49a77568ba7f5100c39f9f295c`  
		Last Modified: Mon, 09 Aug 2021 19:44:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a22827c392d5d8aa35de016791f7037b3a783257bc715118bdca87dbdc3f1623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6ffd715dfd27be255eb10756b6b1dddf856f016349451df5b3d3ca927a22eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:11:32 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 02:11:34 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:23:36 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:45 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:28:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:28:14 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:28:18 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:28:30 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:28:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e4a78feeb863bb4a36ec743301f11db8142e4252ab6db2dd94470d0ffb950`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96967b218a123706ee5fe6b9cf79c4124c016aa86825dec7ba7ddae281301f63`  
		Last Modified: Mon, 09 Aug 2021 19:46:14 GMT  
		Size: 91.4 MB (91371131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b234b373bbf599e2b861274d9dfe19b7b3a14f24555c4b292df94ca2cf425c5`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.12`

```console
$ docker pull mariadb@sha256:59ffa5cb436450aa81cfaf694ab1405f98da9b923693374473503470296f9843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.12` - linux; amd64

```console
$ docker pull mariadb@sha256:714b7e3ed906a2d4a0c11ded8dcadc804dde593be5474ef88f911ce6b54dadad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126860537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9643f47b304c4a77314f35c725cf5dc7e63b29f9a0350e52b99d1e8ca6067276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:25 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 00:06:25 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:25:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:28 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd18312032de063877ef5ff92e06d0c5b2e33d2f09d4ebaca4062371d5919e2`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f5eb96adc50bc11b45b80d6c343b69bfa553f315a2d8a25e9f48221c720b17`  
		Last Modified: Mon, 09 Aug 2021 19:28:57 GMT  
		Size: 86.9 MB (86936993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7dacc2466ab5456742e63e09e203e507a8be337cc4f5bddd587740684f8f9`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ce9db83875c6eab39e3501bdead79302aaeed0d2e14ba1cb7cf949f1330c5f79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63160122130272c449a608a4854767dd9cbffc759fb415be47ff83e2c05edb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_MAJOR=10.5
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:40:30 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:52 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:52 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19f53b76b27a3d5dc6c211cf1c18cb2abc5718796150f603945de04beac187d`  
		Last Modified: Mon, 09 Aug 2021 19:44:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ef71f1ffe0f3f91183b5ccbb2edc474e49a539aca0ad5c84c9201a0d70482`  
		Last Modified: Mon, 09 Aug 2021 19:44:19 GMT  
		Size: 86.1 MB (86101124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b2f8fe9a028c85a303d7caca97e7ac83c15b49a77568ba7f5100c39f9f295c`  
		Last Modified: Mon, 09 Aug 2021 19:44:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a22827c392d5d8aa35de016791f7037b3a783257bc715118bdca87dbdc3f1623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6ffd715dfd27be255eb10756b6b1dddf856f016349451df5b3d3ca927a22eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:11:32 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 02:11:34 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:23:36 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:45 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:28:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:28:14 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:28:18 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:28:30 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:28:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e4a78feeb863bb4a36ec743301f11db8142e4252ab6db2dd94470d0ffb950`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96967b218a123706ee5fe6b9cf79c4124c016aa86825dec7ba7ddae281301f63`  
		Last Modified: Mon, 09 Aug 2021 19:46:14 GMT  
		Size: 91.4 MB (91371131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b234b373bbf599e2b861274d9dfe19b7b3a14f24555c4b292df94ca2cf425c5`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.12-focal`

```console
$ docker pull mariadb@sha256:59ffa5cb436450aa81cfaf694ab1405f98da9b923693374473503470296f9843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.12-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:714b7e3ed906a2d4a0c11ded8dcadc804dde593be5474ef88f911ce6b54dadad
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126860537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9643f47b304c4a77314f35c725cf5dc7e63b29f9a0350e52b99d1e8ca6067276`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:06:25 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 00:06:25 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:25:04 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:25:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:25:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:25:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:25:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:25:27 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:25:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:25:28 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:25:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd18312032de063877ef5ff92e06d0c5b2e33d2f09d4ebaca4062371d5919e2`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f5eb96adc50bc11b45b80d6c343b69bfa553f315a2d8a25e9f48221c720b17`  
		Last Modified: Mon, 09 Aug 2021 19:28:57 GMT  
		Size: 86.9 MB (86936993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a7dacc2466ab5456742e63e09e203e507a8be337cc4f5bddd587740684f8f9`  
		Last Modified: Mon, 09 Aug 2021 19:28:44 GMT  
		Size: 5.6 KB (5611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:ce9db83875c6eab39e3501bdead79302aaeed0d2e14ba1cb7cf949f1330c5f79
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124307132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63160122130272c449a608a4854767dd9cbffc759fb415be47ff83e2c05edb29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_MAJOR=10.5
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:40:30 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:40:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:52 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:52 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19f53b76b27a3d5dc6c211cf1c18cb2abc5718796150f603945de04beac187d`  
		Last Modified: Mon, 09 Aug 2021 19:44:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868ef71f1ffe0f3f91183b5ccbb2edc474e49a539aca0ad5c84c9201a0d70482`  
		Last Modified: Mon, 09 Aug 2021 19:44:19 GMT  
		Size: 86.1 MB (86101124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b2f8fe9a028c85a303d7caca97e7ac83c15b49a77568ba7f5100c39f9f295c`  
		Last Modified: Mon, 09 Aug 2021 19:44:04 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.12-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:a22827c392d5d8aa35de016791f7037b3a783257bc715118bdca87dbdc3f1623
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137580509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6ffd715dfd27be255eb10756b6b1dddf856f016349451df5b3d3ca927a22eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:11:32 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 27 Jul 2021 02:11:34 GMT
ENV MARIADB_MAJOR=10.5
# Mon, 09 Aug 2021 19:23:36 GMT
ARG MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:45 GMT
ENV MARIADB_VERSION=1:10.5.12+maria~focal
# Mon, 09 Aug 2021 19:23:49 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:28:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.12/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:28:14 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:28:18 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:28:30 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:28:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8e4a78feeb863bb4a36ec743301f11db8142e4252ab6db2dd94470d0ffb950`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96967b218a123706ee5fe6b9cf79c4124c016aa86825dec7ba7ddae281301f63`  
		Last Modified: Mon, 09 Aug 2021 19:46:14 GMT  
		Size: 91.4 MB (91371131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b234b373bbf599e2b861274d9dfe19b7b3a14f24555c4b292df94ca2cf425c5`  
		Last Modified: Mon, 09 Aug 2021 19:45:56 GMT  
		Size: 5.6 KB (5614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.4`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.4` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.4-focal`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:efaf2531a0bb19655bf9cf481813f02a706b1ed258984be1c47296fbcac1cf84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:2e955f90e3af94a992b3e63d34c93e875706d0ec672b18202630ded0706dde71
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45eaeedf03deed202dade660cbfe44ae17cac512cfd23ca2becab1cd20b5a6f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:21:39 GMT
ADD file:524e8d93ad65f08a0cb0d144268350186e36f508006b05b8faf2e1289499b59f in / 
# Mon, 26 Jul 2021 21:21:40 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 00:05:00 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 00:05:14 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:15 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 00:05:26 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 00:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 00:05:34 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 00:05:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 00:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 00:05:37 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 00:05:37 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:24:13 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:24:14 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:24:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:24:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:24:55 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:24:55 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:24:55 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:24:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16ec32c2132b43494832a05f2b02f7a822479f8250c173d0ab27b3de78b2f058`  
		Last Modified: Sun, 25 Jul 2021 03:03:29 GMT  
		Size: 28.6 MB (28567944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf20e69555c2118df81cd7906473b0bbef5210f014d45113251b1298fb1c996`  
		Last Modified: Tue, 27 Jul 2021 00:10:02 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69afd1ffc85b8fe385e48d00e89467a4e080c81b2447ce86ebf964f3e43efb9`  
		Last Modified: Tue, 27 Jul 2021 00:10:04 GMT  
		Size: 5.5 MB (5488764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720dc7fcd8609016e69543f354117290ffee7c9ea1bdd97d7ca84bcc06d616`  
		Last Modified: Tue, 27 Jul 2021 00:10:03 GMT  
		Size: 3.6 MB (3582379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81d177e410065c8eec2b5c018ab6ac60b2a5161184890bc3bf7627e78fb2dd`  
		Last Modified: Tue, 27 Jul 2021 00:10:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:827c8c103c898d23db5f0cfc69b6faa45038d27b1ec3c15cb5d5b29ee60fca0b`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.3 MB (2274133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2108ccd013748c7fce6a19a3f7434b860401f78326ac7373c486eafa3c719354`  
		Last Modified: Tue, 27 Jul 2021 00:09:59 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05414cb5e8f4dcf16b70640f3bcf904bafddd184d3971881c10b194fb74e8a0`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6981930106c6d6380293a728b1bda2840d2392194e1b19649b7a863e1174054`  
		Last Modified: Mon, 09 Aug 2021 19:28:09 GMT  
		Size: 87.1 MB (87089293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b7e8d11861e3f00504f9b3ff616177ec6f4e7f14f2e0162b0f92811c73bca`  
		Last Modified: Mon, 09 Aug 2021 19:27:56 GMT  
		Size: 5.6 KB (5613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:deb099498797c6a877d7a5db284e1c7d681230d5561318db978e6df559327b76
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124303689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ec0c73968efa591d65e3a9281be24eb0da9745918a880fecf5f38b2050fec4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 21:48:57 GMT
ADD file:10d7c5e7290ff5627132fb35c51a2143351e184b02e3fb6d9c1c06815ae803ae in / 
# Mon, 26 Jul 2021 21:48:57 GMT
CMD ["bash"]
# Mon, 26 Jul 2021 22:50:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Mon, 26 Jul 2021 22:50:20 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:20 GMT
ENV GOSU_VERSION=1.13
# Mon, 26 Jul 2021 22:50:34 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 26 Jul 2021 22:50:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 26 Jul 2021 22:50:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 22:50:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Mon, 26 Jul 2021 22:50:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_MAJOR=10.6
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:39:59 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:40:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:40:21 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:40:21 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:40:22 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:40:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:be0de17fe24f767ec21bec97d0e8ea8f0d907fe05238a0bf9cce0995f529f7ea`  
		Last Modified: Mon, 26 Jul 2021 21:50:59 GMT  
		Size: 27.2 MB (27170255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a339f37cfc1e44c79a0cb98679b382c2c1645942a16bd6ad10dc7c687f3ff849`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c67083c32b645f0b99ff4ced0757b330faeb8f27d02e356a5526ee1322125f5`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 5.5 MB (5454983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa346ae88e358f1c860b78dedfbadaf565f94196287aa781f56ddcbbe7d52ce`  
		Last Modified: Mon, 26 Jul 2021 22:55:00 GMT  
		Size: 3.4 MB (3367132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bebae3892e3a6ac862467d82068ecf6987dbdf5be9b4a5268e2c689b664a256`  
		Last Modified: Mon, 26 Jul 2021 22:54:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3225dde6a9d2c7bc0f93796f788727e0a4053ca56759f8cea71cc57d6b953d2`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.2 MB (2203316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ddfaa372f1fb2cbcb573471fd8df2834e6bf50c4499322b05a223426946aae`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef65734b6070cd9a6da62183770cf6087689c016e3f32d390a5d2b9a23440b6a`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2da60e5bf16fb03fe450fcbdb080a0093a76a92dc13fdd9f3eede2f5b364a6`  
		Last Modified: Mon, 09 Aug 2021 19:43:33 GMT  
		Size: 86.1 MB (86097678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc2b5ba71ea793d2d6375620770a05eb4597a7e7bbcd4d87f94dcecd6f052`  
		Last Modified: Mon, 09 Aug 2021 19:43:18 GMT  
		Size: 5.6 KB (5612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0cf82c9d58ae3326749b0fe0ed1f094d02516dba9c3e6fdf9d2c193f2fa48b4a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137540073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c817c255cdeba976f7d5a97418f28626785a200c99e223a6450298661f4b64`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:46 GMT
ADD file:68eb628c2202763afa91d554dde9668d8a468fe53fdbd2fe98627a5f91d224b4 in / 
# Mon, 26 Jul 2021 23:12:49 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 02:05:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 27 Jul 2021 02:06:47 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:06:50 GMT
ENV GOSU_VERSION=1.13
# Tue, 27 Jul 2021 02:07:32 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 27 Jul 2021 02:07:42 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 27 Jul 2021 02:08:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 02:08:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 27 Jul 2021 02:08:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 27 Jul 2021 02:08:24 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 27 Jul 2021 02:08:25 GMT
ENV MARIADB_MAJOR=10.6
# Mon, 09 Aug 2021 19:17:05 GMT
ARG MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:08 GMT
ENV MARIADB_VERSION=1:10.6.4+maria~focal
# Mon, 09 Aug 2021 19:17:10 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
# Mon, 09 Aug 2021 19:17:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 09 Aug 2021 19:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.4/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 09 Aug 2021 19:22:56 GMT
VOLUME [/var/lib/mysql]
# Mon, 09 Aug 2021 19:23:00 GMT
COPY file:12b2a6a332e2002415e548cd024d4bdcdc90745b28f202869ff2d205d7a8c8cc in /usr/local/bin/ 
# Mon, 09 Aug 2021 19:23:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Aug 2021 19:23:12 GMT
EXPOSE 3306
# Mon, 09 Aug 2021 19:23:17 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1a396eed835b3b7b4101a9863d174e145ddbb1de1502a63bae726b0f81e7ca93`  
		Last Modified: Mon, 26 Jul 2021 23:15:51 GMT  
		Size: 33.3 MB (33290427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65be85b12a63573ebccb059357c5c0db6046f4a074454eea617c402e3bf99c1f`  
		Last Modified: Tue, 27 Jul 2021 02:26:16 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803c8e5bf0c59b9b01b70cac07bb24bc696bc577d8e74c79ff15bcbd480874b4`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 6.7 MB (6667884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bd7bf9c00152c4fb338b2c1a01d5b241ceda5c58d9e700a353072ab80fb4b9`  
		Last Modified: Tue, 27 Jul 2021 02:26:17 GMT  
		Size: 3.7 MB (3670853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372602ac4ce9a3a693cb97ec9b3e71b449fdafbaded2ce2937fec39cec9c9b6e`  
		Last Modified: Tue, 27 Jul 2021 02:26:14 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80c4de70a1ded78cf0175b1f5fda38b3119857dd2d8d9f1fafcdc39eafef0e`  
		Last Modified: Tue, 27 Jul 2021 02:26:13 GMT  
		Size: 2.6 MB (2569871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc8dec87672a96e86220faa6c3e98577b2a9090fc81d81efb4681fe59e732b7`  
		Last Modified: Tue, 27 Jul 2021 02:26:12 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce893fcc2e86ea1fb70c9730683306fb99ed9b96529607badefbeb824f32081`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2b83ad4dfbaa9a9aa432f398880354589538421ef773a7bdc59bf41856282`  
		Last Modified: Mon, 09 Aug 2021 19:45:24 GMT  
		Size: 91.3 MB (91330692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e301a165b39ae64033fe826324cbfdf9f8e0e01fd8d20d7e69f7a8b771aa41`  
		Last Modified: Mon, 09 Aug 2021 19:45:06 GMT  
		Size: 5.6 KB (5617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
