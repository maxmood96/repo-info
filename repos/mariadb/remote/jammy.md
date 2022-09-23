## `mariadb:jammy`

```console
$ docker pull mariadb@sha256:05b53c3f7ebf1884f37fe9efd02da0b7faa0d03e86d724863f3591f963de632c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:fe33500a347fbdb6f1b095d8d2803ff03fc822967bc59ecb0df6a03e88fbfde2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124059332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aee66fdc314a20fc7dffea84bcfabefad0999d6f14b85dca645eeedab1c7c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:35 GMT
ADD file:a7268f82a86219801950401c224cabbdd83ef510a7c71396b25f70c2639ae4fa in / 
# Thu, 01 Sep 2022 23:46:35 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:41:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 02 Sep 2022 03:42:07 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:42:07 GMT
ENV GOSU_VERSION=1.14
# Fri, 02 Sep 2022 03:42:19 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 03:42:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 03:42:28 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:42:28 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 02 Sep 2022 03:42:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 20 Sep 2022 22:19:52 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 22:19:52 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 22:19:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Tue, 20 Sep 2022 22:19:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 20 Sep 2022 22:20:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 20 Sep 2022 22:20:36 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Sep 2022 22:20:36 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 23 Sep 2022 19:28:03 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Fri, 23 Sep 2022 19:28:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 19:28:04 GMT
EXPOSE 3306
# Fri, 23 Sep 2022 19:28:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:2b55860d4c667a7200a0cb279aec26777df61e5d3530388f223ce7859d566e7a`  
		Last Modified: Tue, 16 Aug 2022 03:03:54 GMT  
		Size: 30.4 MB (30426706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf944e49ffa85996da499d5d92c328463b711fd3a1672b809e2824a964da9fb`  
		Last Modified: Fri, 02 Sep 2022 03:48:07 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020ff2b6bb0b679bc28ad3ec3d451993a1ef2282c86f87ca148774d73593a1cc`  
		Last Modified: Fri, 02 Sep 2022 03:48:05 GMT  
		Size: 3.8 MB (3765427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977397ae9bc646b6dcf2321014794f535cb5a74110c608b1d1c0986ee1eb1424`  
		Last Modified: Fri, 02 Sep 2022 03:48:05 GMT  
		Size: 2.0 MB (1992954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b361cf449d40803e89980d56903e81945ce9fa372a686ea76f4a9c7a646a8337`  
		Last Modified: Fri, 02 Sep 2022 03:48:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d26195015760a28953bf9d2ad8603a66f8508da28d9878f972ddf137a5b34d`  
		Last Modified: Fri, 02 Sep 2022 03:48:05 GMT  
		Size: 2.3 MB (2281503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296a47dd94359e3cf2394add8b9de63828e53d9d2195aa09d903a5e2143e6a9c`  
		Last Modified: Fri, 02 Sep 2022 03:48:02 GMT  
		Size: 2.5 KB (2492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe841bf5cfee395923288f40dd661dd1d9df9af1ca6ec813bcea16824425c6c`  
		Last Modified: Tue, 20 Sep 2022 22:23:30 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758db05dd9214e31c3ee31d800476499810deec933c88598a76f369ca49a45dd`  
		Last Modified: Tue, 20 Sep 2022 22:23:43 GMT  
		Size: 85.6 MB (85577482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c2c0a21c9e6c9172b933d9756ec6a740c27f1767b831eda8ccff0b599314abf`  
		Last Modified: Tue, 20 Sep 2022 22:23:30 GMT  
		Size: 3.5 KB (3494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc311b9359abd389f29c652201b34d770c735108a2205e930f07471cdb8e6a7`  
		Last Modified: Fri, 23 Sep 2022 19:29:16 GMT  
		Size: 7.0 KB (7048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:f7295af8e99919f4b730bc685bef599d13d9f1268834d3f18eaa924a1b3aa76f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118457650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2dd034b4753f6e1a75dc1678e595b0bc1030f4cc19557847167da3998b13ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:51 GMT
ADD file:550e7da19f5f7cef52c6ea160a33daa482f44df086ddecffca8ec9be6385b848 in / 
# Fri, 02 Sep 2022 00:57:52 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:25:50 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 02 Sep 2022 05:26:00 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:26:01 GMT
ENV GOSU_VERSION=1.14
# Fri, 02 Sep 2022 05:26:17 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 05:26:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 05:26:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 05:26:26 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 02 Sep 2022 05:26:28 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 20 Sep 2022 21:39:58 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 21:39:58 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 21:39:59 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Tue, 20 Sep 2022 21:40:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 20 Sep 2022 21:40:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 20 Sep 2022 21:40:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Sep 2022 21:40:27 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 23 Sep 2022 19:41:41 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Fri, 23 Sep 2022 19:41:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 19:41:42 GMT
EXPOSE 3306
# Fri, 23 Sep 2022 19:41:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:00f50047d6061c27e70588a5aab89adada756e87d782a6c6bd08b4139eb8ea10`  
		Last Modified: Fri, 02 Sep 2022 00:59:40 GMT  
		Size: 28.4 MB (28381340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0749552ddbb27b679c4c784814a6bc9cff4dea894b4c50ff08211ac33d7141`  
		Last Modified: Fri, 02 Sep 2022 05:33:56 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f3be11a3a90d15ce271dbf8b58dc49944d979b4199b6a9810b17688f071274`  
		Last Modified: Fri, 02 Sep 2022 05:33:54 GMT  
		Size: 3.6 MB (3593224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c93d9284a3d0f05825c9fdc3591a7d7d3ae34f1ae103b4ff077a235d40e0f`  
		Last Modified: Fri, 02 Sep 2022 05:33:54 GMT  
		Size: 1.9 MB (1898967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:232f4136dd4f7f7c1b1de60c1ce430dfdb5d873cdc0e8cf41ac08e1ece7077c2`  
		Last Modified: Fri, 02 Sep 2022 05:33:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884ccd89de31befb378b3fd447ebd5efc4fc67e5969c98f28f3df064a191ec01`  
		Last Modified: Fri, 02 Sep 2022 05:33:54 GMT  
		Size: 2.2 MB (2194638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea239af7d9b117acb387a6885623fe9b3dd8df83c1e1cd42c1e418f41e14ef3f`  
		Last Modified: Fri, 02 Sep 2022 05:33:51 GMT  
		Size: 2.5 KB (2470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5182594a555e5efa49816cb78b6ab39bcb6d1cb24532dcc7796582f506ee9a2`  
		Last Modified: Tue, 20 Sep 2022 21:44:30 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d864926508e2bc9f46736d08171e99bdf4f9b78a3b5eceff1cd269830d9040`  
		Last Modified: Tue, 20 Sep 2022 21:44:43 GMT  
		Size: 82.4 MB (82374297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8b571c7754193402bd7d0a37bb0362e54e3703af2cd1297840dd121d90371a`  
		Last Modified: Tue, 20 Sep 2022 21:44:30 GMT  
		Size: 3.5 KB (3492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eef15ee88dbaa7e07b8a3620ed82ee70b551dea34f3a0b524ed846f5fd4dd71`  
		Last Modified: Fri, 23 Sep 2022 19:44:13 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b022aa8611ae9951f27799b4258759afc1f9dd19bc69287f156745883bf522a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117047762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c7b12a9737e5b838f7a154737f0aba98232082e64ff274f824e278c958f99d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 01 Sep 2022 23:50:09 GMT
ADD file:39b6fa94f6e1300a6fc4b6094e8250c22ecaa6e7c9f934841765d45b919402c5 in / 
# Thu, 01 Sep 2022 23:50:11 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:52:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 02 Sep 2022 04:53:12 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:53:12 GMT
ENV GOSU_VERSION=1.14
# Fri, 02 Sep 2022 04:53:29 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 04:53:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 04:53:43 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:53:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 02 Sep 2022 04:53:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 20 Sep 2022 22:16:45 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 22:16:45 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 22:16:45 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Tue, 20 Sep 2022 22:16:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 20 Sep 2022 22:17:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 20 Sep 2022 22:17:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Sep 2022 22:17:54 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 23 Sep 2022 19:16:48 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Fri, 23 Sep 2022 19:16:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 19:16:49 GMT
EXPOSE 3306
# Fri, 23 Sep 2022 19:16:50 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9ef77d5e46df05bf9f34e5871097fd038295a2aa5e29f1806ac3a96aa2545b5f`  
		Last Modified: Thu, 01 Sep 2022 23:52:34 GMT  
		Size: 35.7 MB (35721187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55324944c013f5e152ef0fad27126a86f0a45cfff228ed5d376984c8bcb18dbc`  
		Last Modified: Fri, 02 Sep 2022 05:04:43 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc5813595f57876629a096fc5630c832e5d23f1a6f8c52b86f94b395dd72973`  
		Last Modified: Fri, 02 Sep 2022 05:04:42 GMT  
		Size: 4.5 MB (4503005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf53136ad37739b4c4b6d5c9c41623f06a89e1c954299e6487b758572c2129b6`  
		Last Modified: Fri, 02 Sep 2022 05:04:41 GMT  
		Size: 1.9 MB (1922006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e9deaa9bc92d6868ca60db4ace55d593c6da8f7dd776648377d6df75bbcdb2`  
		Last Modified: Fri, 02 Sep 2022 05:04:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88549712edded06fae8bfa5c56fae89c47664fc83e5b4a957c2c2764649ebff`  
		Last Modified: Fri, 02 Sep 2022 05:04:42 GMT  
		Size: 2.4 MB (2389323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a4751f2b2dee4c43d237fe7b4ce6e1273b2374fcce6496c681cb525e8d26c1`  
		Last Modified: Fri, 02 Sep 2022 05:04:38 GMT  
		Size: 2.5 KB (2494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32cacb57e8f72eb46a663e8ec3a59d6ea06db50378afd667b83c17f07953c85`  
		Last Modified: Tue, 20 Sep 2022 22:23:48 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c935a145862c66ac2b22a067d93059fae967fdd1d184c4e8aa4648bd41ff103`  
		Last Modified: Tue, 20 Sep 2022 22:24:07 GMT  
		Size: 72.5 MB (72496972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2794a56f7dd0b838f1bfe09b22c36d4a7e12515dc808c03a1868d4d003948f63`  
		Last Modified: Tue, 20 Sep 2022 22:23:48 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d789792fe800fe9ebb936481f3f9ec41b99fdb1abc5156b7d3d0f80e92bec08c`  
		Last Modified: Fri, 23 Sep 2022 19:19:22 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:04d3092875872655a72d6b7208fcf4d392d21b990d6a669c98632f1ec1ed72d9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105147152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f1bd5af9c257a93f87daf247dd3859975e739a54798ba7a5447349df0791d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:25 GMT
ADD file:aabc057fd7b1b1f9b4b729222b6dc90e98f846a65bfee1ee57cc899b6cee5a10 in / 
# Fri, 02 Sep 2022 01:03:28 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:18:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 02 Sep 2022 02:18:15 GMT
RUN set -ex; 	apt-get update; 	if ! which gpg; then 		apt-get install -y --no-install-recommends gnupg; 	fi; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:18:15 GMT
ENV GOSU_VERSION=1.14
# Fri, 02 Sep 2022 02:18:24 GMT
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends ca-certificates; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 02 Sep 2022 02:18:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Sep 2022 02:18:31 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:18:32 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 02 Sep 2022 02:18:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -ex; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export $GPG_KEYS > /etc/apt/trusted.gpg.d/mariadb.gpg; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -fr "$GNUPGHOME"; 	apt-key list
# Tue, 20 Sep 2022 21:41:56 GMT
ARG MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 21:41:56 GMT
ENV MARIADB_VERSION=1:10.9.3+maria~ubu2204
# Tue, 20 Sep 2022 21:41:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
# Tue, 20 Sep 2022 21:41:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 20 Sep 2022 21:42:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.9.3/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	apt-get install -y 		"mariadb-server=$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	if [ ! -L /etc/mysql/my.cnf ]; then sed -i -e '/includedir/i[mariadb]\nskip-host-cache\nskip-name-resolve\n' /etc/mysql/my.cnf; 	else sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/[mariadbd]\nskip-host-cache\nskip-name-resolve\n\n\2\n\1/}'                 /etc/mysql/mariadb.cnf; fi
# Tue, 20 Sep 2022 21:42:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 20 Sep 2022 21:42:35 GMT
COPY file:03ef406a869fc1d453794e4b0c7e8da3dee6816b3267c63fa57c93b4a38c8c52 in /usr/local/bin/healthcheck.sh 
# Fri, 23 Sep 2022 19:41:55 GMT
COPY file:2a785aba6c73dfab59047fdbb26917b1ca4aa8f73ea780e92ea0891a1e9918df in /usr/local/bin/ 
# Fri, 23 Sep 2022 19:41:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 19:41:55 GMT
EXPOSE 3306
# Fri, 23 Sep 2022 19:41:56 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a32e6a15a6635185097921b9d08997d505b6b6500b6c142ad8e718d87c45ffad`  
		Last Modified: Fri, 02 Sep 2022 01:05:01 GMT  
		Size: 28.6 MB (28643161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75a83a742f8905e65d86bab1137abea13cf130c3c52de601dd27fc4c4188ad7`  
		Last Modified: Fri, 02 Sep 2022 02:23:46 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0074f95048477359d16a331130ff329c74b549bcc5d7a97cd5559fcfe9c7464`  
		Last Modified: Fri, 02 Sep 2022 02:23:45 GMT  
		Size: 3.7 MB (3674479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792e98156ec6717f9a09ef69964b1441fc52ea8407babf26638a445cfbca24a7`  
		Last Modified: Fri, 02 Sep 2022 02:23:45 GMT  
		Size: 2.0 MB (1956114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f52d5f8a1d48c335871d777bb6305d30ca6e0d35472d729f97839e5118e1ed`  
		Last Modified: Fri, 02 Sep 2022 02:23:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b51775573dc421f5d01c30c0385676817ad4cd3ed88f8c69fdfe498f57a5b39`  
		Last Modified: Fri, 02 Sep 2022 02:23:45 GMT  
		Size: 2.2 MB (2200620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c5f2dd2c4f8a5fcba9a6bd048360e2483d370947a8e8499b83147d0878d31d`  
		Last Modified: Fri, 02 Sep 2022 02:23:44 GMT  
		Size: 2.5 KB (2491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750bf5184269e7cd78a1658d1b4df12c568ed012d2a05d666c82664ea9d7e5d8`  
		Last Modified: Tue, 20 Sep 2022 21:46:07 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05938b06b8a011fe416307bd6b15e99ec5bff99dc72be582945fdb974c2ee70b`  
		Last Modified: Tue, 20 Sep 2022 21:46:16 GMT  
		Size: 68.7 MB (68657509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebf9c17772963d1ecd9e9d9d6d0515eb68d20d92ad22ffd82b4d64307b4f978`  
		Last Modified: Tue, 20 Sep 2022 21:46:06 GMT  
		Size: 3.5 KB (3495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c405f598eb8158e8ae12f4c55caf7f9dcea715c74e695644bccb4e281d34af`  
		Last Modified: Fri, 23 Sep 2022 19:43:46 GMT  
		Size: 7.1 KB (7052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
