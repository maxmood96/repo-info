<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-focal`](#mariadb10-focal)
-	[`mariadb:10.2`](#mariadb102)
-	[`mariadb:10.2-bionic`](#mariadb102-bionic)
-	[`mariadb:10.2.43`](#mariadb10243)
-	[`mariadb:10.2.43-bionic`](#mariadb10243-bionic)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.34`](#mariadb10334)
-	[`mariadb:10.3.34-focal`](#mariadb10334-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.24`](#mariadb10424)
-	[`mariadb:10.4.24-focal`](#mariadb10424-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.15`](#mariadb10515)
-	[`mariadb:10.5.15-focal`](#mariadb10515-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.7`](#mariadb1067)
-	[`mariadb:10.6.7-focal`](#mariadb1067-focal)
-	[`mariadb:10.7`](#mariadb107)
-	[`mariadb:10.7-focal`](#mariadb107-focal)
-	[`mariadb:10.7.3`](#mariadb1073)
-	[`mariadb:10.7.3-focal`](#mariadb1073-focal)
-	[`mariadb:10.8-rc`](#mariadb108-rc)
-	[`mariadb:10.8-rc-focal`](#mariadb108-rc-focal)
-	[`mariadb:10.8.2-rc`](#mariadb1082-rc)
-	[`mariadb:10.8.2-rc-focal`](#mariadb1082-rc-focal)
-	[`mariadb:focal`](#mariadbfocal)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-focal`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2`

```console
$ docker pull mariadb@sha256:cbc804d4b4a6e12aff2b9d95fb07992934affec65059162135b0e6be5664bd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2` - linux; amd64

```console
$ docker pull mariadb@sha256:223648f62ed3f709232ed449274b571bc7dc3e31a2d020ce8002bb481ded99c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109314517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2fe61c51d112be6fe439cdd14714554b0413a9cf36940e6820f563f931ac2c`
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
# Fri, 25 Feb 2022 19:05:13 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:05:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:06:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:06:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:06:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:06:09 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:06:09 GMT
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
	-	`sha256:f20894d37f30ec98e97246f995150981ff1fcf540ddd23e7683ae57094329ec6`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c43503ec3e128d0945557ae479c34330bdbd94ff8ac79261066d09d744f1125`  
		Last Modified: Fri, 25 Feb 2022 19:10:51 GMT  
		Size: 72.6 MB (72639284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb4aa2e111d7114c503d64e520d7571b9a4ea7a91e10354808a2512e958092`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 3.5 KB (3457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4ba929c4a13c53a8f8b810b145ca525062a82389a2cc83332912d70a1cfccf`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 6.6 KB (6592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036bda4af7b8bda44067121496ca6e9de1d1b56832c921a0f93353a7c33954e`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
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
$ docker pull mariadb@sha256:0c5e8babb24b39b181f838d7e541f4d6df90b415bfed8b755cdedf50d6d9c1cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ca6ec1a727760c9f1890d7bca1de23073f37ae31569527120b7c8c632af724`
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
# Fri, 25 Feb 2022 19:46:01 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:04 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:46:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:42:41 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:42:44 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:42:46 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:42:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:42:58 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:43:00 GMT
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
	-	`sha256:de63c7902694009c795a691110a7e362d741a5623c33debfa4566b1e5b79bce3`  
		Last Modified: Fri, 25 Feb 2022 19:57:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e64a32acc9fd8f28fd350d7b94e7fb95db1631f1a5b4182691ab54a52a76f7`  
		Last Modified: Wed, 02 Mar 2022 18:49:34 GMT  
		Size: 76.2 MB (76158405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc756eb9719837a7110058678c5a11e9f10f8124ade4d4d91211c593e6e5996c`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282b17ac0152124188ce4b3d25fa819015ee6caa18ebb7b4e1f05f237a6f39e4`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350bef9db6d60d2c072629023e79dc0df45a7e56e0021011f0280f7f5a985db`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2-bionic`

```console
$ docker pull mariadb@sha256:cbc804d4b4a6e12aff2b9d95fb07992934affec65059162135b0e6be5664bd15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.2-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:223648f62ed3f709232ed449274b571bc7dc3e31a2d020ce8002bb481ded99c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109314517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2fe61c51d112be6fe439cdd14714554b0413a9cf36940e6820f563f931ac2c`
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
# Fri, 25 Feb 2022 19:05:13 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:05:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:06:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:06:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:06:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:06:09 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:06:09 GMT
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
	-	`sha256:f20894d37f30ec98e97246f995150981ff1fcf540ddd23e7683ae57094329ec6`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c43503ec3e128d0945557ae479c34330bdbd94ff8ac79261066d09d744f1125`  
		Last Modified: Fri, 25 Feb 2022 19:10:51 GMT  
		Size: 72.6 MB (72639284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb4aa2e111d7114c503d64e520d7571b9a4ea7a91e10354808a2512e958092`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 3.5 KB (3457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4ba929c4a13c53a8f8b810b145ca525062a82389a2cc83332912d70a1cfccf`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 6.6 KB (6592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036bda4af7b8bda44067121496ca6e9de1d1b56832c921a0f93353a7c33954e`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
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
$ docker pull mariadb@sha256:0c5e8babb24b39b181f838d7e541f4d6df90b415bfed8b755cdedf50d6d9c1cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ca6ec1a727760c9f1890d7bca1de23073f37ae31569527120b7c8c632af724`
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
# Fri, 25 Feb 2022 19:46:01 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:04 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:46:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:42:41 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:42:44 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:42:46 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:42:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:42:58 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:43:00 GMT
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
	-	`sha256:de63c7902694009c795a691110a7e362d741a5623c33debfa4566b1e5b79bce3`  
		Last Modified: Fri, 25 Feb 2022 19:57:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e64a32acc9fd8f28fd350d7b94e7fb95db1631f1a5b4182691ab54a52a76f7`  
		Last Modified: Wed, 02 Mar 2022 18:49:34 GMT  
		Size: 76.2 MB (76158405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc756eb9719837a7110058678c5a11e9f10f8124ade4d4d91211c593e6e5996c`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282b17ac0152124188ce4b3d25fa819015ee6caa18ebb7b4e1f05f237a6f39e4`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350bef9db6d60d2c072629023e79dc0df45a7e56e0021011f0280f7f5a985db`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43`

```console
$ docker pull mariadb@sha256:e7bcb243b3ce554f43d46aab87a43a7b142b785a1b23bdc13146ef7b2dec28c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.2.43` - linux; amd64

```console
$ docker pull mariadb@sha256:223648f62ed3f709232ed449274b571bc7dc3e31a2d020ce8002bb481ded99c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109314517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2fe61c51d112be6fe439cdd14714554b0413a9cf36940e6820f563f931ac2c`
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
# Fri, 25 Feb 2022 19:05:13 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:05:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:06:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:06:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:06:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:06:09 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:06:09 GMT
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
	-	`sha256:f20894d37f30ec98e97246f995150981ff1fcf540ddd23e7683ae57094329ec6`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c43503ec3e128d0945557ae479c34330bdbd94ff8ac79261066d09d744f1125`  
		Last Modified: Fri, 25 Feb 2022 19:10:51 GMT  
		Size: 72.6 MB (72639284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb4aa2e111d7114c503d64e520d7571b9a4ea7a91e10354808a2512e958092`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 3.5 KB (3457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4ba929c4a13c53a8f8b810b145ca525062a82389a2cc83332912d70a1cfccf`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 6.6 KB (6592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036bda4af7b8bda44067121496ca6e9de1d1b56832c921a0f93353a7c33954e`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0c5e8babb24b39b181f838d7e541f4d6df90b415bfed8b755cdedf50d6d9c1cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ca6ec1a727760c9f1890d7bca1de23073f37ae31569527120b7c8c632af724`
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
# Fri, 25 Feb 2022 19:46:01 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:04 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:46:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:42:41 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:42:44 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:42:46 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:42:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:42:58 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:43:00 GMT
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
	-	`sha256:de63c7902694009c795a691110a7e362d741a5623c33debfa4566b1e5b79bce3`  
		Last Modified: Fri, 25 Feb 2022 19:57:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e64a32acc9fd8f28fd350d7b94e7fb95db1631f1a5b4182691ab54a52a76f7`  
		Last Modified: Wed, 02 Mar 2022 18:49:34 GMT  
		Size: 76.2 MB (76158405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc756eb9719837a7110058678c5a11e9f10f8124ade4d4d91211c593e6e5996c`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282b17ac0152124188ce4b3d25fa819015ee6caa18ebb7b4e1f05f237a6f39e4`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350bef9db6d60d2c072629023e79dc0df45a7e56e0021011f0280f7f5a985db`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.2.43-bionic`

```console
$ docker pull mariadb@sha256:e7bcb243b3ce554f43d46aab87a43a7b142b785a1b23bdc13146ef7b2dec28c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; ppc64le

### `mariadb:10.2.43-bionic` - linux; amd64

```console
$ docker pull mariadb@sha256:223648f62ed3f709232ed449274b571bc7dc3e31a2d020ce8002bb481ded99c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.3 MB (109314517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2fe61c51d112be6fe439cdd14714554b0413a9cf36940e6820f563f931ac2c`
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
# Fri, 25 Feb 2022 19:05:13 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:05:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:05:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:06:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:06:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:06:07 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:06:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:06:09 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:06:09 GMT
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
	-	`sha256:f20894d37f30ec98e97246f995150981ff1fcf540ddd23e7683ae57094329ec6`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c43503ec3e128d0945557ae479c34330bdbd94ff8ac79261066d09d744f1125`  
		Last Modified: Fri, 25 Feb 2022 19:10:51 GMT  
		Size: 72.6 MB (72639284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb4aa2e111d7114c503d64e520d7571b9a4ea7a91e10354808a2512e958092`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 3.5 KB (3457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4ba929c4a13c53a8f8b810b145ca525062a82389a2cc83332912d70a1cfccf`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 6.6 KB (6592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7036bda4af7b8bda44067121496ca6e9de1d1b56832c921a0f93353a7c33954e`  
		Last Modified: Fri, 25 Feb 2022 19:10:36 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.2.43-bionic` - linux; ppc64le

```console
$ docker pull mariadb@sha256:0c5e8babb24b39b181f838d7e541f4d6df90b415bfed8b755cdedf50d6d9c1cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117714767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ca6ec1a727760c9f1890d7bca1de23073f37ae31569527120b7c8c632af724`
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
# Fri, 25 Feb 2022 19:46:01 GMT
ARG MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:04 GMT
ENV MARIADB_VERSION=1:10.2.43+maria~bionic
# Fri, 25 Feb 2022 19:46:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
# Fri, 25 Feb 2022 19:46:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup-10.2 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:42:41 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:42:44 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:42:46 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:42:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.2.43/repo/ubuntu/ bionic main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:42:58 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:43:00 GMT
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
	-	`sha256:de63c7902694009c795a691110a7e362d741a5623c33debfa4566b1e5b79bce3`  
		Last Modified: Fri, 25 Feb 2022 19:57:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e64a32acc9fd8f28fd350d7b94e7fb95db1631f1a5b4182691ab54a52a76f7`  
		Last Modified: Wed, 02 Mar 2022 18:49:34 GMT  
		Size: 76.2 MB (76158405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc756eb9719837a7110058678c5a11e9f10f8124ade4d4d91211c593e6e5996c`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:282b17ac0152124188ce4b3d25fa819015ee6caa18ebb7b4e1f05f237a6f39e4`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1350bef9db6d60d2c072629023e79dc0df45a7e56e0021011f0280f7f5a985db`  
		Last Modified: Wed, 02 Mar 2022 18:49:19 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:38b353923ef66e9b458e1fe7e42bebc5cfdffa601cba9f5ffea9e1a6d7718fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:5ff563719b69c13176d018523117206ed0928c3a15ea4547618c14eb493d2fa8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c4d949b520a3bda2d53cc35b87df84af0655aade4c6a4b77cc86bcece148f`
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
# Fri, 25 Feb 2022 19:04:24 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:04:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:05:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:05:00 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:05:01 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:05:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:05:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:05:03 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:05:03 GMT
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
	-	`sha256:09068eced0b633eec0c4c85f6e82fb884de56a7285f4d36b3504a6d72fa23731`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf18bfce1213ed3f88c5333e6112a6cba219ecf61b0f8dc45a9b87a166ecac2`  
		Last Modified: Fri, 25 Feb 2022 19:10:17 GMT  
		Size: 80.2 MB (80191098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e703ab2dfb1ebabf11b526ea6418cc872fde0e9228699534ca6502316f429f5`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 3.5 KB (3459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdbba010e4a1689eccb4971867b3ba3a08564e795ec18a5e3c34e415cee1706`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 6.6 KB (6591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472da57979151992035cff2e784a9c871aaef0799eb0ca04a3a3f7ccf8b5777`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c975194aab3491e2215e4ba21256c0b996811bda60c3fa6d74b85d19b541c6ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5528d732983387affc7679385799afa83489016f4a24aaea57613216281215f`
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
# Fri, 25 Feb 2022 17:44:00 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:01 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:44:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:48 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:49 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:51 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:52 GMT
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
	-	`sha256:4bbda986a1859ae04347f486c41518b50dca07012a3d2a1a94d0637613db3733`  
		Last Modified: Fri, 25 Feb 2022 17:49:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd19f638bea3bd2ec8a2474be0002550a2b5b59c755cca7189f99160a5b1a2`  
		Last Modified: Wed, 02 Mar 2022 20:11:42 GMT  
		Size: 79.5 MB (79530975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb537b30bac1f3d1e659fa888f33b1c48df27b4954063a5d04cb9948fb7306b`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db08e1cf9931308d3d9cd96269b9b61e7eeca757a557ca351a1d87392ef52a3`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5279caa3a871a81d83692ffe7bfaa8fd58e4b5eab5f8418a83d39dacf6457311`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4e09114f7013b1ea711f60a008a6bc57bfa85f3544567408c165bbd969aac480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131000876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f480a06c5790b915c7db889d8d1fb536583b69edb6c8ea2c8f6defbdd5ea38`
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
# Fri, 25 Feb 2022 19:39:18 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:29 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:39:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:40:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:40:09 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:40:10 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:40:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:40:19 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:40:22 GMT
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
	-	`sha256:9639be8588c384656a16d878caa23aba18bdeee898dea89009a23f00f9d8f67b`  
		Last Modified: Fri, 25 Feb 2022 19:56:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264321a412caf8bb1e2e39e7d17a327618010de85126721a12b995e2b4fa1035`  
		Last Modified: Wed, 02 Mar 2022 18:48:57 GMT  
		Size: 84.8 MB (84791735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528d98181ab5d2775e5be8f3bea554d3a1e80044b2a4d560194d46c064f70af6`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16848a739b73f253e3ce6c474a0273b320a77320be138c73390a5deff457a87c`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f69703c038780f128cfef6087c3cf0d7a70b438216b1cc70d731a48d37fe70`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:38b353923ef66e9b458e1fe7e42bebc5cfdffa601cba9f5ffea9e1a6d7718fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:5ff563719b69c13176d018523117206ed0928c3a15ea4547618c14eb493d2fa8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c4d949b520a3bda2d53cc35b87df84af0655aade4c6a4b77cc86bcece148f`
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
# Fri, 25 Feb 2022 19:04:24 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:04:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:05:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:05:00 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:05:01 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:05:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:05:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:05:03 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:05:03 GMT
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
	-	`sha256:09068eced0b633eec0c4c85f6e82fb884de56a7285f4d36b3504a6d72fa23731`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf18bfce1213ed3f88c5333e6112a6cba219ecf61b0f8dc45a9b87a166ecac2`  
		Last Modified: Fri, 25 Feb 2022 19:10:17 GMT  
		Size: 80.2 MB (80191098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e703ab2dfb1ebabf11b526ea6418cc872fde0e9228699534ca6502316f429f5`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 3.5 KB (3459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdbba010e4a1689eccb4971867b3ba3a08564e795ec18a5e3c34e415cee1706`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 6.6 KB (6591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472da57979151992035cff2e784a9c871aaef0799eb0ca04a3a3f7ccf8b5777`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c975194aab3491e2215e4ba21256c0b996811bda60c3fa6d74b85d19b541c6ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5528d732983387affc7679385799afa83489016f4a24aaea57613216281215f`
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
# Fri, 25 Feb 2022 17:44:00 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:01 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:44:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:48 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:49 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:51 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:52 GMT
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
	-	`sha256:4bbda986a1859ae04347f486c41518b50dca07012a3d2a1a94d0637613db3733`  
		Last Modified: Fri, 25 Feb 2022 17:49:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd19f638bea3bd2ec8a2474be0002550a2b5b59c755cca7189f99160a5b1a2`  
		Last Modified: Wed, 02 Mar 2022 20:11:42 GMT  
		Size: 79.5 MB (79530975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb537b30bac1f3d1e659fa888f33b1c48df27b4954063a5d04cb9948fb7306b`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db08e1cf9931308d3d9cd96269b9b61e7eeca757a557ca351a1d87392ef52a3`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5279caa3a871a81d83692ffe7bfaa8fd58e4b5eab5f8418a83d39dacf6457311`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4e09114f7013b1ea711f60a008a6bc57bfa85f3544567408c165bbd969aac480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131000876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f480a06c5790b915c7db889d8d1fb536583b69edb6c8ea2c8f6defbdd5ea38`
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
# Fri, 25 Feb 2022 19:39:18 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:29 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:39:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:40:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:40:09 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:40:10 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:40:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:40:19 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:40:22 GMT
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
	-	`sha256:9639be8588c384656a16d878caa23aba18bdeee898dea89009a23f00f9d8f67b`  
		Last Modified: Fri, 25 Feb 2022 19:56:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264321a412caf8bb1e2e39e7d17a327618010de85126721a12b995e2b4fa1035`  
		Last Modified: Wed, 02 Mar 2022 18:48:57 GMT  
		Size: 84.8 MB (84791735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528d98181ab5d2775e5be8f3bea554d3a1e80044b2a4d560194d46c064f70af6`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16848a739b73f253e3ce6c474a0273b320a77320be138c73390a5deff457a87c`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f69703c038780f128cfef6087c3cf0d7a70b438216b1cc70d731a48d37fe70`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34`

```console
$ docker pull mariadb@sha256:38b353923ef66e9b458e1fe7e42bebc5cfdffa601cba9f5ffea9e1a6d7718fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34` - linux; amd64

```console
$ docker pull mariadb@sha256:5ff563719b69c13176d018523117206ed0928c3a15ea4547618c14eb493d2fa8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c4d949b520a3bda2d53cc35b87df84af0655aade4c6a4b77cc86bcece148f`
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
# Fri, 25 Feb 2022 19:04:24 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:04:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:05:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:05:00 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:05:01 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:05:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:05:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:05:03 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:05:03 GMT
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
	-	`sha256:09068eced0b633eec0c4c85f6e82fb884de56a7285f4d36b3504a6d72fa23731`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf18bfce1213ed3f88c5333e6112a6cba219ecf61b0f8dc45a9b87a166ecac2`  
		Last Modified: Fri, 25 Feb 2022 19:10:17 GMT  
		Size: 80.2 MB (80191098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e703ab2dfb1ebabf11b526ea6418cc872fde0e9228699534ca6502316f429f5`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 3.5 KB (3459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdbba010e4a1689eccb4971867b3ba3a08564e795ec18a5e3c34e415cee1706`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 6.6 KB (6591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472da57979151992035cff2e784a9c871aaef0799eb0ca04a3a3f7ccf8b5777`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c975194aab3491e2215e4ba21256c0b996811bda60c3fa6d74b85d19b541c6ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5528d732983387affc7679385799afa83489016f4a24aaea57613216281215f`
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
# Fri, 25 Feb 2022 17:44:00 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:01 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:44:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:48 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:49 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:51 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:52 GMT
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
	-	`sha256:4bbda986a1859ae04347f486c41518b50dca07012a3d2a1a94d0637613db3733`  
		Last Modified: Fri, 25 Feb 2022 17:49:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd19f638bea3bd2ec8a2474be0002550a2b5b59c755cca7189f99160a5b1a2`  
		Last Modified: Wed, 02 Mar 2022 20:11:42 GMT  
		Size: 79.5 MB (79530975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb537b30bac1f3d1e659fa888f33b1c48df27b4954063a5d04cb9948fb7306b`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db08e1cf9931308d3d9cd96269b9b61e7eeca757a557ca351a1d87392ef52a3`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5279caa3a871a81d83692ffe7bfaa8fd58e4b5eab5f8418a83d39dacf6457311`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4e09114f7013b1ea711f60a008a6bc57bfa85f3544567408c165bbd969aac480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131000876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f480a06c5790b915c7db889d8d1fb536583b69edb6c8ea2c8f6defbdd5ea38`
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
# Fri, 25 Feb 2022 19:39:18 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:29 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:39:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:40:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:40:09 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:40:10 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:40:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:40:19 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:40:22 GMT
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
	-	`sha256:9639be8588c384656a16d878caa23aba18bdeee898dea89009a23f00f9d8f67b`  
		Last Modified: Fri, 25 Feb 2022 19:56:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264321a412caf8bb1e2e39e7d17a327618010de85126721a12b995e2b4fa1035`  
		Last Modified: Wed, 02 Mar 2022 18:48:57 GMT  
		Size: 84.8 MB (84791735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528d98181ab5d2775e5be8f3bea554d3a1e80044b2a4d560194d46c064f70af6`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16848a739b73f253e3ce6c474a0273b320a77320be138c73390a5deff457a87c`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f69703c038780f128cfef6087c3cf0d7a70b438216b1cc70d731a48d37fe70`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.34-focal`

```console
$ docker pull mariadb@sha256:38b353923ef66e9b458e1fe7e42bebc5cfdffa601cba9f5ffea9e1a6d7718fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3.34-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:5ff563719b69c13176d018523117206ed0928c3a15ea4547618c14eb493d2fa8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120117250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a9c4d949b520a3bda2d53cc35b87df84af0655aade4c6a4b77cc86bcece148f`
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
# Fri, 25 Feb 2022 19:04:24 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:04:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:04:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:05:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:05:00 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:05:01 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:05:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:05:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:05:03 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:05:03 GMT
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
	-	`sha256:09068eced0b633eec0c4c85f6e82fb884de56a7285f4d36b3504a6d72fa23731`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf18bfce1213ed3f88c5333e6112a6cba219ecf61b0f8dc45a9b87a166ecac2`  
		Last Modified: Fri, 25 Feb 2022 19:10:17 GMT  
		Size: 80.2 MB (80191098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e703ab2dfb1ebabf11b526ea6418cc872fde0e9228699534ca6502316f429f5`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 3.5 KB (3459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdbba010e4a1689eccb4971867b3ba3a08564e795ec18a5e3c34e415cee1706`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 6.6 KB (6591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8472da57979151992035cff2e784a9c871aaef0799eb0ca04a3a3f7ccf8b5777`  
		Last Modified: Fri, 25 Feb 2022 19:10:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c975194aab3491e2215e4ba21256c0b996811bda60c3fa6d74b85d19b541c6ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117610543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5528d732983387affc7679385799afa83489016f4a24aaea57613216281215f`
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
# Fri, 25 Feb 2022 17:44:00 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:01 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 17:44:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:44:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:48 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:49 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:51 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:52 GMT
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
	-	`sha256:4bbda986a1859ae04347f486c41518b50dca07012a3d2a1a94d0637613db3733`  
		Last Modified: Fri, 25 Feb 2022 17:49:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbd19f638bea3bd2ec8a2474be0002550a2b5b59c755cca7189f99160a5b1a2`  
		Last Modified: Wed, 02 Mar 2022 20:11:42 GMT  
		Size: 79.5 MB (79530975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb537b30bac1f3d1e659fa888f33b1c48df27b4954063a5d04cb9948fb7306b`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8db08e1cf9931308d3d9cd96269b9b61e7eeca757a557ca351a1d87392ef52a3`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 6.6 KB (6604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5279caa3a871a81d83692ffe7bfaa8fd58e4b5eab5f8418a83d39dacf6457311`  
		Last Modified: Wed, 02 Mar 2022 20:11:30 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3.34-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4e09114f7013b1ea711f60a008a6bc57bfa85f3544567408c165bbd969aac480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (131000876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50f480a06c5790b915c7db889d8d1fb536583b69edb6c8ea2c8f6defbdd5ea38`
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
# Fri, 25 Feb 2022 19:39:18 GMT
ARG MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:29 GMT
ENV MARIADB_VERSION=1:10.3.34+maria~focal
# Fri, 25 Feb 2022 19:39:41 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:39:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:39:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:40:07 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:40:09 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:40:10 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:40:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.34/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:40:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:40:19 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:40:22 GMT
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
	-	`sha256:9639be8588c384656a16d878caa23aba18bdeee898dea89009a23f00f9d8f67b`  
		Last Modified: Fri, 25 Feb 2022 19:56:42 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264321a412caf8bb1e2e39e7d17a327618010de85126721a12b995e2b4fa1035`  
		Last Modified: Wed, 02 Mar 2022 18:48:57 GMT  
		Size: 84.8 MB (84791735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:528d98181ab5d2775e5be8f3bea554d3a1e80044b2a4d560194d46c064f70af6`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16848a739b73f253e3ce6c474a0273b320a77320be138c73390a5deff457a87c`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f69703c038780f128cfef6087c3cf0d7a70b438216b1cc70d731a48d37fe70`  
		Last Modified: Wed, 02 Mar 2022 18:48:37 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:981e0aaa2bdac4a2941266cf744aaaa38078d388e6a286365f87eb6c20cadd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:4f6a6149b44efcf25e7f42d9eaa0ecfa1064309d52f1010b107be61ef78edd04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e43bdc7cb4b6250eeb8b31049fd432d63f0def53b66039495acf5061bf381`
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
# Fri, 25 Feb 2022 19:03:42 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:04:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:04:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:04:17 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:04:17 GMT
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
	-	`sha256:cf6156b5ae3eab330f960e987f6f8909e66383b40568023750502e35592c3386`  
		Last Modified: Fri, 25 Feb 2022 19:09:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a164602a707b12618fd4f4bd8aaec0793caa4758d50ff5c1ca2e8f94ce42168`  
		Last Modified: Fri, 25 Feb 2022 19:09:41 GMT  
		Size: 85.8 MB (85753048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7737b42b2f9d437e71347b905f24a0b9f609a82deab811d1f7b0c54f30887435`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 3.5 KB (3458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df6a2eee8e484d15aee5deaf795e069c4fb33338acd2d415183a514d767927`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b89880e212bf6dd24e0eee0e0395baebdc93b2997fd22003d8c2717525c0f4`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:60f4f9aef7c3396ce004f792e7c748bfa738dd359e1f58bf8d127e29bf2d391c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aa3f09b5efc9690172e6710c05f82dd86e0b083cc942a14a1d7b43e4493e3e`
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
# Fri, 25 Feb 2022 17:43:09 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:10 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:02 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:03 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:05 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:06 GMT
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
	-	`sha256:24b4cd5c6baf7ad79fff81296377b291354c76f16821f66ad252fe8f1cec5f2e`  
		Last Modified: Fri, 25 Feb 2022 17:48:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d703b7e579396927761978779bb907446519cb47b8b5b767dfa34fbcba4121`  
		Last Modified: Wed, 02 Mar 2022 20:11:11 GMT  
		Size: 84.9 MB (84925476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a016c6dc3233bf747388f07f4ae102dc4079b426918ee98c3b6f5e3e622f72c`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dee9d10f943fc53580ba98967471e10854a7bd6e481fc04eef06310014571e`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 6.6 KB (6603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf4ba258bca787f12bb90a0440feb63c41a33883ab139246d2c5d64a27bea87`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:17997b20c6a6697aa3f89f5acdf1418f2939b0249adb6476ae9de054e0279187
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136555043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2c6b814a3345e61d0b19dd5b11ca5430412c43b24c3bc89f68edba34372709`
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
# Fri, 25 Feb 2022 19:34:36 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:38 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:34:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:36:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:36:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:36:55 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:36:58 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:37:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:37:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:37:21 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:37:23 GMT
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
	-	`sha256:e5f912aa2a2787b948aca725d1044231bb5a9253cc30f0fea0a350bedf54ebed`  
		Last Modified: Fri, 25 Feb 2022 19:56:04 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4474426281bbf873916cef9af2bba74cb0040ff303a0f2eaf5d557e5d2df7`  
		Last Modified: Wed, 02 Mar 2022 18:48:08 GMT  
		Size: 90.3 MB (90345907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dec38e7637b147a987f22b45880d6bd5926b2ed638e7bf5d63c1bf8533037a`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef7f7a3d59c1eec1083c864f6bad6355d66d6f69375e6cf167ab17ca8271bac`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e773c51f8ce6bdbbb3bbebcbcc26d64a64d0b1e96288631acd631768677e5ba3`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:981e0aaa2bdac4a2941266cf744aaaa38078d388e6a286365f87eb6c20cadd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:4f6a6149b44efcf25e7f42d9eaa0ecfa1064309d52f1010b107be61ef78edd04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e43bdc7cb4b6250eeb8b31049fd432d63f0def53b66039495acf5061bf381`
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
# Fri, 25 Feb 2022 19:03:42 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:04:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:04:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:04:17 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:04:17 GMT
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
	-	`sha256:cf6156b5ae3eab330f960e987f6f8909e66383b40568023750502e35592c3386`  
		Last Modified: Fri, 25 Feb 2022 19:09:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a164602a707b12618fd4f4bd8aaec0793caa4758d50ff5c1ca2e8f94ce42168`  
		Last Modified: Fri, 25 Feb 2022 19:09:41 GMT  
		Size: 85.8 MB (85753048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7737b42b2f9d437e71347b905f24a0b9f609a82deab811d1f7b0c54f30887435`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 3.5 KB (3458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df6a2eee8e484d15aee5deaf795e069c4fb33338acd2d415183a514d767927`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b89880e212bf6dd24e0eee0e0395baebdc93b2997fd22003d8c2717525c0f4`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:60f4f9aef7c3396ce004f792e7c748bfa738dd359e1f58bf8d127e29bf2d391c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aa3f09b5efc9690172e6710c05f82dd86e0b083cc942a14a1d7b43e4493e3e`
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
# Fri, 25 Feb 2022 17:43:09 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:10 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:02 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:03 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:05 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:06 GMT
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
	-	`sha256:24b4cd5c6baf7ad79fff81296377b291354c76f16821f66ad252fe8f1cec5f2e`  
		Last Modified: Fri, 25 Feb 2022 17:48:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d703b7e579396927761978779bb907446519cb47b8b5b767dfa34fbcba4121`  
		Last Modified: Wed, 02 Mar 2022 20:11:11 GMT  
		Size: 84.9 MB (84925476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a016c6dc3233bf747388f07f4ae102dc4079b426918ee98c3b6f5e3e622f72c`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dee9d10f943fc53580ba98967471e10854a7bd6e481fc04eef06310014571e`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 6.6 KB (6603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf4ba258bca787f12bb90a0440feb63c41a33883ab139246d2c5d64a27bea87`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:17997b20c6a6697aa3f89f5acdf1418f2939b0249adb6476ae9de054e0279187
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136555043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2c6b814a3345e61d0b19dd5b11ca5430412c43b24c3bc89f68edba34372709`
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
# Fri, 25 Feb 2022 19:34:36 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:38 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:34:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:36:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:36:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:36:55 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:36:58 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:37:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:37:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:37:21 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:37:23 GMT
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
	-	`sha256:e5f912aa2a2787b948aca725d1044231bb5a9253cc30f0fea0a350bedf54ebed`  
		Last Modified: Fri, 25 Feb 2022 19:56:04 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4474426281bbf873916cef9af2bba74cb0040ff303a0f2eaf5d557e5d2df7`  
		Last Modified: Wed, 02 Mar 2022 18:48:08 GMT  
		Size: 90.3 MB (90345907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dec38e7637b147a987f22b45880d6bd5926b2ed638e7bf5d63c1bf8533037a`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef7f7a3d59c1eec1083c864f6bad6355d66d6f69375e6cf167ab17ca8271bac`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e773c51f8ce6bdbbb3bbebcbcc26d64a64d0b1e96288631acd631768677e5ba3`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24`

```console
$ docker pull mariadb@sha256:981e0aaa2bdac4a2941266cf744aaaa38078d388e6a286365f87eb6c20cadd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24` - linux; amd64

```console
$ docker pull mariadb@sha256:4f6a6149b44efcf25e7f42d9eaa0ecfa1064309d52f1010b107be61ef78edd04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e43bdc7cb4b6250eeb8b31049fd432d63f0def53b66039495acf5061bf381`
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
# Fri, 25 Feb 2022 19:03:42 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:04:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:04:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:04:17 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:04:17 GMT
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
	-	`sha256:cf6156b5ae3eab330f960e987f6f8909e66383b40568023750502e35592c3386`  
		Last Modified: Fri, 25 Feb 2022 19:09:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a164602a707b12618fd4f4bd8aaec0793caa4758d50ff5c1ca2e8f94ce42168`  
		Last Modified: Fri, 25 Feb 2022 19:09:41 GMT  
		Size: 85.8 MB (85753048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7737b42b2f9d437e71347b905f24a0b9f609a82deab811d1f7b0c54f30887435`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 3.5 KB (3458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df6a2eee8e484d15aee5deaf795e069c4fb33338acd2d415183a514d767927`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b89880e212bf6dd24e0eee0e0395baebdc93b2997fd22003d8c2717525c0f4`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:60f4f9aef7c3396ce004f792e7c748bfa738dd359e1f58bf8d127e29bf2d391c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aa3f09b5efc9690172e6710c05f82dd86e0b083cc942a14a1d7b43e4493e3e`
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
# Fri, 25 Feb 2022 17:43:09 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:10 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:02 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:03 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:05 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:06 GMT
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
	-	`sha256:24b4cd5c6baf7ad79fff81296377b291354c76f16821f66ad252fe8f1cec5f2e`  
		Last Modified: Fri, 25 Feb 2022 17:48:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d703b7e579396927761978779bb907446519cb47b8b5b767dfa34fbcba4121`  
		Last Modified: Wed, 02 Mar 2022 20:11:11 GMT  
		Size: 84.9 MB (84925476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a016c6dc3233bf747388f07f4ae102dc4079b426918ee98c3b6f5e3e622f72c`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dee9d10f943fc53580ba98967471e10854a7bd6e481fc04eef06310014571e`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 6.6 KB (6603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf4ba258bca787f12bb90a0440feb63c41a33883ab139246d2c5d64a27bea87`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24` - linux; ppc64le

```console
$ docker pull mariadb@sha256:17997b20c6a6697aa3f89f5acdf1418f2939b0249adb6476ae9de054e0279187
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136555043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2c6b814a3345e61d0b19dd5b11ca5430412c43b24c3bc89f68edba34372709`
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
# Fri, 25 Feb 2022 19:34:36 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:38 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:34:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:36:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:36:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:36:55 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:36:58 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:37:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:37:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:37:21 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:37:23 GMT
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
	-	`sha256:e5f912aa2a2787b948aca725d1044231bb5a9253cc30f0fea0a350bedf54ebed`  
		Last Modified: Fri, 25 Feb 2022 19:56:04 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4474426281bbf873916cef9af2bba74cb0040ff303a0f2eaf5d557e5d2df7`  
		Last Modified: Wed, 02 Mar 2022 18:48:08 GMT  
		Size: 90.3 MB (90345907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dec38e7637b147a987f22b45880d6bd5926b2ed638e7bf5d63c1bf8533037a`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef7f7a3d59c1eec1083c864f6bad6355d66d6f69375e6cf167ab17ca8271bac`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e773c51f8ce6bdbbb3bbebcbcc26d64a64d0b1e96288631acd631768677e5ba3`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.24-focal`

```console
$ docker pull mariadb@sha256:981e0aaa2bdac4a2941266cf744aaaa38078d388e6a286365f87eb6c20cadd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4.24-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:4f6a6149b44efcf25e7f42d9eaa0ecfa1064309d52f1010b107be61ef78edd04
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125679196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e43bdc7cb4b6250eeb8b31049fd432d63f0def53b66039495acf5061bf381`
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
# Fri, 25 Feb 2022 19:03:42 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:03:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:04:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:04:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:04:15 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:04:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Feb 2022 19:04:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:04:17 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:04:17 GMT
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
	-	`sha256:cf6156b5ae3eab330f960e987f6f8909e66383b40568023750502e35592c3386`  
		Last Modified: Fri, 25 Feb 2022 19:09:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a164602a707b12618fd4f4bd8aaec0793caa4758d50ff5c1ca2e8f94ce42168`  
		Last Modified: Fri, 25 Feb 2022 19:09:41 GMT  
		Size: 85.8 MB (85753048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7737b42b2f9d437e71347b905f24a0b9f609a82deab811d1f7b0c54f30887435`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 3.5 KB (3458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df6a2eee8e484d15aee5deaf795e069c4fb33338acd2d415183a514d767927`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 6.6 KB (6590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b89880e212bf6dd24e0eee0e0395baebdc93b2997fd22003d8c2717525c0f4`  
		Last Modified: Fri, 25 Feb 2022 19:09:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:60f4f9aef7c3396ce004f792e7c748bfa738dd359e1f58bf8d127e29bf2d391c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123005045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2aa3f09b5efc9690172e6710c05f82dd86e0b083cc942a14a1d7b43e4493e3e`
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
# Fri, 25 Feb 2022 17:43:09 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:10 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 17:43:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:06:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:06:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:06:02 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:06:03 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:06:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 20:06:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:06:05 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:06:06 GMT
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
	-	`sha256:24b4cd5c6baf7ad79fff81296377b291354c76f16821f66ad252fe8f1cec5f2e`  
		Last Modified: Fri, 25 Feb 2022 17:48:36 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d703b7e579396927761978779bb907446519cb47b8b5b767dfa34fbcba4121`  
		Last Modified: Wed, 02 Mar 2022 20:11:11 GMT  
		Size: 84.9 MB (84925476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a016c6dc3233bf747388f07f4ae102dc4079b426918ee98c3b6f5e3e622f72c`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dee9d10f943fc53580ba98967471e10854a7bd6e481fc04eef06310014571e`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 6.6 KB (6603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf4ba258bca787f12bb90a0440feb63c41a33883ab139246d2c5d64a27bea87`  
		Last Modified: Wed, 02 Mar 2022 20:10:57 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4.24-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:17997b20c6a6697aa3f89f5acdf1418f2939b0249adb6476ae9de054e0279187
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136555043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2c6b814a3345e61d0b19dd5b11ca5430412c43b24c3bc89f68edba34372709`
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
# Fri, 25 Feb 2022 19:34:36 GMT
ARG MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:38 GMT
ENV MARIADB_VERSION=1:10.4.24+maria~focal
# Fri, 25 Feb 2022 19:34:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:34:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:36:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:36:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:36:55 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:36:58 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:37:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.24/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 02 Mar 2022 18:37:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:37:21 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:37:23 GMT
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
	-	`sha256:e5f912aa2a2787b948aca725d1044231bb5a9253cc30f0fea0a350bedf54ebed`  
		Last Modified: Fri, 25 Feb 2022 19:56:04 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4474426281bbf873916cef9af2bba74cb0040ff303a0f2eaf5d557e5d2df7`  
		Last Modified: Wed, 02 Mar 2022 18:48:08 GMT  
		Size: 90.3 MB (90345907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dec38e7637b147a987f22b45880d6bd5926b2ed638e7bf5d63c1bf8533037a`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef7f7a3d59c1eec1083c864f6bad6355d66d6f69375e6cf167ab17ca8271bac`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 6.6 KB (6606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e773c51f8ce6bdbbb3bbebcbcc26d64a64d0b1e96288631acd631768677e5ba3`  
		Last Modified: Wed, 02 Mar 2022 18:47:51 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:cfe9dc35d3d37f43e0f4ec6d737387b320b83aafca96a4b889ac1e614a4689c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:7485ec97845ab634ae5d20c6d77cf7e75074a5bf25fdc5fa43d56c02e276b13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127922535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de390e78f76e36b80d2058fe2d03b412dfc2d27a1e9b6adba86046dc4ab6cb8a`
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
# Fri, 25 Feb 2022 19:03:01 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:03:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:03:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:03:34 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:03:35 GMT
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
	-	`sha256:1f04ebe61f0f28bd5b0152200a2b2b391d70185963444625f748b1965b5cc3ed`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1636f5af837d6842067e5e608bfce498c31c97fac419e1f5d28f31033ca664`  
		Last Modified: Fri, 25 Feb 2022 19:09:06 GMT  
		Size: 88.0 MB (87996503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85d8041fbf13d2aec88efee1942f6ab98624568e4cfcb05b55384b27d7b51c`  
		Last Modified: Fri, 25 Feb 2022 19:08:49 GMT  
		Size: 3.5 KB (3460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6007a391685787b262bb862b952fead864d6d88545870ffad22a6032836a5a`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 6.6 KB (6594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:098d91b0041466955595fca80dd126f256c67acd8afcaf48fb9871e9cd74812e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125189063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48d0c779281b4e5d291d34fcb2bc390e5990d8e6f89242e52db90c57b83409d`
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
# Fri, 25 Feb 2022 17:42:25 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:26 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:05:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:05:08 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:05:10 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:05:11 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:05:12 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:05:13 GMT
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
	-	`sha256:909ddc1e4a924d2fbfd551aeb58b73f53118882a59ae7b8b1292c0ab3bbc336f`  
		Last Modified: Fri, 25 Feb 2022 17:48:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a990ae0195fd38dd2247578a70d10f8fd0e422a886aa5a427ed1110e6fed3a`  
		Last Modified: Wed, 02 Mar 2022 20:10:39 GMT  
		Size: 87.1 MB (87109614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a12d88b36914fa06c21d2a213e88b4859bff8408107487553873e320010b62`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb95a55d81898a2cbb80e161e1fc84de0ba8d05132992d1e8b245e99df48815`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e82aba0ea4be9d0f6d7dacb3ad30138bc33f5dd983091dca3b790a9fc982d11f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138776390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f14b3a6a4ea1d8ea5a60e0ebfdcb360fb25f496f9709c588f73a0729177493`
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
# Fri, 25 Feb 2022 19:29:58 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:04 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:30:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:33:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:33:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:33:39 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:33:41 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:33:49 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:33:53 GMT
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
	-	`sha256:020f2977da1a5f3d6b9c778925ec00264ff32a5ca6aa55d127022a97cf18e78b`  
		Last Modified: Fri, 25 Feb 2022 19:55:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fb0583306c8d7f2fa7145ed3190266e0395a5ff420d88ca12a8349206eb672`  
		Last Modified: Wed, 02 Mar 2022 18:47:29 GMT  
		Size: 92.6 MB (92567371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f7a1f84d9bfcc4985c53c9293be6fa5d3a87271362f6af0325ed2b40cdfa9f`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea41f65e9a276cf3eb4c9803b1554a07a571e761da5e3be09b3ac302deb5d191`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:b25ec596e0b803d6fd988c0c7e16ecebc61e95f7f3c269b23fbe7a8f0309d1d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127234688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ee365d07d56d63dd1b1af874006dd9cadbdcc94248873e42cfd7b92d4d9007`
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
# Fri, 25 Feb 2022 17:43:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:43:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:43:32 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:43:32 GMT
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
	-	`sha256:09bbeaa7740ccfdc136df7f83f134c65c756afb9c4c1323685e6c5a09ea1bbe2`  
		Last Modified: Fri, 25 Feb 2022 17:46:25 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f23b45ea49fd398d929d4a4d79ed167bf5f4642dd044a62809e1f03bc78cb8`  
		Last Modified: Wed, 02 Mar 2022 17:46:30 GMT  
		Size: 89.3 MB (89290030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76afad66cec72e1af7009b464e97e49868d1944b5aaca12df54346021a984b99`  
		Last Modified: Wed, 02 Mar 2022 17:46:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0d15398e1a30ba8076ff1c63913f777e49309e7026a19aa50b8e1797a706e5`  
		Last Modified: Wed, 02 Mar 2022 17:46:18 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:cfe9dc35d3d37f43e0f4ec6d737387b320b83aafca96a4b889ac1e614a4689c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7485ec97845ab634ae5d20c6d77cf7e75074a5bf25fdc5fa43d56c02e276b13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127922535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de390e78f76e36b80d2058fe2d03b412dfc2d27a1e9b6adba86046dc4ab6cb8a`
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
# Fri, 25 Feb 2022 19:03:01 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:03:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:03:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:03:34 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:03:35 GMT
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
	-	`sha256:1f04ebe61f0f28bd5b0152200a2b2b391d70185963444625f748b1965b5cc3ed`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1636f5af837d6842067e5e608bfce498c31c97fac419e1f5d28f31033ca664`  
		Last Modified: Fri, 25 Feb 2022 19:09:06 GMT  
		Size: 88.0 MB (87996503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85d8041fbf13d2aec88efee1942f6ab98624568e4cfcb05b55384b27d7b51c`  
		Last Modified: Fri, 25 Feb 2022 19:08:49 GMT  
		Size: 3.5 KB (3460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6007a391685787b262bb862b952fead864d6d88545870ffad22a6032836a5a`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 6.6 KB (6594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:098d91b0041466955595fca80dd126f256c67acd8afcaf48fb9871e9cd74812e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125189063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48d0c779281b4e5d291d34fcb2bc390e5990d8e6f89242e52db90c57b83409d`
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
# Fri, 25 Feb 2022 17:42:25 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:26 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:05:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:05:08 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:05:10 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:05:11 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:05:12 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:05:13 GMT
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
	-	`sha256:909ddc1e4a924d2fbfd551aeb58b73f53118882a59ae7b8b1292c0ab3bbc336f`  
		Last Modified: Fri, 25 Feb 2022 17:48:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a990ae0195fd38dd2247578a70d10f8fd0e422a886aa5a427ed1110e6fed3a`  
		Last Modified: Wed, 02 Mar 2022 20:10:39 GMT  
		Size: 87.1 MB (87109614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a12d88b36914fa06c21d2a213e88b4859bff8408107487553873e320010b62`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb95a55d81898a2cbb80e161e1fc84de0ba8d05132992d1e8b245e99df48815`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e82aba0ea4be9d0f6d7dacb3ad30138bc33f5dd983091dca3b790a9fc982d11f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138776390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f14b3a6a4ea1d8ea5a60e0ebfdcb360fb25f496f9709c588f73a0729177493`
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
# Fri, 25 Feb 2022 19:29:58 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:04 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:30:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:33:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:33:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:33:39 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:33:41 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:33:49 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:33:53 GMT
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
	-	`sha256:020f2977da1a5f3d6b9c778925ec00264ff32a5ca6aa55d127022a97cf18e78b`  
		Last Modified: Fri, 25 Feb 2022 19:55:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fb0583306c8d7f2fa7145ed3190266e0395a5ff420d88ca12a8349206eb672`  
		Last Modified: Wed, 02 Mar 2022 18:47:29 GMT  
		Size: 92.6 MB (92567371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f7a1f84d9bfcc4985c53c9293be6fa5d3a87271362f6af0325ed2b40cdfa9f`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea41f65e9a276cf3eb4c9803b1554a07a571e761da5e3be09b3ac302deb5d191`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b25ec596e0b803d6fd988c0c7e16ecebc61e95f7f3c269b23fbe7a8f0309d1d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127234688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ee365d07d56d63dd1b1af874006dd9cadbdcc94248873e42cfd7b92d4d9007`
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
# Fri, 25 Feb 2022 17:43:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:43:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:43:32 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:43:32 GMT
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
	-	`sha256:09bbeaa7740ccfdc136df7f83f134c65c756afb9c4c1323685e6c5a09ea1bbe2`  
		Last Modified: Fri, 25 Feb 2022 17:46:25 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f23b45ea49fd398d929d4a4d79ed167bf5f4642dd044a62809e1f03bc78cb8`  
		Last Modified: Wed, 02 Mar 2022 17:46:30 GMT  
		Size: 89.3 MB (89290030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76afad66cec72e1af7009b464e97e49868d1944b5aaca12df54346021a984b99`  
		Last Modified: Wed, 02 Mar 2022 17:46:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0d15398e1a30ba8076ff1c63913f777e49309e7026a19aa50b8e1797a706e5`  
		Last Modified: Wed, 02 Mar 2022 17:46:18 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15`

```console
$ docker pull mariadb@sha256:cfe9dc35d3d37f43e0f4ec6d737387b320b83aafca96a4b889ac1e614a4689c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15` - linux; amd64

```console
$ docker pull mariadb@sha256:7485ec97845ab634ae5d20c6d77cf7e75074a5bf25fdc5fa43d56c02e276b13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127922535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de390e78f76e36b80d2058fe2d03b412dfc2d27a1e9b6adba86046dc4ab6cb8a`
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
# Fri, 25 Feb 2022 19:03:01 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:03:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:03:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:03:34 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:03:35 GMT
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
	-	`sha256:1f04ebe61f0f28bd5b0152200a2b2b391d70185963444625f748b1965b5cc3ed`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1636f5af837d6842067e5e608bfce498c31c97fac419e1f5d28f31033ca664`  
		Last Modified: Fri, 25 Feb 2022 19:09:06 GMT  
		Size: 88.0 MB (87996503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85d8041fbf13d2aec88efee1942f6ab98624568e4cfcb05b55384b27d7b51c`  
		Last Modified: Fri, 25 Feb 2022 19:08:49 GMT  
		Size: 3.5 KB (3460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6007a391685787b262bb862b952fead864d6d88545870ffad22a6032836a5a`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 6.6 KB (6594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:098d91b0041466955595fca80dd126f256c67acd8afcaf48fb9871e9cd74812e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125189063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48d0c779281b4e5d291d34fcb2bc390e5990d8e6f89242e52db90c57b83409d`
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
# Fri, 25 Feb 2022 17:42:25 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:26 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:05:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:05:08 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:05:10 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:05:11 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:05:12 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:05:13 GMT
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
	-	`sha256:909ddc1e4a924d2fbfd551aeb58b73f53118882a59ae7b8b1292c0ab3bbc336f`  
		Last Modified: Fri, 25 Feb 2022 17:48:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a990ae0195fd38dd2247578a70d10f8fd0e422a886aa5a427ed1110e6fed3a`  
		Last Modified: Wed, 02 Mar 2022 20:10:39 GMT  
		Size: 87.1 MB (87109614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a12d88b36914fa06c21d2a213e88b4859bff8408107487553873e320010b62`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb95a55d81898a2cbb80e161e1fc84de0ba8d05132992d1e8b245e99df48815`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e82aba0ea4be9d0f6d7dacb3ad30138bc33f5dd983091dca3b790a9fc982d11f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138776390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f14b3a6a4ea1d8ea5a60e0ebfdcb360fb25f496f9709c588f73a0729177493`
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
# Fri, 25 Feb 2022 19:29:58 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:04 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:30:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:33:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:33:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:33:39 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:33:41 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:33:49 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:33:53 GMT
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
	-	`sha256:020f2977da1a5f3d6b9c778925ec00264ff32a5ca6aa55d127022a97cf18e78b`  
		Last Modified: Fri, 25 Feb 2022 19:55:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fb0583306c8d7f2fa7145ed3190266e0395a5ff420d88ca12a8349206eb672`  
		Last Modified: Wed, 02 Mar 2022 18:47:29 GMT  
		Size: 92.6 MB (92567371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f7a1f84d9bfcc4985c53c9293be6fa5d3a87271362f6af0325ed2b40cdfa9f`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea41f65e9a276cf3eb4c9803b1554a07a571e761da5e3be09b3ac302deb5d191`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15` - linux; s390x

```console
$ docker pull mariadb@sha256:b25ec596e0b803d6fd988c0c7e16ecebc61e95f7f3c269b23fbe7a8f0309d1d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127234688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ee365d07d56d63dd1b1af874006dd9cadbdcc94248873e42cfd7b92d4d9007`
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
# Fri, 25 Feb 2022 17:43:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:43:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:43:32 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:43:32 GMT
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
	-	`sha256:09bbeaa7740ccfdc136df7f83f134c65c756afb9c4c1323685e6c5a09ea1bbe2`  
		Last Modified: Fri, 25 Feb 2022 17:46:25 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f23b45ea49fd398d929d4a4d79ed167bf5f4642dd044a62809e1f03bc78cb8`  
		Last Modified: Wed, 02 Mar 2022 17:46:30 GMT  
		Size: 89.3 MB (89290030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76afad66cec72e1af7009b464e97e49868d1944b5aaca12df54346021a984b99`  
		Last Modified: Wed, 02 Mar 2022 17:46:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0d15398e1a30ba8076ff1c63913f777e49309e7026a19aa50b8e1797a706e5`  
		Last Modified: Wed, 02 Mar 2022 17:46:18 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.15-focal`

```console
$ docker pull mariadb@sha256:cfe9dc35d3d37f43e0f4ec6d737387b320b83aafca96a4b889ac1e614a4689c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5.15-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7485ec97845ab634ae5d20c6d77cf7e75074a5bf25fdc5fa43d56c02e276b13b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127922535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de390e78f76e36b80d2058fe2d03b412dfc2d27a1e9b6adba86046dc4ab6cb8a`
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
# Fri, 25 Feb 2022 19:03:01 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:03:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:03:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:03:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:03:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:7b2b830b1a87b166f4a5a732707acff0251efb190222ea81169b87df1e30b0c1 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:03:34 GMT
COPY file:33a8142f1ef606149777b7c7100f497729a65097239aa974a0160afddf7b5c26 in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:03:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:03:34 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:03:35 GMT
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
	-	`sha256:1f04ebe61f0f28bd5b0152200a2b2b391d70185963444625f748b1965b5cc3ed`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1636f5af837d6842067e5e608bfce498c31c97fac419e1f5d28f31033ca664`  
		Last Modified: Fri, 25 Feb 2022 19:09:06 GMT  
		Size: 88.0 MB (87996503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db85d8041fbf13d2aec88efee1942f6ab98624568e4cfcb05b55384b27d7b51c`  
		Last Modified: Fri, 25 Feb 2022 19:08:49 GMT  
		Size: 3.5 KB (3460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6007a391685787b262bb862b952fead864d6d88545870ffad22a6032836a5a`  
		Last Modified: Fri, 25 Feb 2022 19:08:50 GMT  
		Size: 6.6 KB (6594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:098d91b0041466955595fca80dd126f256c67acd8afcaf48fb9871e9cd74812e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.2 MB (125189063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48d0c779281b4e5d291d34fcb2bc390e5990d8e6f89242e52db90c57b83409d`
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
# Fri, 25 Feb 2022 17:42:25 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:26 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:42:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:05:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:05:08 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:05:10 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:05:11 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:05:12 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:05:13 GMT
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
	-	`sha256:909ddc1e4a924d2fbfd551aeb58b73f53118882a59ae7b8b1292c0ab3bbc336f`  
		Last Modified: Fri, 25 Feb 2022 17:48:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a990ae0195fd38dd2247578a70d10f8fd0e422a886aa5a427ed1110e6fed3a`  
		Last Modified: Wed, 02 Mar 2022 20:10:39 GMT  
		Size: 87.1 MB (87109614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a12d88b36914fa06c21d2a213e88b4859bff8408107487553873e320010b62`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb95a55d81898a2cbb80e161e1fc84de0ba8d05132992d1e8b245e99df48815`  
		Last Modified: Wed, 02 Mar 2022 20:10:25 GMT  
		Size: 6.6 KB (6605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e82aba0ea4be9d0f6d7dacb3ad30138bc33f5dd983091dca3b790a9fc982d11f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138776390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72f14b3a6a4ea1d8ea5a60e0ebfdcb360fb25f496f9709c588f73a0729177493`
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
# Fri, 25 Feb 2022 19:29:58 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:04 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 19:30:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:30:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:33:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:33:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:33:39 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:33:41 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:33:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:33:49 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:33:53 GMT
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
	-	`sha256:020f2977da1a5f3d6b9c778925ec00264ff32a5ca6aa55d127022a97cf18e78b`  
		Last Modified: Fri, 25 Feb 2022 19:55:25 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fb0583306c8d7f2fa7145ed3190266e0395a5ff420d88ca12a8349206eb672`  
		Last Modified: Wed, 02 Mar 2022 18:47:29 GMT  
		Size: 92.6 MB (92567371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f7a1f84d9bfcc4985c53c9293be6fa5d3a87271362f6af0325ed2b40cdfa9f`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 3.5 KB (3498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea41f65e9a276cf3eb4c9803b1554a07a571e761da5e3be09b3ac302deb5d191`  
		Last Modified: Wed, 02 Mar 2022 18:47:11 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5.15-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:b25ec596e0b803d6fd988c0c7e16ecebc61e95f7f3c269b23fbe7a8f0309d1d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127234688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1ee365d07d56d63dd1b1af874006dd9cadbdcc94248873e42cfd7b92d4d9007`
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
# Fri, 25 Feb 2022 17:43:40 GMT
ARG MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ENV MARIADB_VERSION=1:10.5.15+maria~focal
# Fri, 25 Feb 2022 17:43:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:43:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.15/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:43:31 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:ce532f6a17eccaa5fe9b3ea2a12e11efb381940167405d65a5d17184d08c3e52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:43:31 GMT
COPY file:05f3e2611ebac993f6f8674a52f9b7cf554603c70791f023bb7786ec99a3e34d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:43:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:43:32 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:43:32 GMT
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
	-	`sha256:09bbeaa7740ccfdc136df7f83f134c65c756afb9c4c1323685e6c5a09ea1bbe2`  
		Last Modified: Fri, 25 Feb 2022 17:46:25 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f23b45ea49fd398d929d4a4d79ed167bf5f4642dd044a62809e1f03bc78cb8`  
		Last Modified: Wed, 02 Mar 2022 17:46:30 GMT  
		Size: 89.3 MB (89290030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76afad66cec72e1af7009b464e97e49868d1944b5aaca12df54346021a984b99`  
		Last Modified: Wed, 02 Mar 2022 17:46:19 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0d15398e1a30ba8076ff1c63913f777e49309e7026a19aa50b8e1797a706e5`  
		Last Modified: Wed, 02 Mar 2022 17:46:18 GMT  
		Size: 6.6 KB (6607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:485ee60b8a352d929c0b0c0288c67ece4a917bd9e866fe03a90c0bb66fb5c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:008e0a5cd570889de96550f509a6a7a0cac1dbbf7e94265f5de497b45de97a1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca1bb790d953c74b114c4ff3b7b5bdad99850bee6e9490e087c3abc57406d82`
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
# Fri, 25 Feb 2022 19:02:20 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:02:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:56 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:57 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:57 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:57 GMT
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
	-	`sha256:2d4becccd3dd4bfdd537199df53c49d74271a594ce337d1995892367406caf71`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73da7c2ac5af5a9e3ba4bafa57276a54b5b51db2f48e9b4098d6fc542e7cef17`  
		Last Modified: Fri, 25 Feb 2022 19:08:33 GMT  
		Size: 88.2 MB (88243453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31163609685e6a5f3a3a18b64e38c1ac6a938f373308b6bf346e7abc80a3f157`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9162f300b21308a5df5bb223206f4e2f3d2e251c179c6be1defdce49b111602`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:44365014d5968c4ad0803ec964894fc8bd47c3eeaef8b014346f20d98b0edee0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36946765a995615560387171980e4e752de619c07e8b9be84b38089af26baf2`
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
# Fri, 25 Feb 2022 17:41:40 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:41 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:04:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:04:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:04:26 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:04:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:04:28 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:04:29 GMT
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
	-	`sha256:38d49800d26cc57960935b2b51c925d67989ccf5ea2e6cb9efdaada4c97de7fe`  
		Last Modified: Fri, 25 Feb 2022 17:47:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e61850d918e98bced3aedafd82da8360d4f195c3dc6a37dc24f527592c8eae3`  
		Last Modified: Wed, 02 Mar 2022 20:10:06 GMT  
		Size: 87.2 MB (87193241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d48a91f7d1d09d13206030cabebdf46edd7272cccd03b3faea162f14f68c8`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93895696e7f8280488ab83add55a5490b875ffcfd74e6b88af049def637f829`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:002243c42428658209235c684778c07ff1ed7038ed81f0b7dd1f970f933db42b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138836717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9faf02d477b86a4da15e365b76495897532f8074d12b45fc72e44fd03a649c`
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
# Fri, 25 Feb 2022 19:23:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:55 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:24:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:30:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:30:47 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:30:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:30:55 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:30:59 GMT
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
	-	`sha256:b0b2f3f3831ed822254a50dffd4da0f4742ef24ef8aa237534f66d93a1353048`  
		Last Modified: Fri, 25 Feb 2022 19:54:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6f79393505277876635158e6e99d6354be90d2f605960102d22a7b33e453f`  
		Last Modified: Wed, 02 Mar 2022 18:46:50 GMT  
		Size: 92.6 MB (92627694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1e062e60b0d5644e22f9512c6647a326413d22e3dacecf5e8c9b30bf8ae0bb`  
		Last Modified: Wed, 02 Mar 2022 18:46:33 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefcf7dc1d8a9a1d1bb6cb4342a5931cc1583b85dd62f2a335da42e1ce2bd1a`  
		Last Modified: Wed, 02 Mar 2022 18:46:32 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:12c87b8b2be084e98a50c460d4a401255e6df5c8a7b131aa0cecc27995a4d4d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab19b1c239eea2d425f343ed9cf545364c6dfb73bdada08af40e8194694fe759`
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
# Fri, 25 Feb 2022 17:43:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:59 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:59 GMT
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
	-	`sha256:124a747d11e0921bbf0eb728acae7edcd82997ff2e2f55fad0a6b88090a5e914`  
		Last Modified: Fri, 25 Feb 2022 17:45:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d9592f7c460865cb2ae2b2014c550e08c2ca52a0bba8846724800f64b5d865`  
		Last Modified: Wed, 02 Mar 2022 17:46:06 GMT  
		Size: 89.3 MB (89316243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f4239b83972fde168dd18e9c890a85b5d81044ce59cb5b556fe6d6c1794ca`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efc49cd126a59bf4414c3fad9b89f125639f22b07a9ad9b95c746d65df03024`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:485ee60b8a352d929c0b0c0288c67ece4a917bd9e866fe03a90c0bb66fb5c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:008e0a5cd570889de96550f509a6a7a0cac1dbbf7e94265f5de497b45de97a1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca1bb790d953c74b114c4ff3b7b5bdad99850bee6e9490e087c3abc57406d82`
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
# Fri, 25 Feb 2022 19:02:20 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:02:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:56 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:57 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:57 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:57 GMT
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
	-	`sha256:2d4becccd3dd4bfdd537199df53c49d74271a594ce337d1995892367406caf71`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73da7c2ac5af5a9e3ba4bafa57276a54b5b51db2f48e9b4098d6fc542e7cef17`  
		Last Modified: Fri, 25 Feb 2022 19:08:33 GMT  
		Size: 88.2 MB (88243453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31163609685e6a5f3a3a18b64e38c1ac6a938f373308b6bf346e7abc80a3f157`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9162f300b21308a5df5bb223206f4e2f3d2e251c179c6be1defdce49b111602`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:44365014d5968c4ad0803ec964894fc8bd47c3eeaef8b014346f20d98b0edee0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36946765a995615560387171980e4e752de619c07e8b9be84b38089af26baf2`
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
# Fri, 25 Feb 2022 17:41:40 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:41 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:04:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:04:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:04:26 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:04:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:04:28 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:04:29 GMT
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
	-	`sha256:38d49800d26cc57960935b2b51c925d67989ccf5ea2e6cb9efdaada4c97de7fe`  
		Last Modified: Fri, 25 Feb 2022 17:47:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e61850d918e98bced3aedafd82da8360d4f195c3dc6a37dc24f527592c8eae3`  
		Last Modified: Wed, 02 Mar 2022 20:10:06 GMT  
		Size: 87.2 MB (87193241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d48a91f7d1d09d13206030cabebdf46edd7272cccd03b3faea162f14f68c8`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93895696e7f8280488ab83add55a5490b875ffcfd74e6b88af049def637f829`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:002243c42428658209235c684778c07ff1ed7038ed81f0b7dd1f970f933db42b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138836717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9faf02d477b86a4da15e365b76495897532f8074d12b45fc72e44fd03a649c`
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
# Fri, 25 Feb 2022 19:23:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:55 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:24:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:30:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:30:47 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:30:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:30:55 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:30:59 GMT
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
	-	`sha256:b0b2f3f3831ed822254a50dffd4da0f4742ef24ef8aa237534f66d93a1353048`  
		Last Modified: Fri, 25 Feb 2022 19:54:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6f79393505277876635158e6e99d6354be90d2f605960102d22a7b33e453f`  
		Last Modified: Wed, 02 Mar 2022 18:46:50 GMT  
		Size: 92.6 MB (92627694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1e062e60b0d5644e22f9512c6647a326413d22e3dacecf5e8c9b30bf8ae0bb`  
		Last Modified: Wed, 02 Mar 2022 18:46:33 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefcf7dc1d8a9a1d1bb6cb4342a5931cc1583b85dd62f2a335da42e1ce2bd1a`  
		Last Modified: Wed, 02 Mar 2022 18:46:32 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:12c87b8b2be084e98a50c460d4a401255e6df5c8a7b131aa0cecc27995a4d4d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab19b1c239eea2d425f343ed9cf545364c6dfb73bdada08af40e8194694fe759`
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
# Fri, 25 Feb 2022 17:43:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:59 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:59 GMT
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
	-	`sha256:124a747d11e0921bbf0eb728acae7edcd82997ff2e2f55fad0a6b88090a5e914`  
		Last Modified: Fri, 25 Feb 2022 17:45:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d9592f7c460865cb2ae2b2014c550e08c2ca52a0bba8846724800f64b5d865`  
		Last Modified: Wed, 02 Mar 2022 17:46:06 GMT  
		Size: 89.3 MB (89316243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f4239b83972fde168dd18e9c890a85b5d81044ce59cb5b556fe6d6c1794ca`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efc49cd126a59bf4414c3fad9b89f125639f22b07a9ad9b95c746d65df03024`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7`

```console
$ docker pull mariadb@sha256:485ee60b8a352d929c0b0c0288c67ece4a917bd9e866fe03a90c0bb66fb5c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7` - linux; amd64

```console
$ docker pull mariadb@sha256:008e0a5cd570889de96550f509a6a7a0cac1dbbf7e94265f5de497b45de97a1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca1bb790d953c74b114c4ff3b7b5bdad99850bee6e9490e087c3abc57406d82`
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
# Fri, 25 Feb 2022 19:02:20 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:02:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:56 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:57 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:57 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:57 GMT
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
	-	`sha256:2d4becccd3dd4bfdd537199df53c49d74271a594ce337d1995892367406caf71`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73da7c2ac5af5a9e3ba4bafa57276a54b5b51db2f48e9b4098d6fc542e7cef17`  
		Last Modified: Fri, 25 Feb 2022 19:08:33 GMT  
		Size: 88.2 MB (88243453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31163609685e6a5f3a3a18b64e38c1ac6a938f373308b6bf346e7abc80a3f157`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9162f300b21308a5df5bb223206f4e2f3d2e251c179c6be1defdce49b111602`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:44365014d5968c4ad0803ec964894fc8bd47c3eeaef8b014346f20d98b0edee0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36946765a995615560387171980e4e752de619c07e8b9be84b38089af26baf2`
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
# Fri, 25 Feb 2022 17:41:40 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:41 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:04:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:04:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:04:26 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:04:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:04:28 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:04:29 GMT
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
	-	`sha256:38d49800d26cc57960935b2b51c925d67989ccf5ea2e6cb9efdaada4c97de7fe`  
		Last Modified: Fri, 25 Feb 2022 17:47:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e61850d918e98bced3aedafd82da8360d4f195c3dc6a37dc24f527592c8eae3`  
		Last Modified: Wed, 02 Mar 2022 20:10:06 GMT  
		Size: 87.2 MB (87193241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d48a91f7d1d09d13206030cabebdf46edd7272cccd03b3faea162f14f68c8`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93895696e7f8280488ab83add55a5490b875ffcfd74e6b88af049def637f829`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:002243c42428658209235c684778c07ff1ed7038ed81f0b7dd1f970f933db42b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138836717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9faf02d477b86a4da15e365b76495897532f8074d12b45fc72e44fd03a649c`
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
# Fri, 25 Feb 2022 19:23:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:55 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:24:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:30:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:30:47 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:30:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:30:55 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:30:59 GMT
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
	-	`sha256:b0b2f3f3831ed822254a50dffd4da0f4742ef24ef8aa237534f66d93a1353048`  
		Last Modified: Fri, 25 Feb 2022 19:54:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6f79393505277876635158e6e99d6354be90d2f605960102d22a7b33e453f`  
		Last Modified: Wed, 02 Mar 2022 18:46:50 GMT  
		Size: 92.6 MB (92627694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1e062e60b0d5644e22f9512c6647a326413d22e3dacecf5e8c9b30bf8ae0bb`  
		Last Modified: Wed, 02 Mar 2022 18:46:33 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefcf7dc1d8a9a1d1bb6cb4342a5931cc1583b85dd62f2a335da42e1ce2bd1a`  
		Last Modified: Wed, 02 Mar 2022 18:46:32 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7` - linux; s390x

```console
$ docker pull mariadb@sha256:12c87b8b2be084e98a50c460d4a401255e6df5c8a7b131aa0cecc27995a4d4d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab19b1c239eea2d425f343ed9cf545364c6dfb73bdada08af40e8194694fe759`
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
# Fri, 25 Feb 2022 17:43:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:59 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:59 GMT
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
	-	`sha256:124a747d11e0921bbf0eb728acae7edcd82997ff2e2f55fad0a6b88090a5e914`  
		Last Modified: Fri, 25 Feb 2022 17:45:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d9592f7c460865cb2ae2b2014c550e08c2ca52a0bba8846724800f64b5d865`  
		Last Modified: Wed, 02 Mar 2022 17:46:06 GMT  
		Size: 89.3 MB (89316243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f4239b83972fde168dd18e9c890a85b5d81044ce59cb5b556fe6d6c1794ca`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efc49cd126a59bf4414c3fad9b89f125639f22b07a9ad9b95c746d65df03024`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.7-focal`

```console
$ docker pull mariadb@sha256:485ee60b8a352d929c0b0c0288c67ece4a917bd9e866fe03a90c0bb66fb5c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:008e0a5cd570889de96550f509a6a7a0cac1dbbf7e94265f5de497b45de97a1c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128169486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca1bb790d953c74b114c4ff3b7b5bdad99850bee6e9490e087c3abc57406d82`
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
# Fri, 25 Feb 2022 19:02:20 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:02:20 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:02:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:56 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:57 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:57 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:57 GMT
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
	-	`sha256:2d4becccd3dd4bfdd537199df53c49d74271a594ce337d1995892367406caf71`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73da7c2ac5af5a9e3ba4bafa57276a54b5b51db2f48e9b4098d6fc542e7cef17`  
		Last Modified: Fri, 25 Feb 2022 19:08:33 GMT  
		Size: 88.2 MB (88243453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31163609685e6a5f3a3a18b64e38c1ac6a938f373308b6bf346e7abc80a3f157`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9162f300b21308a5df5bb223206f4e2f3d2e251c179c6be1defdce49b111602`  
		Last Modified: Fri, 25 Feb 2022 19:08:19 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:44365014d5968c4ad0803ec964894fc8bd47c3eeaef8b014346f20d98b0edee0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125272703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36946765a995615560387171980e4e752de619c07e8b9be84b38089af26baf2`
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
# Fri, 25 Feb 2022 17:41:40 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:41 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:41:42 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:04:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:04:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:04:26 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:04:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:04:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:04:28 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:04:29 GMT
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
	-	`sha256:38d49800d26cc57960935b2b51c925d67989ccf5ea2e6cb9efdaada4c97de7fe`  
		Last Modified: Fri, 25 Feb 2022 17:47:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e61850d918e98bced3aedafd82da8360d4f195c3dc6a37dc24f527592c8eae3`  
		Last Modified: Wed, 02 Mar 2022 20:10:06 GMT  
		Size: 87.2 MB (87193241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d48a91f7d1d09d13206030cabebdf46edd7272cccd03b3faea162f14f68c8`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93895696e7f8280488ab83add55a5490b875ffcfd74e6b88af049def637f829`  
		Last Modified: Wed, 02 Mar 2022 20:09:52 GMT  
		Size: 6.6 KB (6613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:002243c42428658209235c684778c07ff1ed7038ed81f0b7dd1f970f933db42b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138836717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9faf02d477b86a4da15e365b76495897532f8074d12b45fc72e44fd03a649c`
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
# Fri, 25 Feb 2022 19:23:48 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:55 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 19:23:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:24:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:30:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:30:44 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:30:47 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:30:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:30:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:30:55 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:30:59 GMT
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
	-	`sha256:b0b2f3f3831ed822254a50dffd4da0f4742ef24ef8aa237534f66d93a1353048`  
		Last Modified: Fri, 25 Feb 2022 19:54:44 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f6f79393505277876635158e6e99d6354be90d2f605960102d22a7b33e453f`  
		Last Modified: Wed, 02 Mar 2022 18:46:50 GMT  
		Size: 92.6 MB (92627694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1e062e60b0d5644e22f9512c6647a326413d22e3dacecf5e8c9b30bf8ae0bb`  
		Last Modified: Wed, 02 Mar 2022 18:46:33 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aefcf7dc1d8a9a1d1bb6cb4342a5931cc1583b85dd62f2a335da42e1ce2bd1a`  
		Last Modified: Wed, 02 Mar 2022 18:46:32 GMT  
		Size: 6.6 KB (6610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:12c87b8b2be084e98a50c460d4a401255e6df5c8a7b131aa0cecc27995a4d4d4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127260900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab19b1c239eea2d425f343ed9cf545364c6dfb73bdada08af40e8194694fe759`
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
# Fri, 25 Feb 2022 17:43:08 GMT
ARG MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ENV MARIADB_VERSION=1:10.6.7+maria~focal
# Fri, 25 Feb 2022 17:43:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:43:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:59 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:59 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:59 GMT
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
	-	`sha256:124a747d11e0921bbf0eb728acae7edcd82997ff2e2f55fad0a6b88090a5e914`  
		Last Modified: Fri, 25 Feb 2022 17:45:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d9592f7c460865cb2ae2b2014c550e08c2ca52a0bba8846724800f64b5d865`  
		Last Modified: Wed, 02 Mar 2022 17:46:06 GMT  
		Size: 89.3 MB (89316243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570f4239b83972fde168dd18e9c890a85b5d81044ce59cb5b556fe6d6c1794ca`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efc49cd126a59bf4414c3fad9b89f125639f22b07a9ad9b95c746d65df03024`  
		Last Modified: Wed, 02 Mar 2022 17:45:54 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.3-focal`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7.3-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc`

```console
$ docker pull mariadb@sha256:008c42c48ff22e48c175a67fa8ae2a151a69caf79e1230decc855070e9a6a971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:026e324f54887dab40d22949b5f6f051ffb86a3848fc2d02df9739276f1ddd04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7454273ba6cd5ccf7752257c51dfc1b6367d61f0dc3c20b74a6764dd844b0197`
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
# Fri, 25 Feb 2022 17:40:05 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:05 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:06 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:07 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:02:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:02:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:02:48 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:02:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:02:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:02:50 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:02:51 GMT
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
	-	`sha256:bf563ddfeccb077f605d11cb85db1f63dde8f511a61ac8c6b9068a3ceb696c5f`  
		Last Modified: Fri, 25 Feb 2022 17:46:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684251b0d4b843a4979f21582f0b2bc7e752b66a7670ce3beeb515134adce4e`  
		Last Modified: Wed, 02 Mar 2022 20:08:37 GMT  
		Size: 87.6 MB (87574394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a756ed4f092b5a775b5916e3c2931120dc8b709a6487b26d49efa97b34ef6e13`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8d244f7eb188652e672d46b6c1881ce43364dfa821c89af0af9f0731e288f2`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:75b669c5c0171075e6408de0355c116fce7f2125da921d2a96329c90c447a60f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139615214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a4e86f93aae474b1c90170aec68aaf46e91421019bdbd15991bc51750d3ce8`
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
# Fri, 25 Feb 2022 19:12:24 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:36 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:40 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:12:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:22:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:22:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:22:29 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:22:33 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:22:41 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:22:46 GMT
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
	-	`sha256:a14a5fccb8be7a86c2f4525978a4f9f4ec12c4668c23e02907143a1a13f41fd3`  
		Last Modified: Fri, 25 Feb 2022 19:52:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97de7c63e8b65ebc6161dd44854d101d1b6a48731d50d1f462328e8216e25a62`  
		Last Modified: Wed, 02 Mar 2022 18:45:12 GMT  
		Size: 93.4 MB (93406188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c540d3aa87926abffcbe15d7bf797855c9f7560a02689cf7cfddf6b54d1521`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1168cb102481cb0898255f629f8fa8c4ee972d85ecb77a5683328eeab0183`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:6d5e5320a0aa618ec5dfd67dd4d096ebd02610d597cf5e55172f9a31094c6bd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127724235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011528f6a3ddf75c93880ae76f4e9428935266c0d923a1b5bbdacedc5045340f`
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
# Fri, 25 Feb 2022 17:41:48 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:41:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:41:57 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:41:57 GMT
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
	-	`sha256:29fc756bd7cc38827f64e2e9271c3a39e72cb00a329f75cf8d122bbc8d3df32a`  
		Last Modified: Fri, 25 Feb 2022 17:44:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3626b93e3eeced20a043156752d4c8474ea24e106e5a8dd501c5a5d17863293`  
		Last Modified: Wed, 02 Mar 2022 17:44:33 GMT  
		Size: 89.8 MB (89779581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54db803b8b356e7e28e99f5af6bcc3a3bf77973ce5f03e99372d0ed56b083b`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4795142c10d1bab5cb02152eb534f253501667fc877638326a64113251331f`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-rc-focal`

```console
$ docker pull mariadb@sha256:008c42c48ff22e48c175a67fa8ae2a151a69caf79e1230decc855070e9a6a971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:026e324f54887dab40d22949b5f6f051ffb86a3848fc2d02df9739276f1ddd04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7454273ba6cd5ccf7752257c51dfc1b6367d61f0dc3c20b74a6764dd844b0197`
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
# Fri, 25 Feb 2022 17:40:05 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:05 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:06 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:07 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:02:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:02:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:02:48 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:02:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:02:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:02:50 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:02:51 GMT
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
	-	`sha256:bf563ddfeccb077f605d11cb85db1f63dde8f511a61ac8c6b9068a3ceb696c5f`  
		Last Modified: Fri, 25 Feb 2022 17:46:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684251b0d4b843a4979f21582f0b2bc7e752b66a7670ce3beeb515134adce4e`  
		Last Modified: Wed, 02 Mar 2022 20:08:37 GMT  
		Size: 87.6 MB (87574394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a756ed4f092b5a775b5916e3c2931120dc8b709a6487b26d49efa97b34ef6e13`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8d244f7eb188652e672d46b6c1881ce43364dfa821c89af0af9f0731e288f2`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:75b669c5c0171075e6408de0355c116fce7f2125da921d2a96329c90c447a60f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139615214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a4e86f93aae474b1c90170aec68aaf46e91421019bdbd15991bc51750d3ce8`
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
# Fri, 25 Feb 2022 19:12:24 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:36 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:40 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:12:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:22:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:22:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:22:29 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:22:33 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:22:41 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:22:46 GMT
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
	-	`sha256:a14a5fccb8be7a86c2f4525978a4f9f4ec12c4668c23e02907143a1a13f41fd3`  
		Last Modified: Fri, 25 Feb 2022 19:52:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97de7c63e8b65ebc6161dd44854d101d1b6a48731d50d1f462328e8216e25a62`  
		Last Modified: Wed, 02 Mar 2022 18:45:12 GMT  
		Size: 93.4 MB (93406188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c540d3aa87926abffcbe15d7bf797855c9f7560a02689cf7cfddf6b54d1521`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1168cb102481cb0898255f629f8fa8c4ee972d85ecb77a5683328eeab0183`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:6d5e5320a0aa618ec5dfd67dd4d096ebd02610d597cf5e55172f9a31094c6bd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127724235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011528f6a3ddf75c93880ae76f4e9428935266c0d923a1b5bbdacedc5045340f`
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
# Fri, 25 Feb 2022 17:41:48 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:41:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:41:57 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:41:57 GMT
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
	-	`sha256:29fc756bd7cc38827f64e2e9271c3a39e72cb00a329f75cf8d122bbc8d3df32a`  
		Last Modified: Fri, 25 Feb 2022 17:44:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3626b93e3eeced20a043156752d4c8474ea24e106e5a8dd501c5a5d17863293`  
		Last Modified: Wed, 02 Mar 2022 17:44:33 GMT  
		Size: 89.8 MB (89779581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54db803b8b356e7e28e99f5af6bcc3a3bf77973ce5f03e99372d0ed56b083b`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4795142c10d1bab5cb02152eb534f253501667fc877638326a64113251331f`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc`

```console
$ docker pull mariadb@sha256:008c42c48ff22e48c175a67fa8ae2a151a69caf79e1230decc855070e9a6a971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:026e324f54887dab40d22949b5f6f051ffb86a3848fc2d02df9739276f1ddd04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7454273ba6cd5ccf7752257c51dfc1b6367d61f0dc3c20b74a6764dd844b0197`
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
# Fri, 25 Feb 2022 17:40:05 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:05 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:06 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:07 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:02:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:02:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:02:48 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:02:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:02:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:02:50 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:02:51 GMT
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
	-	`sha256:bf563ddfeccb077f605d11cb85db1f63dde8f511a61ac8c6b9068a3ceb696c5f`  
		Last Modified: Fri, 25 Feb 2022 17:46:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684251b0d4b843a4979f21582f0b2bc7e752b66a7670ce3beeb515134adce4e`  
		Last Modified: Wed, 02 Mar 2022 20:08:37 GMT  
		Size: 87.6 MB (87574394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a756ed4f092b5a775b5916e3c2931120dc8b709a6487b26d49efa97b34ef6e13`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8d244f7eb188652e672d46b6c1881ce43364dfa821c89af0af9f0731e288f2`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:75b669c5c0171075e6408de0355c116fce7f2125da921d2a96329c90c447a60f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139615214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a4e86f93aae474b1c90170aec68aaf46e91421019bdbd15991bc51750d3ce8`
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
# Fri, 25 Feb 2022 19:12:24 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:36 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:40 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:12:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:22:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:22:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:22:29 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:22:33 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:22:41 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:22:46 GMT
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
	-	`sha256:a14a5fccb8be7a86c2f4525978a4f9f4ec12c4668c23e02907143a1a13f41fd3`  
		Last Modified: Fri, 25 Feb 2022 19:52:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97de7c63e8b65ebc6161dd44854d101d1b6a48731d50d1f462328e8216e25a62`  
		Last Modified: Wed, 02 Mar 2022 18:45:12 GMT  
		Size: 93.4 MB (93406188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c540d3aa87926abffcbe15d7bf797855c9f7560a02689cf7cfddf6b54d1521`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1168cb102481cb0898255f629f8fa8c4ee972d85ecb77a5683328eeab0183`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:6d5e5320a0aa618ec5dfd67dd4d096ebd02610d597cf5e55172f9a31094c6bd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127724235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011528f6a3ddf75c93880ae76f4e9428935266c0d923a1b5bbdacedc5045340f`
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
# Fri, 25 Feb 2022 17:41:48 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:41:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:41:57 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:41:57 GMT
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
	-	`sha256:29fc756bd7cc38827f64e2e9271c3a39e72cb00a329f75cf8d122bbc8d3df32a`  
		Last Modified: Fri, 25 Feb 2022 17:44:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3626b93e3eeced20a043156752d4c8474ea24e106e5a8dd501c5a5d17863293`  
		Last Modified: Wed, 02 Mar 2022 17:44:33 GMT  
		Size: 89.8 MB (89779581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54db803b8b356e7e28e99f5af6bcc3a3bf77973ce5f03e99372d0ed56b083b`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4795142c10d1bab5cb02152eb534f253501667fc877638326a64113251331f`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.2-rc-focal`

```console
$ docker pull mariadb@sha256:008c42c48ff22e48c175a67fa8ae2a151a69caf79e1230decc855070e9a6a971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8.2-rc-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:026e324f54887dab40d22949b5f6f051ffb86a3848fc2d02df9739276f1ddd04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125653854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7454273ba6cd5ccf7752257c51dfc1b6367d61f0dc3c20b74a6764dd844b0197`
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
# Fri, 25 Feb 2022 17:40:05 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:05 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:40:06 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:07 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:40:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:02:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:02:46 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:02:48 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:02:49 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:02:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:02:50 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:02:51 GMT
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
	-	`sha256:bf563ddfeccb077f605d11cb85db1f63dde8f511a61ac8c6b9068a3ceb696c5f`  
		Last Modified: Fri, 25 Feb 2022 17:46:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c684251b0d4b843a4979f21582f0b2bc7e752b66a7670ce3beeb515134adce4e`  
		Last Modified: Wed, 02 Mar 2022 20:08:37 GMT  
		Size: 87.6 MB (87574394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a756ed4f092b5a775b5916e3c2931120dc8b709a6487b26d49efa97b34ef6e13`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8d244f7eb188652e672d46b6c1881ce43364dfa821c89af0af9f0731e288f2`  
		Last Modified: Wed, 02 Mar 2022 20:08:23 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:75b669c5c0171075e6408de0355c116fce7f2125da921d2a96329c90c447a60f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139615214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a4e86f93aae474b1c90170aec68aaf46e91421019bdbd15991bc51750d3ce8`
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
# Fri, 25 Feb 2022 19:12:24 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:32 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 19:12:36 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:40 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 19:12:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:12:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:22:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:22:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:22:29 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:22:33 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:22:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:22:41 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:22:46 GMT
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
	-	`sha256:a14a5fccb8be7a86c2f4525978a4f9f4ec12c4668c23e02907143a1a13f41fd3`  
		Last Modified: Fri, 25 Feb 2022 19:52:19 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97de7c63e8b65ebc6161dd44854d101d1b6a48731d50d1f462328e8216e25a62`  
		Last Modified: Wed, 02 Mar 2022 18:45:12 GMT  
		Size: 93.4 MB (93406188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c540d3aa87926abffcbe15d7bf797855c9f7560a02689cf7cfddf6b54d1521`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e1168cb102481cb0898255f629f8fa8c4ee972d85ecb77a5683328eeab0183`  
		Last Modified: Wed, 02 Mar 2022 18:44:43 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8.2-rc-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:6d5e5320a0aa618ec5dfd67dd4d096ebd02610d597cf5e55172f9a31094c6bd7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127724235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011528f6a3ddf75c93880ae76f4e9428935266c0d923a1b5bbdacedc5045340f`
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
# Fri, 25 Feb 2022 17:41:48 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 25 Feb 2022 17:41:49 GMT
ARG MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ENV MARIADB_VERSION=1:10.8.2+maria~focal
# Fri, 25 Feb 2022 17:41:50 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:41:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:41:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.2/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:41:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:41:57 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:41:57 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:41:57 GMT
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
	-	`sha256:29fc756bd7cc38827f64e2e9271c3a39e72cb00a329f75cf8d122bbc8d3df32a`  
		Last Modified: Fri, 25 Feb 2022 17:44:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3626b93e3eeced20a043156752d4c8474ea24e106e5a8dd501c5a5d17863293`  
		Last Modified: Wed, 02 Mar 2022 17:44:33 GMT  
		Size: 89.8 MB (89779581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e54db803b8b356e7e28e99f5af6bcc3a3bf77973ce5f03e99372d0ed56b083b`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4795142c10d1bab5cb02152eb534f253501667fc877638326a64113251331f`  
		Last Modified: Wed, 02 Mar 2022 17:44:20 GMT  
		Size: 6.6 KB (6608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:focal`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:focal` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:focal` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:aa4387fa64770ef3b708315a4cb2a7f5525db9f6a24c7f4edbfefbc245c19ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:0fed5d91ed5beb07acfb64b268e29d4c958b2692cba3911c596d6021537e5149
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128668144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539871f8c20e7bf54159322bfe2b3c25eddb9f6ff61074c1ceeb42c9c81d96d2`
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
# Fri, 25 Feb 2022 19:01:39 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:01:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:01:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 25 Feb 2022 19:02:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Fri, 25 Feb 2022 19:02:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:f693e5845f70db80415072fbc1b9ad23eb585c105d71de03f85effee169e3220 in /usr/local/bin/healthcheck.sh 
# Fri, 25 Feb 2022 19:02:11 GMT
COPY file:d5d79d09980467bc2d89c305ca6c877b5500a08d8bfc8e1accc338acff89339f in /usr/local/bin/ 
# Fri, 25 Feb 2022 19:02:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Feb 2022 19:02:12 GMT
EXPOSE 3306
# Fri, 25 Feb 2022 19:02:12 GMT
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
	-	`sha256:caac2a47a26c1d5ac110c8c8160d78c46633c515fabc02aeead42a929abb3f34`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d95be4fc3ed23b3da3e0b23d8207ff984583950c9f475029a113d470656273`  
		Last Modified: Fri, 25 Feb 2022 19:07:50 GMT  
		Size: 88.7 MB (88742109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed1a87df3e4e40283a0f746897cbb88bfbd00077e0fa0548901288ab4bf7eee`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 3.5 KB (3456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323680a6eb6da7bb7518c7bc1e4ea7ed5ee8ae6d9743a0ab57b622438a3b788`  
		Last Modified: Fri, 25 Feb 2022 19:07:35 GMT  
		Size: 6.6 KB (6598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f8f8b3fd5a9f2440d17167b38c728afb10fea8ace09769ccea4785aa11802ba6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125722770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a88e4295a57632a79a1a00ca9b04360d1c62ddabbf24fd8cc1c4da991b02a`
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
# Fri, 25 Feb 2022 17:40:56 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:57 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:40:58 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 20:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 20:03:34 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 20:03:36 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 20:03:37 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 20:03:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 20:03:38 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 20:03:39 GMT
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
	-	`sha256:24d5701620936a9434a752e612b26e7ef401d732951312b4cb3ba8e0d56624b6`  
		Last Modified: Fri, 25 Feb 2022 17:46:45 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effa16dcf86a6585a2d1ab8bfed9b1d9a04e463c6f52dd029dab6b2ca1b5b239`  
		Last Modified: Wed, 02 Mar 2022 20:09:19 GMT  
		Size: 87.6 MB (87643307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329787a82e90dca9663551b3242410e1a6d58f8a38c67f27c75df37f5791c65e`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 3.5 KB (3500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d91f5f875e7fd1b8275629f31244a2668df92e00000ad0934630a5f9dba4fd`  
		Last Modified: Wed, 02 Mar 2022 20:09:05 GMT  
		Size: 6.6 KB (6614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2d5ca8d255b2eba980805a4b6a3acd0919232eb8c4bfef257bdb97ba129f23f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.5 MB (139532903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d21f98bb5e99f67ac12caae1bb51d56ad33e383e31f1dac9571e4ff80a3cc`
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
# Fri, 25 Feb 2022 19:18:25 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:28 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 19:18:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 19:18:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 18:26:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 18:26:37 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 18:26:40 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 18:26:42 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 18:26:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 18:26:56 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 18:27:00 GMT
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
	-	`sha256:db7481c2c4ac6a4a45dd245be97969eed2905194365236565671b1b00929aaaf`  
		Last Modified: Fri, 25 Feb 2022 19:53:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e251fefcbabaefff8050c654d270073db6cf3214c8972febd4c87cc7a6f05cbf`  
		Last Modified: Wed, 02 Mar 2022 18:45:53 GMT  
		Size: 93.3 MB (93323878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2fddcbc367e82db327f1c8e43fd49be8979275f2082869982ee1e5933d0c8d`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 3.5 KB (3499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f5f94d545bd8cd54a8bd18a63d830f2ec56b18649da85938bf043a2a83bc87`  
		Last Modified: Wed, 02 Mar 2022 18:45:34 GMT  
		Size: 6.6 KB (6612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:99b6ec2eb383d9a7cce5e22560678d3184383188a9155f80bba31b1b67c164de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127759683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89ea46720eabec42747028e6095b506954f158d76232d22e3c1b635eae4c28f`
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
# Fri, 25 Feb 2022 17:42:33 GMT
ARG MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ENV MARIADB_VERSION=1:10.7.3+maria~focal
# Fri, 25 Feb 2022 17:42:33 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
# Fri, 25 Feb 2022 17:42:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Mar 2022 17:42:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.3/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" 		mariadb-backup 		socat 	; 	sed --follow-symlinks -i -e 's/--loose-disable-plugin-file-key-management//' /usr/bin/mysql_install_db ; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Mar 2022 17:42:27 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:0fba56e5dc10e3c33d13bb50fb484703f651fc83023b8cb76587db8c1c297e7f in /usr/local/bin/healthcheck.sh 
# Wed, 02 Mar 2022 17:42:27 GMT
COPY file:b8e07732c3935e7f1f06d41cbbc3bb55a1dfe7cc9488afc1861b4cc1537a564d in /usr/local/bin/ 
# Wed, 02 Mar 2022 17:42:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Mar 2022 17:42:27 GMT
EXPOSE 3306
# Wed, 02 Mar 2022 17:42:27 GMT
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
	-	`sha256:702f91bfef0abb95f814177f9a921283357b4afaa60cdb435acb8fe7a1402906`  
		Last Modified: Fri, 25 Feb 2022 17:45:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6036789322b3acd83fa92130309b4fc9c6a8c25d36111e3afa4f0f71514bf3e`  
		Last Modified: Wed, 02 Mar 2022 17:45:21 GMT  
		Size: 89.8 MB (89815024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0a3604a36169ae6d4ad755169b3aa3e12576a460dc593f618ed42e5d93cdbc`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae0c5e939e869a31f1e13b7a81f76d6133b715802728018c9a69cd587b0fc74`  
		Last Modified: Wed, 02 Mar 2022 17:45:09 GMT  
		Size: 6.6 KB (6611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
