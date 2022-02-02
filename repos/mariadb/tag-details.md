<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.41`](#mariadb10241)
-	[`mariadb:10.2.41-bionic`](#mariadb10241-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.32`](#mariadb10332)
-	[`mariadb:10.3.32-focal`](#mariadb10332-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.22`](#mariadb10422)
-	[`mariadb:10.4.22-focal`](#mariadb10422-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.13`](#mariadb10513)
-	[`mariadb:10.5.13-focal`](#mariadb10513-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.5`](#mariadb1065)
-	[`mariadb:10.6.5-focal`](#mariadb1065-focal)
-	[`mariadb:10.7`](#mariadb107)
-	[`mariadb:10.7-focal`](#mariadb107-focal)
-	[`mariadb:10.7.1`](#mariadb1071)
-	[`mariadb:10.7.1-focal`](#mariadb1071-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:007327c75f5e9e405577882062e7eda1d36100f904c4dc77ecb054e4f26d81d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:48e60803b8f918efb1ed21ded9081552f367b5216d9ac06aa7b5e181450db736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109369129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd91d1eaa8d5095823ca3b2159f1e6bef35a2f6af76439611fb5a82d7b27497`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:48:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:48:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:48:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:48:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:48:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:49:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 03:49:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:50:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:50:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:50:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:50:05 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:50:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07efdb86cae7e435924d7a9e50100f074c88cba99444bfff1d80715115980a97`  
		Last Modified: Wed, 02 Feb 2022 03:53:25 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060731bdf4df0f74621d939ac11c89e450590bf7c1dbfb105ac8b7f9c98f0955`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 4.8 MB (4813104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f687d67df15eef4572ca1225fb9c265057a09f90f8d9feab521301db6a7edb9`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 3.6 MB (3552933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323b153f8d8f0a953f57b7826a84da98ce091b402f27cb8a08c2863b34c02155`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3694ff0bb5f01f872cf149cd4a44ade573695d2f8cc1e34fa78109cbc4e73e`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 1.6 MB (1583439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be50f6f15fc5e2b073a82c355d1aa91461c24ef7587f679e9e701768123eaa9e`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383528fad00d7a0dfb15e608d24fa86016c0cb2958a3955d378018b2554befe`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0d9644a75b0d8b71d2b305a999a29fcaff5fabbbb855c19fd5617709462e0e`  
		Last Modified: Wed, 02 Feb 2022 03:53:32 GMT  
		Size: 72.7 MB (72698322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7580b88fa9d355df616b08e170e6eb55f5b6bd528d2b17392c571eda79269636`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258aa25b26ded56d5b7eb32dcd83d7b6dd2905c593e465274463811a3033f002`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:037f2a18cf7603c2e0abcabbf473a47033e2844299afef52e9d75e25ac8daf98
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104236656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af1a2a8b723f2432291c45b98b044ae96240e022f39a8c8dd4907e7d684fdf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:52:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:52:53 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:52:54 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:53:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:53:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:53:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:53:33 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:54:11 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:12 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 04:54:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:56:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:56:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:56:26 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:56:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:56:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:56:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d51d5555b0be323004789a04cced02ff0e994d6f064b233ba55f2726783a5`  
		Last Modified: Wed, 02 Feb 2022 05:00:54 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f080fb063742c7cdc76ad616a47481da1dedcb1af5c6f33945940fdd731ab`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 4.3 MB (4261558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf986fb556112d7708edf0691efbf12e3c96272d66d64a23f482fed60196b1`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 3.2 MB (3207341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f4aef644fe2bd25dd2f14a2d5c045c287b4ecb29b20b230570f72556d3eb03`  
		Last Modified: Wed, 02 Feb 2022 05:00:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243e84742e7b6d15fc971bd7866e82c5199dd4fd6974c566d30acb0d11cc536`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 1.5 MB (1529550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53ce770cae28b46d4ac524f9bd2cc33d3addc94350747a5a75a2a16346bdbe2`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1a1e628afb1ef1aaf8495a07d9404153bfc33f67f1abd15d77c2a747817660`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b429f0258d8be046f3dd1d898cd67cc76fc03b6f3c22de3210b231b80a38eab`  
		Last Modified: Wed, 02 Feb 2022 05:01:00 GMT  
		Size: 71.5 MB (71495285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c683bd532a9dd067683f9b4b93037c1e5603affbee76a346e0a9dc2e0b268ef6`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb263c423a2c8a3ed22929cdd18072d3a484d1900e88c05419216ea19d8e763`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e958613c57ccbf4e8768d163d6957ba27059861f569d6d112b92e5653a98fe65
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117704061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8c49875d8331251cd8570bfe137e21fd43ad3159d8d18147c469ca3b0a79b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:29:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:31:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:31:41 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:32:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:32:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:33:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:33:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:34:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:34:19 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:26 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:31 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 06:34:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:37:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:37:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:37:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:37:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:37:48 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:37:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3793cab5129185e888d0cee887241418d1ab6bc8f9732c017ce237abf9ba603f`  
		Last Modified: Wed, 02 Feb 2022 06:42:30 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f854f2b0750783f2c07f28d4092d70b3f72c8cacbc291ccabaf20c127e4a8197`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 5.6 MB (5630392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd0ff847987b2597bfce989e412181c3a87e74caf26341386b3e44512468fce`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 3.5 MB (3533539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e94deaa3d6268f01abfaad4b94e150724f7ccde85fdc38aaedbc56aa82a33a`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2fd884dff08b0b653b850c03d468bc1f5e8e12118d26593d7e1536f8c067b0`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 1.9 MB (1936987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a364db5113e11c5a0ab07dc75a3015c70ad00c20c361a8229ff1fc89125b2e1`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8eea891be4608f10efd1189eced892aa2a3f9f106ca6b915b601f6dc97819f`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f079ad3feda07854f4daea77cbbce606947624731953c8d3a32ff1f6ecd28`  
		Last Modified: Wed, 02 Feb 2022 06:42:39 GMT  
		Size: 76.2 MB (76152173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226296a8caaf21598031e74515460ed40cc4517ef7d0b9fbc0af24e31881f1d9`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0dd6375913a29fac6d04e896628cfb3858ae0756379cb88439e4628434739b`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:007327c75f5e9e405577882062e7eda1d36100f904c4dc77ecb054e4f26d81d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:48e60803b8f918efb1ed21ded9081552f367b5216d9ac06aa7b5e181450db736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109369129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd91d1eaa8d5095823ca3b2159f1e6bef35a2f6af76439611fb5a82d7b27497`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:48:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:48:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:48:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:48:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:48:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:49:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 03:49:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:50:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:50:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:50:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:50:05 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:50:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07efdb86cae7e435924d7a9e50100f074c88cba99444bfff1d80715115980a97`  
		Last Modified: Wed, 02 Feb 2022 03:53:25 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060731bdf4df0f74621d939ac11c89e450590bf7c1dbfb105ac8b7f9c98f0955`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 4.8 MB (4813104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f687d67df15eef4572ca1225fb9c265057a09f90f8d9feab521301db6a7edb9`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 3.6 MB (3552933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323b153f8d8f0a953f57b7826a84da98ce091b402f27cb8a08c2863b34c02155`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3694ff0bb5f01f872cf149cd4a44ade573695d2f8cc1e34fa78109cbc4e73e`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 1.6 MB (1583439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be50f6f15fc5e2b073a82c355d1aa91461c24ef7587f679e9e701768123eaa9e`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383528fad00d7a0dfb15e608d24fa86016c0cb2958a3955d378018b2554befe`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0d9644a75b0d8b71d2b305a999a29fcaff5fabbbb855c19fd5617709462e0e`  
		Last Modified: Wed, 02 Feb 2022 03:53:32 GMT  
		Size: 72.7 MB (72698322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7580b88fa9d355df616b08e170e6eb55f5b6bd528d2b17392c571eda79269636`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258aa25b26ded56d5b7eb32dcd83d7b6dd2905c593e465274463811a3033f002`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:037f2a18cf7603c2e0abcabbf473a47033e2844299afef52e9d75e25ac8daf98
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104236656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af1a2a8b723f2432291c45b98b044ae96240e022f39a8c8dd4907e7d684fdf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:52:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:52:53 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:52:54 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:53:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:53:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:53:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:53:33 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:54:11 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:12 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 04:54:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:56:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:56:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:56:26 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:56:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:56:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:56:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d51d5555b0be323004789a04cced02ff0e994d6f064b233ba55f2726783a5`  
		Last Modified: Wed, 02 Feb 2022 05:00:54 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f080fb063742c7cdc76ad616a47481da1dedcb1af5c6f33945940fdd731ab`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 4.3 MB (4261558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf986fb556112d7708edf0691efbf12e3c96272d66d64a23f482fed60196b1`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 3.2 MB (3207341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f4aef644fe2bd25dd2f14a2d5c045c287b4ecb29b20b230570f72556d3eb03`  
		Last Modified: Wed, 02 Feb 2022 05:00:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243e84742e7b6d15fc971bd7866e82c5199dd4fd6974c566d30acb0d11cc536`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 1.5 MB (1529550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53ce770cae28b46d4ac524f9bd2cc33d3addc94350747a5a75a2a16346bdbe2`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1a1e628afb1ef1aaf8495a07d9404153bfc33f67f1abd15d77c2a747817660`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b429f0258d8be046f3dd1d898cd67cc76fc03b6f3c22de3210b231b80a38eab`  
		Last Modified: Wed, 02 Feb 2022 05:01:00 GMT  
		Size: 71.5 MB (71495285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c683bd532a9dd067683f9b4b93037c1e5603affbee76a346e0a9dc2e0b268ef6`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb263c423a2c8a3ed22929cdd18072d3a484d1900e88c05419216ea19d8e763`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e958613c57ccbf4e8768d163d6957ba27059861f569d6d112b92e5653a98fe65
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117704061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8c49875d8331251cd8570bfe137e21fd43ad3159d8d18147c469ca3b0a79b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:29:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:31:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:31:41 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:32:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:32:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:33:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:33:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:34:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:34:19 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:26 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:31 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 06:34:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:37:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:37:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:37:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:37:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:37:48 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:37:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3793cab5129185e888d0cee887241418d1ab6bc8f9732c017ce237abf9ba603f`  
		Last Modified: Wed, 02 Feb 2022 06:42:30 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f854f2b0750783f2c07f28d4092d70b3f72c8cacbc291ccabaf20c127e4a8197`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 5.6 MB (5630392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd0ff847987b2597bfce989e412181c3a87e74caf26341386b3e44512468fce`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 3.5 MB (3533539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e94deaa3d6268f01abfaad4b94e150724f7ccde85fdc38aaedbc56aa82a33a`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2fd884dff08b0b653b850c03d468bc1f5e8e12118d26593d7e1536f8c067b0`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 1.9 MB (1936987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a364db5113e11c5a0ab07dc75a3015c70ad00c20c361a8229ff1fc89125b2e1`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8eea891be4608f10efd1189eced892aa2a3f9f106ca6b915b601f6dc97819f`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f079ad3feda07854f4daea77cbbce606947624731953c8d3a32ff1f6ecd28`  
		Last Modified: Wed, 02 Feb 2022 06:42:39 GMT  
		Size: 76.2 MB (76152173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226296a8caaf21598031e74515460ed40cc4517ef7d0b9fbc0af24e31881f1d9`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0dd6375913a29fac6d04e896628cfb3858ae0756379cb88439e4628434739b`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.41`

```console
$ docker pull mariadb@sha256:007327c75f5e9e405577882062e7eda1d36100f904c4dc77ecb054e4f26d81d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.41` - linux; amd64

```console
$ docker pull mariadb@sha256:48e60803b8f918efb1ed21ded9081552f367b5216d9ac06aa7b5e181450db736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109369129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd91d1eaa8d5095823ca3b2159f1e6bef35a2f6af76439611fb5a82d7b27497`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:48:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:48:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:48:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:48:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:48:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:49:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 03:49:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:50:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:50:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:50:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:50:05 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:50:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07efdb86cae7e435924d7a9e50100f074c88cba99444bfff1d80715115980a97`  
		Last Modified: Wed, 02 Feb 2022 03:53:25 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060731bdf4df0f74621d939ac11c89e450590bf7c1dbfb105ac8b7f9c98f0955`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 4.8 MB (4813104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f687d67df15eef4572ca1225fb9c265057a09f90f8d9feab521301db6a7edb9`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 3.6 MB (3552933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323b153f8d8f0a953f57b7826a84da98ce091b402f27cb8a08c2863b34c02155`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3694ff0bb5f01f872cf149cd4a44ade573695d2f8cc1e34fa78109cbc4e73e`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 1.6 MB (1583439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be50f6f15fc5e2b073a82c355d1aa91461c24ef7587f679e9e701768123eaa9e`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383528fad00d7a0dfb15e608d24fa86016c0cb2958a3955d378018b2554befe`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0d9644a75b0d8b71d2b305a999a29fcaff5fabbbb855c19fd5617709462e0e`  
		Last Modified: Wed, 02 Feb 2022 03:53:32 GMT  
		Size: 72.7 MB (72698322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7580b88fa9d355df616b08e170e6eb55f5b6bd528d2b17392c571eda79269636`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258aa25b26ded56d5b7eb32dcd83d7b6dd2905c593e465274463811a3033f002`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:037f2a18cf7603c2e0abcabbf473a47033e2844299afef52e9d75e25ac8daf98
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104236656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af1a2a8b723f2432291c45b98b044ae96240e022f39a8c8dd4907e7d684fdf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:52:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:52:53 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:52:54 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:53:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:53:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:53:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:53:33 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:54:11 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:12 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 04:54:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:56:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:56:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:56:26 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:56:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:56:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:56:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d51d5555b0be323004789a04cced02ff0e994d6f064b233ba55f2726783a5`  
		Last Modified: Wed, 02 Feb 2022 05:00:54 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f080fb063742c7cdc76ad616a47481da1dedcb1af5c6f33945940fdd731ab`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 4.3 MB (4261558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf986fb556112d7708edf0691efbf12e3c96272d66d64a23f482fed60196b1`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 3.2 MB (3207341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f4aef644fe2bd25dd2f14a2d5c045c287b4ecb29b20b230570f72556d3eb03`  
		Last Modified: Wed, 02 Feb 2022 05:00:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243e84742e7b6d15fc971bd7866e82c5199dd4fd6974c566d30acb0d11cc536`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 1.5 MB (1529550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53ce770cae28b46d4ac524f9bd2cc33d3addc94350747a5a75a2a16346bdbe2`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1a1e628afb1ef1aaf8495a07d9404153bfc33f67f1abd15d77c2a747817660`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b429f0258d8be046f3dd1d898cd67cc76fc03b6f3c22de3210b231b80a38eab`  
		Last Modified: Wed, 02 Feb 2022 05:01:00 GMT  
		Size: 71.5 MB (71495285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c683bd532a9dd067683f9b4b93037c1e5603affbee76a346e0a9dc2e0b268ef6`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb263c423a2c8a3ed22929cdd18072d3a484d1900e88c05419216ea19d8e763`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e958613c57ccbf4e8768d163d6957ba27059861f569d6d112b92e5653a98fe65
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117704061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8c49875d8331251cd8570bfe137e21fd43ad3159d8d18147c469ca3b0a79b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:29:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:31:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:31:41 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:32:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:32:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:33:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:33:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:34:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:34:19 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:26 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:31 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 06:34:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:37:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:37:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:37:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:37:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:37:48 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:37:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3793cab5129185e888d0cee887241418d1ab6bc8f9732c017ce237abf9ba603f`  
		Last Modified: Wed, 02 Feb 2022 06:42:30 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f854f2b0750783f2c07f28d4092d70b3f72c8cacbc291ccabaf20c127e4a8197`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 5.6 MB (5630392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd0ff847987b2597bfce989e412181c3a87e74caf26341386b3e44512468fce`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 3.5 MB (3533539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e94deaa3d6268f01abfaad4b94e150724f7ccde85fdc38aaedbc56aa82a33a`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2fd884dff08b0b653b850c03d468bc1f5e8e12118d26593d7e1536f8c067b0`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 1.9 MB (1936987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a364db5113e11c5a0ab07dc75a3015c70ad00c20c361a8229ff1fc89125b2e1`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8eea891be4608f10efd1189eced892aa2a3f9f106ca6b915b601f6dc97819f`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f079ad3feda07854f4daea77cbbce606947624731953c8d3a32ff1f6ecd28`  
		Last Modified: Wed, 02 Feb 2022 06:42:39 GMT  
		Size: 76.2 MB (76152173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226296a8caaf21598031e74515460ed40cc4517ef7d0b9fbc0af24e31881f1d9`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0dd6375913a29fac6d04e896628cfb3858ae0756379cb88439e4628434739b`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.41-bionic`

```console
$ docker pull mariadb@sha256:007327c75f5e9e405577882062e7eda1d36100f904c4dc77ecb054e4f26d81d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2.41-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:48e60803b8f918efb1ed21ded9081552f367b5216d9ac06aa7b5e181450db736
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.4 MB (109369129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd91d1eaa8d5095823ca3b2159f1e6bef35a2f6af76439611fb5a82d7b27497`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:36 GMT
ADD file:c6039a4f004b6b6c2e4c281a228d64d8410cb9fdf0c67776f84bb173d3522be1 in / 
# Wed, 02 Feb 2022 02:14:36 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:48:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:48:22 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:48:36 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:48:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:48:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:48:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:49:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 03:49:21 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 03:49:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 03:49:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:50:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:50:04 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:50:04 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:50:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:50:05 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:50:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:68e7bb398b9ff421236990bfeaf5c1feab26c590eed93489e245375c23551e2a`  
		Last Modified: Sat, 29 Jan 2022 14:35:20 GMT  
		Size: 26.7 MB (26708066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07efdb86cae7e435924d7a9e50100f074c88cba99444bfff1d80715115980a97`  
		Last Modified: Wed, 02 Feb 2022 03:53:25 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060731bdf4df0f74621d939ac11c89e450590bf7c1dbfb105ac8b7f9c98f0955`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 4.8 MB (4813104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f687d67df15eef4572ca1225fb9c265057a09f90f8d9feab521301db6a7edb9`  
		Last Modified: Wed, 02 Feb 2022 03:53:24 GMT  
		Size: 3.6 MB (3552933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323b153f8d8f0a953f57b7826a84da98ce091b402f27cb8a08c2863b34c02155`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3694ff0bb5f01f872cf149cd4a44ade573695d2f8cc1e34fa78109cbc4e73e`  
		Last Modified: Wed, 02 Feb 2022 03:53:23 GMT  
		Size: 1.6 MB (1583439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be50f6f15fc5e2b073a82c355d1aa91461c24ef7587f679e9e701768123eaa9e`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.2 KB (5171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383528fad00d7a0dfb15e608d24fa86016c0cb2958a3955d378018b2554befe`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0d9644a75b0d8b71d2b305a999a29fcaff5fabbbb855c19fd5617709462e0e`  
		Last Modified: Wed, 02 Feb 2022 03:53:32 GMT  
		Size: 72.7 MB (72698322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7580b88fa9d355df616b08e170e6eb55f5b6bd528d2b17392c571eda79269636`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258aa25b26ded56d5b7eb32dcd83d7b6dd2905c593e465274463811a3033f002`  
		Last Modified: Wed, 02 Feb 2022 03:53:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41-bionic` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:037f2a18cf7603c2e0abcabbf473a47033e2844299afef52e9d75e25ac8daf98
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104236656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af1a2a8b723f2432291c45b98b044ae96240e022f39a8c8dd4907e7d684fdf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:18 GMT
ADD file:6c6588e8deb686903374087994742c9d5e77393babbbffd56aea9d4e6c888aa7 in / 
# Wed, 02 Feb 2022 03:19:18 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:52:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:52:53 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:52:54 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:53:16 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:53:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:53:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:53:33 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:54:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:54:11 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:12 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 04:54:13 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:14 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 04:54:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 04:54:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:56:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:56:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:56:26 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:56:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:56:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:56:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:02b7ffdbddc71205d24598c17b9c600df7cc8d35fb49e550250299ce97e1c96e`  
		Last Modified: Wed, 02 Feb 2022 03:21:06 GMT  
		Size: 23.7 MB (23729736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d51d5555b0be323004789a04cced02ff0e994d6f064b233ba55f2726783a5`  
		Last Modified: Wed, 02 Feb 2022 05:00:54 GMT  
		Size: 1.9 KB (1851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f080fb063742c7cdc76ad616a47481da1dedcb1af5c6f33945940fdd731ab`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 4.3 MB (4261558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf986fb556112d7708edf0691efbf12e3c96272d66d64a23f482fed60196b1`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 3.2 MB (3207341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f4aef644fe2bd25dd2f14a2d5c045c287b4ecb29b20b230570f72556d3eb03`  
		Last Modified: Wed, 02 Feb 2022 05:00:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243e84742e7b6d15fc971bd7866e82c5199dd4fd6974c566d30acb0d11cc536`  
		Last Modified: Wed, 02 Feb 2022 05:00:52 GMT  
		Size: 1.5 MB (1529550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53ce770cae28b46d4ac524f9bd2cc33d3addc94350747a5a75a2a16346bdbe2`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.1 KB (5147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1a1e628afb1ef1aaf8495a07d9404153bfc33f67f1abd15d77c2a747817660`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b429f0258d8be046f3dd1d898cd67cc76fc03b6f3c22de3210b231b80a38eab`  
		Last Modified: Wed, 02 Feb 2022 05:01:00 GMT  
		Size: 71.5 MB (71495285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c683bd532a9dd067683f9b4b93037c1e5603affbee76a346e0a9dc2e0b268ef6`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb263c423a2c8a3ed22929cdd18072d3a484d1900e88c05419216ea19d8e763`  
		Last Modified: Wed, 02 Feb 2022 05:00:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.41-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e958613c57ccbf4e8768d163d6957ba27059861f569d6d112b92e5653a98fe65
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117704061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8c49875d8331251cd8570bfe137e21fd43ad3159d8d18147c469ca3b0a79b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:49:58 GMT
ADD file:19b6b516bfde37805273abae0012aaceb45030dcc0c1dbc11828a4dfa6549c29 in / 
# Wed, 02 Feb 2022 03:50:03 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:29:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:31:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:31:41 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:32:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:32:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:33:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc1 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:33:29 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:34:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:34:19 GMT
ARG MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:23 GMT
ENV MARIADB_MAJOR=10.2
# Wed, 02 Feb 2022 06:34:26 GMT
ARG MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:31 GMT
ENV MARIADB_VERSION=1:10.2.41+maria~bionic
# Wed, 02 Feb 2022 06:34:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
# Wed, 02 Feb 2022 06:34:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:37:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:37:32 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:37:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.41/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:37:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:37:48 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:37:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1dc99fe180768d17487534d27fca7d2aea3e7473c284314a65af7be77144eeaa`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 30.4 MB (30437685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3793cab5129185e888d0cee887241418d1ab6bc8f9732c017ce237abf9ba603f`  
		Last Modified: Wed, 02 Feb 2022 06:42:30 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f854f2b0750783f2c07f28d4092d70b3f72c8cacbc291ccabaf20c127e4a8197`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 5.6 MB (5630392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd0ff847987b2597bfce989e412181c3a87e74caf26341386b3e44512468fce`  
		Last Modified: Wed, 02 Feb 2022 06:42:28 GMT  
		Size: 3.5 MB (3533539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e94deaa3d6268f01abfaad4b94e150724f7ccde85fdc38aaedbc56aa82a33a`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2fd884dff08b0b653b850c03d468bc1f5e8e12118d26593d7e1536f8c067b0`  
		Last Modified: Wed, 02 Feb 2022 06:42:27 GMT  
		Size: 1.9 MB (1936987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a364db5113e11c5a0ab07dc75a3015c70ad00c20c361a8229ff1fc89125b2e1`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.2 KB (5173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c8eea891be4608f10efd1189eced892aa2a3f9f106ca6b915b601f6dc97819f`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e0f079ad3feda07854f4daea77cbbce606947624731953c8d3a32ff1f6ecd28`  
		Last Modified: Wed, 02 Feb 2022 06:42:39 GMT  
		Size: 76.2 MB (76152173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226296a8caaf21598031e74515460ed40cc4517ef7d0b9fbc0af24e31881f1d9`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0dd6375913a29fac6d04e896628cfb3858ae0756379cb88439e4628434739b`  
		Last Modified: Wed, 02 Feb 2022 06:42:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:a25e7c87fe20c6d035fe81003937a8d732574ecf54466d0294da3423b64af80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:d6cc105c8baf52721ca0262b65dc1dff052297a78210d6ee3aef21abd3c2e5e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120109623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d01679c3b287ed73096d4ab595c64dcd49861ae3c3afa5d6ed3d46170093c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:59 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:48:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14f6657b5012974c330aa61fda56ad428cdb122487025b044c35b7b120720b5`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020be96129bacda3f951bb8abc57497de86a67e795a1597ba66ee63d428d1946`  
		Last Modified: Wed, 02 Feb 2022 03:53:04 GMT  
		Size: 80.2 MB (80187895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a486976bcda3aff4bea48c0f0f227d0a6a4e8952b280bf6065fbd652f0fb36`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3911f3f865240dfab0f331fec343ce0774717fd728a25bc70096d6d119062a8`  
		Last Modified: Wed, 02 Feb 2022 03:52:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3c249faca616b07726405956519b2b71bd69cf8689b5372d71d5fb0711d9bf5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117607720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5519cd809348cdad66374f4d07261b64b8ee0b059e50fcfde4e081e150f86a35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:49:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:44 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:45 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:46 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:49:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:52:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:52:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:52:29 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:52:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:52:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:52:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678769c76a50c67030c5a1e90a7774234cba02836cb78c79f737f8ebe034cd8a`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf16155dea7332141307a55607f7f670dd436220f999aaa8b44b7425ded11c5`  
		Last Modified: Wed, 02 Feb 2022 05:00:03 GMT  
		Size: 79.5 MB (79532623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7039bab2ea841283f082ef9e31ee71740f7c58eef5633518bd0d3295e61cb`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee4e7796f36d979a8a5e5e464c4d256a68eca1290e71629430ff5e38547fbd`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0a9f3761f792825d26131e6dd836b389c11d9744570cd4c28decef9b4fb74adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130989765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a16fc01c356f2cef9736753d4be409542af6a7eb671c891274a684d29bfbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:24:11 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:14 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:18 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:21 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:24:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:28:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:28:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:28:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:28:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:28:54 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:29:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3b1ab7b85e06c4533dfd28abcf42980715b35a04ebbfeae2b2d7e5c7b3ef6`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f8905242f2496fc2affaeaf880ea5a6a5b3d74f5462a15c116c91e9a376bc9`  
		Last Modified: Wed, 02 Feb 2022 06:42:01 GMT  
		Size: 84.8 MB (84785104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678426eb561b01ae11ac3b45e61f1d4b24b0da25b0a83da69fb58be44188ce20`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931d168ecad36931705df37e8bf67cca09f3ff3a704e7bf7f8fc11778d1842e5`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:a25e7c87fe20c6d035fe81003937a8d732574ecf54466d0294da3423b64af80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:d6cc105c8baf52721ca0262b65dc1dff052297a78210d6ee3aef21abd3c2e5e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120109623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d01679c3b287ed73096d4ab595c64dcd49861ae3c3afa5d6ed3d46170093c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:59 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:48:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14f6657b5012974c330aa61fda56ad428cdb122487025b044c35b7b120720b5`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020be96129bacda3f951bb8abc57497de86a67e795a1597ba66ee63d428d1946`  
		Last Modified: Wed, 02 Feb 2022 03:53:04 GMT  
		Size: 80.2 MB (80187895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a486976bcda3aff4bea48c0f0f227d0a6a4e8952b280bf6065fbd652f0fb36`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3911f3f865240dfab0f331fec343ce0774717fd728a25bc70096d6d119062a8`  
		Last Modified: Wed, 02 Feb 2022 03:52:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3c249faca616b07726405956519b2b71bd69cf8689b5372d71d5fb0711d9bf5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117607720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5519cd809348cdad66374f4d07261b64b8ee0b059e50fcfde4e081e150f86a35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:49:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:44 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:45 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:46 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:49:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:52:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:52:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:52:29 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:52:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:52:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:52:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678769c76a50c67030c5a1e90a7774234cba02836cb78c79f737f8ebe034cd8a`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf16155dea7332141307a55607f7f670dd436220f999aaa8b44b7425ded11c5`  
		Last Modified: Wed, 02 Feb 2022 05:00:03 GMT  
		Size: 79.5 MB (79532623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7039bab2ea841283f082ef9e31ee71740f7c58eef5633518bd0d3295e61cb`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee4e7796f36d979a8a5e5e464c4d256a68eca1290e71629430ff5e38547fbd`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0a9f3761f792825d26131e6dd836b389c11d9744570cd4c28decef9b4fb74adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130989765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a16fc01c356f2cef9736753d4be409542af6a7eb671c891274a684d29bfbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:24:11 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:14 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:18 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:21 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:24:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:28:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:28:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:28:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:28:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:28:54 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:29:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3b1ab7b85e06c4533dfd28abcf42980715b35a04ebbfeae2b2d7e5c7b3ef6`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f8905242f2496fc2affaeaf880ea5a6a5b3d74f5462a15c116c91e9a376bc9`  
		Last Modified: Wed, 02 Feb 2022 06:42:01 GMT  
		Size: 84.8 MB (84785104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678426eb561b01ae11ac3b45e61f1d4b24b0da25b0a83da69fb58be44188ce20`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931d168ecad36931705df37e8bf67cca09f3ff3a704e7bf7f8fc11778d1842e5`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.32`

```console
$ docker pull mariadb@sha256:a25e7c87fe20c6d035fe81003937a8d732574ecf54466d0294da3423b64af80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.32` - linux; amd64

```console
$ docker pull mariadb@sha256:d6cc105c8baf52721ca0262b65dc1dff052297a78210d6ee3aef21abd3c2e5e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120109623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d01679c3b287ed73096d4ab595c64dcd49861ae3c3afa5d6ed3d46170093c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:59 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:48:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14f6657b5012974c330aa61fda56ad428cdb122487025b044c35b7b120720b5`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020be96129bacda3f951bb8abc57497de86a67e795a1597ba66ee63d428d1946`  
		Last Modified: Wed, 02 Feb 2022 03:53:04 GMT  
		Size: 80.2 MB (80187895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a486976bcda3aff4bea48c0f0f227d0a6a4e8952b280bf6065fbd652f0fb36`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3911f3f865240dfab0f331fec343ce0774717fd728a25bc70096d6d119062a8`  
		Last Modified: Wed, 02 Feb 2022 03:52:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3c249faca616b07726405956519b2b71bd69cf8689b5372d71d5fb0711d9bf5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117607720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5519cd809348cdad66374f4d07261b64b8ee0b059e50fcfde4e081e150f86a35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:49:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:44 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:45 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:46 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:49:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:52:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:52:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:52:29 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:52:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:52:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:52:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678769c76a50c67030c5a1e90a7774234cba02836cb78c79f737f8ebe034cd8a`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf16155dea7332141307a55607f7f670dd436220f999aaa8b44b7425ded11c5`  
		Last Modified: Wed, 02 Feb 2022 05:00:03 GMT  
		Size: 79.5 MB (79532623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7039bab2ea841283f082ef9e31ee71740f7c58eef5633518bd0d3295e61cb`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee4e7796f36d979a8a5e5e464c4d256a68eca1290e71629430ff5e38547fbd`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0a9f3761f792825d26131e6dd836b389c11d9744570cd4c28decef9b4fb74adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130989765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a16fc01c356f2cef9736753d4be409542af6a7eb671c891274a684d29bfbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:24:11 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:14 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:18 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:21 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:24:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:28:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:28:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:28:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:28:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:28:54 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:29:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3b1ab7b85e06c4533dfd28abcf42980715b35a04ebbfeae2b2d7e5c7b3ef6`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f8905242f2496fc2affaeaf880ea5a6a5b3d74f5462a15c116c91e9a376bc9`  
		Last Modified: Wed, 02 Feb 2022 06:42:01 GMT  
		Size: 84.8 MB (84785104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678426eb561b01ae11ac3b45e61f1d4b24b0da25b0a83da69fb58be44188ce20`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931d168ecad36931705df37e8bf67cca09f3ff3a704e7bf7f8fc11778d1842e5`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.32-focal`

```console
$ docker pull mariadb@sha256:a25e7c87fe20c6d035fe81003937a8d732574ecf54466d0294da3423b64af80c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.32-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:d6cc105c8baf52721ca0262b65dc1dff052297a78210d6ee3aef21abd3c2e5e3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120109623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8d01679c3b287ed73096d4ab595c64dcd49861ae3c3afa5d6ed3d46170093c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 03:47:26 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 03:47:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:47:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:58 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:59 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:48:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14f6657b5012974c330aa61fda56ad428cdb122487025b044c35b7b120720b5`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020be96129bacda3f951bb8abc57497de86a67e795a1597ba66ee63d428d1946`  
		Last Modified: Wed, 02 Feb 2022 03:53:04 GMT  
		Size: 80.2 MB (80187895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a486976bcda3aff4bea48c0f0f227d0a6a4e8952b280bf6065fbd652f0fb36`  
		Last Modified: Wed, 02 Feb 2022 03:52:51 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3911f3f865240dfab0f331fec343ce0774717fd728a25bc70096d6d119062a8`  
		Last Modified: Wed, 02 Feb 2022 03:52:52 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3c249faca616b07726405956519b2b71bd69cf8689b5372d71d5fb0711d9bf5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117607720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5519cd809348cdad66374f4d07261b64b8ee0b059e50fcfde4e081e150f86a35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:49:43 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:44 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 04:49:45 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:46 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 04:49:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:49:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:52:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:52:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:52:29 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:52:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:52:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:52:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:52:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678769c76a50c67030c5a1e90a7774234cba02836cb78c79f737f8ebe034cd8a`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf16155dea7332141307a55607f7f670dd436220f999aaa8b44b7425ded11c5`  
		Last Modified: Wed, 02 Feb 2022 05:00:03 GMT  
		Size: 79.5 MB (79532623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab7039bab2ea841283f082ef9e31ee71740f7c58eef5633518bd0d3295e61cb`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee4e7796f36d979a8a5e5e464c4d256a68eca1290e71629430ff5e38547fbd`  
		Last Modified: Wed, 02 Feb 2022 04:59:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.32-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0a9f3761f792825d26131e6dd836b389c11d9744570cd4c28decef9b4fb74adf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130989765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a16fc01c356f2cef9736753d4be409542af6a7eb671c891274a684d29bfbf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:24:11 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:14 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 02 Feb 2022 06:24:18 GMT
ARG MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:21 GMT
ENV MARIADB_VERSION=1:10.3.32+maria~focal
# Wed, 02 Feb 2022 06:24:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:24:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:28:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:28:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:28:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:28:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.32/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:28:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:28:54 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:29:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3b1ab7b85e06c4533dfd28abcf42980715b35a04ebbfeae2b2d7e5c7b3ef6`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f8905242f2496fc2affaeaf880ea5a6a5b3d74f5462a15c116c91e9a376bc9`  
		Last Modified: Wed, 02 Feb 2022 06:42:01 GMT  
		Size: 84.8 MB (84785104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678426eb561b01ae11ac3b45e61f1d4b24b0da25b0a83da69fb58be44188ce20`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931d168ecad36931705df37e8bf67cca09f3ff3a704e7bf7f8fc11778d1842e5`  
		Last Modified: Wed, 02 Feb 2022 06:41:44 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:899ac0fa8149f6c64de3a740f6c96200c3f73ccb363ca837d5e7ef153ef382ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:928f5cf48a3a0795901fa8cfb330959b77d954380bbb13d31e4c0864ce5d58c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124831213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc356de1c6ab01d8ec79a51fa4c9ab72d13391af44195981f5aa654843dffbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:52 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:53 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:47:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea625dc2b78c5315ab364b7c7a255d6598b19b772017f4d9a92240bc5af447a7`  
		Last Modified: Wed, 02 Feb 2022 03:52:24 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1c1f207df79f8b44a38cb881788663cfec7c8dcf7ccf071675b0277ec7dd71`  
		Last Modified: Wed, 02 Feb 2022 03:52:36 GMT  
		Size: 84.9 MB (84909487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34485df234aa1a38cc92ed31ae9b2e98e5a4b7f71db16d9ee93812657cdeb4e9`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0145e4699418aae9a29a84986813250fa7fdcf20304aca90a96f79a5a3375`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:228c2e670c5803be52115ac67b0cbfef83ece00beb270c3031a21116150c6eed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122255009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a1d8f8b9766b8425b217e1aa3bc73150b75a3a6b50fa52ec27a0143396e506`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:47:00 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:00 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:01 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:02 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:47:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:49:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:49:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:49:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:49:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:49:36 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:49:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe3750024fa312193ddb12a1119a7e5544c28a7c1987444acd4a9d7638c37b7`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42733c23b3a102eb929494c6dfc5bae8981e22698031f4c7fca404abd0fcf1e1`  
		Last Modified: Wed, 02 Feb 2022 04:59:28 GMT  
		Size: 84.2 MB (84179912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030494b95b91a4c6a55d6fe5579bebb1d2b2a79b6f9dae3da0624ab23c9c205f`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909734fe02d9075cbb36b64b76fcb1f7488255e633cbf9672f1d99e6bb48a536`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8ac062e3f5787cb5f91688cc9349d0d2aac79264fce394210445ba675e47fc5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135595732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d19710c1ca20a943bfe61843818ddc6523c80045c4b892ee4f06ffb298167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:20:45 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:49 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:20:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:21:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:21:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:23:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:23:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:23:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:23:46 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:23:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6570be9de70a14fcc9de9959b7a1c8d984bdfbddb345e8689dff921e8c5a33d3`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07a6cb8d20b19032086d6e8896d2f8204e31c015733e580eb0e89d0d31d8a7f`  
		Last Modified: Wed, 02 Feb 2022 06:41:25 GMT  
		Size: 89.4 MB (89391070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8b71ab431fd2487c83a51e490389713822d6d774fa474caba5b867e239576`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e345e87748fa5e011bd5cc0661e58b534f6ea21d33f14a37f5cac4563892a0`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:899ac0fa8149f6c64de3a740f6c96200c3f73ccb363ca837d5e7ef153ef382ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:928f5cf48a3a0795901fa8cfb330959b77d954380bbb13d31e4c0864ce5d58c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124831213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc356de1c6ab01d8ec79a51fa4c9ab72d13391af44195981f5aa654843dffbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:52 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:53 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:47:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea625dc2b78c5315ab364b7c7a255d6598b19b772017f4d9a92240bc5af447a7`  
		Last Modified: Wed, 02 Feb 2022 03:52:24 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1c1f207df79f8b44a38cb881788663cfec7c8dcf7ccf071675b0277ec7dd71`  
		Last Modified: Wed, 02 Feb 2022 03:52:36 GMT  
		Size: 84.9 MB (84909487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34485df234aa1a38cc92ed31ae9b2e98e5a4b7f71db16d9ee93812657cdeb4e9`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0145e4699418aae9a29a84986813250fa7fdcf20304aca90a96f79a5a3375`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:228c2e670c5803be52115ac67b0cbfef83ece00beb270c3031a21116150c6eed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122255009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a1d8f8b9766b8425b217e1aa3bc73150b75a3a6b50fa52ec27a0143396e506`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:47:00 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:00 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:01 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:02 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:47:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:49:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:49:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:49:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:49:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:49:36 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:49:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe3750024fa312193ddb12a1119a7e5544c28a7c1987444acd4a9d7638c37b7`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42733c23b3a102eb929494c6dfc5bae8981e22698031f4c7fca404abd0fcf1e1`  
		Last Modified: Wed, 02 Feb 2022 04:59:28 GMT  
		Size: 84.2 MB (84179912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030494b95b91a4c6a55d6fe5579bebb1d2b2a79b6f9dae3da0624ab23c9c205f`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909734fe02d9075cbb36b64b76fcb1f7488255e633cbf9672f1d99e6bb48a536`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8ac062e3f5787cb5f91688cc9349d0d2aac79264fce394210445ba675e47fc5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135595732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d19710c1ca20a943bfe61843818ddc6523c80045c4b892ee4f06ffb298167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:20:45 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:49 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:20:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:21:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:21:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:23:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:23:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:23:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:23:46 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:23:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6570be9de70a14fcc9de9959b7a1c8d984bdfbddb345e8689dff921e8c5a33d3`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07a6cb8d20b19032086d6e8896d2f8204e31c015733e580eb0e89d0d31d8a7f`  
		Last Modified: Wed, 02 Feb 2022 06:41:25 GMT  
		Size: 89.4 MB (89391070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8b71ab431fd2487c83a51e490389713822d6d774fa474caba5b867e239576`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e345e87748fa5e011bd5cc0661e58b534f6ea21d33f14a37f5cac4563892a0`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.22`

```console
$ docker pull mariadb@sha256:899ac0fa8149f6c64de3a740f6c96200c3f73ccb363ca837d5e7ef153ef382ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.22` - linux; amd64

```console
$ docker pull mariadb@sha256:928f5cf48a3a0795901fa8cfb330959b77d954380bbb13d31e4c0864ce5d58c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124831213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc356de1c6ab01d8ec79a51fa4c9ab72d13391af44195981f5aa654843dffbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:52 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:53 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:47:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea625dc2b78c5315ab364b7c7a255d6598b19b772017f4d9a92240bc5af447a7`  
		Last Modified: Wed, 02 Feb 2022 03:52:24 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1c1f207df79f8b44a38cb881788663cfec7c8dcf7ccf071675b0277ec7dd71`  
		Last Modified: Wed, 02 Feb 2022 03:52:36 GMT  
		Size: 84.9 MB (84909487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34485df234aa1a38cc92ed31ae9b2e98e5a4b7f71db16d9ee93812657cdeb4e9`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0145e4699418aae9a29a84986813250fa7fdcf20304aca90a96f79a5a3375`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:228c2e670c5803be52115ac67b0cbfef83ece00beb270c3031a21116150c6eed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122255009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a1d8f8b9766b8425b217e1aa3bc73150b75a3a6b50fa52ec27a0143396e506`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:47:00 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:00 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:01 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:02 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:47:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:49:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:49:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:49:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:49:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:49:36 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:49:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe3750024fa312193ddb12a1119a7e5544c28a7c1987444acd4a9d7638c37b7`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42733c23b3a102eb929494c6dfc5bae8981e22698031f4c7fca404abd0fcf1e1`  
		Last Modified: Wed, 02 Feb 2022 04:59:28 GMT  
		Size: 84.2 MB (84179912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030494b95b91a4c6a55d6fe5579bebb1d2b2a79b6f9dae3da0624ab23c9c205f`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909734fe02d9075cbb36b64b76fcb1f7488255e633cbf9672f1d99e6bb48a536`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8ac062e3f5787cb5f91688cc9349d0d2aac79264fce394210445ba675e47fc5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135595732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d19710c1ca20a943bfe61843818ddc6523c80045c4b892ee4f06ffb298167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:20:45 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:49 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:20:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:21:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:21:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:23:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:23:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:23:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:23:46 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:23:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6570be9de70a14fcc9de9959b7a1c8d984bdfbddb345e8689dff921e8c5a33d3`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07a6cb8d20b19032086d6e8896d2f8204e31c015733e580eb0e89d0d31d8a7f`  
		Last Modified: Wed, 02 Feb 2022 06:41:25 GMT  
		Size: 89.4 MB (89391070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8b71ab431fd2487c83a51e490389713822d6d774fa474caba5b867e239576`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e345e87748fa5e011bd5cc0661e58b534f6ea21d33f14a37f5cac4563892a0`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.22-focal`

```console
$ docker pull mariadb@sha256:899ac0fa8149f6c64de3a740f6c96200c3f73ccb363ca837d5e7ef153ef382ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.22-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:928f5cf48a3a0795901fa8cfb330959b77d954380bbb13d31e4c0864ce5d58c6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124831213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc356de1c6ab01d8ec79a51fa4c9ab72d13391af44195981f5aa654843dffbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:52 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:52 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 03:46:53 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 03:46:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:47:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:47:18 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:47:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:47:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 03:47:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:47:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:47:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea625dc2b78c5315ab364b7c7a255d6598b19b772017f4d9a92240bc5af447a7`  
		Last Modified: Wed, 02 Feb 2022 03:52:24 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1c1f207df79f8b44a38cb881788663cfec7c8dcf7ccf071675b0277ec7dd71`  
		Last Modified: Wed, 02 Feb 2022 03:52:36 GMT  
		Size: 84.9 MB (84909487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34485df234aa1a38cc92ed31ae9b2e98e5a4b7f71db16d9ee93812657cdeb4e9`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00d0145e4699418aae9a29a84986813250fa7fdcf20304aca90a96f79a5a3375`  
		Last Modified: Wed, 02 Feb 2022 03:52:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:228c2e670c5803be52115ac67b0cbfef83ece00beb270c3031a21116150c6eed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.3 MB (122255009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a1d8f8b9766b8425b217e1aa3bc73150b75a3a6b50fa52ec27a0143396e506`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:47:00 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:00 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 04:47:01 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:02 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 04:47:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:47:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:49:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:49:32 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:49:34 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:49:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 04:49:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:49:36 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:49:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe3750024fa312193ddb12a1119a7e5544c28a7c1987444acd4a9d7638c37b7`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42733c23b3a102eb929494c6dfc5bae8981e22698031f4c7fca404abd0fcf1e1`  
		Last Modified: Wed, 02 Feb 2022 04:59:28 GMT  
		Size: 84.2 MB (84179912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030494b95b91a4c6a55d6fe5579bebb1d2b2a79b6f9dae3da0624ab23c9c205f`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909734fe02d9075cbb36b64b76fcb1f7488255e633cbf9672f1d99e6bb48a536`  
		Last Modified: Wed, 02 Feb 2022 04:59:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.22-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8ac062e3f5787cb5f91688cc9349d0d2aac79264fce394210445ba675e47fc5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135595732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955d19710c1ca20a943bfe61843818ddc6523c80045c4b892ee4f06ffb298167`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:20:45 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:47 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 02 Feb 2022 06:20:49 GMT
ARG MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:20:53 GMT
ENV MARIADB_VERSION=1:10.4.22+maria~focal
# Wed, 02 Feb 2022 06:21:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:21:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:23:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:23:20 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:23:23 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:23:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.22/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Feb 2022 06:23:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:23:46 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:23:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6570be9de70a14fcc9de9959b7a1c8d984bdfbddb345e8689dff921e8c5a33d3`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07a6cb8d20b19032086d6e8896d2f8204e31c015733e580eb0e89d0d31d8a7f`  
		Last Modified: Wed, 02 Feb 2022 06:41:25 GMT  
		Size: 89.4 MB (89391070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba8b71ab431fd2487c83a51e490389713822d6d774fa474caba5b867e239576`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e345e87748fa5e011bd5cc0661e58b534f6ea21d33f14a37f5cac4563892a0`  
		Last Modified: Wed, 02 Feb 2022 06:41:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:5de92aeb70c440cf8622f391a08299281be870961c84a8450e037507ff0b283a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:149713eb2aff0d25b2f6f6734cbf01b595e90ad92f098d208c0e5aadef66702c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448c94b603062f51056988138d6e7b954c7f09a6e74d7a97f36bf3a6fe1b1797`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:49 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:49 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2464794388ce587eb9b8dec5424a03436465843da96cfd4949eb32a0d98b67`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8420024d863d640017dcb81f0b57876499c0e9770bc88b27e70c808b1696985`  
		Last Modified: Wed, 02 Feb 2022 03:52:07 GMT  
		Size: 87.1 MB (87091331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b551b100d050f1658f0862b1cd6f9e27f935f17109a5478fa91ec7ab2dc35e4`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a783bcf719679a40111f4cf6d641286959ba9dc5206d323ae1448d03d06f7f1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124285240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41d146edacee704594c810974dfb7ebcbe00ae67840cacf01643d662343ef8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:45:33 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:34 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:35 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:36 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:45:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:46:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:46:51 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:46:52 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:46:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e213c59a498843d4fa74ba2ea86ce086fda34db7a6388d9b65730276edfd656b`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a087dacb57663e0d83d6e6bbae5ea6c00dab2b8334e5665de158acabcfce2b18`  
		Last Modified: Wed, 02 Feb 2022 04:58:58 GMT  
		Size: 86.2 MB (86210264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352afa665ebd31712f9bfa4440f0b2dc79e8cce2972ef3d45cbac94ec11e3629`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f86309b5a56f8b47101d59b7c9793f3ba34ffdc2ce74e8c781c7f14e840dede2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170e658df65dde6947464925b6b410cf0502bea0f83d26e733735e0d2aec108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:17:47 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:53 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:54 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:18:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:20:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:20:25 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:20:27 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:20:32 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:20:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd46e649db8d71980e62fd014d8e9857cdb4f7bf0136bf0697e34bc369fc89`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7781f6d5825ff6d2e9b6090a9150ce7e1d919d6f944d283e9bfdb85d6607dda2`  
		Last Modified: Wed, 02 Feb 2022 06:40:48 GMT  
		Size: 91.5 MB (91535115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e421fd251f8ee6e6b7be7f7a3062d234ca234a48942b62a4617f357b5ca9a`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:c5ffdb927ba927c1fb0629651057b3849ad084ab9c4258d167ee39878715db09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126206694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86d6314346590bd13976ea4665a0d5d7af36e3a1fdb6661fbed5dbdb2f92d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:03:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:03:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:03:14 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:03:14 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:03:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe178bac3f54b971ab42cc9e840171f4a51c5feb194475a6530b8e98c7e3968`  
		Last Modified: Wed, 02 Feb 2022 02:04:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c55f7cc56a152d5d861a4f273b7b2a578ebf6a27abe1d5426e33a88295554e`  
		Last Modified: Wed, 02 Feb 2022 02:05:06 GMT  
		Size: 88.3 MB (88266519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107255f77109e4849ba8fffaaf111fead9a9aa37214d925ab0267362120db90f`  
		Last Modified: Wed, 02 Feb 2022 02:04:53 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:5de92aeb70c440cf8622f391a08299281be870961c84a8450e037507ff0b283a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:149713eb2aff0d25b2f6f6734cbf01b595e90ad92f098d208c0e5aadef66702c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448c94b603062f51056988138d6e7b954c7f09a6e74d7a97f36bf3a6fe1b1797`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:49 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:49 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2464794388ce587eb9b8dec5424a03436465843da96cfd4949eb32a0d98b67`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8420024d863d640017dcb81f0b57876499c0e9770bc88b27e70c808b1696985`  
		Last Modified: Wed, 02 Feb 2022 03:52:07 GMT  
		Size: 87.1 MB (87091331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b551b100d050f1658f0862b1cd6f9e27f935f17109a5478fa91ec7ab2dc35e4`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a783bcf719679a40111f4cf6d641286959ba9dc5206d323ae1448d03d06f7f1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124285240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41d146edacee704594c810974dfb7ebcbe00ae67840cacf01643d662343ef8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:45:33 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:34 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:35 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:36 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:45:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:46:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:46:51 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:46:52 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:46:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e213c59a498843d4fa74ba2ea86ce086fda34db7a6388d9b65730276edfd656b`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a087dacb57663e0d83d6e6bbae5ea6c00dab2b8334e5665de158acabcfce2b18`  
		Last Modified: Wed, 02 Feb 2022 04:58:58 GMT  
		Size: 86.2 MB (86210264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352afa665ebd31712f9bfa4440f0b2dc79e8cce2972ef3d45cbac94ec11e3629`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f86309b5a56f8b47101d59b7c9793f3ba34ffdc2ce74e8c781c7f14e840dede2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170e658df65dde6947464925b6b410cf0502bea0f83d26e733735e0d2aec108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:17:47 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:53 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:54 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:18:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:20:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:20:25 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:20:27 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:20:32 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:20:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd46e649db8d71980e62fd014d8e9857cdb4f7bf0136bf0697e34bc369fc89`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7781f6d5825ff6d2e9b6090a9150ce7e1d919d6f944d283e9bfdb85d6607dda2`  
		Last Modified: Wed, 02 Feb 2022 06:40:48 GMT  
		Size: 91.5 MB (91535115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e421fd251f8ee6e6b7be7f7a3062d234ca234a48942b62a4617f357b5ca9a`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:c5ffdb927ba927c1fb0629651057b3849ad084ab9c4258d167ee39878715db09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126206694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86d6314346590bd13976ea4665a0d5d7af36e3a1fdb6661fbed5dbdb2f92d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:03:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:03:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:03:14 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:03:14 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:03:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe178bac3f54b971ab42cc9e840171f4a51c5feb194475a6530b8e98c7e3968`  
		Last Modified: Wed, 02 Feb 2022 02:04:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c55f7cc56a152d5d861a4f273b7b2a578ebf6a27abe1d5426e33a88295554e`  
		Last Modified: Wed, 02 Feb 2022 02:05:06 GMT  
		Size: 88.3 MB (88266519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107255f77109e4849ba8fffaaf111fead9a9aa37214d925ab0267362120db90f`  
		Last Modified: Wed, 02 Feb 2022 02:04:53 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.13`

```console
$ docker pull mariadb@sha256:5de92aeb70c440cf8622f391a08299281be870961c84a8450e037507ff0b283a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.13` - linux; amd64

```console
$ docker pull mariadb@sha256:149713eb2aff0d25b2f6f6734cbf01b595e90ad92f098d208c0e5aadef66702c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448c94b603062f51056988138d6e7b954c7f09a6e74d7a97f36bf3a6fe1b1797`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:49 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:49 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2464794388ce587eb9b8dec5424a03436465843da96cfd4949eb32a0d98b67`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8420024d863d640017dcb81f0b57876499c0e9770bc88b27e70c808b1696985`  
		Last Modified: Wed, 02 Feb 2022 03:52:07 GMT  
		Size: 87.1 MB (87091331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b551b100d050f1658f0862b1cd6f9e27f935f17109a5478fa91ec7ab2dc35e4`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a783bcf719679a40111f4cf6d641286959ba9dc5206d323ae1448d03d06f7f1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124285240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41d146edacee704594c810974dfb7ebcbe00ae67840cacf01643d662343ef8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:45:33 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:34 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:35 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:36 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:45:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:46:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:46:51 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:46:52 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:46:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e213c59a498843d4fa74ba2ea86ce086fda34db7a6388d9b65730276edfd656b`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a087dacb57663e0d83d6e6bbae5ea6c00dab2b8334e5665de158acabcfce2b18`  
		Last Modified: Wed, 02 Feb 2022 04:58:58 GMT  
		Size: 86.2 MB (86210264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352afa665ebd31712f9bfa4440f0b2dc79e8cce2972ef3d45cbac94ec11e3629`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f86309b5a56f8b47101d59b7c9793f3ba34ffdc2ce74e8c781c7f14e840dede2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170e658df65dde6947464925b6b410cf0502bea0f83d26e733735e0d2aec108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:17:47 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:53 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:54 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:18:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:20:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:20:25 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:20:27 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:20:32 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:20:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd46e649db8d71980e62fd014d8e9857cdb4f7bf0136bf0697e34bc369fc89`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7781f6d5825ff6d2e9b6090a9150ce7e1d919d6f944d283e9bfdb85d6607dda2`  
		Last Modified: Wed, 02 Feb 2022 06:40:48 GMT  
		Size: 91.5 MB (91535115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e421fd251f8ee6e6b7be7f7a3062d234ca234a48942b62a4617f357b5ca9a`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13` - linux; s390x

```console
$ docker pull mariadb@sha256:c5ffdb927ba927c1fb0629651057b3849ad084ab9c4258d167ee39878715db09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126206694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86d6314346590bd13976ea4665a0d5d7af36e3a1fdb6661fbed5dbdb2f92d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:03:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:03:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:03:14 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:03:14 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:03:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe178bac3f54b971ab42cc9e840171f4a51c5feb194475a6530b8e98c7e3968`  
		Last Modified: Wed, 02 Feb 2022 02:04:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c55f7cc56a152d5d861a4f273b7b2a578ebf6a27abe1d5426e33a88295554e`  
		Last Modified: Wed, 02 Feb 2022 02:05:06 GMT  
		Size: 88.3 MB (88266519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107255f77109e4849ba8fffaaf111fead9a9aa37214d925ab0267362120db90f`  
		Last Modified: Wed, 02 Feb 2022 02:04:53 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.13-focal`

```console
$ docker pull mariadb@sha256:5de92aeb70c440cf8622f391a08299281be870961c84a8450e037507ff0b283a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.13-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:149713eb2aff0d25b2f6f6734cbf01b595e90ad92f098d208c0e5aadef66702c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127012933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448c94b603062f51056988138d6e7b954c7f09a6e74d7a97f36bf3a6fe1b1797`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 03:46:24 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 03:46:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:46:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:49 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:49 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2464794388ce587eb9b8dec5424a03436465843da96cfd4949eb32a0d98b67`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8420024d863d640017dcb81f0b57876499c0e9770bc88b27e70c808b1696985`  
		Last Modified: Wed, 02 Feb 2022 03:52:07 GMT  
		Size: 87.1 MB (87091331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b551b100d050f1658f0862b1cd6f9e27f935f17109a5478fa91ec7ab2dc35e4`  
		Last Modified: Wed, 02 Feb 2022 03:51:55 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:a783bcf719679a40111f4cf6d641286959ba9dc5206d323ae1448d03d06f7f1e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124285240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41d146edacee704594c810974dfb7ebcbe00ae67840cacf01643d662343ef8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:45:33 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:34 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 04:45:35 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:36 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 04:45:37 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:45:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:46:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:46:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:46:51 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:46:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:46:52 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:46:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e213c59a498843d4fa74ba2ea86ce086fda34db7a6388d9b65730276edfd656b`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a087dacb57663e0d83d6e6bbae5ea6c00dab2b8334e5665de158acabcfce2b18`  
		Last Modified: Wed, 02 Feb 2022 04:58:58 GMT  
		Size: 86.2 MB (86210264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352afa665ebd31712f9bfa4440f0b2dc79e8cce2972ef3d45cbac94ec11e3629`  
		Last Modified: Wed, 02 Feb 2022 04:58:44 GMT  
		Size: 5.6 KB (5627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:f86309b5a56f8b47101d59b7c9793f3ba34ffdc2ce74e8c781c7f14e840dede2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137739655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a170e658df65dde6947464925b6b410cf0502bea0f83d26e733735e0d2aec108`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:17:47 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:51 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 06:17:53 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:54 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 06:17:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:18:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:20:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:20:25 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:20:27 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:20:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:20:32 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:20:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebbd46e649db8d71980e62fd014d8e9857cdb4f7bf0136bf0697e34bc369fc89`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7781f6d5825ff6d2e9b6090a9150ce7e1d919d6f944d283e9bfdb85d6607dda2`  
		Last Modified: Wed, 02 Feb 2022 06:40:48 GMT  
		Size: 91.5 MB (91535115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685e421fd251f8ee6e6b7be7f7a3062d234ca234a48942b62a4617f357b5ca9a`  
		Last Modified: Wed, 02 Feb 2022 06:40:30 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.13-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:c5ffdb927ba927c1fb0629651057b3849ad084ab9c4258d167ee39878715db09
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126206694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86d6314346590bd13976ea4665a0d5d7af36e3a1fdb6661fbed5dbdb2f92d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:40 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 02 Feb 2022 02:02:41 GMT
ARG MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ENV MARIADB_VERSION=1:10.5.13+maria~focal
# Wed, 02 Feb 2022 02:02:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:03:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.13/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:03:14 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:03:14 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:03:14 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:03:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe178bac3f54b971ab42cc9e840171f4a51c5feb194475a6530b8e98c7e3968`  
		Last Modified: Wed, 02 Feb 2022 02:04:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0c55f7cc56a152d5d861a4f273b7b2a578ebf6a27abe1d5426e33a88295554e`  
		Last Modified: Wed, 02 Feb 2022 02:05:06 GMT  
		Size: 88.3 MB (88266519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107255f77109e4849ba8fffaaf111fead9a9aa37214d925ab0267362120db90f`  
		Last Modified: Wed, 02 Feb 2022 02:04:53 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.5`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.5` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.5-focal`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:5a8009369ee57c85b6f4a08406147bd9c505cde6b8250d16a27d2a5febfdead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:1a09a9175c80d49ccbcbcc821472449bc4f83169d8393296736eaac9180d5484
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127710135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a24127bba8bf4d1faea346defc7c7d3bf219cf0469b45c2812c007d6b45b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:03 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:45:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:45:45 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:45:45 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:45:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588f335cb3e733630411f0635cc5b74193b0daa2e85771583032dc26efc021d7`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a910b505cb14de105d661ddd0d6314c847ec9de51faac430d59a9113d64f67`  
		Last Modified: Wed, 02 Feb 2022 03:50:55 GMT  
		Size: 87.8 MB (87788534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f133fff2932b98b7202653a2f47a32431215957b9e197d81f9baae6b486df81`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f867f89923e74c07508158c51df012f3fbed59760c859581f4520f2106b8b609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124867889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400651f5c24b79c03a4bf596152cee7fc2da1f07360d8a0d13f9677b14572b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:41:18 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:19 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:20 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:41:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:41:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:41:55 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:41:56 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:41:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96926b7e95477064de9aebf6caccdb77a7e3c7a62208f167506dd4372de0689`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d7a882f0186a2a4a45e4e377c24f675c90a2c1b1ecfd1b1fa22d974735b23`  
		Last Modified: Wed, 02 Feb 2022 04:57:45 GMT  
		Size: 86.8 MB (86792917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f440489c50869ecaa8f72b4a885dda75bf569f60b037f3d352ef458f80a62`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e78f45a4fd3b6d3d5bf092d77d619cb5e87da4610cb05973595539351ab7b889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138431241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add620545f586c51173aa45cbb8f0f7722302aa7f01c0e6740ebd193cc33d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:10:08 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:12 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:17 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:13:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:13:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:13:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:13:39 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:13:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3da0822a098c42c0d8f9ca68906bb94fd6d49a76dd4a6b21b980ba7ba33d87`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb178f81363c8e872ae4193eac1a1f08bbaf95fea23ae74a8f7155c24ecfe030`  
		Last Modified: Wed, 02 Feb 2022 06:39:20 GMT  
		Size: 92.2 MB (92226700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752395e0c34c6e94de81e5c5783e7f0a8e972fb82fa795676a992f2b8da62e53`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:3e26eaffa45eadff8468cb2a90dfe8afa2308450173b45090dcbd3bdac3d9ea3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126699248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddd8d0b695707f8c97cc97b05fd58bf1376a2675e2a326cb72f4b36122327b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:01:20 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:20 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:21 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:01:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:01:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:01:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:01:47 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:01:47 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:01:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d96a8c7b962bba29e40b7d1171432bf633e868b4778dd0ebbd4912da4a33b9`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ce131ccec8e6684446b7a0e851fb41c41f8474f5e11ada5614248a02d9baf`  
		Last Modified: Wed, 02 Feb 2022 02:04:11 GMT  
		Size: 88.8 MB (88759070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6c00b0d9ee0064ea8f6afb51bb29ee1cf5a41164c71bae324ef8f5b3b07fcc`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:5a8009369ee57c85b6f4a08406147bd9c505cde6b8250d16a27d2a5febfdead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1a09a9175c80d49ccbcbcc821472449bc4f83169d8393296736eaac9180d5484
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127710135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a24127bba8bf4d1faea346defc7c7d3bf219cf0469b45c2812c007d6b45b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:03 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:45:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:45:45 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:45:45 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:45:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588f335cb3e733630411f0635cc5b74193b0daa2e85771583032dc26efc021d7`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a910b505cb14de105d661ddd0d6314c847ec9de51faac430d59a9113d64f67`  
		Last Modified: Wed, 02 Feb 2022 03:50:55 GMT  
		Size: 87.8 MB (87788534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f133fff2932b98b7202653a2f47a32431215957b9e197d81f9baae6b486df81`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f867f89923e74c07508158c51df012f3fbed59760c859581f4520f2106b8b609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124867889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400651f5c24b79c03a4bf596152cee7fc2da1f07360d8a0d13f9677b14572b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:41:18 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:19 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:20 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:41:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:41:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:41:55 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:41:56 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:41:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96926b7e95477064de9aebf6caccdb77a7e3c7a62208f167506dd4372de0689`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d7a882f0186a2a4a45e4e377c24f675c90a2c1b1ecfd1b1fa22d974735b23`  
		Last Modified: Wed, 02 Feb 2022 04:57:45 GMT  
		Size: 86.8 MB (86792917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f440489c50869ecaa8f72b4a885dda75bf569f60b037f3d352ef458f80a62`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e78f45a4fd3b6d3d5bf092d77d619cb5e87da4610cb05973595539351ab7b889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138431241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add620545f586c51173aa45cbb8f0f7722302aa7f01c0e6740ebd193cc33d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:10:08 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:12 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:17 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:13:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:13:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:13:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:13:39 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:13:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3da0822a098c42c0d8f9ca68906bb94fd6d49a76dd4a6b21b980ba7ba33d87`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb178f81363c8e872ae4193eac1a1f08bbaf95fea23ae74a8f7155c24ecfe030`  
		Last Modified: Wed, 02 Feb 2022 06:39:20 GMT  
		Size: 92.2 MB (92226700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752395e0c34c6e94de81e5c5783e7f0a8e972fb82fa795676a992f2b8da62e53`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:3e26eaffa45eadff8468cb2a90dfe8afa2308450173b45090dcbd3bdac3d9ea3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126699248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddd8d0b695707f8c97cc97b05fd58bf1376a2675e2a326cb72f4b36122327b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:01:20 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:20 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:21 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:01:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:01:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:01:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:01:47 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:01:47 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:01:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d96a8c7b962bba29e40b7d1171432bf633e868b4778dd0ebbd4912da4a33b9`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ce131ccec8e6684446b7a0e851fb41c41f8474f5e11ada5614248a02d9baf`  
		Last Modified: Wed, 02 Feb 2022 02:04:11 GMT  
		Size: 88.8 MB (88759070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6c00b0d9ee0064ea8f6afb51bb29ee1cf5a41164c71bae324ef8f5b3b07fcc`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.1`

```console
$ docker pull mariadb@sha256:5a8009369ee57c85b6f4a08406147bd9c505cde6b8250d16a27d2a5febfdead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.1` - linux; amd64

```console
$ docker pull mariadb@sha256:1a09a9175c80d49ccbcbcc821472449bc4f83169d8393296736eaac9180d5484
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127710135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a24127bba8bf4d1faea346defc7c7d3bf219cf0469b45c2812c007d6b45b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:03 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:45:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:45:45 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:45:45 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:45:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588f335cb3e733630411f0635cc5b74193b0daa2e85771583032dc26efc021d7`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a910b505cb14de105d661ddd0d6314c847ec9de51faac430d59a9113d64f67`  
		Last Modified: Wed, 02 Feb 2022 03:50:55 GMT  
		Size: 87.8 MB (87788534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f133fff2932b98b7202653a2f47a32431215957b9e197d81f9baae6b486df81`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f867f89923e74c07508158c51df012f3fbed59760c859581f4520f2106b8b609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124867889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400651f5c24b79c03a4bf596152cee7fc2da1f07360d8a0d13f9677b14572b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:41:18 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:19 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:20 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:41:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:41:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:41:55 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:41:56 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:41:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96926b7e95477064de9aebf6caccdb77a7e3c7a62208f167506dd4372de0689`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d7a882f0186a2a4a45e4e377c24f675c90a2c1b1ecfd1b1fa22d974735b23`  
		Last Modified: Wed, 02 Feb 2022 04:57:45 GMT  
		Size: 86.8 MB (86792917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f440489c50869ecaa8f72b4a885dda75bf569f60b037f3d352ef458f80a62`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e78f45a4fd3b6d3d5bf092d77d619cb5e87da4610cb05973595539351ab7b889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138431241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add620545f586c51173aa45cbb8f0f7722302aa7f01c0e6740ebd193cc33d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:10:08 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:12 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:17 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:13:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:13:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:13:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:13:39 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:13:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3da0822a098c42c0d8f9ca68906bb94fd6d49a76dd4a6b21b980ba7ba33d87`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb178f81363c8e872ae4193eac1a1f08bbaf95fea23ae74a8f7155c24ecfe030`  
		Last Modified: Wed, 02 Feb 2022 06:39:20 GMT  
		Size: 92.2 MB (92226700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752395e0c34c6e94de81e5c5783e7f0a8e972fb82fa795676a992f2b8da62e53`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1` - linux; s390x

```console
$ docker pull mariadb@sha256:3e26eaffa45eadff8468cb2a90dfe8afa2308450173b45090dcbd3bdac3d9ea3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126699248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddd8d0b695707f8c97cc97b05fd58bf1376a2675e2a326cb72f4b36122327b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:01:20 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:20 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:21 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:01:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:01:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:01:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:01:47 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:01:47 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:01:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d96a8c7b962bba29e40b7d1171432bf633e868b4778dd0ebbd4912da4a33b9`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ce131ccec8e6684446b7a0e851fb41c41f8474f5e11ada5614248a02d9baf`  
		Last Modified: Wed, 02 Feb 2022 02:04:11 GMT  
		Size: 88.8 MB (88759070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6c00b0d9ee0064ea8f6afb51bb29ee1cf5a41164c71bae324ef8f5b3b07fcc`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.1-focal`

```console
$ docker pull mariadb@sha256:5a8009369ee57c85b6f4a08406147bd9c505cde6b8250d16a27d2a5febfdead7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.1-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:1a09a9175c80d49ccbcbcc821472449bc4f83169d8393296736eaac9180d5484
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127710135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a24127bba8bf4d1faea346defc7c7d3bf219cf0469b45c2812c007d6b45b54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:03 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 03:45:04 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 03:45:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:45:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:45:45 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:45:45 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:45:45 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:45:45 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588f335cb3e733630411f0635cc5b74193b0daa2e85771583032dc26efc021d7`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a910b505cb14de105d661ddd0d6314c847ec9de51faac430d59a9113d64f67`  
		Last Modified: Wed, 02 Feb 2022 03:50:55 GMT  
		Size: 87.8 MB (87788534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f133fff2932b98b7202653a2f47a32431215957b9e197d81f9baae6b486df81`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f867f89923e74c07508158c51df012f3fbed59760c859581f4520f2106b8b609
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124867889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400651f5c24b79c03a4bf596152cee7fc2da1f07360d8a0d13f9677b14572b97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:41:18 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:19 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 04:41:20 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 04:41:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:41:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:41:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:41:55 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:41:56 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:41:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e96926b7e95477064de9aebf6caccdb77a7e3c7a62208f167506dd4372de0689`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f4d7a882f0186a2a4a45e4e377c24f675c90a2c1b1ecfd1b1fa22d974735b23`  
		Last Modified: Wed, 02 Feb 2022 04:57:45 GMT  
		Size: 86.8 MB (86792917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50f440489c50869ecaa8f72b4a885dda75bf569f60b037f3d352ef458f80a62`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 5.6 KB (5625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e78f45a4fd3b6d3d5bf092d77d619cb5e87da4610cb05973595539351ab7b889
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138431241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add620545f586c51173aa45cbb8f0f7722302aa7f01c0e6740ebd193cc33d4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:10:08 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:12 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 06:10:15 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:17 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 06:10:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:10:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:13:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:13:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:13:33 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:13:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:13:39 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:13:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce3da0822a098c42c0d8f9ca68906bb94fd6d49a76dd4a6b21b980ba7ba33d87`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb178f81363c8e872ae4193eac1a1f08bbaf95fea23ae74a8f7155c24ecfe030`  
		Last Modified: Wed, 02 Feb 2022 06:39:20 GMT  
		Size: 92.2 MB (92226700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752395e0c34c6e94de81e5c5783e7f0a8e972fb82fa795676a992f2b8da62e53`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.1-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:3e26eaffa45eadff8468cb2a90dfe8afa2308450173b45090dcbd3bdac3d9ea3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126699248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddd8d0b695707f8c97cc97b05fd58bf1376a2675e2a326cb72f4b36122327b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:01:20 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:20 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 02 Feb 2022 02:01:21 GMT
ARG MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ENV MARIADB_VERSION=1:10.7.1+maria~focal
# Wed, 02 Feb 2022 02:01:21 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:01:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:01:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.1/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:01:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:01:47 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:01:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:01:47 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:01:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d96a8c7b962bba29e40b7d1171432bf633e868b4778dd0ebbd4912da4a33b9`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889ce131ccec8e6684446b7a0e851fb41c41f8474f5e11ada5614248a02d9baf`  
		Last Modified: Wed, 02 Feb 2022 02:04:11 GMT  
		Size: 88.8 MB (88759070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6c00b0d9ee0064ea8f6afb51bb29ee1cf5a41164c71bae324ef8f5b3b07fcc`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 5.6 KB (5629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:ca31f38b6e325ece985d857db7eba1fe59928b4fd83ff8a55cb912c9684b9e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:6aede9b2573833b2271f413ae12268796499fdaa5073681f9902f5ab2c60b84a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127202819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a5a43e143af98426bbfe31e66dbc2e2283565405d7b9f22c23549a80da40a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 02:14:45 GMT
ADD file:3ccf747d646089ed7fbb43c40c45dd43e86f0674115f856efada93c7e4a63624 in / 
# Wed, 02 Feb 2022 02:14:46 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:44:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 03:44:10 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:10 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 03:44:22 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 03:44:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 03:44:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:31 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 03:45:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 03:45:54 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 03:45:55 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 03:45:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 03:46:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 03:46:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 03:46:19 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 03:46:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 03:46:20 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 03:46:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:08c01a0ec47e82ebe2bec112f373d160983a6d1e9e66627f66a3322bc403221b`  
		Last Modified: Wed, 02 Feb 2022 02:16:20 GMT  
		Size: 28.6 MB (28564099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2bcb14c13a16d41b62e37e326b8a6f8c624abc25a69c124f4adc0efe20cd699`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c56760f8795a481e78e45a17a5be161f3e783bc3706500c78438d786664145`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 5.5 MB (5488714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95000a218fc379d12546e703c2c5053c762fa18cd2b4f9bdbd18262de3ab830`  
		Last Modified: Wed, 02 Feb 2022 03:50:45 GMT  
		Size: 3.6 MB (3585297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a765d76e68d91020e9f23c79d526959e31827ebb8beaa3c2dbdab96e0b3fcb49`  
		Last Modified: Wed, 02 Feb 2022 03:50:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6945738f085b358ec9b3e38bcdd7791eec1d2a390d686f16c498dc512b39cd8`  
		Last Modified: Wed, 02 Feb 2022 03:50:43 GMT  
		Size: 2.3 MB (2273154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62787b7c58c5b4583c32aae1c05a7754bbe015bcc7befeadb18724d1d30b880f`  
		Last Modified: Wed, 02 Feb 2022 03:50:42 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2987a30cfe4f2e679b38e5def94025937ee7c887e552e4028a46d6a61ae83c9`  
		Last Modified: Wed, 02 Feb 2022 03:51:11 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc65983d8b539ad56194a9bf30f7676e922ec29c59e45e84195a607a21049a0`  
		Last Modified: Wed, 02 Feb 2022 03:51:23 GMT  
		Size: 87.3 MB (87281214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db216f91595e72154d6c9213bad986720e5513782cde33c5c00821f609a902bc`  
		Last Modified: Wed, 02 Feb 2022 03:51:10 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1408054d02962e9c2140014dda1b0a44a870d9c20848f355b0937118e5c491eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124377633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7185139442f4eaa5415c6528afa2ebeeb2b2235b646ee763e7d66422a9c91bec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:27 GMT
ADD file:3acc741be29b0b58e44d7302ab5ce65bf65ea1b35922be58a2cee9cb708d006a in / 
# Wed, 02 Feb 2022 03:19:27 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:39:39 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 04:40:05 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 04:40:31 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 04:40:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 04:40:40 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:40:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 04:41:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 04:42:06 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:06 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 04:42:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 04:42:09 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 04:42:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 04:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 04:45:17 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 04:45:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 04:45:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 04:45:19 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 04:45:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bbf2fb66fa6e06dd46eb26f518f93171ee7c48be68aafb213aa7c2c12f4018ca`  
		Last Modified: Wed, 02 Feb 2022 03:21:24 GMT  
		Size: 27.2 MB (27169640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f406123c735827ddca5013c4dbaec303a0bbde59e31c312fe60c4a3c4eeef62c`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414755d47c502f9964427595a679ddd698eff61c209060f6955a264d4ee98981`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 5.3 MB (5320804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a72e3f9adedebed74ad9cc9b32baa8e4bdd52883d9faff9419213a4b6a5e82a`  
		Last Modified: Wed, 02 Feb 2022 04:57:34 GMT  
		Size: 3.4 MB (3370594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90b1b1182692e22e0260cdfb1a4f2257ae7d2dcccc416216bc53eec22a1d5a48`  
		Last Modified: Wed, 02 Feb 2022 04:57:33 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620b0eb464ebca108fe2b78540a25bc563ea53b8c917bb9174e44344bff9775`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.2 MB (2203676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c610e5ec0f6e73427891b2add972f5779ba9e99583f0a6c4c657d8532eda6c`  
		Last Modified: Wed, 02 Feb 2022 04:57:31 GMT  
		Size: 2.5 KB (2467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9687dff79d4733929adcf20ce8c3de767bffa2a3a813d3f40d4ba204e51828f`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772e6d2e6f99a9a1ea5519be3dccd34c912e4141ebf0d95aede302e182cc33fb`  
		Last Modified: Wed, 02 Feb 2022 04:58:15 GMT  
		Size: 86.3 MB (86302662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ab12fa963e6afc982587d3be1ab5c77059184d8f81827d522ca6d8cbd46e`  
		Last Modified: Wed, 02 Feb 2022 04:58:02 GMT  
		Size: 5.6 KB (5623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:26365cfc20ce97ce9359b32d5774b0cd623e503cd1dc0a5ddbc065b92fa9e70a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137783748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737496717e740b26172016c9c63dbeb5ae8ee2a178eb689b4f8a4c9176d37b99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 03:50:21 GMT
ADD file:e27da75ca1655de0ac82ef9879f868863388ea992e031aeace61195495bc21bc in / 
# Wed, 02 Feb 2022 03:50:25 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 06:07:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 06:08:34 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:08:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 06:09:21 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 06:09:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 06:09:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 06:09:55 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 06:10:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 06:14:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:05 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 06:14:07 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:08 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 06:14:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 06:14:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 06:16:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 06:17:15 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 06:17:18 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 06:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 06:17:28 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 06:17:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e4ad98202983f0b602991305f807e9b8460bb3fdb617889c276ccbd4b92c69b4`  
		Last Modified: Wed, 02 Feb 2022 03:53:11 GMT  
		Size: 33.3 MB (33284717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eaa6ddf04a6d9ff5571f3581411a5c5599f359efc06218aa8d7c98b19a55901`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ae472154410dbc918378510614e56d08dd8a080b560ff9c32dda5245513274`  
		Last Modified: Wed, 02 Feb 2022 06:39:05 GMT  
		Size: 6.7 MB (6667616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e257a32b5e76c486ebf42a085bb256e66387304f2229a5ea755f81fd4ff043`  
		Last Modified: Wed, 02 Feb 2022 06:39:04 GMT  
		Size: 3.7 MB (3672907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ba19c6c72ddf1ef6540af7465f5ebce217aa9ae4262681c6f8dab092d1c4f2`  
		Last Modified: Wed, 02 Feb 2022 06:39:03 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a1d4520ce5fb6b4de48cceee5ec288b0d16ed237ac7a5803a60e47a5b30485`  
		Last Modified: Wed, 02 Feb 2022 06:39:01 GMT  
		Size: 2.6 MB (2568961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e484cec9b927076854980caeef8520dfe1aa90b9caf1af6321de484c1afd41`  
		Last Modified: Wed, 02 Feb 2022 06:39:00 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4683b2a4076da23a58c3d55ec3193591331e38c1da0cd871cb108e31c76984ec`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cedf38ea121b3c6203ec8682b97afed76dc9815da29af531bf48951ecbed21`  
		Last Modified: Wed, 02 Feb 2022 06:39:57 GMT  
		Size: 91.6 MB (91579209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca079698384d698aa1ec8a2a18c8458fbed546951d84d331a3d168d4dd4acba`  
		Last Modified: Wed, 02 Feb 2022 06:39:39 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:ca77f8441f0bdf29a8e8a8c6081a787cfc746498cba023689c46f38151b4923f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126211717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936f2cc6fbfa42f5bd4bbb952f5fe0803757a63f90b24da57e5e21b1c6fd5b7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:16 GMT
ADD file:f35a5307585c918b783420eea01f5947181ac58f8eeb855a8f73f38f1477700f in / 
# Wed, 02 Feb 2022 01:42:17 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:00:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Feb 2022 02:00:24 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	if ! gpg --version | grep -q '^gpg (GnuPG) 1\.'; then 		apt-get install -y --no-install-recommends dirmngr; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:24 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Feb 2022 02:00:35 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Feb 2022 02:00:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Feb 2022 02:00:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:00:41 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Feb 2022 02:01:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Feb 2022 02:02:03 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:03 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 02 Feb 2022 02:02:04 GMT
ARG MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ENV MARIADB_VERSION=1:10.6.5+maria~focal
# Wed, 02 Feb 2022 02:02:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
# Wed, 02 Feb 2022 02:02:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Feb 2022 02:02:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.5/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Feb 2022 02:02:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Feb 2022 02:02:31 GMT
COPY file:3d431099953246ba9f86475bec3d0dd982f00a61aadadc1bc6d8c1083ec64129 in /usr/local/bin/ 
# Wed, 02 Feb 2022 02:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Feb 2022 02:02:31 GMT
EXPOSE 3306
# Wed, 02 Feb 2022 02:02:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:723da7fec7371c2b30effc8da0790968bef9dd221f5e34b5c8f7d2eff90fbd5e`  
		Last Modified: Wed, 02 Feb 2022 01:44:01 GMT  
		Size: 27.1 MB (27118737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2efba31bb782a719396206842603ef1b2a8a771ab834a5eceff66d64f0a5918f`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54055a30f227d69198e91da1931c1ee5d7effcbc8f0ad640a2dbb2b5ba57f7`  
		Last Modified: Wed, 02 Feb 2022 02:04:00 GMT  
		Size: 5.4 MB (5380988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1175de9b14ef6cc481f92baa7df6265e3348404e267fd8607ff1a48cd81f9791`  
		Last Modified: Wed, 02 Feb 2022 02:04:02 GMT  
		Size: 3.2 MB (3244533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8905d7a3550001eeac1668b17f2089d9dfe90316c19d635333e81d4a3f70dbe0`  
		Last Modified: Wed, 02 Feb 2022 02:03:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27deea83714266cb24dd1fe4acbbfa21514b978790242c8b83cc5c85eae85472`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.2 MB (2185574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b06a0b2eb1cb2dea04f21477e6c1ebead902b9d5db32337e092dcfb65bce74`  
		Last Modified: Wed, 02 Feb 2022 02:03:58 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d97b8af1d5e1d2514a5ef01a9bd07bd8ef9e2c5c05b040454f71c534fa14ad9`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588a11956dbce20366aa7f3a51f4f133931bb91269836939c19404ebc36c4b6a`  
		Last Modified: Wed, 02 Feb 2022 02:04:35 GMT  
		Size: 88.3 MB (88271543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841746409f24a4a6a944d9e28a3d0040f80f535c866261e0d30de21f9cecbae3`  
		Last Modified: Wed, 02 Feb 2022 02:04:22 GMT  
		Size: 5.6 KB (5626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
