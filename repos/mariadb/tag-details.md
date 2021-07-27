<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.39`](#mariadb10239)
-	[`mariadb:10.2.39-bionic`](#mariadb10239-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.30`](#mariadb10330)
-	[`mariadb:10.3.30-focal`](#mariadb10330-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.20`](#mariadb10420)
-	[`mariadb:10.4.20-focal`](#mariadb10420-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.11`](#mariadb10511)
-	[`mariadb:10.5.11-focal`](#mariadb10511-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.3`](#mariadb1063)
-	[`mariadb:10.6.3-focal`](#mariadb1063-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:916f530ae7417fb7d931bea36393c60a52664609428c187e7f5c10ce10b4c8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
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
$ docker pull mariadb@sha256:114d11abcb84ebc9454b0c5518cbe2ee0415da48feaa147c363cd724d61fe31a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117631233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad22b475e7bdb9d924434ef90ce5c34175e51ed68ea80e18e1227957ed29de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 05:16:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 05:18:07 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:18:15 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 05:19:27 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 05:19:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 05:20:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:20:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 05:20:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:20:52 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:20:55 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:21:07 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:11 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 05:21:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:27:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:27:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:27:44 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:27:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:27:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:28:05 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:28:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc1a4f2a6e5340400c7d1743f57829ac980465b950eb1f83134a2eb687b30a7`  
		Last Modified: Wed, 14 Jul 2021 05:32:21 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292930dcdf394d716d86d8757eb3c523e8ee953fe1706df150d17d4f9362f156`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 5.6 MB (5630442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6639bce78c6b08955c2811318c4a4405f56d66f9cbdcdf8c6dd89fe0d5379e84`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 3.5 MB (3528903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd82d7b69d04c102fb42f9ba4ca3ee679a96cc325f0b30ba1244372edfb19230`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8c86b1624bb20b557f7e6a3bc085a5e8e3d6942c3250a165fd38ead02e8fc`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 1.9 MB (1938665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51445da201ca93a7b1254fadacf5ddfde3cb7d990c9dbc95efd38a4cae452ccd`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acefbafab0d89c09b03ec90f4c477baa4c96f3d3ffcbbd707cf4942fd3f44a4`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9791c838dadf0c99af1d47f3b3a49ffcca12203b69f6e7aa7d22850b075c8355`  
		Last Modified: Wed, 14 Jul 2021 05:32:30 GMT  
		Size: 76.1 MB (76091975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af4b531aad54096936f4f631ea90bcb30fd266d08e4580dad559b590a6407ed`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2aa2634195bff171df267763ee6ec446cffa1b712eb7b4fc81f4ac7410ee5`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:916f530ae7417fb7d931bea36393c60a52664609428c187e7f5c10ce10b4c8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
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
$ docker pull mariadb@sha256:114d11abcb84ebc9454b0c5518cbe2ee0415da48feaa147c363cd724d61fe31a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117631233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad22b475e7bdb9d924434ef90ce5c34175e51ed68ea80e18e1227957ed29de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 05:16:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 05:18:07 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:18:15 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 05:19:27 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 05:19:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 05:20:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:20:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 05:20:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:20:52 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:20:55 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:21:07 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:11 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 05:21:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:27:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:27:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:27:44 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:27:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:27:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:28:05 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:28:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc1a4f2a6e5340400c7d1743f57829ac980465b950eb1f83134a2eb687b30a7`  
		Last Modified: Wed, 14 Jul 2021 05:32:21 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292930dcdf394d716d86d8757eb3c523e8ee953fe1706df150d17d4f9362f156`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 5.6 MB (5630442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6639bce78c6b08955c2811318c4a4405f56d66f9cbdcdf8c6dd89fe0d5379e84`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 3.5 MB (3528903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd82d7b69d04c102fb42f9ba4ca3ee679a96cc325f0b30ba1244372edfb19230`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8c86b1624bb20b557f7e6a3bc085a5e8e3d6942c3250a165fd38ead02e8fc`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 1.9 MB (1938665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51445da201ca93a7b1254fadacf5ddfde3cb7d990c9dbc95efd38a4cae452ccd`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acefbafab0d89c09b03ec90f4c477baa4c96f3d3ffcbbd707cf4942fd3f44a4`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9791c838dadf0c99af1d47f3b3a49ffcca12203b69f6e7aa7d22850b075c8355`  
		Last Modified: Wed, 14 Jul 2021 05:32:30 GMT  
		Size: 76.1 MB (76091975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af4b531aad54096936f4f631ea90bcb30fd266d08e4580dad559b590a6407ed`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2aa2634195bff171df267763ee6ec446cffa1b712eb7b4fc81f4ac7410ee5`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.39`

```console
$ docker pull mariadb@sha256:916f530ae7417fb7d931bea36393c60a52664609428c187e7f5c10ce10b4c8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.39` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.39` - linux; arm64 variant v8

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

### `mariadb:10.2.39` - linux; ppc64le

```console
$ docker pull mariadb@sha256:114d11abcb84ebc9454b0c5518cbe2ee0415da48feaa147c363cd724d61fe31a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117631233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad22b475e7bdb9d924434ef90ce5c34175e51ed68ea80e18e1227957ed29de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 05:16:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 05:18:07 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:18:15 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 05:19:27 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 05:19:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 05:20:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:20:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 05:20:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:20:52 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:20:55 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:21:07 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:11 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 05:21:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:27:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:27:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:27:44 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:27:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:27:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:28:05 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:28:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc1a4f2a6e5340400c7d1743f57829ac980465b950eb1f83134a2eb687b30a7`  
		Last Modified: Wed, 14 Jul 2021 05:32:21 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292930dcdf394d716d86d8757eb3c523e8ee953fe1706df150d17d4f9362f156`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 5.6 MB (5630442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6639bce78c6b08955c2811318c4a4405f56d66f9cbdcdf8c6dd89fe0d5379e84`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 3.5 MB (3528903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd82d7b69d04c102fb42f9ba4ca3ee679a96cc325f0b30ba1244372edfb19230`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8c86b1624bb20b557f7e6a3bc085a5e8e3d6942c3250a165fd38ead02e8fc`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 1.9 MB (1938665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51445da201ca93a7b1254fadacf5ddfde3cb7d990c9dbc95efd38a4cae452ccd`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acefbafab0d89c09b03ec90f4c477baa4c96f3d3ffcbbd707cf4942fd3f44a4`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9791c838dadf0c99af1d47f3b3a49ffcca12203b69f6e7aa7d22850b075c8355`  
		Last Modified: Wed, 14 Jul 2021 05:32:30 GMT  
		Size: 76.1 MB (76091975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af4b531aad54096936f4f631ea90bcb30fd266d08e4580dad559b590a6407ed`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2aa2634195bff171df267763ee6ec446cffa1b712eb7b4fc81f4ac7410ee5`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.39-bionic`

```console
$ docker pull mariadb@sha256:916f530ae7417fb7d931bea36393c60a52664609428c187e7f5c10ce10b4c8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.39-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:5c0e9eb27ad2c186cb9b10d0310f3f30eeb5ecc09e9ecf36e432f782f570e9e0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109304876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ecaf9c767e5b4386e0943490478c267578da00339064a347064fdccabf6ac8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:15 GMT
ADD file:7274ece1917848683250bbeda9eacf6eb7510481cbaa177880e3a60b4133e35b in / 
# Tue, 13 Jul 2021 22:29:15 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:59:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:59:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:59:41 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:59:59 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 01:00:00 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 01:00:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 01:00:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 01:00:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 01:00:23 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:26 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 01:00:28 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:30 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 01:00:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 01:00:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 01:01:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 01:01:35 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 01:01:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 01:01:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 01:01:38 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 01:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e7ae86ffe2df0787131a4c49ace1b018fd38d62929b007d86bdd1f825e56a852`  
		Last Modified: Tue, 13 Jul 2021 22:31:03 GMT  
		Size: 26.7 MB (26706145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02f3767f093ff77f35d70e64fabf43d7e4f3328f83e55442f0496a755cc4d64b`  
		Last Modified: Wed, 14 Jul 2021 01:05:30 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f57ce2f183ce7276382d0923cc09ec6d5b032340a6e77fae51524c3d53e1cd`  
		Last Modified: Wed, 14 Jul 2021 01:05:29 GMT  
		Size: 4.8 MB (4813397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72574b5b8e280c2c544716ac987bb628a29dffddf0b834fe1f49ac5cc597e668`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 3.5 MB (3547597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03b95e8526938e2cfe043471fa153a469217921fefd07794dc79b692a9ec070`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73bc88eeea165da977334c6a9b104bab922ac53ee71c974a3a2d24cd323e8e6`  
		Last Modified: Wed, 14 Jul 2021 01:05:28 GMT  
		Size: 1.6 MB (1585899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56fbed1b6870267362f5204259d106fb13d92c0573c9f16e4e151ccf98b2035`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1976b29470905458e13aab07a8c0662107ea44f4f2be580aaa7f05409390f96`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec62c50c2339447743375b73310b58b3553a584c23819c8a8a6b750e6d0ae0`  
		Last Modified: Wed, 14 Jul 2021 01:05:37 GMT  
		Size: 72.6 MB (72638596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f53eb6cd79a22c0ea3ee1450aba9c8eadd87915610aed9b86159e1acd565be`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b9776cfa8c66e0b0996411fda717994fd2616e335532df5e6150a2a528cd5`  
		Last Modified: Wed, 14 Jul 2021 01:05:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.39-bionic` - linux; arm64 variant v8

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

### `mariadb:10.2.39-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:114d11abcb84ebc9454b0c5518cbe2ee0415da48feaa147c363cd724d61fe31a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117631233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad22b475e7bdb9d924434ef90ce5c34175e51ed68ea80e18e1227957ed29de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:21:55 GMT
ADD file:45b627081344651e16f78f7bbb0da81c1dcc0300835ab0f4bdd6dd93621e461d in / 
# Tue, 13 Jul 2021 23:22:00 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 05:16:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 05:18:07 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:18:15 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 05:19:27 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 05:19:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 05:20:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 05:20:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 05:20:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:20:52 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:20:55 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 14 Jul 2021 05:21:07 GMT
ARG MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:11 GMT
ENV MARIADB_VERSION=1:10.2.39+maria~bionic
# Wed, 14 Jul 2021 05:21:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
# Wed, 14 Jul 2021 05:21:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:27:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:27:39 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:27:44 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:27:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.39/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:27:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:28:05 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:28:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b4e702a7ed6378fce702bcf7ca7d37185cd6d8387370cd090b9dc4bf5844f47c`  
		Last Modified: Tue, 13 Jul 2021 23:27:12 GMT  
		Size: 30.4 MB (30427987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc1a4f2a6e5340400c7d1743f57829ac980465b950eb1f83134a2eb687b30a7`  
		Last Modified: Wed, 14 Jul 2021 05:32:21 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292930dcdf394d716d86d8757eb3c523e8ee953fe1706df150d17d4f9362f156`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 5.6 MB (5630442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6639bce78c6b08955c2811318c4a4405f56d66f9cbdcdf8c6dd89fe0d5379e84`  
		Last Modified: Wed, 14 Jul 2021 05:32:18 GMT  
		Size: 3.5 MB (3528903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd82d7b69d04c102fb42f9ba4ca3ee679a96cc325f0b30ba1244372edfb19230`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d8c86b1624bb20b557f7e6a3bc085a5e8e3d6942c3250a165fd38ead02e8fc`  
		Last Modified: Wed, 14 Jul 2021 05:32:17 GMT  
		Size: 1.9 MB (1938665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51445da201ca93a7b1254fadacf5ddfde3cb7d990c9dbc95efd38a4cae452ccd`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acefbafab0d89c09b03ec90f4c477baa4c96f3d3ffcbbd707cf4942fd3f44a4`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9791c838dadf0c99af1d47f3b3a49ffcca12203b69f6e7aa7d22850b075c8355`  
		Last Modified: Wed, 14 Jul 2021 05:32:30 GMT  
		Size: 76.1 MB (76091975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af4b531aad54096936f4f631ea90bcb30fd266d08e4580dad559b590a6407ed`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 5.6 KB (5595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc2aa2634195bff171df267763ee6ec446cffa1b712eb7b4fc81f4ac7410ee5`  
		Last Modified: Wed, 14 Jul 2021 05:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:61f4ff79ee04c3f6aeb8ba584703a5fd3e84ba080b4fece16fc56bffb90f1b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0102d7bd369fd38b8592573f23829f4070e507777d349021860e48650cc878f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117601380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a136bad675ee6e64e345e01c3c841ad40c8ca965b5e1180538ecad7b8b94955b`
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
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:52:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:43 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:44 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:44 GMT
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
	-	`sha256:7d77971fbcccb558d07507e2e85d537011ae7aadb0e93c80f0bbd3cc3189edd8`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0df2d3625018a9c3ca341cda01fd9890880f70abffbcfdc35812e5501738d7`  
		Last Modified: Mon, 26 Jul 2021 22:57:14 GMT  
		Size: 79.4 MB (79395269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e700aabcbd11ee1be66439444f7e33f92b448ff571eeadbcfc0e1965ebc739e5`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac5ce70c6ec5689935793d125923c05555372b0cabaac9ad17466ff98bf95e`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:634eb2f32ddd177800ec0f5a10e3ed49cd0596a4b11e779976e2568bd54a836e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130866534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fbe8645a7da2eb9bd87a4589168b742dd21804947514ba3374070a618dd6fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:07:28 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:36 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:50 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:08:27 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:09:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:09:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:13:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:13:52 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:13:55 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:14:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:14:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:14:26 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:14:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d589b30fd663302db8f8b76122ae650b044bb44e3d6db554e78ce92ae8f58f`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe703049695be76baebba42e3ae1bff84360ef5ba6a10ff7868b8944b19fa9cd`  
		Last Modified: Wed, 14 Jul 2021 05:31:54 GMT  
		Size: 84.7 MB (84659138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2316195d6491cccadc01ba26a66738afce0e62d18faaa3d741aa60dde92cb048`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eeb22418619223a089e9dac56484b3c79d16a862e3915e09834ac1af38c465`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:61f4ff79ee04c3f6aeb8ba584703a5fd3e84ba080b4fece16fc56bffb90f1b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0102d7bd369fd38b8592573f23829f4070e507777d349021860e48650cc878f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117601380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a136bad675ee6e64e345e01c3c841ad40c8ca965b5e1180538ecad7b8b94955b`
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
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:52:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:43 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:44 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:44 GMT
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
	-	`sha256:7d77971fbcccb558d07507e2e85d537011ae7aadb0e93c80f0bbd3cc3189edd8`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0df2d3625018a9c3ca341cda01fd9890880f70abffbcfdc35812e5501738d7`  
		Last Modified: Mon, 26 Jul 2021 22:57:14 GMT  
		Size: 79.4 MB (79395269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e700aabcbd11ee1be66439444f7e33f92b448ff571eeadbcfc0e1965ebc739e5`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac5ce70c6ec5689935793d125923c05555372b0cabaac9ad17466ff98bf95e`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:634eb2f32ddd177800ec0f5a10e3ed49cd0596a4b11e779976e2568bd54a836e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130866534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fbe8645a7da2eb9bd87a4589168b742dd21804947514ba3374070a618dd6fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:07:28 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:36 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:50 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:08:27 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:09:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:09:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:13:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:13:52 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:13:55 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:14:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:14:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:14:26 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:14:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d589b30fd663302db8f8b76122ae650b044bb44e3d6db554e78ce92ae8f58f`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe703049695be76baebba42e3ae1bff84360ef5ba6a10ff7868b8944b19fa9cd`  
		Last Modified: Wed, 14 Jul 2021 05:31:54 GMT  
		Size: 84.7 MB (84659138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2316195d6491cccadc01ba26a66738afce0e62d18faaa3d741aa60dde92cb048`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eeb22418619223a089e9dac56484b3c79d16a862e3915e09834ac1af38c465`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.30`

```console
$ docker pull mariadb@sha256:61f4ff79ee04c3f6aeb8ba584703a5fd3e84ba080b4fece16fc56bffb90f1b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.30` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0102d7bd369fd38b8592573f23829f4070e507777d349021860e48650cc878f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117601380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a136bad675ee6e64e345e01c3c841ad40c8ca965b5e1180538ecad7b8b94955b`
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
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:52:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:43 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:44 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:44 GMT
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
	-	`sha256:7d77971fbcccb558d07507e2e85d537011ae7aadb0e93c80f0bbd3cc3189edd8`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0df2d3625018a9c3ca341cda01fd9890880f70abffbcfdc35812e5501738d7`  
		Last Modified: Mon, 26 Jul 2021 22:57:14 GMT  
		Size: 79.4 MB (79395269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e700aabcbd11ee1be66439444f7e33f92b448ff571eeadbcfc0e1965ebc739e5`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac5ce70c6ec5689935793d125923c05555372b0cabaac9ad17466ff98bf95e`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30` - linux; ppc64le

```console
$ docker pull mariadb@sha256:634eb2f32ddd177800ec0f5a10e3ed49cd0596a4b11e779976e2568bd54a836e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130866534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fbe8645a7da2eb9bd87a4589168b742dd21804947514ba3374070a618dd6fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:07:28 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:36 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:50 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:08:27 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:09:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:09:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:13:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:13:52 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:13:55 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:14:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:14:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:14:26 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:14:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d589b30fd663302db8f8b76122ae650b044bb44e3d6db554e78ce92ae8f58f`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe703049695be76baebba42e3ae1bff84360ef5ba6a10ff7868b8944b19fa9cd`  
		Last Modified: Wed, 14 Jul 2021 05:31:54 GMT  
		Size: 84.7 MB (84659138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2316195d6491cccadc01ba26a66738afce0e62d18faaa3d741aa60dde92cb048`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eeb22418619223a089e9dac56484b3c79d16a862e3915e09834ac1af38c465`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.30-focal`

```console
$ docker pull mariadb@sha256:61f4ff79ee04c3f6aeb8ba584703a5fd3e84ba080b4fece16fc56bffb90f1b9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.30-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:2200220af8c594c85bec2f87015d556864bd09bf79ec400e4352736c2cce0cff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (120006043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea064dffdcbbab8e6c0474e513499b6f69e8b8c5b9e7d41b0daa515f21a59ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:58:29 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:30 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 00:58:31 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:31 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 00:58:32 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:58:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:59:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:59:05 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:59:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:59:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:59:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:59:07 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:59:07 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7485473b128a37cd5bc980f9d450777b261aa523889ed65a8d9639852e3eae`  
		Last Modified: Wed, 14 Jul 2021 01:04:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21c09395a910de4b94bff08d273244e33aecc775ab7a2716597a3b1d7e1aaf8`  
		Last Modified: Wed, 14 Jul 2021 01:05:07 GMT  
		Size: 80.1 MB (80084453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae821e04294bc113a0af411372e4882c95010797b6c4f1699ea571cc9e9989a`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fa297a84b058873441d197f56558c7e377dcd8e0f09f5a182faf1475bdc52`  
		Last Modified: Wed, 14 Jul 2021 01:04:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0102d7bd369fd38b8592573f23829f4070e507777d349021860e48650cc878f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117601380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a136bad675ee6e64e345e01c3c841ad40c8ca965b5e1180538ecad7b8b94955b`
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
# Mon, 26 Jul 2021 22:52:15 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Mon, 26 Jul 2021 22:52:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:52:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:43 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:44 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:44 GMT
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
	-	`sha256:7d77971fbcccb558d07507e2e85d537011ae7aadb0e93c80f0bbd3cc3189edd8`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc0df2d3625018a9c3ca341cda01fd9890880f70abffbcfdc35812e5501738d7`  
		Last Modified: Mon, 26 Jul 2021 22:57:14 GMT  
		Size: 79.4 MB (79395269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e700aabcbd11ee1be66439444f7e33f92b448ff571eeadbcfc0e1965ebc739e5`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eac5ce70c6ec5689935793d125923c05555372b0cabaac9ad17466ff98bf95e`  
		Last Modified: Mon, 26 Jul 2021 22:57:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.30-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:634eb2f32ddd177800ec0f5a10e3ed49cd0596a4b11e779976e2568bd54a836e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.9 MB (130866534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44fbe8645a7da2eb9bd87a4589168b742dd21804947514ba3374070a618dd6fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:07:28 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:36 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 14 Jul 2021 05:07:50 GMT
ARG MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:08:27 GMT
ENV MARIADB_VERSION=1:10.3.30+maria~focal
# Wed, 14 Jul 2021 05:09:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:09:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:13:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:13:52 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:13:55 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:14:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.30/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:14:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:14:26 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:14:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d589b30fd663302db8f8b76122ae650b044bb44e3d6db554e78ce92ae8f58f`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe703049695be76baebba42e3ae1bff84360ef5ba6a10ff7868b8944b19fa9cd`  
		Last Modified: Wed, 14 Jul 2021 05:31:54 GMT  
		Size: 84.7 MB (84659138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2316195d6491cccadc01ba26a66738afce0e62d18faaa3d741aa60dde92cb048`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eeb22418619223a089e9dac56484b3c79d16a862e3915e09834ac1af38c465`  
		Last Modified: Wed, 14 Jul 2021 05:31:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:e0c348a309279223844ebce865475f92cf6a4e3cc472d9ea7e7737d7c3a3f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b6f90b1695ee00f316ad178ced5fd60a899b6ff65b6c906007be10c1f6c5a057
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2492fcc02ad0bb125001e905a4b8ce33e52d79b607d9e1fc75fbf3b76578f6d`
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
# Mon, 26 Jul 2021 22:51:44 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:06 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:07 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:08 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:08 GMT
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
	-	`sha256:f3b8db7843fd6a90dd813f00a73b0901f7f5531a7513706c4b6207299c53280f`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ca3c10283ff7231f9d9b57da458cc4a0b482ffa128d8d0b1e8d2f70708a29`  
		Last Modified: Mon, 26 Jul 2021 22:56:40 GMT  
		Size: 84.0 MB (84008857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904b7dd0f751fddd4cbe0b9f408ea86bd811810332adc63310df8d8e3d1781e1`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee93ce3da0898b85874f145d171a0d731da8758b028a119962107faad93406d3`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:022cb8562c3c18840e4d2221a34d6505b8dd10b4830116cc553045e157700012
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135437406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d08d8f088c1dc8fb35c961177c59a18ebb9d1388c7d9efca7814845e9a6ea7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:02:18 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:24 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:27 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:31 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:02:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:06:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:06:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:06:28 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:06:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:06:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:07:00 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececdc130ffd22a30ef27f6828d332c8bc886f657461a5e30c3ceb97af9d386c`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25643a7bc86a53cd1c89faf857ff136ab06156dc173a3bcc196f537a775bcea0`  
		Last Modified: Wed, 14 Jul 2021 05:31:15 GMT  
		Size: 89.2 MB (89230011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3207ce185af93bd6bdab2e65523caa6ded605ec30a38e9e8383f01813737ca`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c58811d44be3959f6a2d3261022aab143708ccf9bce80b1022fda8987421a`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:e0c348a309279223844ebce865475f92cf6a4e3cc472d9ea7e7737d7c3a3f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b6f90b1695ee00f316ad178ced5fd60a899b6ff65b6c906007be10c1f6c5a057
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2492fcc02ad0bb125001e905a4b8ce33e52d79b607d9e1fc75fbf3b76578f6d`
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
# Mon, 26 Jul 2021 22:51:44 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:06 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:07 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:08 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:08 GMT
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
	-	`sha256:f3b8db7843fd6a90dd813f00a73b0901f7f5531a7513706c4b6207299c53280f`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ca3c10283ff7231f9d9b57da458cc4a0b482ffa128d8d0b1e8d2f70708a29`  
		Last Modified: Mon, 26 Jul 2021 22:56:40 GMT  
		Size: 84.0 MB (84008857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904b7dd0f751fddd4cbe0b9f408ea86bd811810332adc63310df8d8e3d1781e1`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee93ce3da0898b85874f145d171a0d731da8758b028a119962107faad93406d3`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:022cb8562c3c18840e4d2221a34d6505b8dd10b4830116cc553045e157700012
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135437406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d08d8f088c1dc8fb35c961177c59a18ebb9d1388c7d9efca7814845e9a6ea7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:02:18 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:24 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:27 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:31 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:02:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:06:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:06:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:06:28 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:06:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:06:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:07:00 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececdc130ffd22a30ef27f6828d332c8bc886f657461a5e30c3ceb97af9d386c`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25643a7bc86a53cd1c89faf857ff136ab06156dc173a3bcc196f537a775bcea0`  
		Last Modified: Wed, 14 Jul 2021 05:31:15 GMT  
		Size: 89.2 MB (89230011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3207ce185af93bd6bdab2e65523caa6ded605ec30a38e9e8383f01813737ca`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c58811d44be3959f6a2d3261022aab143708ccf9bce80b1022fda8987421a`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.20`

```console
$ docker pull mariadb@sha256:e0c348a309279223844ebce865475f92cf6a4e3cc472d9ea7e7737d7c3a3f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.20` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b6f90b1695ee00f316ad178ced5fd60a899b6ff65b6c906007be10c1f6c5a057
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2492fcc02ad0bb125001e905a4b8ce33e52d79b607d9e1fc75fbf3b76578f6d`
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
# Mon, 26 Jul 2021 22:51:44 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:06 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:07 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:08 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:08 GMT
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
	-	`sha256:f3b8db7843fd6a90dd813f00a73b0901f7f5531a7513706c4b6207299c53280f`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ca3c10283ff7231f9d9b57da458cc4a0b482ffa128d8d0b1e8d2f70708a29`  
		Last Modified: Mon, 26 Jul 2021 22:56:40 GMT  
		Size: 84.0 MB (84008857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904b7dd0f751fddd4cbe0b9f408ea86bd811810332adc63310df8d8e3d1781e1`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee93ce3da0898b85874f145d171a0d731da8758b028a119962107faad93406d3`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20` - linux; ppc64le

```console
$ docker pull mariadb@sha256:022cb8562c3c18840e4d2221a34d6505b8dd10b4830116cc553045e157700012
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135437406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d08d8f088c1dc8fb35c961177c59a18ebb9d1388c7d9efca7814845e9a6ea7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:02:18 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:24 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:27 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:31 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:02:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:06:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:06:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:06:28 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:06:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:06:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:07:00 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececdc130ffd22a30ef27f6828d332c8bc886f657461a5e30c3ceb97af9d386c`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25643a7bc86a53cd1c89faf857ff136ab06156dc173a3bcc196f537a775bcea0`  
		Last Modified: Wed, 14 Jul 2021 05:31:15 GMT  
		Size: 89.2 MB (89230011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3207ce185af93bd6bdab2e65523caa6ded605ec30a38e9e8383f01813737ca`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c58811d44be3959f6a2d3261022aab143708ccf9bce80b1022fda8987421a`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.20-focal`

```console
$ docker pull mariadb@sha256:e0c348a309279223844ebce865475f92cf6a4e3cc472d9ea7e7737d7c3a3f1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.20-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:873e9aaaa7780da10c339f3337abf52882a310cae2ddfd2fb3fa85c78dd44350
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124698892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4271ce8f6f798b83d152e870b3fbeaf9729badd41cf51a61c004be0ac7b578d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:57:51 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 00:57:52 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:52 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 00:57:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:58:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:58:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:58:21 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:58:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 00:58:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:58:23 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:58:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22892204a1dcc32ac7a09fbaabbd878f2b4eef3ee20dd0c577d92294c8b11a26`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a277be0f6c45f67f0267866a6cf0c2bc8d2111ba881cb0973953afd23c3164`  
		Last Modified: Wed, 14 Jul 2021 01:04:23 GMT  
		Size: 84.8 MB (84777306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54988cc2ae8f9e448e7d2bd52f22bebe8bea5b0a54fc645d6d767f63429e59f4`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb1763fc3dea70e993f8df4666cd3011f50983aabcfc90380564544584389cda`  
		Last Modified: Wed, 14 Jul 2021 01:04:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:b6f90b1695ee00f316ad178ced5fd60a899b6ff65b6c906007be10c1f6c5a057
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122214966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2492fcc02ad0bb125001e905a4b8ce33e52d79b607d9e1fc75fbf3b76578f6d`
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
# Mon, 26 Jul 2021 22:51:44 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Mon, 26 Jul 2021 22:51:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:52:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:52:06 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:52:07 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:52:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Mon, 26 Jul 2021 22:52:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:52:08 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:52:08 GMT
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
	-	`sha256:f3b8db7843fd6a90dd813f00a73b0901f7f5531a7513706c4b6207299c53280f`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ca3c10283ff7231f9d9b57da458cc4a0b482ffa128d8d0b1e8d2f70708a29`  
		Last Modified: Mon, 26 Jul 2021 22:56:40 GMT  
		Size: 84.0 MB (84008857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:904b7dd0f751fddd4cbe0b9f408ea86bd811810332adc63310df8d8e3d1781e1`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee93ce3da0898b85874f145d171a0d731da8758b028a119962107faad93406d3`  
		Last Modified: Mon, 26 Jul 2021 22:56:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.20-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:022cb8562c3c18840e4d2221a34d6505b8dd10b4830116cc553045e157700012
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135437406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d08d8f088c1dc8fb35c961177c59a18ebb9d1388c7d9efca7814845e9a6ea7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 05:02:18 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:24 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 14 Jul 2021 05:02:27 GMT
ARG MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:31 GMT
ENV MARIADB_VERSION=1:10.4.20+maria~focal
# Wed, 14 Jul 2021 05:02:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 05:02:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:06:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:06:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:06:28 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:06:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.20/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 14 Jul 2021 05:06:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:07:00 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:07:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececdc130ffd22a30ef27f6828d332c8bc886f657461a5e30c3ceb97af9d386c`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25643a7bc86a53cd1c89faf857ff136ab06156dc173a3bcc196f537a775bcea0`  
		Last Modified: Wed, 14 Jul 2021 05:31:15 GMT  
		Size: 89.2 MB (89230011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d3207ce185af93bd6bdab2e65523caa6ded605ec30a38e9e8383f01813737ca`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250c58811d44be3959f6a2d3261022aab143708ccf9bce80b1022fda8987421a`  
		Last Modified: Wed, 14 Jul 2021 05:30:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:ff92e3ea64cc2daeead8683c83bd71d59dd89c9a18f5028a403c13d4169c897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7ec0dfabb903994a993251d60d8f17ec8cde405c47d3e874f90e8d9c02d98b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124299430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4190528d7697cb4fa3e82dac7a6ed8060aad8b4903ce51115a5e7f54595520bc`
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
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:36 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:37 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:37 GMT
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
	-	`sha256:6604b04c1f52339a96859bebd33f91343289890f072cb201d45b99a89f848a0f`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb415985cd93e9f5e4e28152112d41fcc0650cf3967615f4090c28a7eb1f166`  
		Last Modified: Mon, 26 Jul 2021 22:56:05 GMT  
		Size: 86.1 MB (86093440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc506c3547349750331654d3499e343258c737e8de63523277f0129de6b0fe07`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3c4e958063e668c4b60be9353162ea168c839459014b51b69da78bb591892596
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137548326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f167b9d0653d93290a37a13092eaeaebec025fc0c61ef7eebacac0bf2aedab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:58:28 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:31 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:36 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:39 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:58:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:01:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:01:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:01:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:01:52 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:01:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d174c6ed51c5115f6d195f03fb6c627fc2c0946632b2c075a99a3d4d63c6054`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1046737457c61117b6d07d65fe0d006ff536aa2e78063d86ee064a09aacce5ff`  
		Last Modified: Wed, 14 Jul 2021 05:30:37 GMT  
		Size: 91.3 MB (91341053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f3707e70f46632320810e434316f9e9b3dd5ff46e3bb747849474dce8abfc`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:ff92e3ea64cc2daeead8683c83bd71d59dd89c9a18f5028a403c13d4169c897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7ec0dfabb903994a993251d60d8f17ec8cde405c47d3e874f90e8d9c02d98b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124299430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4190528d7697cb4fa3e82dac7a6ed8060aad8b4903ce51115a5e7f54595520bc`
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
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:36 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:37 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:37 GMT
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
	-	`sha256:6604b04c1f52339a96859bebd33f91343289890f072cb201d45b99a89f848a0f`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb415985cd93e9f5e4e28152112d41fcc0650cf3967615f4090c28a7eb1f166`  
		Last Modified: Mon, 26 Jul 2021 22:56:05 GMT  
		Size: 86.1 MB (86093440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc506c3547349750331654d3499e343258c737e8de63523277f0129de6b0fe07`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3c4e958063e668c4b60be9353162ea168c839459014b51b69da78bb591892596
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137548326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f167b9d0653d93290a37a13092eaeaebec025fc0c61ef7eebacac0bf2aedab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:58:28 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:31 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:36 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:39 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:58:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:01:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:01:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:01:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:01:52 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:01:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d174c6ed51c5115f6d195f03fb6c627fc2c0946632b2c075a99a3d4d63c6054`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1046737457c61117b6d07d65fe0d006ff536aa2e78063d86ee064a09aacce5ff`  
		Last Modified: Wed, 14 Jul 2021 05:30:37 GMT  
		Size: 91.3 MB (91341053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f3707e70f46632320810e434316f9e9b3dd5ff46e3bb747849474dce8abfc`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.11`

```console
$ docker pull mariadb@sha256:ff92e3ea64cc2daeead8683c83bd71d59dd89c9a18f5028a403c13d4169c897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.11` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7ec0dfabb903994a993251d60d8f17ec8cde405c47d3e874f90e8d9c02d98b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124299430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4190528d7697cb4fa3e82dac7a6ed8060aad8b4903ce51115a5e7f54595520bc`
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
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:36 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:37 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:37 GMT
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
	-	`sha256:6604b04c1f52339a96859bebd33f91343289890f072cb201d45b99a89f848a0f`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb415985cd93e9f5e4e28152112d41fcc0650cf3967615f4090c28a7eb1f166`  
		Last Modified: Mon, 26 Jul 2021 22:56:05 GMT  
		Size: 86.1 MB (86093440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc506c3547349750331654d3499e343258c737e8de63523277f0129de6b0fe07`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3c4e958063e668c4b60be9353162ea168c839459014b51b69da78bb591892596
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137548326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f167b9d0653d93290a37a13092eaeaebec025fc0c61ef7eebacac0bf2aedab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:58:28 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:31 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:36 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:39 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:58:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:01:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:01:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:01:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:01:52 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:01:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d174c6ed51c5115f6d195f03fb6c627fc2c0946632b2c075a99a3d4d63c6054`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1046737457c61117b6d07d65fe0d006ff536aa2e78063d86ee064a09aacce5ff`  
		Last Modified: Wed, 14 Jul 2021 05:30:37 GMT  
		Size: 91.3 MB (91341053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f3707e70f46632320810e434316f9e9b3dd5ff46e3bb747849474dce8abfc`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.11-focal`

```console
$ docker pull mariadb@sha256:ff92e3ea64cc2daeead8683c83bd71d59dd89c9a18f5028a403c13d4169c897a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.5.11-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:274de17495adb706879e52d682a4874e8a854c11ecd4d751af997b7ad6d5a15f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126864725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff83ee8fca90abb3f0ff9891da7de437edecef4e1a8e4108a90d8304caebc6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:59 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 00:57:00 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 00:57:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:57:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:57:42 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:57:42 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:57:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:57:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:57:44 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:57:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a720369b47fdd0f149e8c143bdf5c51dd13c1b27ef04d1342b05069c361ce1b3`  
		Last Modified: Wed, 14 Jul 2021 01:03:38 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c976e521f0a64e4b3f652b4a3773e75bfae5c9cd6e6faeeaa3ed055b6f24030`  
		Last Modified: Wed, 14 Jul 2021 01:03:51 GMT  
		Size: 86.9 MB (86943256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a09dfea021b87a2385efabc7278606a4b2c7b29a8ef8d4a5261b6ebd14a81c6`  
		Last Modified: Wed, 14 Jul 2021 01:03:37 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d7ec0dfabb903994a993251d60d8f17ec8cde405c47d3e874f90e8d9c02d98b9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124299430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4190528d7697cb4fa3e82dac7a6ed8060aad8b4903ce51115a5e7f54595520bc`
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
# Mon, 26 Jul 2021 22:51:15 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Mon, 26 Jul 2021 22:51:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:51:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:36 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:36 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:37 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:37 GMT
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
	-	`sha256:6604b04c1f52339a96859bebd33f91343289890f072cb201d45b99a89f848a0f`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb415985cd93e9f5e4e28152112d41fcc0650cf3967615f4090c28a7eb1f166`  
		Last Modified: Mon, 26 Jul 2021 22:56:05 GMT  
		Size: 86.1 MB (86093440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc506c3547349750331654d3499e343258c737e8de63523277f0129de6b0fe07`  
		Last Modified: Mon, 26 Jul 2021 22:55:50 GMT  
		Size: 5.6 KB (5593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.11-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3c4e958063e668c4b60be9353162ea168c839459014b51b69da78bb591892596
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137548326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f167b9d0653d93290a37a13092eaeaebec025fc0c61ef7eebacac0bf2aedab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:58:28 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:31 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 14 Jul 2021 04:58:36 GMT
ARG MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:39 GMT
ENV MARIADB_VERSION=1:10.5.11+maria~focal
# Wed, 14 Jul 2021 04:58:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:58:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 05:01:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 05:01:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 05:01:43 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 05:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 05:01:52 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 05:01:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d174c6ed51c5115f6d195f03fb6c627fc2c0946632b2c075a99a3d4d63c6054`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1046737457c61117b6d07d65fe0d006ff536aa2e78063d86ee064a09aacce5ff`  
		Last Modified: Wed, 14 Jul 2021 05:30:37 GMT  
		Size: 91.3 MB (91341053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f3707e70f46632320810e434316f9e9b3dd5ff46e3bb747849474dce8abfc`  
		Last Modified: Wed, 14 Jul 2021 05:30:18 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.3`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.3` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.3-focal`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.6.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:ce2ca7d909faae04c5f93a29eaf81ac4c24fb21a6fad60f93160c236df7062f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:84075fa0ee8106f8e2975dca79d3c6f9587b41afefa7aec57e76a2fc9506df6c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127023853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55fb7cb2f36d945c3bcb38d86768a3cd7415352889132ebcc5b59137442f7b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 22:29:34 GMT
ADD file:5c3d9d2597e01d1cee8513ff0e1344e7791e6f582be2cbd1d5777dd204780f1c in / 
# Tue, 13 Jul 2021 22:29:34 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 00:55:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 00:55:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:35 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 00:55:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 00:55:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 00:55:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 00:55:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 00:56:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 00:56:01 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 00:56:04 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:04 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 00:56:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 00:56:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 00:56:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 00:56:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 00:56:47 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 00:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 00:56:50 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 00:56:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a31c7b29f4ad2bd946738970f040825704a523ded1b9d6f9c7c7cafc6ab731df`  
		Last Modified: Tue, 13 Jul 2021 22:31:20 GMT  
		Size: 28.6 MB (28565863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7579f0f5a5a89c78a83267563c5b496c2f962d70ff4fc79aed0ac0f9bdfa39`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 1.7 KB (1744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b053ac8beecc2f1a318de9d9073b5f7ec29480f6874c04f7bc1191bce40d4d85`  
		Last Modified: Wed, 14 Jul 2021 01:02:53 GMT  
		Size: 5.5 MB (5488810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ca9dedd40093104857c4d20368d64942336b341d1b1044866870b278602ae5`  
		Last Modified: Wed, 14 Jul 2021 01:02:52 GMT  
		Size: 3.6 MB (3582311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa935b0083f7acbae5b94431989e42f3721636b152696790cd8dc11da7b595f`  
		Last Modified: Wed, 14 Jul 2021 01:02:51 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54214fc6446bc2d176c7030d9a5f1ff912db7d957dcbccb7d0fe4bd82229d653`  
		Last Modified: Wed, 14 Jul 2021 01:02:50 GMT  
		Size: 2.3 MB (2274183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82046f626e095c4c6458537555f8a53b268b966aaedc55d25fe25d61ead95b2f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f67396c69087b4c158c740418189dc548868f00089519364e979f81c58f309f`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d09818ae9aa9a470b937b7d904ccabe8466a5bcc652444a4f56e0d353f687c8`  
		Last Modified: Wed, 14 Jul 2021 01:03:03 GMT  
		Size: 87.1 MB (87102386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a8d2dc66083582d10b1a06eb98d416c85292af9fec2d58d8af70537d0b01c2`  
		Last Modified: Wed, 14 Jul 2021 01:02:48 GMT  
		Size: 5.6 KB (5592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:56f5d1d559f55e10be50862e2f731067c79097c14e62e4745b570c0fba2bc4a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124306161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f58908da62d61a71a5c5886ef11d2b267d51da22aa4f6f318760d3b87870fa`
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
# Mon, 26 Jul 2021 22:50:43 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Mon, 26 Jul 2021 22:50:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Mon, 26 Jul 2021 22:50:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Mon, 26 Jul 2021 22:51:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Mon, 26 Jul 2021 22:51:05 GMT
VOLUME [/var/lib/mysql]
# Mon, 26 Jul 2021 22:51:06 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Mon, 26 Jul 2021 22:51:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 26 Jul 2021 22:51:06 GMT
EXPOSE 3306
# Mon, 26 Jul 2021 22:51:06 GMT
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
	-	`sha256:e9e83ee51734f9cf9f46bc48e48875e563c4b70316c500ac7f2010ce8380588b`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0390133d4c7b343d3233693946da783d3d5b341f823418439e2189e4013f27`  
		Last Modified: Mon, 26 Jul 2021 22:55:12 GMT  
		Size: 86.1 MB (86100177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2cb115734fc3860082d1b4ed342d3347655e84bb803a3c0f48c664ed021cbd`  
		Last Modified: Mon, 26 Jul 2021 22:54:57 GMT  
		Size: 5.6 KB (5588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:074acf267fdf6422f350b62091c15b265ab9966d32e447bd5d50e734bbce7e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.5 MB (137513563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfcbc41fe13a3a8a37dd4b81f47ffec75904a0255725acf0ece3d34d0f269b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Jul 2021 23:22:24 GMT
ADD file:cdca4c00902f291c6bc305420b891f5149b6833b5f9892232ea690d38adfff3f in / 
# Tue, 13 Jul 2021 23:22:32 GMT
CMD ["bash"]
# Wed, 14 Jul 2021 04:49:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 14 Jul 2021 04:50:57 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:51:04 GMT
ENV GOSU_VERSION=1.13
# Wed, 14 Jul 2021 04:52:08 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 14 Jul 2021 04:52:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jul 2021 04:52:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 14 Jul 2021 04:52:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 14 Jul 2021 04:53:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 14 Jul 2021 04:53:21 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:33 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 14 Jul 2021 04:53:40 GMT
ARG MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:46 GMT
ENV MARIADB_VERSION=1:10.6.3+maria~focal
# Wed, 14 Jul 2021 04:53:51 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
# Wed, 14 Jul 2021 04:54:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 14 Jul 2021 04:57:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 14 Jul 2021 04:57:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 14 Jul 2021 04:57:49 GMT
COPY file:b3c92236ffa4530a3affc90901b4ff364200997f53728db206774632c54ed4bb in /usr/local/bin/ 
# Wed, 14 Jul 2021 04:57:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jul 2021 04:58:04 GMT
EXPOSE 3306
# Wed, 14 Jul 2021 04:58:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:157ef43c951ca9b65226089aef70b09df64b81636884260390a329c24a3c614b`  
		Last Modified: Tue, 13 Jul 2021 23:27:34 GMT  
		Size: 33.3 MB (33287846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fba8d2b8c94da007ff451842c8d94605ebf267b2fcc3fe089ce57d46869c8e`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41e53864a355951a59100a07a2800cea64227113c627a2a21440806ebd39088`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 6.7 MB (6668099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9afcdff768d8eb3c7b07a4111293d9a6af7101546e56e3581b3b6f549a3f2e`  
		Last Modified: Wed, 14 Jul 2021 05:29:28 GMT  
		Size: 3.7 MB (3670962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e242a937b290757904b3c75f01cbf8b7550419d28ec4ff6d76894a8e2b608a`  
		Last Modified: Wed, 14 Jul 2021 05:29:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c413116b1ce76674d6e27a230ccd38712c160e3f8608b2972a15ecf4c17e630e`  
		Last Modified: Wed, 14 Jul 2021 05:29:24 GMT  
		Size: 2.6 MB (2570051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424f504b7020052d75c3de99c1df20bdf6897320c1203cc2d2b1f36f8b06ffc6`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a319d032b9e794d17d44dba20a51bc4289f00439c623d690ce9f73a461fb16`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20da7fbebefd975ba9d65985baf8c330392252419cab3d1bea5d4093c8572bed`  
		Last Modified: Wed, 14 Jul 2021 05:29:42 GMT  
		Size: 91.3 MB (91306289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d33ddfad851991d1a9cd5e8e6ebcbb4dbd9f30404e065ba8908bcc577a6cf2`  
		Last Modified: Wed, 14 Jul 2021 05:29:23 GMT  
		Size: 5.6 KB (5594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
