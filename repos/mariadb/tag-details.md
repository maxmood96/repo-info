<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mariadb`

-	[`mariadb:10`](#mariadb10)
-	[`mariadb:10-jammy`](#mariadb10-jammy)
-	[`mariadb:10.10-rc`](#mariadb1010-rc)
-	[`mariadb:10.10-rc-jammy`](#mariadb1010-rc-jammy)
-	[`mariadb:10.10.1-rc`](#mariadb10101-rc)
-	[`mariadb:10.10.1-rc-jammy`](#mariadb10101-rc-jammy)
-	[`mariadb:10.3`](#mariadb103)
-	[`mariadb:10.3-focal`](#mariadb103-focal)
-	[`mariadb:10.3.37`](#mariadb10337)
-	[`mariadb:10.3.37-focal`](#mariadb10337-focal)
-	[`mariadb:10.4`](#mariadb104)
-	[`mariadb:10.4-focal`](#mariadb104-focal)
-	[`mariadb:10.4.27`](#mariadb10427)
-	[`mariadb:10.4.27-focal`](#mariadb10427-focal)
-	[`mariadb:10.5`](#mariadb105)
-	[`mariadb:10.5-focal`](#mariadb105-focal)
-	[`mariadb:10.5.18`](#mariadb10518)
-	[`mariadb:10.5.18-focal`](#mariadb10518-focal)
-	[`mariadb:10.6`](#mariadb106)
-	[`mariadb:10.6-focal`](#mariadb106-focal)
-	[`mariadb:10.6.11`](#mariadb10611)
-	[`mariadb:10.6.11-focal`](#mariadb10611-focal)
-	[`mariadb:10.7`](#mariadb107)
-	[`mariadb:10.7-focal`](#mariadb107-focal)
-	[`mariadb:10.7.7`](#mariadb1077)
-	[`mariadb:10.7.7-focal`](#mariadb1077-focal)
-	[`mariadb:10.8`](#mariadb108)
-	[`mariadb:10.8-jammy`](#mariadb108-jammy)
-	[`mariadb:10.8.6`](#mariadb1086)
-	[`mariadb:10.8.6-jammy`](#mariadb1086-jammy)
-	[`mariadb:10.9`](#mariadb109)
-	[`mariadb:10.9-jammy`](#mariadb109-jammy)
-	[`mariadb:10.9.4`](#mariadb1094)
-	[`mariadb:10.9.4-jammy`](#mariadb1094-jammy)
-	[`mariadb:jammy`](#mariadbjammy)
-	[`mariadb:latest`](#mariadblatest)

## `mariadb:10`

```console
$ docker pull mariadb@sha256:eeb8e0dd5043b82dccaadd366c17b37e73802f0a508a77d877d1bbfa7084989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31f677ba9b50beef8d48a3bbcab29485f5aa3a90677d1ebc44039bbc9bc8bde4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118604917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe889c390f208ce09bf8bfa7869b7d342d999c4279a8809e3a2d2a14332cf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:36 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:08:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:55 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:55 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5452b6a0ce3706d857279cfa1cdaef7c8b6bc76d8d6a4b1c43367203b766cd2f`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628f7ef3cedd084f9a47495aa153853592da56561a6e3231a78435d95ff9949`  
		Last Modified: Wed, 02 Nov 2022 20:10:44 GMT  
		Size: 82.4 MB (82378919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e903661ffaca59211d235a8061c23cc51afe2459c91999d6e191b263897d86d0`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ecec752f0246a09512597065787135cfb39650e56b627521d6b7a25b44bec`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; ppc64le

```console
$ docker pull mariadb@sha256:986c35ba43c2850b7911d84081331f918000e38549e853630add39e459d49f28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117016669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e47acd883e8abe5eff966b7822646acd0bed0c6a192953367a3f79b231e3b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:14:08 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:14:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:14:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:14:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:59 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:59 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c2e50062f28f25572934e1354be67087ba900f512bdaad143946434e750a18`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba9ea9acad2d162a2570367cc2f21af52c0b3e528d239dd2d8af13c327724ad`  
		Last Modified: Wed, 02 Nov 2022 19:18:49 GMT  
		Size: 72.5 MB (72480320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd098559b30b498d64f7740fcf0fe3bdd0372711b2d118558adf7b2cc0f7a9`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7613b448a79282dac8e97b54a740faeda580f7c7410e3ddaef69d39f3f1e995a`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10` - linux; s390x

```console
$ docker pull mariadb@sha256:18498ac00e522618f92dc59b38e9e956ceecbbdd98523c622dd07f0c13d83c2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105142329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba90c3535e8905fd0a9e8b72aa707eafe97c2d0ee6d23f3142013b50b8860e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:59 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:28:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:28:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:28:36 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:28:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89802ca4242938a62ea9e93dcc84679d6208be5a8ef8a7dbf368c196ddafc596`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b10a0c4c56eda5ee314ee192394ab23400a90fcf6536a7fa5eec78854ac46a`  
		Last Modified: Wed, 02 Nov 2022 19:31:40 GMT  
		Size: 68.7 MB (68655104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b25788d86165ab3008742f36bd0cd6bfb36679d1928144085e0b200ae38a9d`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4f3538ccb9ee39af5e436a70e5c49fcb1724dead6cb95f3c0aa7942a62c12`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:eeb8e0dd5043b82dccaadd366c17b37e73802f0a508a77d877d1bbfa7084989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31f677ba9b50beef8d48a3bbcab29485f5aa3a90677d1ebc44039bbc9bc8bde4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118604917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe889c390f208ce09bf8bfa7869b7d342d999c4279a8809e3a2d2a14332cf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:36 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:08:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:55 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:55 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5452b6a0ce3706d857279cfa1cdaef7c8b6bc76d8d6a4b1c43367203b766cd2f`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628f7ef3cedd084f9a47495aa153853592da56561a6e3231a78435d95ff9949`  
		Last Modified: Wed, 02 Nov 2022 20:10:44 GMT  
		Size: 82.4 MB (82378919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e903661ffaca59211d235a8061c23cc51afe2459c91999d6e191b263897d86d0`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ecec752f0246a09512597065787135cfb39650e56b627521d6b7a25b44bec`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:986c35ba43c2850b7911d84081331f918000e38549e853630add39e459d49f28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117016669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e47acd883e8abe5eff966b7822646acd0bed0c6a192953367a3f79b231e3b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:14:08 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:14:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:14:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:14:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:59 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:59 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c2e50062f28f25572934e1354be67087ba900f512bdaad143946434e750a18`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba9ea9acad2d162a2570367cc2f21af52c0b3e528d239dd2d8af13c327724ad`  
		Last Modified: Wed, 02 Nov 2022 19:18:49 GMT  
		Size: 72.5 MB (72480320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd098559b30b498d64f7740fcf0fe3bdd0372711b2d118558adf7b2cc0f7a9`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7613b448a79282dac8e97b54a740faeda580f7c7410e3ddaef69d39f3f1e995a`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:18498ac00e522618f92dc59b38e9e956ceecbbdd98523c622dd07f0c13d83c2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105142329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba90c3535e8905fd0a9e8b72aa707eafe97c2d0ee6d23f3142013b50b8860e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:59 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:28:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:28:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:28:36 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:28:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89802ca4242938a62ea9e93dcc84679d6208be5a8ef8a7dbf368c196ddafc596`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b10a0c4c56eda5ee314ee192394ab23400a90fcf6536a7fa5eec78854ac46a`  
		Last Modified: Wed, 02 Nov 2022 19:31:40 GMT  
		Size: 68.7 MB (68655104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b25788d86165ab3008742f36bd0cd6bfb36679d1928144085e0b200ae38a9d`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4f3538ccb9ee39af5e436a70e5c49fcb1724dead6cb95f3c0aa7942a62c12`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10-rc`

```console
$ docker pull mariadb@sha256:e37adecf4da3e44a40412422cb19dc0c2776eb16481b2273a757e9207adc9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:a3b14c15225b4788b562d48f1910ba34eeb4282d3ca62f0db3d2bf4db4621144
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125335699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57de3e4d4a4748bd9f256af1c8adae44736c8aaece6f7137449c6186da2ec20f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:48:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.10.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:48:17 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:48:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:50:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:50:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:25990863e4bd169447bf1d169dbaf3eeaf1299650f69524839fe736dc4358be0 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:50:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:50:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:50:49 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4e42c6b3fe74b8807bf126325d60167b163c7c5bd9ee0b7460cf9926995c66`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eff5b9b68025fd41eb88195a612cf7b369d1b72e362cc866379a52576b6c9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:44 GMT  
		Size: 89.4 MB (89368635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd587236afdff8a5bf7d9da2aeaee605fbe028289b1c2cb3bb60da87afd907a`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5532f5c0f6753ade67cf121ab73589101b07dbc713333a77c9f1ccdf55bba93`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 7.0 KB (7022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:963f93b32ec3cf17946c29f0fcc3a88fa3e9c938dc28840c0df410ae22c0eec3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104564191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10e5a505ae3328dff1184514c083e7d637f801fb9176dc3f8645070c1a394c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:07:53 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:26 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16759adaacc369b316e50cfb18576aea210022969ccdde95d0ae70cb4a0cffc3`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee076b67e8d0c5d62c7f7050a79ad3b8c0be044937447d244161f5bc46393e`  
		Last Modified: Wed, 02 Nov 2022 20:10:18 GMT  
		Size: 68.3 MB (68338186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062fe35f14777880e0fe5635d6e44b97fd9656588003d18fa32f537d2022c606`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966f81b6128476aa69662040adf0f309bd0cd1e7040b7204a13f8cc59a2087af`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:df1026fab4d879c7dae98410339d4f5ff07342d07d87c4698d485ebc7099053b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118852132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f0a1c07c4033de9f42110f5c28f420a4abef95e07ccc06315ceab2ab8e4ccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:13:01 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:01 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:13:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:13:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:13:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:01 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:14:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5152e5d64618b6b05d2684f989764bf203439e2a1cf9fbee8496dea67faa718c`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c01fd63c6f9cc57f6c9d18a1a809f00b33f1f598cf16ea1a93bc8a887a4db19`  
		Last Modified: Wed, 02 Nov 2022 19:18:08 GMT  
		Size: 74.3 MB (74315786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a9db4181ee8f82faa3d1e743e165e793b2ff980cf27a0de82608852b6722e4`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f0d37882dfdd3e15826bf4df89eff73d8f24a63f4d427f1580142d362daef`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:36070d4d060760a4c24219b8aface95df237e72a55f85591deb2d18ea49aa9d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107294477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea92a04f6d3b13eed882dd2defa6d9efc616145041230abe131e6d08f5d2f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:05 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:27:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:27:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:27:50 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:27:51 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:27:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae554b3bf685c681cb82869aad08ce1b8a102dbcc48076cb8a1d4c2000b9549`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6a1b98c8a014695b96e24a86ddfff8f0066dc616dc1be787a55fef437f27b`  
		Last Modified: Wed, 02 Nov 2022 19:31:15 GMT  
		Size: 70.8 MB (70807254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0346caab6232f6cffc3c727baac14a7898defc7d18ef606a70d844247c245a`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88753d7dcc3c5f63b9d7ac2f2b4f0e50ce37b962bf0cee353927a2f3f7b90c6f`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10-rc-jammy`

```console
$ docker pull mariadb@sha256:e37adecf4da3e44a40412422cb19dc0c2776eb16481b2273a757e9207adc9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10-rc-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:a3b14c15225b4788b562d48f1910ba34eeb4282d3ca62f0db3d2bf4db4621144
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125335699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57de3e4d4a4748bd9f256af1c8adae44736c8aaece6f7137449c6186da2ec20f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:48:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.10.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:48:17 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:48:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:50:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:50:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:25990863e4bd169447bf1d169dbaf3eeaf1299650f69524839fe736dc4358be0 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:50:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:50:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:50:49 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4e42c6b3fe74b8807bf126325d60167b163c7c5bd9ee0b7460cf9926995c66`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eff5b9b68025fd41eb88195a612cf7b369d1b72e362cc866379a52576b6c9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:44 GMT  
		Size: 89.4 MB (89368635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd587236afdff8a5bf7d9da2aeaee605fbe028289b1c2cb3bb60da87afd907a`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5532f5c0f6753ade67cf121ab73589101b07dbc713333a77c9f1ccdf55bba93`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 7.0 KB (7022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:963f93b32ec3cf17946c29f0fcc3a88fa3e9c938dc28840c0df410ae22c0eec3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104564191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10e5a505ae3328dff1184514c083e7d637f801fb9176dc3f8645070c1a394c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:07:53 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:26 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16759adaacc369b316e50cfb18576aea210022969ccdde95d0ae70cb4a0cffc3`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee076b67e8d0c5d62c7f7050a79ad3b8c0be044937447d244161f5bc46393e`  
		Last Modified: Wed, 02 Nov 2022 20:10:18 GMT  
		Size: 68.3 MB (68338186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062fe35f14777880e0fe5635d6e44b97fd9656588003d18fa32f537d2022c606`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966f81b6128476aa69662040adf0f309bd0cd1e7040b7204a13f8cc59a2087af`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:df1026fab4d879c7dae98410339d4f5ff07342d07d87c4698d485ebc7099053b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118852132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f0a1c07c4033de9f42110f5c28f420a4abef95e07ccc06315ceab2ab8e4ccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:13:01 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:01 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:13:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:13:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:13:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:01 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:14:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5152e5d64618b6b05d2684f989764bf203439e2a1cf9fbee8496dea67faa718c`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c01fd63c6f9cc57f6c9d18a1a809f00b33f1f598cf16ea1a93bc8a887a4db19`  
		Last Modified: Wed, 02 Nov 2022 19:18:08 GMT  
		Size: 74.3 MB (74315786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a9db4181ee8f82faa3d1e743e165e793b2ff980cf27a0de82608852b6722e4`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f0d37882dfdd3e15826bf4df89eff73d8f24a63f4d427f1580142d362daef`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10-rc-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:36070d4d060760a4c24219b8aface95df237e72a55f85591deb2d18ea49aa9d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107294477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea92a04f6d3b13eed882dd2defa6d9efc616145041230abe131e6d08f5d2f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:05 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:27:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:27:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:27:50 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:27:51 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:27:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae554b3bf685c681cb82869aad08ce1b8a102dbcc48076cb8a1d4c2000b9549`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6a1b98c8a014695b96e24a86ddfff8f0066dc616dc1be787a55fef437f27b`  
		Last Modified: Wed, 02 Nov 2022 19:31:15 GMT  
		Size: 70.8 MB (70807254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0346caab6232f6cffc3c727baac14a7898defc7d18ef606a70d844247c245a`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88753d7dcc3c5f63b9d7ac2f2b4f0e50ce37b962bf0cee353927a2f3f7b90c6f`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10.1-rc`

```console
$ docker pull mariadb@sha256:e37adecf4da3e44a40412422cb19dc0c2776eb16481b2273a757e9207adc9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10.1-rc` - linux; amd64

```console
$ docker pull mariadb@sha256:a3b14c15225b4788b562d48f1910ba34eeb4282d3ca62f0db3d2bf4db4621144
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125335699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57de3e4d4a4748bd9f256af1c8adae44736c8aaece6f7137449c6186da2ec20f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:48:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.10.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:48:17 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:48:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:50:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:50:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:25990863e4bd169447bf1d169dbaf3eeaf1299650f69524839fe736dc4358be0 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:50:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:50:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:50:49 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4e42c6b3fe74b8807bf126325d60167b163c7c5bd9ee0b7460cf9926995c66`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eff5b9b68025fd41eb88195a612cf7b369d1b72e362cc866379a52576b6c9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:44 GMT  
		Size: 89.4 MB (89368635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd587236afdff8a5bf7d9da2aeaee605fbe028289b1c2cb3bb60da87afd907a`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5532f5c0f6753ade67cf121ab73589101b07dbc713333a77c9f1ccdf55bba93`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 7.0 KB (7022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:963f93b32ec3cf17946c29f0fcc3a88fa3e9c938dc28840c0df410ae22c0eec3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104564191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10e5a505ae3328dff1184514c083e7d637f801fb9176dc3f8645070c1a394c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:07:53 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:26 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16759adaacc369b316e50cfb18576aea210022969ccdde95d0ae70cb4a0cffc3`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee076b67e8d0c5d62c7f7050a79ad3b8c0be044937447d244161f5bc46393e`  
		Last Modified: Wed, 02 Nov 2022 20:10:18 GMT  
		Size: 68.3 MB (68338186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062fe35f14777880e0fe5635d6e44b97fd9656588003d18fa32f537d2022c606`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966f81b6128476aa69662040adf0f309bd0cd1e7040b7204a13f8cc59a2087af`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc` - linux; ppc64le

```console
$ docker pull mariadb@sha256:df1026fab4d879c7dae98410339d4f5ff07342d07d87c4698d485ebc7099053b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118852132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f0a1c07c4033de9f42110f5c28f420a4abef95e07ccc06315ceab2ab8e4ccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:13:01 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:01 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:13:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:13:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:13:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:01 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:14:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5152e5d64618b6b05d2684f989764bf203439e2a1cf9fbee8496dea67faa718c`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c01fd63c6f9cc57f6c9d18a1a809f00b33f1f598cf16ea1a93bc8a887a4db19`  
		Last Modified: Wed, 02 Nov 2022 19:18:08 GMT  
		Size: 74.3 MB (74315786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a9db4181ee8f82faa3d1e743e165e793b2ff980cf27a0de82608852b6722e4`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f0d37882dfdd3e15826bf4df89eff73d8f24a63f4d427f1580142d362daef`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc` - linux; s390x

```console
$ docker pull mariadb@sha256:36070d4d060760a4c24219b8aface95df237e72a55f85591deb2d18ea49aa9d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107294477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea92a04f6d3b13eed882dd2defa6d9efc616145041230abe131e6d08f5d2f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:05 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:27:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:27:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:27:50 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:27:51 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:27:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae554b3bf685c681cb82869aad08ce1b8a102dbcc48076cb8a1d4c2000b9549`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6a1b98c8a014695b96e24a86ddfff8f0066dc616dc1be787a55fef437f27b`  
		Last Modified: Wed, 02 Nov 2022 19:31:15 GMT  
		Size: 70.8 MB (70807254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0346caab6232f6cffc3c727baac14a7898defc7d18ef606a70d844247c245a`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88753d7dcc3c5f63b9d7ac2f2b4f0e50ce37b962bf0cee353927a2f3f7b90c6f`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.10.1-rc-jammy`

```console
$ docker pull mariadb@sha256:e37adecf4da3e44a40412422cb19dc0c2776eb16481b2273a757e9207adc9097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.10.1-rc-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:a3b14c15225b4788b562d48f1910ba34eeb4282d3ca62f0db3d2bf4db4621144
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125335699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57de3e4d4a4748bd9f256af1c8adae44736c8aaece6f7137449c6186da2ec20f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:48:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.10.1 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:48:17 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Fri, 11 Nov 2022 01:48:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:48:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:50:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:50:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:50:49 GMT
COPY file:25990863e4bd169447bf1d169dbaf3eeaf1299650f69524839fe736dc4358be0 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:50:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:50:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:50:49 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4e42c6b3fe74b8807bf126325d60167b163c7c5bd9ee0b7460cf9926995c66`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eff5b9b68025fd41eb88195a612cf7b369d1b72e362cc866379a52576b6c9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:44 GMT  
		Size: 89.4 MB (89368635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd587236afdff8a5bf7d9da2aeaee605fbe028289b1c2cb3bb60da87afd907a`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5532f5c0f6753ade67cf121ab73589101b07dbc713333a77c9f1ccdf55bba93`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 7.0 KB (7022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:963f93b32ec3cf17946c29f0fcc3a88fa3e9c938dc28840c0df410ae22c0eec3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104564191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10e5a505ae3328dff1184514c083e7d637f801fb9176dc3f8645070c1a394c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:07:53 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 20:07:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:26 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:26 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:26 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16759adaacc369b316e50cfb18576aea210022969ccdde95d0ae70cb4a0cffc3`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee076b67e8d0c5d62c7f7050a79ad3b8c0be044937447d244161f5bc46393e`  
		Last Modified: Wed, 02 Nov 2022 20:10:18 GMT  
		Size: 68.3 MB (68338186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062fe35f14777880e0fe5635d6e44b97fd9656588003d18fa32f537d2022c606`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966f81b6128476aa69662040adf0f309bd0cd1e7040b7204a13f8cc59a2087af`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:df1026fab4d879c7dae98410339d4f5ff07342d07d87c4698d485ebc7099053b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118852132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f0a1c07c4033de9f42110f5c28f420a4abef95e07ccc06315ceab2ab8e4ccd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:13:01 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:01 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:13:02 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:13:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:13:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:13:59 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:00 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:01 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:14:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5152e5d64618b6b05d2684f989764bf203439e2a1cf9fbee8496dea67faa718c`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c01fd63c6f9cc57f6c9d18a1a809f00b33f1f598cf16ea1a93bc8a887a4db19`  
		Last Modified: Wed, 02 Nov 2022 19:18:08 GMT  
		Size: 74.3 MB (74315786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a9db4181ee8f82faa3d1e743e165e793b2ff980cf27a0de82608852b6722e4`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f0d37882dfdd3e15826bf4df89eff73d8f24a63f4d427f1580142d362daef`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.10.1-rc-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:36070d4d060760a4c24219b8aface95df237e72a55f85591deb2d18ea49aa9d3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107294477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fea92a04f6d3b13eed882dd2defa6d9efc616145041230abe131e6d08f5d2f1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:05 GMT
ARG MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ENV MARIADB_VERSION=1:10.10.1+maria~ubu2204
# Wed, 02 Nov 2022 19:27:05 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:27:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:27:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.10.1/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:27:50 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:27:50 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:27:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:27:51 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:27:51 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae554b3bf685c681cb82869aad08ce1b8a102dbcc48076cb8a1d4c2000b9549`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a6a1b98c8a014695b96e24a86ddfff8f0066dc616dc1be787a55fef437f27b`  
		Last Modified: Wed, 02 Nov 2022 19:31:15 GMT  
		Size: 70.8 MB (70807254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0346caab6232f6cffc3c727baac14a7898defc7d18ef606a70d844247c245a`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88753d7dcc3c5f63b9d7ac2f2b4f0e50ce37b962bf0cee353927a2f3f7b90c6f`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3`

```console
$ docker pull mariadb@sha256:6256048b859aafa703d597b6d7e55f2f241be5eb26dc8dc39fbbe49e99852003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3` - linux; amd64

```console
$ docker pull mariadb@sha256:88315725f8961ab4d91c20fbecd9fe8ed94e1308d9a43753dc854e2e9b77d5e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116254671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dbf81334e66564cf622ceeb3ef2eba25496f89c496016d75511dc84a95b4b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:56:07 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.3.37 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:56:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:07 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:08 GMT
ARG MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ENV MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:56:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865982e3cee20383fcd698d2e069997a2f6e75285bfbdbe4e22055a6490e7583`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b4fed4869f52bf82650dd21e0c0b857c7bc2e11cbbf1ad0a9d051e4be78f7`  
		Last Modified: Fri, 11 Nov 2022 02:01:16 GMT  
		Size: 80.6 MB (80605489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4df2cb047830c5e95e3da6b86db4229c039c3e17b9fc0480b40cf10782630`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb4369125e079bbfc6b7f6d2c178a984eb2df90f4cdf804f49b3f04f019f69d`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e319f1926e9374c6947ec1cf5edac811e8c43a541e638b30a56174497b19d99`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:6e1cf33ddb9f60daf2d5589c37a8cd52b5608e336a293ce7baf8437de0ed2dd1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117887693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e60a10768f8fd0ac693422371c236789581d64b3c669eb01ad39c772a4971`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:06:56 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 26 Oct 2022 02:06:56 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 26 Oct 2022 02:06:56 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 26 Oct 2022 02:06:56 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 26 Oct 2022 02:06:56 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:06:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:07:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:07:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:07:23 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:07:23 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:07:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 26 Oct 2022 02:07:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:07:24 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:07:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5e4ae6fa721db243d094858081ca19bdd1913dd7dbc52cebf012b7f4b5f28e`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d6ed2e45c44a5242ab5143fb2cde22180df8de6443f78bac2b820fd86fe611`  
		Last Modified: Wed, 26 Oct 2022 02:11:46 GMT  
		Size: 79.6 MB (79647166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04ed73a30385efc9f1556a2ba502e00fc1f363c08dcbc006c2d2253a7da2283`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ab85d4aef4566129044d4bc578b3368544bbd868b6fa582e9b948564b7a0d3`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b97fe511cff91cce26db83a9eb005fa3938f985894b873de070b22ee6c9ea6`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2c5e130757705c368cda7bdc49a1f9ff7376cd024dca7173c795e90a9317fb80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131150169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7ec1503a9f68ed169a8f4f3b573125b21c2ae08e17f22e20f24d161c1d7ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:50:30 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 25 Oct 2022 14:50:30 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 Oct 2022 14:50:30 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 25 Oct 2022 14:50:31 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 25 Oct 2022 14:50:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:51:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:51:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:51:21 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:51:22 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:51:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 Oct 2022 14:51:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:51:23 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:51:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1d3f92f042f153fa7306ad4c0e5c33ec36117a2b7d9eea6760e3b3765294c2`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb5b1f59d614481ade7083be2d303d1ba770d233091cc3cae3bc5b2a9eee3b4`  
		Last Modified: Tue, 25 Oct 2022 14:58:27 GMT  
		Size: 84.9 MB (84914666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad1aa3f7368efd7f18cbd620b5be1831f51281da52723c037a9f29d57c672b3`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f048c92ebda308793438c4e4bb85e5cfffecddb4a95d6891bc7850510b960c2`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eabc245de636899188eab0506f3918b5b330a13fe2fab8cb2fee36de46ffd3b`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3-focal`

```console
$ docker pull mariadb@sha256:6256048b859aafa703d597b6d7e55f2f241be5eb26dc8dc39fbbe49e99852003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.3-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:88315725f8961ab4d91c20fbecd9fe8ed94e1308d9a43753dc854e2e9b77d5e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116254671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dbf81334e66564cf622ceeb3ef2eba25496f89c496016d75511dc84a95b4b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:56:07 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.3.37 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:56:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:07 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:08 GMT
ARG MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ENV MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:56:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865982e3cee20383fcd698d2e069997a2f6e75285bfbdbe4e22055a6490e7583`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b4fed4869f52bf82650dd21e0c0b857c7bc2e11cbbf1ad0a9d051e4be78f7`  
		Last Modified: Fri, 11 Nov 2022 02:01:16 GMT  
		Size: 80.6 MB (80605489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4df2cb047830c5e95e3da6b86db4229c039c3e17b9fc0480b40cf10782630`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb4369125e079bbfc6b7f6d2c178a984eb2df90f4cdf804f49b3f04f019f69d`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e319f1926e9374c6947ec1cf5edac811e8c43a541e638b30a56174497b19d99`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:6e1cf33ddb9f60daf2d5589c37a8cd52b5608e336a293ce7baf8437de0ed2dd1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.9 MB (117887693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729e60a10768f8fd0ac693422371c236789581d64b3c669eb01ad39c772a4971`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:06:56 GMT
ARG MARIADB_MAJOR=10.3
# Wed, 26 Oct 2022 02:06:56 GMT
ENV MARIADB_MAJOR=10.3
# Wed, 26 Oct 2022 02:06:56 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 26 Oct 2022 02:06:56 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Wed, 26 Oct 2022 02:06:56 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:06:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:07:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:07:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:07:23 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:07:23 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:07:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 26 Oct 2022 02:07:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:07:24 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:07:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5e4ae6fa721db243d094858081ca19bdd1913dd7dbc52cebf012b7f4b5f28e`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d6ed2e45c44a5242ab5143fb2cde22180df8de6443f78bac2b820fd86fe611`  
		Last Modified: Wed, 26 Oct 2022 02:11:46 GMT  
		Size: 79.6 MB (79647166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04ed73a30385efc9f1556a2ba502e00fc1f363c08dcbc006c2d2253a7da2283`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ab85d4aef4566129044d4bc578b3368544bbd868b6fa582e9b948564b7a0d3`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b97fe511cff91cce26db83a9eb005fa3938f985894b873de070b22ee6c9ea6`  
		Last Modified: Wed, 26 Oct 2022 02:11:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.3-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:2c5e130757705c368cda7bdc49a1f9ff7376cd024dca7173c795e90a9317fb80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131150169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7ec1503a9f68ed169a8f4f3b573125b21c2ae08e17f22e20f24d161c1d7ace`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:50:30 GMT
ARG MARIADB_MAJOR=10.3
# Tue, 25 Oct 2022 14:50:30 GMT
ENV MARIADB_MAJOR=10.3
# Tue, 25 Oct 2022 14:50:30 GMT
ARG MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 25 Oct 2022 14:50:31 GMT
ENV MARIADB_VERSION=1:10.3.36+maria~ubu2004
# Tue, 25 Oct 2022 14:50:31 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:50:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:51:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:51:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:51:21 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:51:22 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:51:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.36/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 Oct 2022 14:51:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:51:23 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:51:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1d3f92f042f153fa7306ad4c0e5c33ec36117a2b7d9eea6760e3b3765294c2`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adb5b1f59d614481ade7083be2d303d1ba770d233091cc3cae3bc5b2a9eee3b4`  
		Last Modified: Tue, 25 Oct 2022 14:58:27 GMT  
		Size: 84.9 MB (84914666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad1aa3f7368efd7f18cbd620b5be1831f51281da52723c037a9f29d57c672b3`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f048c92ebda308793438c4e4bb85e5cfffecddb4a95d6891bc7850510b960c2`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eabc245de636899188eab0506f3918b5b330a13fe2fab8cb2fee36de46ffd3b`  
		Last Modified: Tue, 25 Oct 2022 14:58:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.37`

```console
$ docker pull mariadb@sha256:91eb32efa605db187ef572aceca31f30c7fb4f89acdb8d5929bcb2d65685ad4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.3.37` - linux; amd64

```console
$ docker pull mariadb@sha256:88315725f8961ab4d91c20fbecd9fe8ed94e1308d9a43753dc854e2e9b77d5e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116254671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dbf81334e66564cf622ceeb3ef2eba25496f89c496016d75511dc84a95b4b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:56:07 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.3.37 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:56:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:07 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:08 GMT
ARG MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ENV MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:56:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865982e3cee20383fcd698d2e069997a2f6e75285bfbdbe4e22055a6490e7583`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b4fed4869f52bf82650dd21e0c0b857c7bc2e11cbbf1ad0a9d051e4be78f7`  
		Last Modified: Fri, 11 Nov 2022 02:01:16 GMT  
		Size: 80.6 MB (80605489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4df2cb047830c5e95e3da6b86db4229c039c3e17b9fc0480b40cf10782630`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb4369125e079bbfc6b7f6d2c178a984eb2df90f4cdf804f49b3f04f019f69d`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e319f1926e9374c6947ec1cf5edac811e8c43a541e638b30a56174497b19d99`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.3.37-focal`

```console
$ docker pull mariadb@sha256:91eb32efa605db187ef572aceca31f30c7fb4f89acdb8d5929bcb2d65685ad4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.3.37-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:88315725f8961ab4d91c20fbecd9fe8ed94e1308d9a43753dc854e2e9b77d5e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.3 MB (116254671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12dbf81334e66564cf622ceeb3ef2eba25496f89c496016d75511dc84a95b4b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:56:07 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.3.37 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:56:07 GMT
ARG MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:07 GMT
ENV MARIADB_MAJOR=10.3
# Fri, 11 Nov 2022 01:56:08 GMT
ARG MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ENV MARIADB_VERSION=1:10.3.37+maria~ubu2004
# Fri, 11 Nov 2022 01:56:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:56:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:48 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:48 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.3.37/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:49 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865982e3cee20383fcd698d2e069997a2f6e75285bfbdbe4e22055a6490e7583`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11b4fed4869f52bf82650dd21e0c0b857c7bc2e11cbbf1ad0a9d051e4be78f7`  
		Last Modified: Fri, 11 Nov 2022 02:01:16 GMT  
		Size: 80.6 MB (80605489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab4df2cb047830c5e95e3da6b86db4229c039c3e17b9fc0480b40cf10782630`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb4369125e079bbfc6b7f6d2c178a984eb2df90f4cdf804f49b3f04f019f69d`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e319f1926e9374c6947ec1cf5edac811e8c43a541e638b30a56174497b19d99`  
		Last Modified: Fri, 11 Nov 2022 02:01:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4`

```console
$ docker pull mariadb@sha256:6ff55fadbf2c6fffc5b35a3b7f736d140f045d65351d3f292ddc3db582ce9b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4` - linux; amd64

```console
$ docker pull mariadb@sha256:d7f7680b742731010cbcc86d15b0bfec0eec95b6fcaef8a5160241d148ad6bd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121923597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220d96a2feed7c791377c09fe450448290a4c327cbe8477f9fc0d4963b1c5ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:55:33 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.27 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ENV MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:55:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:03 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:04 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:04 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6e90cd3bce21ed4946e731cfc8f23169254aadcbcc1a016c7d6baa294132bc`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a943b84fc5e1a1e6556772cf850dc2060ab41fda93afc28797a587610c14c72`  
		Last Modified: Fri, 11 Nov 2022 02:00:48 GMT  
		Size: 86.3 MB (86274416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ebae0292e37c961340e710b8a36d30134c6916fe57276d18a377a33b66d61`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d204f8bf4f983cca85995bfa2a0cc87fbeece980a77e8cb6300648352f41f156`  
		Last Modified: Fri, 11 Nov 2022 02:00:36 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ae61fef4ff1b53edbaf36e2879572e437e1dbce6da8dfb81855cc29b58511`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3130c8b3cfe902ca64fc1acd954018418a9d6fe08cba5b7d546bd0cd0655a697
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123380408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd7aa1b396921e68965a55c3a268a8cb5d705d13f6a33eeb3b76a1d3aa74e9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:06:27 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 26 Oct 2022 02:06:27 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 26 Oct 2022 02:06:27 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 26 Oct 2022 02:06:28 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 26 Oct 2022 02:06:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:06:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:06:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:06:52 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:06:52 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:06:52 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:06:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 26 Oct 2022 02:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:06:53 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:06:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49abf541d1422a95d8e41b69fd3e1486aab8e60372a17f173741885d2eaed6a`  
		Last Modified: Wed, 26 Oct 2022 02:11:11 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8db3abcfcfa29a6cb75bb8bdd527882817830b1210f3ea6d3490c1fd840525`  
		Last Modified: Wed, 26 Oct 2022 02:11:21 GMT  
		Size: 85.1 MB (85139880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d7cb4e1258ee2bab27a064345a399aa11b2255737f7900fab8a91a01fbb93b`  
		Last Modified: Wed, 26 Oct 2022 02:11:10 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d748f549470cd2311d8ec1bce4581218a4d585a4759631c469c1de18781d66`  
		Last Modified: Wed, 26 Oct 2022 02:11:11 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853e58f14536007bd56cd2f752f47936667c94b867d5b48081d21cb7958257d7`  
		Last Modified: Wed, 26 Oct 2022 02:11:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd7d5cdcae639125101650fad291e9dad31a55952d3fc871e79cc02344a821cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136762099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df37e158b34f685843951abeaefa1dab7950ac6afe3eb1a0611ffd286200a4b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:49:28 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 25 Oct 2022 14:49:29 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 Oct 2022 14:49:29 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 25 Oct 2022 14:49:29 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 25 Oct 2022 14:49:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:49:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:50:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:50:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:50:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:50:22 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:50:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 Oct 2022 14:50:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:50:23 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:50:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf6e59cad7b9c45f3b776ae8c87f0c71ac2c814928ec5e8c9612c4116a34fc4`  
		Last Modified: Tue, 25 Oct 2022 14:57:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27362baed08ca928ffd43b2b814973357540c44c673181c6c227627ff81cc7b3`  
		Last Modified: Tue, 25 Oct 2022 14:57:45 GMT  
		Size: 90.5 MB (90526593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fdfb8e7543bd960285f812a880686fb1e3e56f19d33f94897841b52631c9b3`  
		Last Modified: Tue, 25 Oct 2022 14:57:21 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa78dd6f6312b99d48e4b660427e6263b6bf936a13b8fad8af1e0843ff9f99fa`  
		Last Modified: Tue, 25 Oct 2022 14:57:21 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc728e087a42406c3214d697d1f7042ed66d3a40309d6e88870203bf4297fefa`  
		Last Modified: Tue, 25 Oct 2022 14:57:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4-focal`

```console
$ docker pull mariadb@sha256:6ff55fadbf2c6fffc5b35a3b7f736d140f045d65351d3f292ddc3db582ce9b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `mariadb:10.4-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:d7f7680b742731010cbcc86d15b0bfec0eec95b6fcaef8a5160241d148ad6bd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121923597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220d96a2feed7c791377c09fe450448290a4c327cbe8477f9fc0d4963b1c5ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:55:33 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.27 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ENV MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:55:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:03 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:04 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:04 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6e90cd3bce21ed4946e731cfc8f23169254aadcbcc1a016c7d6baa294132bc`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a943b84fc5e1a1e6556772cf850dc2060ab41fda93afc28797a587610c14c72`  
		Last Modified: Fri, 11 Nov 2022 02:00:48 GMT  
		Size: 86.3 MB (86274416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ebae0292e37c961340e710b8a36d30134c6916fe57276d18a377a33b66d61`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d204f8bf4f983cca85995bfa2a0cc87fbeece980a77e8cb6300648352f41f156`  
		Last Modified: Fri, 11 Nov 2022 02:00:36 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ae61fef4ff1b53edbaf36e2879572e437e1dbce6da8dfb81855cc29b58511`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:3130c8b3cfe902ca64fc1acd954018418a9d6fe08cba5b7d546bd0cd0655a697
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.4 MB (123380408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd7aa1b396921e68965a55c3a268a8cb5d705d13f6a33eeb3b76a1d3aa74e9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:06:27 GMT
ARG MARIADB_MAJOR=10.4
# Wed, 26 Oct 2022 02:06:27 GMT
ENV MARIADB_MAJOR=10.4
# Wed, 26 Oct 2022 02:06:27 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 26 Oct 2022 02:06:28 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Wed, 26 Oct 2022 02:06:28 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:06:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:06:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:06:52 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:06:52 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:06:52 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:06:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 26 Oct 2022 02:06:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:06:53 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:06:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49abf541d1422a95d8e41b69fd3e1486aab8e60372a17f173741885d2eaed6a`  
		Last Modified: Wed, 26 Oct 2022 02:11:11 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8db3abcfcfa29a6cb75bb8bdd527882817830b1210f3ea6d3490c1fd840525`  
		Last Modified: Wed, 26 Oct 2022 02:11:21 GMT  
		Size: 85.1 MB (85139880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d7cb4e1258ee2bab27a064345a399aa11b2255737f7900fab8a91a01fbb93b`  
		Last Modified: Wed, 26 Oct 2022 02:11:10 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d748f549470cd2311d8ec1bce4581218a4d585a4759631c469c1de18781d66`  
		Last Modified: Wed, 26 Oct 2022 02:11:11 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853e58f14536007bd56cd2f752f47936667c94b867d5b48081d21cb7958257d7`  
		Last Modified: Wed, 26 Oct 2022 02:11:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.4-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:cd7d5cdcae639125101650fad291e9dad31a55952d3fc871e79cc02344a821cb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136762099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df37e158b34f685843951abeaefa1dab7950ac6afe3eb1a0611ffd286200a4b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:49:28 GMT
ARG MARIADB_MAJOR=10.4
# Tue, 25 Oct 2022 14:49:29 GMT
ENV MARIADB_MAJOR=10.4
# Tue, 25 Oct 2022 14:49:29 GMT
ARG MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 25 Oct 2022 14:49:29 GMT
ENV MARIADB_VERSION=1:10.4.26+maria~ubu2004
# Tue, 25 Oct 2022 14:49:29 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:49:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:50:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:50:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:50:22 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:50:22 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:50:23 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.26/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Tue, 25 Oct 2022 14:50:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:50:23 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:50:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf6e59cad7b9c45f3b776ae8c87f0c71ac2c814928ec5e8c9612c4116a34fc4`  
		Last Modified: Tue, 25 Oct 2022 14:57:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27362baed08ca928ffd43b2b814973357540c44c673181c6c227627ff81cc7b3`  
		Last Modified: Tue, 25 Oct 2022 14:57:45 GMT  
		Size: 90.5 MB (90526593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fdfb8e7543bd960285f812a880686fb1e3e56f19d33f94897841b52631c9b3`  
		Last Modified: Tue, 25 Oct 2022 14:57:21 GMT  
		Size: 3.5 KB (3497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa78dd6f6312b99d48e4b660427e6263b6bf936a13b8fad8af1e0843ff9f99fa`  
		Last Modified: Tue, 25 Oct 2022 14:57:21 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc728e087a42406c3214d697d1f7042ed66d3a40309d6e88870203bf4297fefa`  
		Last Modified: Tue, 25 Oct 2022 14:57:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.27`

```console
$ docker pull mariadb@sha256:39ebed85294e7302f39111a65d5d72bdee5399b0fddbe8ade25971bbce6552f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.4.27` - linux; amd64

```console
$ docker pull mariadb@sha256:d7f7680b742731010cbcc86d15b0bfec0eec95b6fcaef8a5160241d148ad6bd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121923597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220d96a2feed7c791377c09fe450448290a4c327cbe8477f9fc0d4963b1c5ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:55:33 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.27 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ENV MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:55:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:03 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:04 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:04 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6e90cd3bce21ed4946e731cfc8f23169254aadcbcc1a016c7d6baa294132bc`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a943b84fc5e1a1e6556772cf850dc2060ab41fda93afc28797a587610c14c72`  
		Last Modified: Fri, 11 Nov 2022 02:00:48 GMT  
		Size: 86.3 MB (86274416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ebae0292e37c961340e710b8a36d30134c6916fe57276d18a377a33b66d61`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d204f8bf4f983cca85995bfa2a0cc87fbeece980a77e8cb6300648352f41f156`  
		Last Modified: Fri, 11 Nov 2022 02:00:36 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ae61fef4ff1b53edbaf36e2879572e437e1dbce6da8dfb81855cc29b58511`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.4.27-focal`

```console
$ docker pull mariadb@sha256:39ebed85294e7302f39111a65d5d72bdee5399b0fddbe8ade25971bbce6552f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.4.27-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:d7f7680b742731010cbcc86d15b0bfec0eec95b6fcaef8a5160241d148ad6bd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121923597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7220d96a2feed7c791377c09fe450448290a4c327cbe8477f9fc0d4963b1c5ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:55:33 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.4.27 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ENV MARIADB_MAJOR=10.4
# Fri, 11 Nov 2022 01:55:33 GMT
ARG MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ENV MARIADB_VERSION=1:10.4.27+maria~ubu2004
# Fri, 11 Nov 2022 01:55:34 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:55:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:56:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:56:03 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:56:03 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:56:04 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:56:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.4.27/repo/ubuntu/ focal main
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 11 Nov 2022 01:56:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:56:04 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:56:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6e90cd3bce21ed4946e731cfc8f23169254aadcbcc1a016c7d6baa294132bc`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a943b84fc5e1a1e6556772cf850dc2060ab41fda93afc28797a587610c14c72`  
		Last Modified: Fri, 11 Nov 2022 02:00:48 GMT  
		Size: 86.3 MB (86274416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1ebae0292e37c961340e710b8a36d30134c6916fe57276d18a377a33b66d61`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 3.5 KB (3496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d204f8bf4f983cca85995bfa2a0cc87fbeece980a77e8cb6300648352f41f156`  
		Last Modified: Fri, 11 Nov 2022 02:00:36 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ae61fef4ff1b53edbaf36e2879572e437e1dbce6da8dfb81855cc29b58511`  
		Last Modified: Fri, 11 Nov 2022 02:00:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5`

```console
$ docker pull mariadb@sha256:5688830295eca497c090f3fd016a2d0420d00d37d3132c7c963ac02defcebcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5` - linux; amd64

```console
$ docker pull mariadb@sha256:7dbef335ec2b32219491e718e93170598ba42bc1e7c8de77018c75ffe9824f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124186245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ff56a02874cff48f63dd41974a64ecb00305e98f56f011da318079ab3a2aca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.18 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:55:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:55:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:55:28 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:55:29 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:55:29 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:55:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff10c4143de9f3ad7e4dd0d9a4cb9b28a940a5b3ffc25088a06deeec8c0bf0ce`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86940c6e6b472adeee37ad0dfc05851e4c586adf0ac914c7eaa2088a89dd0bd2`  
		Last Modified: Fri, 11 Nov 2022 02:00:20 GMT  
		Size: 88.5 MB (88537185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb690670c568195e04ea4a7b82f19e5ae97cd9c7cff01d58fcda25d34afef844`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c944b15571b4cca5909e3c98ad41fd5646e5a058476d4772dc89f06e8fed9`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:75147e4a7b58fbfa6073548d3ff6a71c666f8471a82d3051b36ee7ff496e5d6f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125598592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2997900745409815ed380f76f0f3b02a73491e05d762c6e3ee84e056538b1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:06:00 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 26 Oct 2022 02:06:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 26 Oct 2022 02:06:00 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 26 Oct 2022 02:06:00 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 26 Oct 2022 02:06:00 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:06:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:06:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:06:21 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:06:21 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:06:22 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:06:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:06:22 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:06:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9317c133d22bf1a053a47870a13631dfaaa76e4aa19884640b0ada12d4392a`  
		Last Modified: Wed, 26 Oct 2022 02:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f30e678460e0f8e823655d65ea2b9548d676018bff8779c02d4e18849e3cfa`  
		Last Modified: Wed, 26 Oct 2022 02:10:55 GMT  
		Size: 87.4 MB (87358188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b426e3a31bb98d15adcd307617ecfcde7b58d10667ab34f285af458393b4919`  
		Last Modified: Wed, 26 Oct 2022 02:10:44 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3365d363ba6d0608da76aac797894b103b784e955279bfbdf9f58345101395d`  
		Last Modified: Wed, 26 Oct 2022 02:10:44 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b54af5f443c6d04912638107acfc92ad89a6ab7319ba56a23a36ae77dd08f432
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139035766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee0f95de6cd174b86eabe4a8cf48066a6775db76d148a7ef8e17161c276b12f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:48:29 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 14:48:29 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 14:48:29 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 14:48:29 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 14:48:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:48:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:49:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:49:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:49:18 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:49:18 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:49:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:49:19 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f961f9f3f04a93e21f0a6a0301266d39bf54b15bf8fe2e7e6c60043aa823837`  
		Last Modified: Tue, 25 Oct 2022 14:56:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26648a1799ae35301fa80e9e2e7ea6c1a0f65d2d818132bad6f2250e8385bec`  
		Last Modified: Tue, 25 Oct 2022 14:57:00 GMT  
		Size: 92.8 MB (92800387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e970ad17ab660ad7549d49919b829024ac439a59447ee247c8d9a7ed6f47cc`  
		Last Modified: Tue, 25 Oct 2022 14:56:35 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1c88f22d4a1896c85b2ddd83b8d693797975ed9d79a90ab3dcef25deeb5de4`  
		Last Modified: Tue, 25 Oct 2022 14:56:35 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5` - linux; s390x

```console
$ docker pull mariadb@sha256:c65b5c4885c1fa24d71bbbb27752ede1bd8cb4ab9a4f51f79a83f9065ca95b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127317038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9665426a1e532e4cb4f2d086225b2b2841f3142279771074f0fea57987f6b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:51:28 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 08:51:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:40 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 08:51:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 08:51:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 08:51:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 08:51:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 08:53:17 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 08:53:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 08:53:17 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 08:53:17 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 08:53:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 08:53:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 08:54:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 08:54:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 08:54:26 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 08:54:26 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:54:28 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 08:54:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c5044aaae9e9803c63085684d6340fffb48767ac91fa592d662702d71aff1`  
		Last Modified: Tue, 25 Oct 2022 08:57:06 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a613b90c876878a9a94cbe3f205e854e0e796efe95e25a57da6b039f2ac97d9`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 5.4 MB (5365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cddf62974e459d6f0a5e307c9359e0e06a9a0264484f72bb95a6f381b6bd6`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 3.2 MB (3240368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dabd3c9246a9b8e82469971f252b012b98e560773247c285b21e9a9e37f90`  
		Last Modified: Tue, 25 Oct 2022 08:57:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0369aaa883fcaa78bfe09a26fe173f3c93a893e45eb5a7ff6806ccdc402a1ab`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 2.2 MB (2168258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3408446731db62b9762fcab8cfd4a46c250b4f345dfd9e58ca04ae6efd4d84`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21c359cd423844747d0b308e28e6f7ef24a2a3b96defe9645af62fde954ecbc`  
		Last Modified: Tue, 25 Oct 2022 08:57:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbb07ad16457f22a898a729973e915e2d010510a5ff4c6fae20b9ae4ae688a9`  
		Last Modified: Tue, 25 Oct 2022 08:58:07 GMT  
		Size: 89.5 MB (89511936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aa57038edb5a8583aaebee68e3dfcea0fbcfb52cf41b06615b9b911e1ae3f8`  
		Last Modified: Tue, 25 Oct 2022 08:57:54 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566e9e37413dda4f72f9bfe3ea56d83ebafedbd028c80453882151996e47d629`  
		Last Modified: Tue, 25 Oct 2022 08:57:54 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5-focal`

```console
$ docker pull mariadb@sha256:5688830295eca497c090f3fd016a2d0420d00d37d3132c7c963ac02defcebcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.5-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7dbef335ec2b32219491e718e93170598ba42bc1e7c8de77018c75ffe9824f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124186245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ff56a02874cff48f63dd41974a64ecb00305e98f56f011da318079ab3a2aca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.18 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:55:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:55:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:55:28 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:55:29 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:55:29 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:55:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff10c4143de9f3ad7e4dd0d9a4cb9b28a940a5b3ffc25088a06deeec8c0bf0ce`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86940c6e6b472adeee37ad0dfc05851e4c586adf0ac914c7eaa2088a89dd0bd2`  
		Last Modified: Fri, 11 Nov 2022 02:00:20 GMT  
		Size: 88.5 MB (88537185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb690670c568195e04ea4a7b82f19e5ae97cd9c7cff01d58fcda25d34afef844`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c944b15571b4cca5909e3c98ad41fd5646e5a058476d4772dc89f06e8fed9`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:75147e4a7b58fbfa6073548d3ff6a71c666f8471a82d3051b36ee7ff496e5d6f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125598592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2997900745409815ed380f76f0f3b02a73491e05d762c6e3ee84e056538b1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:06:00 GMT
ARG MARIADB_MAJOR=10.5
# Wed, 26 Oct 2022 02:06:00 GMT
ENV MARIADB_MAJOR=10.5
# Wed, 26 Oct 2022 02:06:00 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 26 Oct 2022 02:06:00 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Wed, 26 Oct 2022 02:06:00 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:06:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:06:20 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:06:21 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:06:21 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:06:22 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:06:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:06:22 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:06:22 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9317c133d22bf1a053a47870a13631dfaaa76e4aa19884640b0ada12d4392a`  
		Last Modified: Wed, 26 Oct 2022 02:10:44 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f30e678460e0f8e823655d65ea2b9548d676018bff8779c02d4e18849e3cfa`  
		Last Modified: Wed, 26 Oct 2022 02:10:55 GMT  
		Size: 87.4 MB (87358188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b426e3a31bb98d15adcd307617ecfcde7b58d10667ab34f285af458393b4919`  
		Last Modified: Wed, 26 Oct 2022 02:10:44 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3365d363ba6d0608da76aac797894b103b784e955279bfbdf9f58345101395d`  
		Last Modified: Wed, 26 Oct 2022 02:10:44 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b54af5f443c6d04912638107acfc92ad89a6ab7319ba56a23a36ae77dd08f432
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139035766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee0f95de6cd174b86eabe4a8cf48066a6775db76d148a7ef8e17161c276b12f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:48:29 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 14:48:29 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 14:48:29 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 14:48:29 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 14:48:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:48:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:49:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:49:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:49:18 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:49:18 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:49:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:49:19 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:49:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f961f9f3f04a93e21f0a6a0301266d39bf54b15bf8fe2e7e6c60043aa823837`  
		Last Modified: Tue, 25 Oct 2022 14:56:35 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26648a1799ae35301fa80e9e2e7ea6c1a0f65d2d818132bad6f2250e8385bec`  
		Last Modified: Tue, 25 Oct 2022 14:57:00 GMT  
		Size: 92.8 MB (92800387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e970ad17ab660ad7549d49919b829024ac439a59447ee247c8d9a7ed6f47cc`  
		Last Modified: Tue, 25 Oct 2022 14:56:35 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1c88f22d4a1896c85b2ddd83b8d693797975ed9d79a90ab3dcef25deeb5de4`  
		Last Modified: Tue, 25 Oct 2022 14:56:35 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.5-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:c65b5c4885c1fa24d71bbbb27752ede1bd8cb4ab9a4f51f79a83f9065ca95b0a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127317038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9665426a1e532e4cb4f2d086225b2b2841f3142279771074f0fea57987f6b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:51:28 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 08:51:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:40 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 08:51:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 08:51:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 08:51:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 08:51:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 08:53:17 GMT
ARG MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 08:53:17 GMT
ENV MARIADB_MAJOR=10.5
# Tue, 25 Oct 2022 08:53:17 GMT
ARG MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 08:53:17 GMT
ENV MARIADB_VERSION=1:10.5.17+maria~ubu2004
# Tue, 25 Oct 2022 08:53:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 08:53:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 08:54:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.17/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 08:54:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 08:54:26 GMT
COPY file:64ef9edc0b6d64f19618d1f2ffc8c4cc3c2a1e0e90591a283cdeda8bbe9f9a14 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 08:54:26 GMT
COPY file:1cbfae6200694fb67440ab571faea87cbbd737228ff9f3193338e54312e6bd67 in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:54:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:54:28 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 08:54:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c5044aaae9e9803c63085684d6340fffb48767ac91fa592d662702d71aff1`  
		Last Modified: Tue, 25 Oct 2022 08:57:06 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a613b90c876878a9a94cbe3f205e854e0e796efe95e25a57da6b039f2ac97d9`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 5.4 MB (5365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cddf62974e459d6f0a5e307c9359e0e06a9a0264484f72bb95a6f381b6bd6`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 3.2 MB (3240368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dabd3c9246a9b8e82469971f252b012b98e560773247c285b21e9a9e37f90`  
		Last Modified: Tue, 25 Oct 2022 08:57:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0369aaa883fcaa78bfe09a26fe173f3c93a893e45eb5a7ff6806ccdc402a1ab`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 2.2 MB (2168258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3408446731db62b9762fcab8cfd4a46c250b4f345dfd9e58ca04ae6efd4d84`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21c359cd423844747d0b308e28e6f7ef24a2a3b96defe9645af62fde954ecbc`  
		Last Modified: Tue, 25 Oct 2022 08:57:54 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cbb07ad16457f22a898a729973e915e2d010510a5ff4c6fae20b9ae4ae688a9`  
		Last Modified: Tue, 25 Oct 2022 08:58:07 GMT  
		Size: 89.5 MB (89511936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aa57038edb5a8583aaebee68e3dfcea0fbcfb52cf41b06615b9b911e1ae3f8`  
		Last Modified: Tue, 25 Oct 2022 08:57:54 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566e9e37413dda4f72f9bfe3ea56d83ebafedbd028c80453882151996e47d629`  
		Last Modified: Tue, 25 Oct 2022 08:57:54 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.18`

```console
$ docker pull mariadb@sha256:f8678d66016d90f5b6b147b5f192bb9acc9a07ed7619dc966acfac91b8d3dee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.5.18` - linux; amd64

```console
$ docker pull mariadb@sha256:7dbef335ec2b32219491e718e93170598ba42bc1e7c8de77018c75ffe9824f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124186245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ff56a02874cff48f63dd41974a64ecb00305e98f56f011da318079ab3a2aca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.18 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:55:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:55:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:55:28 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:55:29 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:55:29 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:55:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff10c4143de9f3ad7e4dd0d9a4cb9b28a940a5b3ffc25088a06deeec8c0bf0ce`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86940c6e6b472adeee37ad0dfc05851e4c586adf0ac914c7eaa2088a89dd0bd2`  
		Last Modified: Fri, 11 Nov 2022 02:00:20 GMT  
		Size: 88.5 MB (88537185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb690670c568195e04ea4a7b82f19e5ae97cd9c7cff01d58fcda25d34afef844`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c944b15571b4cca5909e3c98ad41fd5646e5a058476d4772dc89f06e8fed9`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.5.18-focal`

```console
$ docker pull mariadb@sha256:f8678d66016d90f5b6b147b5f192bb9acc9a07ed7619dc966acfac91b8d3dee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.5.18-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:7dbef335ec2b32219491e718e93170598ba42bc1e7c8de77018c75ffe9824f40
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124186245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ff56a02874cff48f63dd41974a64ecb00305e98f56f011da318079ab3a2aca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.5.18 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_MAJOR=10.5
# Fri, 11 Nov 2022 01:54:53 GMT
ARG MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ENV MARIADB_VERSION=1:10.5.18+maria~ubu2004
# Fri, 11 Nov 2022 01:54:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:55:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.5.18/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:55:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:55:28 GMT
COPY file:d1ef29581ac31aa4bb2834dc97545a6c5a3ee728dfcb95fd3598dfb219fdbae2 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:55:29 GMT
COPY file:a20d2f4de06cbd6bb5b32b07e5ddff51f8660c1cbb71d7a08ae07c03fee2ca23 in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:55:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:55:29 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:55:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff10c4143de9f3ad7e4dd0d9a4cb9b28a940a5b3ffc25088a06deeec8c0bf0ce`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86940c6e6b472adeee37ad0dfc05851e4c586adf0ac914c7eaa2088a89dd0bd2`  
		Last Modified: Fri, 11 Nov 2022 02:00:20 GMT  
		Size: 88.5 MB (88537185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb690670c568195e04ea4a7b82f19e5ae97cd9c7cff01d58fcda25d34afef844`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c944b15571b4cca5909e3c98ad41fd5646e5a058476d4772dc89f06e8fed9`  
		Last Modified: Fri, 11 Nov 2022 02:00:07 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6`

```console
$ docker pull mariadb@sha256:ebb9d9fea034fdfcdad995e1abbb8571261b2644771bb742a986621ea3932c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6` - linux; amd64

```console
$ docker pull mariadb@sha256:ebccdc459d1ce2ba66c059e04c2a08a3492dac725ce67de56e9b1df8ff8eb6fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124522623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62052ec34aae490abf35935ded23fba9883587aade6bd5246b7157780123e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:12 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ARG MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:54:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:47 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:47 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e88c034ffbaf266a05262f08f7f9bde72b1e74b96d5181053c04d8d0843f8`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09b3c6023668be566065d638891e53842370b25a83c884957f078c582bd297f`  
		Last Modified: Fri, 11 Nov 2022 01:59:50 GMT  
		Size: 88.9 MB (88873565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f95913b8f606ae2ff63227c21bef2c6adcdc19cac4ed807b7bf7d559a61f`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad640b19225b4117f87d139ea72fb0b7c5a57faa252ee8aa8680af3e74cd96d`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2a4f16d88b588f35d86e3f1c1ad18d0ff236715aa47a8429ffe91d21c2cd7919
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125656180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7eec748da3421b54980609f12fcf11ede45e59de3d5918644524c3b458f8010`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:05:36 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 26 Oct 2022 02:05:36 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 26 Oct 2022 02:05:36 GMT
ARG MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Wed, 26 Oct 2022 02:05:36 GMT
ENV MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Wed, 26 Oct 2022 02:05:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:05:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:05:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:05:57 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:05:57 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:05:57 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:05:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb80a602c36bdad83f2a5208bdb9c55afd09d123f55e4a001d82579340f5c4d4`  
		Last Modified: Wed, 26 Oct 2022 02:10:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded0a0306f3bc15969e0b35a7782db48ddd8b3e77abd90e2407ad3dabc91238e`  
		Last Modified: Wed, 26 Oct 2022 02:10:23 GMT  
		Size: 87.4 MB (87415771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb00dea3c2afef8409982977b52d0e8271c4189878780038deaa1a7633ad4181`  
		Last Modified: Wed, 26 Oct 2022 02:10:12 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96961d266794c3ecf3e736699988bec9d35bfde44628b7406d4c656b09069bc`  
		Last Modified: Wed, 26 Oct 2022 02:10:12 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d36248018951d79d2f1e3042ca26b8b20018f7038a3dc82ec45421894566619c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139119643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d054f37b648a2972f854c402f64af984920282cc388b7f3968c1099df124c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:47:28 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 14:47:29 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 14:47:29 GMT
ARG MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 14:47:29 GMT
ENV MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 14:47:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:47:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:48:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:48:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:48:22 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:48:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:48:22 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:48:23 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f480ab67dba9f982defb105cc0ed354878dee0bb88f52c1d909abdb40b4194ea`  
		Last Modified: Tue, 25 Oct 2022 14:55:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daccce68a68caddb60e950f923ba6ec39887a804f0e50bd4beaea89a18f47b11`  
		Last Modified: Tue, 25 Oct 2022 14:56:15 GMT  
		Size: 92.9 MB (92884262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b26ac76ed1d68c6da262d00b8c098337b48d20a66db66b8a6d8e853ee11ab3`  
		Last Modified: Tue, 25 Oct 2022 14:55:50 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58aa6b937daf39522cbf5d2ad8ae59f1391140ba123eab1a90d3dd3ee9c3187b`  
		Last Modified: Tue, 25 Oct 2022 14:55:50 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6` - linux; s390x

```console
$ docker pull mariadb@sha256:3c2b5bf07f96ec9ba5886e018fc58097c38a0be68a7e87320dd1322427b12aa7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127383044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdcf9c69f5407981b6e643ae31377374c60d5188136e2fc56db1e544ac2a7e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:51:28 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 08:51:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:40 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 08:51:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 08:51:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 08:51:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 08:51:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 08:52:45 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 08:52:45 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 08:52:46 GMT
ARG MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 08:52:46 GMT
ENV MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 08:52:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 08:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 08:53:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 08:53:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 08:53:09 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 08:53:09 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:53:09 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 08:53:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c5044aaae9e9803c63085684d6340fffb48767ac91fa592d662702d71aff1`  
		Last Modified: Tue, 25 Oct 2022 08:57:06 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a613b90c876878a9a94cbe3f205e854e0e796efe95e25a57da6b039f2ac97d9`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 5.4 MB (5365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cddf62974e459d6f0a5e307c9359e0e06a9a0264484f72bb95a6f381b6bd6`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 3.2 MB (3240368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dabd3c9246a9b8e82469971f252b012b98e560773247c285b21e9a9e37f90`  
		Last Modified: Tue, 25 Oct 2022 08:57:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0369aaa883fcaa78bfe09a26fe173f3c93a893e45eb5a7ff6806ccdc402a1ab`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 2.2 MB (2168258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3408446731db62b9762fcab8cfd4a46c250b4f345dfd9e58ca04ae6efd4d84`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a024a75fab4f702b1de36e5d3b4399dfbc66a3412d7b1c1eb59c578eb06730ca`  
		Last Modified: Tue, 25 Oct 2022 08:57:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e10292a939ab193d8c12747719407ed8b688eb8ce71d0a54a8c87e655e46aab`  
		Last Modified: Tue, 25 Oct 2022 08:57:42 GMT  
		Size: 89.6 MB (89577948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d3a676ce7bf70b6357d50bb3bcc0c52e7809599da417e9b18b8f75d535985`  
		Last Modified: Tue, 25 Oct 2022 08:57:29 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd0b13d6c76061faf3e51a83a82a9cfb8cf705ea6a6460ade128c171b7f0fd`  
		Last Modified: Tue, 25 Oct 2022 08:57:29 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6-focal`

```console
$ docker pull mariadb@sha256:ebb9d9fea034fdfcdad995e1abbb8571261b2644771bb742a986621ea3932c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.6-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:ebccdc459d1ce2ba66c059e04c2a08a3492dac725ce67de56e9b1df8ff8eb6fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124522623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62052ec34aae490abf35935ded23fba9883587aade6bd5246b7157780123e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:12 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ARG MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:54:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:47 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:47 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e88c034ffbaf266a05262f08f7f9bde72b1e74b96d5181053c04d8d0843f8`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09b3c6023668be566065d638891e53842370b25a83c884957f078c582bd297f`  
		Last Modified: Fri, 11 Nov 2022 01:59:50 GMT  
		Size: 88.9 MB (88873565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f95913b8f606ae2ff63227c21bef2c6adcdc19cac4ed807b7bf7d559a61f`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad640b19225b4117f87d139ea72fb0b7c5a57faa252ee8aa8680af3e74cd96d`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2a4f16d88b588f35d86e3f1c1ad18d0ff236715aa47a8429ffe91d21c2cd7919
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.7 MB (125656180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7eec748da3421b54980609f12fcf11ede45e59de3d5918644524c3b458f8010`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:05:36 GMT
ARG MARIADB_MAJOR=10.6
# Wed, 26 Oct 2022 02:05:36 GMT
ENV MARIADB_MAJOR=10.6
# Wed, 26 Oct 2022 02:05:36 GMT
ARG MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Wed, 26 Oct 2022 02:05:36 GMT
ENV MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Wed, 26 Oct 2022 02:05:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:05:37 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:05:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:05:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:05:57 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:05:57 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:05:57 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:05:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb80a602c36bdad83f2a5208bdb9c55afd09d123f55e4a001d82579340f5c4d4`  
		Last Modified: Wed, 26 Oct 2022 02:10:13 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded0a0306f3bc15969e0b35a7782db48ddd8b3e77abd90e2407ad3dabc91238e`  
		Last Modified: Wed, 26 Oct 2022 02:10:23 GMT  
		Size: 87.4 MB (87415771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb00dea3c2afef8409982977b52d0e8271c4189878780038deaa1a7633ad4181`  
		Last Modified: Wed, 26 Oct 2022 02:10:12 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96961d266794c3ecf3e736699988bec9d35bfde44628b7406d4c656b09069bc`  
		Last Modified: Wed, 26 Oct 2022 02:10:12 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:d36248018951d79d2f1e3042ca26b8b20018f7038a3dc82ec45421894566619c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139119643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d054f37b648a2972f854c402f64af984920282cc388b7f3968c1099df124c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:47:28 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 14:47:29 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 14:47:29 GMT
ARG MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 14:47:29 GMT
ENV MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 14:47:30 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:47:31 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:48:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:48:21 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:48:21 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:48:22 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:48:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:48:22 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:48:23 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f480ab67dba9f982defb105cc0ed354878dee0bb88f52c1d909abdb40b4194ea`  
		Last Modified: Tue, 25 Oct 2022 14:55:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daccce68a68caddb60e950f923ba6ec39887a804f0e50bd4beaea89a18f47b11`  
		Last Modified: Tue, 25 Oct 2022 14:56:15 GMT  
		Size: 92.9 MB (92884262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b26ac76ed1d68c6da262d00b8c098337b48d20a66db66b8a6d8e853ee11ab3`  
		Last Modified: Tue, 25 Oct 2022 14:55:50 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58aa6b937daf39522cbf5d2ad8ae59f1391140ba123eab1a90d3dd3ee9c3187b`  
		Last Modified: Tue, 25 Oct 2022 14:55:50 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.6-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:3c2b5bf07f96ec9ba5886e018fc58097c38a0be68a7e87320dd1322427b12aa7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127383044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cdcf9c69f5407981b6e643ae31377374c60d5188136e2fc56db1e544ac2a7e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:51:28 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 08:51:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:40 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 08:51:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 08:51:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 08:51:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 08:51:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 08:52:45 GMT
ARG MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 08:52:45 GMT
ENV MARIADB_MAJOR=10.6
# Tue, 25 Oct 2022 08:52:46 GMT
ARG MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 08:52:46 GMT
ENV MARIADB_VERSION=1:10.6.10+maria~ubu2004
# Tue, 25 Oct 2022 08:52:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 08:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 08:53:05 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.10/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 08:53:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 08:53:09 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 08:53:09 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:53:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:53:09 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 08:53:09 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c5044aaae9e9803c63085684d6340fffb48767ac91fa592d662702d71aff1`  
		Last Modified: Tue, 25 Oct 2022 08:57:06 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a613b90c876878a9a94cbe3f205e854e0e796efe95e25a57da6b039f2ac97d9`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 5.4 MB (5365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cddf62974e459d6f0a5e307c9359e0e06a9a0264484f72bb95a6f381b6bd6`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 3.2 MB (3240368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dabd3c9246a9b8e82469971f252b012b98e560773247c285b21e9a9e37f90`  
		Last Modified: Tue, 25 Oct 2022 08:57:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0369aaa883fcaa78bfe09a26fe173f3c93a893e45eb5a7ff6806ccdc402a1ab`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 2.2 MB (2168258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3408446731db62b9762fcab8cfd4a46c250b4f345dfd9e58ca04ae6efd4d84`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a024a75fab4f702b1de36e5d3b4399dfbc66a3412d7b1c1eb59c578eb06730ca`  
		Last Modified: Tue, 25 Oct 2022 08:57:29 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e10292a939ab193d8c12747719407ed8b688eb8ce71d0a54a8c87e655e46aab`  
		Last Modified: Tue, 25 Oct 2022 08:57:42 GMT  
		Size: 89.6 MB (89577948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d3a676ce7bf70b6357d50bb3bcc0c52e7809599da417e9b18b8f75d535985`  
		Last Modified: Tue, 25 Oct 2022 08:57:29 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd0b13d6c76061faf3e51a83a82a9cfb8cf705ea6a6460ade128c171b7f0fd`  
		Last Modified: Tue, 25 Oct 2022 08:57:29 GMT  
		Size: 7.0 KB (7050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.11`

```console
$ docker pull mariadb@sha256:b9df4587d24cbe1e27ba8e81d67166b0078c2a5a430cc19cce2a3ca540e28238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.6.11` - linux; amd64

```console
$ docker pull mariadb@sha256:ebccdc459d1ce2ba66c059e04c2a08a3492dac725ce67de56e9b1df8ff8eb6fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124522623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62052ec34aae490abf35935ded23fba9883587aade6bd5246b7157780123e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:12 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ARG MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:54:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:47 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:47 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e88c034ffbaf266a05262f08f7f9bde72b1e74b96d5181053c04d8d0843f8`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09b3c6023668be566065d638891e53842370b25a83c884957f078c582bd297f`  
		Last Modified: Fri, 11 Nov 2022 01:59:50 GMT  
		Size: 88.9 MB (88873565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f95913b8f606ae2ff63227c21bef2c6adcdc19cac4ed807b7bf7d559a61f`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad640b19225b4117f87d139ea72fb0b7c5a57faa252ee8aa8680af3e74cd96d`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.6.11-focal`

```console
$ docker pull mariadb@sha256:b9df4587d24cbe1e27ba8e81d67166b0078c2a5a430cc19cce2a3ca540e28238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.6.11-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:ebccdc459d1ce2ba66c059e04c2a08a3492dac725ce67de56e9b1df8ff8eb6fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124522623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62052ec34aae490abf35935ded23fba9883587aade6bd5246b7157780123e6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:54:12 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.6.11 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:54:12 GMT
ARG MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_MAJOR=10.6
# Fri, 11 Nov 2022 01:54:13 GMT
ARG MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ENV MARIADB_VERSION=1:10.6.11+maria~ubu2004
# Fri, 11 Nov 2022 01:54:13 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:54:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:54:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.6.11/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:47 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:47 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:47 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:47 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5e88c034ffbaf266a05262f08f7f9bde72b1e74b96d5181053c04d8d0843f8`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09b3c6023668be566065d638891e53842370b25a83c884957f078c582bd297f`  
		Last Modified: Fri, 11 Nov 2022 01:59:50 GMT  
		Size: 88.9 MB (88873565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9896f95913b8f606ae2ff63227c21bef2c6adcdc19cac4ed807b7bf7d559a61f`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad640b19225b4117f87d139ea72fb0b7c5a57faa252ee8aa8680af3e74cd96d`  
		Last Modified: Fri, 11 Nov 2022 01:59:37 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7`

```console
$ docker pull mariadb@sha256:f3bb9dc597455bb090e671e305376368c2c3821bf4963409ea32884e55fe2869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7` - linux; amd64

```console
$ docker pull mariadb@sha256:cfb614d5a9c5befd2438d996fc50197ec6a8c3fd91a66f55e2baa79a477eb903
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125004791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ed88878a8e3f0bf043eeb7480f859f83742b39c5929e53bda8dacaebce0bd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:52:47 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.7.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:52:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:53:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:00 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f3842c61594161a6ca84cb0f7b12e885dbb45c556ddf4cbf1ce79fc70e779c`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ef296df01678ff544a14617156e7e555e8bf30a3a40c906509012f1e99fb73`  
		Last Modified: Fri, 11 Nov 2022 01:59:21 GMT  
		Size: 89.4 MB (89355727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b81fc14995cdef8ab793a00b3219bd7c062a9ee8aa2192d7e1906402f4afca`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f85c6b03d8a9c90ab88f7f0b9c5826ae1e571047821250d7a13d8434250d38`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 7.0 KB (6953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:87a98538fd9b4cbbe6741e040e4fdad13c497012b35cc2012639955e25de1eb2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126160016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91f3cd238ac241f4e4da3b1caf3e14ea8792c13440e97d7dc5cc9f976f1f5ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:04:46 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 26 Oct 2022 02:04:46 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 26 Oct 2022 02:04:46 GMT
ARG MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Wed, 26 Oct 2022 02:04:46 GMT
ENV MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Wed, 26 Oct 2022 02:04:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:04:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:05:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:05:25 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:05:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:05:26 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:05:26 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:05:26 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e285a7096945cbc4dbb08b241e3e872668020d36c615adc856668a633722ffb`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d1d716822a5771930e74151a206729f0a0c4a01df00dd92c2ee3469f43f9f5`  
		Last Modified: Wed, 26 Oct 2022 02:09:54 GMT  
		Size: 87.9 MB (87919613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e9ea41ac711c364318e34a2f5d8ca8bea481e0ba0efd241c162a6260c0b6c0`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a3527aa4cc989f38e19d428becfb3ad46ab44e94e58598f3463af18fe21ec0`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; ppc64le

```console
$ docker pull mariadb@sha256:75735f3e2d0db81afacc42be8d96c804f62eae56742e0b9d3677dca50836ddd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28616701b0ac2d41ea285eda877be5ace1cc33749ff334fd02cceb1f15998e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:46:07 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 14:46:07 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 14:46:07 GMT
ARG MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 14:46:08 GMT
ENV MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 14:46:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:46:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:47:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:47:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:47:11 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:47:11 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:47:12 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:47:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1bdf054e93508832e1a7e133d9c75481f44e52eecfbd846acd47f629405c3c`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2579e73dc319f5d4423abe44e354d01d18ccb6fc6066c686ce35bec6c831c5`  
		Last Modified: Tue, 25 Oct 2022 14:55:29 GMT  
		Size: 93.6 MB (93602335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afb50caf35e8740e45fb6908a7a4036389c8c69546b9f056d86727ce35f95f0`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c84f1874619ce85cdd788a81f3f521ec6b6f0af9da246ce9cae57e11e8d54`  
		Last Modified: Tue, 25 Oct 2022 14:55:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7` - linux; s390x

```console
$ docker pull mariadb@sha256:d29e9d1768d09cf046ea721850f6aaaa530e1d819728878806261ee3deeddd02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127886860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a25aa0f649a0769be207d4bae03a30a5f245750bd86cbf7812c4ed0b89913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:51:28 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 08:51:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:40 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 08:51:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 08:51:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 08:51:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 08:51:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 08:51:58 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 08:51:58 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 08:51:59 GMT
ARG MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 08:51:59 GMT
ENV MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 08:51:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 08:51:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 08:52:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 08:52:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 08:52:32 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 08:52:32 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:52:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:52:32 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 08:52:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c5044aaae9e9803c63085684d6340fffb48767ac91fa592d662702d71aff1`  
		Last Modified: Tue, 25 Oct 2022 08:57:06 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a613b90c876878a9a94cbe3f205e854e0e796efe95e25a57da6b039f2ac97d9`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 5.4 MB (5365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cddf62974e459d6f0a5e307c9359e0e06a9a0264484f72bb95a6f381b6bd6`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 3.2 MB (3240368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dabd3c9246a9b8e82469971f252b012b98e560773247c285b21e9a9e37f90`  
		Last Modified: Tue, 25 Oct 2022 08:57:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0369aaa883fcaa78bfe09a26fe173f3c93a893e45eb5a7ff6806ccdc402a1ab`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 2.2 MB (2168258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3408446731db62b9762fcab8cfd4a46c250b4f345dfd9e58ca04ae6efd4d84`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a088e6ee6bc8604db966958e0ed8ff9c88d93eb15e2f9e3afc4c389d1c3f0b`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c02e893db98bf55209501ce08eef0a59e107637b9a714dff844154a7e1e8e1`  
		Last Modified: Tue, 25 Oct 2022 08:57:16 GMT  
		Size: 90.1 MB (90081759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5641b030cf058344ecd6eed02f6374597172baf6a8389707795a19c934ef4324`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5a2bac3f7b2acec84e7cb2503bc0d606efa968cb406254e4564eb0624ccd39`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7-focal`

```console
$ docker pull mariadb@sha256:f3bb9dc597455bb090e671e305376368c2c3821bf4963409ea32884e55fe2869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:cfb614d5a9c5befd2438d996fc50197ec6a8c3fd91a66f55e2baa79a477eb903
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125004791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ed88878a8e3f0bf043eeb7480f859f83742b39c5929e53bda8dacaebce0bd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:52:47 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.7.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:52:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:53:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:00 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f3842c61594161a6ca84cb0f7b12e885dbb45c556ddf4cbf1ce79fc70e779c`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ef296df01678ff544a14617156e7e555e8bf30a3a40c906509012f1e99fb73`  
		Last Modified: Fri, 11 Nov 2022 01:59:21 GMT  
		Size: 89.4 MB (89355727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b81fc14995cdef8ab793a00b3219bd7c062a9ee8aa2192d7e1906402f4afca`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f85c6b03d8a9c90ab88f7f0b9c5826ae1e571047821250d7a13d8434250d38`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 7.0 KB (6953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:87a98538fd9b4cbbe6741e040e4fdad13c497012b35cc2012639955e25de1eb2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126160016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e91f3cd238ac241f4e4da3b1caf3e14ea8792c13440e97d7dc5cc9f976f1f5ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 02:04:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 26 Oct 2022 02:04:28 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 02:04:38 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 26 Oct 2022 02:04:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 26 Oct 2022 02:04:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 02:04:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 26 Oct 2022 02:04:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 26 Oct 2022 02:04:46 GMT
ARG MARIADB_MAJOR=10.7
# Wed, 26 Oct 2022 02:04:46 GMT
ENV MARIADB_MAJOR=10.7
# Wed, 26 Oct 2022 02:04:46 GMT
ARG MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Wed, 26 Oct 2022 02:04:46 GMT
ENV MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Wed, 26 Oct 2022 02:04:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
# Wed, 26 Oct 2022 02:04:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 26 Oct 2022 02:05:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 26 Oct 2022 02:05:25 GMT
VOLUME [/var/lib/mysql]
# Wed, 26 Oct 2022 02:05:26 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 26 Oct 2022 02:05:26 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 26 Oct 2022 02:05:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Oct 2022 02:05:26 GMT
EXPOSE 3306
# Wed, 26 Oct 2022 02:05:26 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5059476c4efaaefd5639d62272cf873b43fc4dd354f29aa2d424f5672f98d7`  
		Last Modified: Wed, 26 Oct 2022 02:09:48 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b512e3647ec22a314bc3b404b44b891220289f7918fc3fb90dec28d934b622f7`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 5.5 MB (5474279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4034a198751d9b8465f987f8cd51acc3b45288510ea70f4f50588aca7ab03e`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 3.4 MB (3368397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a303c93f3f2afdbf7461aaa57d2e0376745b909ca61dc1ab04bed8a727844135`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a95ecb4d8b5c99728b7e239140c0c9127f6b8286e033494da3d7b938d10669`  
		Last Modified: Wed, 26 Oct 2022 02:09:46 GMT  
		Size: 2.2 MB (2186475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c381f22b0bfdceb13b81f9105a5b0965c5d34d0a2800bc7ae58461d1661aae`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e285a7096945cbc4dbb08b241e3e872668020d36c615adc856668a633722ffb`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d1d716822a5771930e74151a206729f0a0c4a01df00dd92c2ee3469f43f9f5`  
		Last Modified: Wed, 26 Oct 2022 02:09:54 GMT  
		Size: 87.9 MB (87919613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e9ea41ac711c364318e34a2f5d8ca8bea481e0ba0efd241c162a6260c0b6c0`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a3527aa4cc989f38e19d428becfb3ad46ab44e94e58598f3463af18fe21ec0`  
		Last Modified: Wed, 26 Oct 2022 02:09:43 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; ppc64le

```console
$ docker pull mariadb@sha256:75735f3e2d0db81afacc42be8d96c804f62eae56742e0b9d3677dca50836ddd2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28616701b0ac2d41ea285eda877be5ace1cc33749ff334fd02cceb1f15998e74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 03:25:47 GMT
ADD file:013ddcea49540903962069a03762fe471452e8cf00bafeb530724940405797e1 in / 
# Tue, 25 Oct 2022 03:25:49 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 14:45:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 14:45:29 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:45:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 14:45:48 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 14:45:49 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 14:46:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 14:46:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 14:46:06 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 14:46:07 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 14:46:07 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 14:46:07 GMT
ARG MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 14:46:08 GMT
ENV MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 14:46:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 14:46:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 14:47:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 14:47:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 14:47:11 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 14:47:11 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 14:47:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 14:47:12 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 14:47:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:42e5f4d60d38e5070be91d6965be1cff1294e6dc275038002dc2ef1812233b0e`  
		Last Modified: Tue, 25 Oct 2022 03:27:44 GMT  
		Size: 33.3 MB (33300542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83da4aca0ded73831bac1900cce993de71ec5e346c23dedb306464348a16f0ff`  
		Last Modified: Tue, 25 Oct 2022 14:55:10 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29c70f2a7dd8420c704124d2a43aef4dc74083e080b275ac0eaebd0b9d2e7267`  
		Last Modified: Tue, 25 Oct 2022 14:55:11 GMT  
		Size: 6.7 MB (6699037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c99487690c6d4a7306215d7028c71b7e7d31b717cdf4d867a2a20c3b543b93`  
		Last Modified: Tue, 25 Oct 2022 14:55:08 GMT  
		Size: 3.7 MB (3669865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0a3e9489dff43b6f6398075e6d36dad4631d2edd119c6fdc2e6c3d6db2ded0`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc7d5c05b4a04cdfe632c68caa8b9895d8cff3dae74ccb4da007f42a2cb71f9`  
		Last Modified: Tue, 25 Oct 2022 14:55:07 GMT  
		Size: 2.6 MB (2550679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c6181697fa50ab583a8a8f8bb3586fe93996e07b311047d7bea87dbdc68d23`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 2.5 KB (2488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd1bdf054e93508832e1a7e133d9c75481f44e52eecfbd846acd47f629405c3c`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2579e73dc319f5d4423abe44e354d01d18ccb6fc6066c686ce35bec6c831c5`  
		Last Modified: Tue, 25 Oct 2022 14:55:29 GMT  
		Size: 93.6 MB (93602335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afb50caf35e8740e45fb6908a7a4036389c8c69546b9f056d86727ce35f95f0`  
		Last Modified: Tue, 25 Oct 2022 14:55:04 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174c84f1874619ce85cdd788a81f3f521ec6b6f0af9da246ce9cae57e11e8d54`  
		Last Modified: Tue, 25 Oct 2022 14:55:05 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.7-focal` - linux; s390x

```console
$ docker pull mariadb@sha256:d29e9d1768d09cf046ea721850f6aaaa530e1d819728878806261ee3deeddd02
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127886860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0a25aa0f649a0769be207d4bae03a30a5f245750bd86cbf7812c4ed0b89913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:23:11 GMT
ADD file:c657b467ecb15f1f4a49a5f04a525f38924750c8187c9ef9f0b886d0264e21f1 in / 
# Tue, 25 Oct 2022 01:23:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 08:51:28 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 08:51:40 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:40 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 08:51:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 08:51:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 08:51:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 08:51:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 25 Oct 2022 08:51:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 25 Oct 2022 08:51:58 GMT
ARG MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 08:51:58 GMT
ENV MARIADB_MAJOR=10.7
# Tue, 25 Oct 2022 08:51:59 GMT
ARG MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 08:51:59 GMT
ENV MARIADB_VERSION=1:10.7.6+maria~ubu2004
# Tue, 25 Oct 2022 08:51:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
# Tue, 25 Oct 2022 08:51:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 25 Oct 2022 08:52:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.6/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 25 Oct 2022 08:52:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 08:52:32 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Tue, 25 Oct 2022 08:52:32 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Tue, 25 Oct 2022 08:52:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 08:52:32 GMT
EXPOSE 3306
# Tue, 25 Oct 2022 08:52:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a63328f08dbd14148b5ffe154c18846ead48e759779d007b78ec3fb19f5f43a5`  
		Last Modified: Tue, 25 Oct 2022 01:24:36 GMT  
		Size: 27.0 MB (27016028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c5044aaae9e9803c63085684d6340fffb48767ac91fa592d662702d71aff1`  
		Last Modified: Tue, 25 Oct 2022 08:57:06 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a613b90c876878a9a94cbe3f205e854e0e796efe95e25a57da6b039f2ac97d9`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 5.4 MB (5365188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cddf62974e459d6f0a5e307c9359e0e06a9a0264484f72bb95a6f381b6bd6`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 3.2 MB (3240368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028dabd3c9246a9b8e82469971f252b012b98e560773247c285b21e9a9e37f90`  
		Last Modified: Tue, 25 Oct 2022 08:57:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0369aaa883fcaa78bfe09a26fe173f3c93a893e45eb5a7ff6806ccdc402a1ab`  
		Last Modified: Tue, 25 Oct 2022 08:57:05 GMT  
		Size: 2.2 MB (2168258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3408446731db62b9762fcab8cfd4a46c250b4f345dfd9e58ca04ae6efd4d84`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 2.5 KB (2490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a088e6ee6bc8604db966958e0ed8ff9c88d93eb15e2f9e3afc4c389d1c3f0b`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c02e893db98bf55209501ce08eef0a59e107637b9a714dff844154a7e1e8e1`  
		Last Modified: Tue, 25 Oct 2022 08:57:16 GMT  
		Size: 90.1 MB (90081759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5641b030cf058344ecd6eed02f6374597172baf6a8389707795a19c934ef4324`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5a2bac3f7b2acec84e7cb2503bc0d606efa968cb406254e4564eb0624ccd39`  
		Last Modified: Tue, 25 Oct 2022 08:57:03 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.7`

```console
$ docker pull mariadb@sha256:d24bb1ec86003ed39570d73c16e0d696d43e181b6967416d7376f0195e488e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.7.7` - linux; amd64

```console
$ docker pull mariadb@sha256:cfb614d5a9c5befd2438d996fc50197ec6a8c3fd91a66f55e2baa79a477eb903
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125004791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ed88878a8e3f0bf043eeb7480f859f83742b39c5929e53bda8dacaebce0bd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:52:47 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.7.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:52:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:53:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:00 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f3842c61594161a6ca84cb0f7b12e885dbb45c556ddf4cbf1ce79fc70e779c`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ef296df01678ff544a14617156e7e555e8bf30a3a40c906509012f1e99fb73`  
		Last Modified: Fri, 11 Nov 2022 01:59:21 GMT  
		Size: 89.4 MB (89355727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b81fc14995cdef8ab793a00b3219bd7c062a9ee8aa2192d7e1906402f4afca`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f85c6b03d8a9c90ab88f7f0b9c5826ae1e571047821250d7a13d8434250d38`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 7.0 KB (6953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.7.7-focal`

```console
$ docker pull mariadb@sha256:d24bb1ec86003ed39570d73c16e0d696d43e181b6967416d7376f0195e488e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.7.7-focal` - linux; amd64

```console
$ docker pull mariadb@sha256:cfb614d5a9c5befd2438d996fc50197ec6a8c3fd91a66f55e2baa79a477eb903
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.0 MB (125004791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41ed88878a8e3f0bf043eeb7480f859f83742b39c5929e53bda8dacaebce0bd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 17:11:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:52:19 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:52:19 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:52:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:52:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:52:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:52:47 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:focal org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.7.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_MAJOR=10.7
# Fri, 11 Nov 2022 01:52:47 GMT
ARG MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ENV MARIADB_VERSION=1:10.7.7+maria~ubu2004
# Fri, 11 Nov 2022 01:52:47 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
# Fri, 11 Nov 2022 01:52:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:53:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.7.7/repo/ubuntu/ focal main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:54:00 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:54:00 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:54:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:54:00 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:54:01 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f4832182b9d366cc9cf48f4786dbc0b688c5f2d0a819d5ed74f31bef53555`  
		Last Modified: Wed, 26 Oct 2022 16:20:02 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed3156c4156966693d0f4fbacae9b7b499afd7c6c674e6667c0cb8fda31a80`  
		Last Modified: Fri, 11 Nov 2022 01:59:11 GMT  
		Size: 7.1 MB (7058561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adc5c9f5ec1426f7463c719d7680ab9fc690d0f91c348854cb16d24b879082`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f3842c61594161a6ca84cb0f7b12e885dbb45c556ddf4cbf1ce79fc70e779c`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ef296df01678ff544a14617156e7e555e8bf30a3a40c906509012f1e99fb73`  
		Last Modified: Fri, 11 Nov 2022 01:59:21 GMT  
		Size: 89.4 MB (89355727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b81fc14995cdef8ab793a00b3219bd7c062a9ee8aa2192d7e1906402f4afca`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f85c6b03d8a9c90ab88f7f0b9c5826ae1e571047821250d7a13d8434250d38`  
		Last Modified: Fri, 11 Nov 2022 01:59:08 GMT  
		Size: 7.0 KB (6953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8`

```console
$ docker pull mariadb@sha256:a02eebaaf7d3f5f2d3f180c749b2202a3a0721b3d88cc5798d160c95a8c80c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8` - linux; amd64

```console
$ docker pull mariadb@sha256:d47a903023cae4ebab6c95a599f782d0e8c8dafdf9ad0c2717e4807f7b87dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121737861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58efcb2d614137096fbd3417547e8132238b68e87b66fa6e65716ffa3abc88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:51:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:51:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:52:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:52:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:52:12 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877c2d880362f31777c760a2d1948796a53c2635e67b5bf0fd6f79b53f322af3`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ba98b683265be4819670212b19e17535e23905e66e489112b6835a75bbe3`  
		Last Modified: Fri, 11 Nov 2022 01:58:52 GMT  
		Size: 85.8 MB (85770866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd72dca1315bd7f57b5a126213a37a0c7245319d62150d17e5e67128fba934d`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1e28fc0e59ab6f523fa3d60e503a7ec2db653a80c76a93a37901dfae776336`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0fb2878bc86064e2f6e3a23fb7c6b4000369966a515b60c171f411beabfc6bca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118516515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80346687bfec3eaa67e3f424e9728c48f36592572dab6769e4232c408b5b632d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:59 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 20:08:59 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 20:08:59 GMT
ARG MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 20:08:59 GMT
ENV MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 20:08:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:09:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:09:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:09:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:09:19 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:09:19 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:09:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:09:20 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:09:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f6dfb067d988f79d0ab038a1eca9d6a03131a6ca4eea8bf9ccd36e165b70`  
		Last Modified: Wed, 02 Nov 2022 20:11:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14a98a30f182adcc4fdf5d93432421c616ee1cae7c56208e20ccecab70c19a`  
		Last Modified: Wed, 02 Nov 2022 20:11:24 GMT  
		Size: 82.3 MB (82290513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489f5524a391d9156536b82a6f3cf4ff2e2c5d924cafedcdc1d28bda8e6d0e3`  
		Last Modified: Wed, 02 Nov 2022 20:11:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e52a7f78fc68eb4a754c260178976cc5046720f644b07bec438292e3b8b14ed`  
		Last Modified: Wed, 02 Nov 2022 20:11:13 GMT  
		Size: 7.0 KB (7047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8` - linux; ppc64le

```console
$ docker pull mariadb@sha256:607ada3edc9e4b683e9de67998fdf0b98e7bef5fc9fdd87f848dff07a974128b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116911775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5366b551769ff24838db695109cf31cac4f3481dbc2cabd7af152c8217f1f748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:15:09 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:15:09 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:15:10 GMT
ARG MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:15:10 GMT
ENV MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:15:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:15:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:15:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:15:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:15:57 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:15:57 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:15:58 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f737f7deaddf9cb6eb37cd43e6a185f1b4983b122f6a7616605522158fc7e7`  
		Last Modified: Wed, 02 Nov 2022 19:19:25 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec91ea164a119076b6fd314af0056f666aeeb05b4a42a58e60d17dd4f45073ae`  
		Last Modified: Wed, 02 Nov 2022 19:19:44 GMT  
		Size: 72.4 MB (72375436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582701229dc2b4040e5f72a3c4a6efab983ef2ad780a427f4237142952fb5793`  
		Last Modified: Wed, 02 Nov 2022 19:19:26 GMT  
		Size: 3.5 KB (3488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d74312faf6024fb5340750d6259489139fc8f30d53252b1a31857140de8643d`  
		Last Modified: Wed, 02 Nov 2022 19:19:25 GMT  
		Size: 7.0 KB (7047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8` - linux; s390x

```console
$ docker pull mariadb@sha256:3708f423455bc38cb891cf9bda75aa636e493610c71fbddf1637b0a6c7ac02a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b2af7df33516d538419cd36aa2e9168a8b39e6b9d688b4cd79615abfd1a207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:28:47 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:28:47 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:28:47 GMT
ARG MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:28:48 GMT
ENV MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:28:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:29:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:29:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:29:30 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:29:30 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:29:31 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:29:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e0567814f939b123df0a0a81b1b9bbb596f11661efe7555dc92fecd8c7fe78`  
		Last Modified: Wed, 02 Nov 2022 19:32:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defbfb4f78b5c758551189d026587f6462903ec5b618c442d5b26e0f8b95bd6`  
		Last Modified: Wed, 02 Nov 2022 19:32:28 GMT  
		Size: 68.6 MB (68559013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a61d54369c9dd67e82f950eb8582f39ccfea0c6f0da4b31919074c4ea941184`  
		Last Modified: Wed, 02 Nov 2022 19:32:18 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae8e604e2a7c640d2fb553792f3556536800dc26eb1024582d95ce6c2d56f4a`  
		Last Modified: Wed, 02 Nov 2022 19:32:18 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8-jammy`

```console
$ docker pull mariadb@sha256:a02eebaaf7d3f5f2d3f180c749b2202a3a0721b3d88cc5798d160c95a8c80c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.8-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:d47a903023cae4ebab6c95a599f782d0e8c8dafdf9ad0c2717e4807f7b87dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121737861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58efcb2d614137096fbd3417547e8132238b68e87b66fa6e65716ffa3abc88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:51:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:51:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:52:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:52:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:52:12 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877c2d880362f31777c760a2d1948796a53c2635e67b5bf0fd6f79b53f322af3`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ba98b683265be4819670212b19e17535e23905e66e489112b6835a75bbe3`  
		Last Modified: Fri, 11 Nov 2022 01:58:52 GMT  
		Size: 85.8 MB (85770866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd72dca1315bd7f57b5a126213a37a0c7245319d62150d17e5e67128fba934d`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1e28fc0e59ab6f523fa3d60e503a7ec2db653a80c76a93a37901dfae776336`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:0fb2878bc86064e2f6e3a23fb7c6b4000369966a515b60c171f411beabfc6bca
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118516515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80346687bfec3eaa67e3f424e9728c48f36592572dab6769e4232c408b5b632d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:59 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 20:08:59 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 20:08:59 GMT
ARG MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 20:08:59 GMT
ENV MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 20:08:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:09:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:09:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:09:19 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:09:19 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:09:19 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:09:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:09:20 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:09:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7f6dfb067d988f79d0ab038a1eca9d6a03131a6ca4eea8bf9ccd36e165b70`  
		Last Modified: Wed, 02 Nov 2022 20:11:13 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c14a98a30f182adcc4fdf5d93432421c616ee1cae7c56208e20ccecab70c19a`  
		Last Modified: Wed, 02 Nov 2022 20:11:24 GMT  
		Size: 82.3 MB (82290513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3489f5524a391d9156536b82a6f3cf4ff2e2c5d924cafedcdc1d28bda8e6d0e3`  
		Last Modified: Wed, 02 Nov 2022 20:11:13 GMT  
		Size: 3.5 KB (3490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e52a7f78fc68eb4a754c260178976cc5046720f644b07bec438292e3b8b14ed`  
		Last Modified: Wed, 02 Nov 2022 20:11:13 GMT  
		Size: 7.0 KB (7047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:607ada3edc9e4b683e9de67998fdf0b98e7bef5fc9fdd87f848dff07a974128b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.9 MB (116911775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5366b551769ff24838db695109cf31cac4f3481dbc2cabd7af152c8217f1f748`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:15:09 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:15:09 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:15:10 GMT
ARG MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:15:10 GMT
ENV MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:15:11 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:15:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:15:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:15:56 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:15:57 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:15:57 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:15:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:15:58 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f737f7deaddf9cb6eb37cd43e6a185f1b4983b122f6a7616605522158fc7e7`  
		Last Modified: Wed, 02 Nov 2022 19:19:25 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec91ea164a119076b6fd314af0056f666aeeb05b4a42a58e60d17dd4f45073ae`  
		Last Modified: Wed, 02 Nov 2022 19:19:44 GMT  
		Size: 72.4 MB (72375436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582701229dc2b4040e5f72a3c4a6efab983ef2ad780a427f4237142952fb5793`  
		Last Modified: Wed, 02 Nov 2022 19:19:26 GMT  
		Size: 3.5 KB (3488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d74312faf6024fb5340750d6259489139fc8f30d53252b1a31857140de8643d`  
		Last Modified: Wed, 02 Nov 2022 19:19:25 GMT  
		Size: 7.0 KB (7047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.8-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:3708f423455bc38cb891cf9bda75aa636e493610c71fbddf1637b0a6c7ac02a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (105046238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b2af7df33516d538419cd36aa2e9168a8b39e6b9d688b4cd79615abfd1a207`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:28:47 GMT
ARG MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:28:47 GMT
ENV MARIADB_MAJOR=10.8
# Wed, 02 Nov 2022 19:28:47 GMT
ARG MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:28:48 GMT
ENV MARIADB_VERSION=1:10.8.5+maria~ubu2204
# Wed, 02 Nov 2022 19:28:48 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:29:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.5/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:29:30 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:29:30 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:29:30 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:29:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:29:31 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:29:31 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e0567814f939b123df0a0a81b1b9bbb596f11661efe7555dc92fecd8c7fe78`  
		Last Modified: Wed, 02 Nov 2022 19:32:18 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9defbfb4f78b5c758551189d026587f6462903ec5b618c442d5b26e0f8b95bd6`  
		Last Modified: Wed, 02 Nov 2022 19:32:28 GMT  
		Size: 68.6 MB (68559013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a61d54369c9dd67e82f950eb8582f39ccfea0c6f0da4b31919074c4ea941184`  
		Last Modified: Wed, 02 Nov 2022 19:32:18 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae8e604e2a7c640d2fb553792f3556536800dc26eb1024582d95ce6c2d56f4a`  
		Last Modified: Wed, 02 Nov 2022 19:32:18 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.6`

```console
$ docker pull mariadb@sha256:dc291dedbcd7bb1ebcf77ab5a8b833f84b082a327912e419ce9ec56a44a307d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.8.6` - linux; amd64

```console
$ docker pull mariadb@sha256:d47a903023cae4ebab6c95a599f782d0e8c8dafdf9ad0c2717e4807f7b87dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121737861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58efcb2d614137096fbd3417547e8132238b68e87b66fa6e65716ffa3abc88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:51:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:51:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:52:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:52:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:52:12 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877c2d880362f31777c760a2d1948796a53c2635e67b5bf0fd6f79b53f322af3`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ba98b683265be4819670212b19e17535e23905e66e489112b6835a75bbe3`  
		Last Modified: Fri, 11 Nov 2022 01:58:52 GMT  
		Size: 85.8 MB (85770866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd72dca1315bd7f57b5a126213a37a0c7245319d62150d17e5e67128fba934d`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1e28fc0e59ab6f523fa3d60e503a7ec2db653a80c76a93a37901dfae776336`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.8.6-jammy`

```console
$ docker pull mariadb@sha256:dc291dedbcd7bb1ebcf77ab5a8b833f84b082a327912e419ce9ec56a44a307d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.8.6-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:d47a903023cae4ebab6c95a599f782d0e8c8dafdf9ad0c2717e4807f7b87dacf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121737861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58efcb2d614137096fbd3417547e8132238b68e87b66fa6e65716ffa3abc88a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:51:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.8.6 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_MAJOR=10.8
# Fri, 11 Nov 2022 01:51:39 GMT
ARG MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ENV MARIADB_VERSION=1:10.8.6+maria~ubu2204
# Fri, 11 Nov 2022 01:51:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:51:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:52:10 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.8.6/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password password 'unused'; 		echo "mariadb-server-$MARIADB_MAJOR" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:52:11 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:52:11 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:52:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:52:12 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:52:12 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877c2d880362f31777c760a2d1948796a53c2635e67b5bf0fd6f79b53f322af3`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d5ba98b683265be4819670212b19e17535e23905e66e489112b6835a75bbe3`  
		Last Modified: Fri, 11 Nov 2022 01:58:52 GMT  
		Size: 85.8 MB (85770866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd72dca1315bd7f57b5a126213a37a0c7245319d62150d17e5e67128fba934d`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 3.5 KB (3491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1e28fc0e59ab6f523fa3d60e503a7ec2db653a80c76a93a37901dfae776336`  
		Last Modified: Fri, 11 Nov 2022 01:58:40 GMT  
		Size: 7.0 KB (6951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9`

```console
$ docker pull mariadb@sha256:eeb8e0dd5043b82dccaadd366c17b37e73802f0a508a77d877d1bbfa7084989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.9` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31f677ba9b50beef8d48a3bbcab29485f5aa3a90677d1ebc44039bbc9bc8bde4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118604917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe889c390f208ce09bf8bfa7869b7d342d999c4279a8809e3a2d2a14332cf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:36 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:08:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:55 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:55 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5452b6a0ce3706d857279cfa1cdaef7c8b6bc76d8d6a4b1c43367203b766cd2f`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628f7ef3cedd084f9a47495aa153853592da56561a6e3231a78435d95ff9949`  
		Last Modified: Wed, 02 Nov 2022 20:10:44 GMT  
		Size: 82.4 MB (82378919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e903661ffaca59211d235a8061c23cc51afe2459c91999d6e191b263897d86d0`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ecec752f0246a09512597065787135cfb39650e56b627521d6b7a25b44bec`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9` - linux; ppc64le

```console
$ docker pull mariadb@sha256:986c35ba43c2850b7911d84081331f918000e38549e853630add39e459d49f28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117016669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e47acd883e8abe5eff966b7822646acd0bed0c6a192953367a3f79b231e3b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:14:08 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:14:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:14:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:14:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:59 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:59 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c2e50062f28f25572934e1354be67087ba900f512bdaad143946434e750a18`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba9ea9acad2d162a2570367cc2f21af52c0b3e528d239dd2d8af13c327724ad`  
		Last Modified: Wed, 02 Nov 2022 19:18:49 GMT  
		Size: 72.5 MB (72480320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd098559b30b498d64f7740fcf0fe3bdd0372711b2d118558adf7b2cc0f7a9`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7613b448a79282dac8e97b54a740faeda580f7c7410e3ddaef69d39f3f1e995a`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9` - linux; s390x

```console
$ docker pull mariadb@sha256:18498ac00e522618f92dc59b38e9e956ceecbbdd98523c622dd07f0c13d83c2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105142329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba90c3535e8905fd0a9e8b72aa707eafe97c2d0ee6d23f3142013b50b8860e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:59 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:28:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:28:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:28:36 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:28:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89802ca4242938a62ea9e93dcc84679d6208be5a8ef8a7dbf368c196ddafc596`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b10a0c4c56eda5ee314ee192394ab23400a90fcf6536a7fa5eec78854ac46a`  
		Last Modified: Wed, 02 Nov 2022 19:31:40 GMT  
		Size: 68.7 MB (68655104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b25788d86165ab3008742f36bd0cd6bfb36679d1928144085e0b200ae38a9d`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4f3538ccb9ee39af5e436a70e5c49fcb1724dead6cb95f3c0aa7942a62c12`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9-jammy`

```console
$ docker pull mariadb@sha256:eeb8e0dd5043b82dccaadd366c17b37e73802f0a508a77d877d1bbfa7084989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10.9-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31f677ba9b50beef8d48a3bbcab29485f5aa3a90677d1ebc44039bbc9bc8bde4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118604917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe889c390f208ce09bf8bfa7869b7d342d999c4279a8809e3a2d2a14332cf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:36 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:08:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:55 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:55 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5452b6a0ce3706d857279cfa1cdaef7c8b6bc76d8d6a4b1c43367203b766cd2f`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628f7ef3cedd084f9a47495aa153853592da56561a6e3231a78435d95ff9949`  
		Last Modified: Wed, 02 Nov 2022 20:10:44 GMT  
		Size: 82.4 MB (82378919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e903661ffaca59211d235a8061c23cc51afe2459c91999d6e191b263897d86d0`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ecec752f0246a09512597065787135cfb39650e56b627521d6b7a25b44bec`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:986c35ba43c2850b7911d84081331f918000e38549e853630add39e459d49f28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117016669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e47acd883e8abe5eff966b7822646acd0bed0c6a192953367a3f79b231e3b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:14:08 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:14:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:14:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:14:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:59 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:59 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c2e50062f28f25572934e1354be67087ba900f512bdaad143946434e750a18`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba9ea9acad2d162a2570367cc2f21af52c0b3e528d239dd2d8af13c327724ad`  
		Last Modified: Wed, 02 Nov 2022 19:18:49 GMT  
		Size: 72.5 MB (72480320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd098559b30b498d64f7740fcf0fe3bdd0372711b2d118558adf7b2cc0f7a9`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7613b448a79282dac8e97b54a740faeda580f7c7410e3ddaef69d39f3f1e995a`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10.9-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:18498ac00e522618f92dc59b38e9e956ceecbbdd98523c622dd07f0c13d83c2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105142329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba90c3535e8905fd0a9e8b72aa707eafe97c2d0ee6d23f3142013b50b8860e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:59 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:28:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:28:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:28:36 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:28:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89802ca4242938a62ea9e93dcc84679d6208be5a8ef8a7dbf368c196ddafc596`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b10a0c4c56eda5ee314ee192394ab23400a90fcf6536a7fa5eec78854ac46a`  
		Last Modified: Wed, 02 Nov 2022 19:31:40 GMT  
		Size: 68.7 MB (68655104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b25788d86165ab3008742f36bd0cd6bfb36679d1928144085e0b200ae38a9d`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4f3538ccb9ee39af5e436a70e5c49fcb1724dead6cb95f3c0aa7942a62c12`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9.4`

```console
$ docker pull mariadb@sha256:ec50027ceae2267c4f3dbdc9b93e9c73d69d9f71f9925fe709d6b319ec457f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.9.4` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:10.9.4-jammy`

```console
$ docker pull mariadb@sha256:ec50027ceae2267c4f3dbdc9b93e9c73d69d9f71f9925fe709d6b319ec457f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mariadb:10.9.4-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:jammy`

```console
$ docker pull mariadb@sha256:eeb8e0dd5043b82dccaadd366c17b37e73802f0a508a77d877d1bbfa7084989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31f677ba9b50beef8d48a3bbcab29485f5aa3a90677d1ebc44039bbc9bc8bde4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118604917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe889c390f208ce09bf8bfa7869b7d342d999c4279a8809e3a2d2a14332cf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:36 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:08:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:55 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:55 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5452b6a0ce3706d857279cfa1cdaef7c8b6bc76d8d6a4b1c43367203b766cd2f`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628f7ef3cedd084f9a47495aa153853592da56561a6e3231a78435d95ff9949`  
		Last Modified: Wed, 02 Nov 2022 20:10:44 GMT  
		Size: 82.4 MB (82378919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e903661ffaca59211d235a8061c23cc51afe2459c91999d6e191b263897d86d0`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ecec752f0246a09512597065787135cfb39650e56b627521d6b7a25b44bec`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:986c35ba43c2850b7911d84081331f918000e38549e853630add39e459d49f28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117016669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e47acd883e8abe5eff966b7822646acd0bed0c6a192953367a3f79b231e3b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:14:08 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:14:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:14:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:14:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:59 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:59 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c2e50062f28f25572934e1354be67087ba900f512bdaad143946434e750a18`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba9ea9acad2d162a2570367cc2f21af52c0b3e528d239dd2d8af13c327724ad`  
		Last Modified: Wed, 02 Nov 2022 19:18:49 GMT  
		Size: 72.5 MB (72480320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd098559b30b498d64f7740fcf0fe3bdd0372711b2d118558adf7b2cc0f7a9`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7613b448a79282dac8e97b54a740faeda580f7c7410e3ddaef69d39f3f1e995a`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:18498ac00e522618f92dc59b38e9e956ceecbbdd98523c622dd07f0c13d83c2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105142329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba90c3535e8905fd0a9e8b72aa707eafe97c2d0ee6d23f3142013b50b8860e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:59 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:28:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:28:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:28:36 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:28:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89802ca4242938a62ea9e93dcc84679d6208be5a8ef8a7dbf368c196ddafc596`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b10a0c4c56eda5ee314ee192394ab23400a90fcf6536a7fa5eec78854ac46a`  
		Last Modified: Wed, 02 Nov 2022 19:31:40 GMT  
		Size: 68.7 MB (68655104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b25788d86165ab3008742f36bd0cd6bfb36679d1928144085e0b200ae38a9d`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4f3538ccb9ee39af5e436a70e5c49fcb1724dead6cb95f3c0aa7942a62c12`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mariadb:latest`

```console
$ docker pull mariadb@sha256:eeb8e0dd5043b82dccaadd366c17b37e73802f0a508a77d877d1bbfa7084989a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:91323beb7c5c2fb134d13874504aea4e4608304370423019f277b1f70882f9ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121852276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825ad7e31db8cfc5ffa434e1171060e9f60db49279dd675fc562466da3bc0ea0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:56:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 11 Nov 2022 01:47:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 11 Nov 2022 01:47:50 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 11 Nov 2022 01:48:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 11 Nov 2022 01:48:17 GMT
ENV LANG=C.UTF-8
# Fri, 11 Nov 2022 01:50:58 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.9.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 11 Nov 2022 01:50:59 GMT
ARG MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ENV MARIADB_VERSION=1:10.9.4+maria~ubu2204
# Fri, 11 Nov 2022 01:50:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
# Fri, 11 Nov 2022 01:50:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 11 Nov 2022 01:51:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 11 Nov 2022 01:51:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:889339e755ad928a437caeaa979e26ba168ae42039fb519e6d5b31d29bcce082 in /usr/local/bin/healthcheck.sh 
# Fri, 11 Nov 2022 01:51:33 GMT
COPY file:8ff49c407a76d8990281701d57bd3af69835977acdff7e2905ae6052323b3ebd in /usr/local/bin/ 
# Fri, 11 Nov 2022 01:51:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Nov 2022 01:51:33 GMT
EXPOSE 3306
# Fri, 11 Nov 2022 01:51:33 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13360dd5ccba7386fb34c2af66a6c1fea57fb7e83869864e15e1402d8ab746c5`  
		Last Modified: Wed, 02 Nov 2022 19:59:11 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5c4b73b9256bb9ce55509f5e24eda1b080780ceff0db42ce80783cb99efa02`  
		Last Modified: Fri, 11 Nov 2022 01:57:33 GMT  
		Size: 5.5 MB (5528722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f870965a3fa10b9d6b698cec208936020049fc24c1171e5d6f6142fa0282467`  
		Last Modified: Fri, 11 Nov 2022 01:57:30 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:070ea015f843833e7db49738387776c15cc20eafdf70ef5045dff63f0737b4f2`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c861410f2b3e963a06afa4ca24fda97e00c496b9dc2a3ced1f8affa8f94293f`  
		Last Modified: Fri, 11 Nov 2022 01:58:12 GMT  
		Size: 85.9 MB (85885285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46193445bc4f96aba11e38a4481b43380bee2c095422d3df722641dcad6bc477`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262eb9124c0aca8d6780dfa07f0a43ff16308aa84d6f2c84e5566a0d975bd9dd`  
		Last Modified: Fri, 11 Nov 2022 01:57:59 GMT  
		Size: 7.0 KB (6950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:31f677ba9b50beef8d48a3bbcab29485f5aa3a90677d1ebc44039bbc9bc8bde4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118604917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe889c390f208ce09bf8bfa7869b7d342d999c4279a8809e3a2d2a14332cf10`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 20:07:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 20:07:35 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:35 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 20:07:45 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 20:07:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 20:07:52 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 20:07:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 20:07:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 20:08:36 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 20:08:36 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 20:08:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 20:08:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 20:08:55 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 20:08:55 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 20:08:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 20:08:55 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 20:08:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf568f815bdc2b755b642d6cad079d9e2e71dd364d2806bf4a9a3cb0fe3d18b7`  
		Last Modified: Wed, 02 Nov 2022 20:10:14 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5a27635d8616b3a361adc11c7e5712c05d3edef95c0573370b2c92058ed582`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 3.7 MB (3737825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbce0b0cfd1e867e47d514f1de07a5da365d36bfb15513e7cf310802577ab13c`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 1.9 MB (1898793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd291b4a9d31c95c30d2580b470dd4ecbe4d2d10c11e47967a037f8b939146e`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d505d811110d4c6311181f11307bd36ac49e38d1ab561c611e562b293b90a9ef`  
		Last Modified: Wed, 02 Nov 2022 20:10:12 GMT  
		Size: 2.2 MB (2191982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf7ac4a18820861abff79a668773c9f881f45b6f47d10f21df0661e7190013b`  
		Last Modified: Wed, 02 Nov 2022 20:10:09 GMT  
		Size: 2.5 KB (2489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5452b6a0ce3706d857279cfa1cdaef7c8b6bc76d8d6a4b1c43367203b766cd2f`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2628f7ef3cedd084f9a47495aa153853592da56561a6e3231a78435d95ff9949`  
		Last Modified: Wed, 02 Nov 2022 20:10:44 GMT  
		Size: 82.4 MB (82378919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e903661ffaca59211d235a8061c23cc51afe2459c91999d6e191b263897d86d0`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 3.5 KB (3489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8ecec752f0246a09512597065787135cfb39650e56b627521d6b7a25b44bec`  
		Last Modified: Wed, 02 Nov 2022 20:10:34 GMT  
		Size: 7.0 KB (7046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:986c35ba43c2850b7911d84081331f918000e38549e853630add39e459d49f28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117016669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e47acd883e8abe5eff966b7822646acd0bed0c6a192953367a3f79b231e3b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:17:30 GMT
ADD file:e50d53011f99a82c70508eaba072b194b6498693db105f1b1e78adb85ea2f07a in / 
# Wed, 02 Nov 2022 18:17:33 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:12:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:12:26 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:26 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:12:44 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:12:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:12:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:12:58 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:13:01 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:14:08 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:14:08 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:14:09 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:14:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:14:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:14:58 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:14:59 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:14:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:14:59 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:15:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:02f24970cf7d1a154c6565b42f393ba6a0e2c23a067c7571a6004bf88a1de8db`  
		Last Modified: Wed, 02 Nov 2022 18:18:59 GMT  
		Size: 35.7 MB (35707582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac86ff494d3eaf7d95f57bc74e48f4685e8a686b8520aa0c196d6add814e1664`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfeb46b3a1843b7ee9d01cc3d48d5188828832d30e02658a1f40e173b56774e`  
		Last Modified: Wed, 02 Nov 2022 19:17:53 GMT  
		Size: 4.5 MB (4503387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e67838a2b5666564d1410b1813495680475321a9fafc2c1181fd2c890ee43b4`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 1.9 MB (1922247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:004a22c7ec4673456e7895bcc12a8260c27e5d63f8cfbb89e497188c0ff56c06`  
		Last Modified: Wed, 02 Nov 2022 19:17:51 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a81eb319d6a4b7adfa30e05763ab3f2ee3a8f692c43979b744cc4b7a898543`  
		Last Modified: Wed, 02 Nov 2022 19:17:52 GMT  
		Size: 2.4 MB (2387882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8d479fa2d2c6c503cc8ea2b4deb0b6c5af2ff6a58b3a48ec94346053a5f4de`  
		Last Modified: Wed, 02 Nov 2022 19:17:49 GMT  
		Size: 2.5 KB (2487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c2e50062f28f25572934e1354be67087ba900f512bdaad143946434e750a18`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba9ea9acad2d162a2570367cc2f21af52c0b3e528d239dd2d8af13c327724ad`  
		Last Modified: Wed, 02 Nov 2022 19:18:49 GMT  
		Size: 72.5 MB (72480320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8bd098559b30b498d64f7740fcf0fe3bdd0372711b2d118558adf7b2cc0f7a9`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 3.5 KB (3493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7613b448a79282dac8e97b54a740faeda580f7c7410e3ddaef69d39f3f1e995a`  
		Last Modified: Wed, 02 Nov 2022 19:18:31 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:18498ac00e522618f92dc59b38e9e956ceecbbdd98523c622dd07f0c13d83c2b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105142329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba90c3535e8905fd0a9e8b72aa707eafe97c2d0ee6d23f3142013b50b8860e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 02 Nov 2022 18:42:26 GMT
ADD file:0b95c08f7bfd486b0e82a12f0bc21062e9ae48f030f076c8e069bdeb00455043 in / 
# Wed, 02 Nov 2022 18:42:30 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:26:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 02 Nov 2022 19:26:37 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:26:37 GMT
ENV GOSU_VERSION=1.14
# Wed, 02 Nov 2022 19:26:51 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 02 Nov 2022 19:26:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 02 Nov 2022 19:27:01 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:27:02 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 02 Nov 2022 19:27:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Wed, 02 Nov 2022 19:27:59 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Wed, 02 Nov 2022 19:27:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Wed, 02 Nov 2022 19:28:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Wed, 02 Nov 2022 19:28:30 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Wed, 02 Nov 2022 19:28:35 GMT
VOLUME [/var/lib/mysql]
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Wed, 02 Nov 2022 19:28:35 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Wed, 02 Nov 2022 19:28:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Nov 2022 19:28:36 GMT
EXPOSE 3306
# Wed, 02 Nov 2022 19:28:36 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:eafd4874fb95ca754b4f86ad490a07439fba0dbde1b416c882494a56e25e92e1`  
		Last Modified: Wed, 02 Nov 2022 18:44:00 GMT  
		Size: 28.6 MB (28640756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bea011dce2c7655ef5645f35951603af4d860c6c6653b26c7670e0f6b1da9ea`  
		Last Modified: Wed, 02 Nov 2022 19:31:11 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8d6923a043a793e468e7adb84dfe8e59e498c7ec421a7a5d045563d0f55c5f6`  
		Last Modified: Wed, 02 Nov 2022 19:31:12 GMT  
		Size: 3.7 MB (3675116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e572fb6172341fddd1f6b3353620c959e02c6e91878c938ba0b3cb37672fb664`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.0 MB (1956780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c36a3af33b545e0f76f6ac57ea341b57bd51c189de6bb09d0946fcc20ffc648`  
		Last Modified: Wed, 02 Nov 2022 19:31:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e562694e4f06ec88fbe8e579c9ca66a2f205012812ce19ea9d11d4eb2615a7`  
		Last Modified: Wed, 02 Nov 2022 19:31:07 GMT  
		Size: 2.2 MB (2199313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db891bdac11eb4ad276dce571884d2ceead2b0c4a1630b7323ede0719364336b`  
		Last Modified: Wed, 02 Nov 2022 19:31:05 GMT  
		Size: 2.5 KB (2493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89802ca4242938a62ea9e93dcc84679d6208be5a8ef8a7dbf368c196ddafc596`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b10a0c4c56eda5ee314ee192394ab23400a90fcf6536a7fa5eec78854ac46a`  
		Last Modified: Wed, 02 Nov 2022 19:31:40 GMT  
		Size: 68.7 MB (68655104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b25788d86165ab3008742f36bd0cd6bfb36679d1928144085e0b200ae38a9d`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa4f3538ccb9ee39af5e436a70e5c49fcb1724dead6cb95f3c0aa7942a62c12`  
		Last Modified: Wed, 02 Nov 2022 19:31:30 GMT  
		Size: 7.1 KB (7051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
