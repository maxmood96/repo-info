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
