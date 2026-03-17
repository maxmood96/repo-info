## `mariadb:noble`

```console
$ docker pull mariadb@sha256:e16f61b8f6ed25111adbb1c5c19bbc2904efc8ed14029999af0cbe1c7ae18bf1
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
$ docker pull mariadb@sha256:d54593c6b915461645fc717e2e8e673904bf04f47647d3243c726737db951748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106784212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a5cac035622f78e3c8f3c08803ca983575b7811a8dc69c22251ef4f40fafe2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:40:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Mar 2026 01:40:43 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:40:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Mar 2026 01:40:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:40:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:40:43 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:40:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Mar 2026 01:40:43 GMT
ARG MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 01:40:43 GMT
ENV MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 01:40:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
# Tue, 17 Mar 2026 01:40:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Mar 2026 01:40:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Mar 2026 01:40:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Mar 2026 01:40:59 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Mar 2026 01:40:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:40:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:40:59 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Mar 2026 01:40:59 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9feb2f7987f3047aaccbbcb307c9477b4b574973026293a0bd18752dab60554`  
		Last Modified: Tue, 17 Mar 2026 01:41:13 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2712d6dc880726c05587828ee1106a600817b22957b2b6cee88ab8f49e410d`  
		Last Modified: Tue, 17 Mar 2026 01:41:14 GMT  
		Size: 5.3 MB (5288026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b90120c6661d46a231faa61de9ad9087f358c86200ea0a0da8fa1cf6ee3e04`  
		Last Modified: Tue, 17 Mar 2026 01:41:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e06fb80927d25dbef391725465c5257c509717688f35550d0e39b2906b394d`  
		Last Modified: Tue, 17 Mar 2026 01:41:13 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acc8dacec090800da7542688d2d1e83f057e59a547015419bfc6d616908316c`  
		Last Modified: Tue, 17 Mar 2026 01:41:16 GMT  
		Size: 71.7 MB (71749973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef13546effa3fce581a3e64265b357bba7a80bc9514a64676ba79eda2b847a3f`  
		Last Modified: Tue, 17 Mar 2026 01:41:15 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a71e654f6a4f785e4e5c1ec5a1ad0392ab72a1555e48fc291ba83eac979b83`  
		Last Modified: Tue, 17 Mar 2026 01:41:15 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:eb1fcb02095987af507382b732f444a21f7f6920cf3f922afb7dc6bae867a26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc6ba5a4957481beeddeb0d9839ba7810f4a42e753e9b18ebf663d5cc7090f6`

```dockerfile
```

-	Layers:
	-	`sha256:fd951202f379cd90ad989113b6af8e3376c03bdcc16ec397c8e76a2a2e537784`  
		Last Modified: Tue, 17 Mar 2026 01:41:14 GMT  
		Size: 4.3 MB (4273723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d29571c5e761d9989eedf222979d427da386a4bb13fc7ffed97cb37c37607c6`  
		Last Modified: Tue, 17 Mar 2026 01:41:13 GMT  
		Size: 31.4 KB (31440 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9ea003c508b9d38226f61199fcd0def6423bd2d301160f2bd2ddfb395a9d5b9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104694337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592415c7857ffe1d787094b5fa6b74716db8f57d338de88d0f6f8700459f57e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:41:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Mar 2026 01:42:07 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 01:42:07 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Mar 2026 01:42:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 01:42:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 01:42:07 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:42:07 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Mar 2026 01:42:07 GMT
ARG MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 01:42:07 GMT
ENV MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 01:42:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
# Tue, 17 Mar 2026 01:42:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Mar 2026 01:42:25 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Mar 2026 01:42:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Mar 2026 01:42:25 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Mar 2026 01:42:25 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 01:42:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 01:42:25 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Mar 2026 01:42:25 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3a0750fecce1a128d72c1bbf5573d653a7713039df32cb2c776a335be4252`  
		Last Modified: Tue, 17 Mar 2026 01:42:41 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2198c67f0b26b5ab3d71545dcd71b103900b41b1d7769e41f703a4aa353225`  
		Last Modified: Tue, 17 Mar 2026 01:42:41 GMT  
		Size: 5.1 MB (5098380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6960ee89ead83d757b22f6e80772188f3879bab9781c55971a0be376ee67799c`  
		Last Modified: Tue, 17 Mar 2026 01:42:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b12883913a00be4b9a95ede1ab8a5fbff23f3abd671e8329f680788f05f614`  
		Last Modified: Tue, 17 Mar 2026 01:42:41 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e9eeed8c773f7e1263fce094c53bbbb4b44a15fed7213243c914ebae802014`  
		Last Modified: Tue, 17 Mar 2026 01:42:43 GMT  
		Size: 70.7 MB (70712018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c2ac162ca1962772dd60141c8b6ac3af88d9cbab55996d655ba22f0ea54d30`  
		Last Modified: Tue, 17 Mar 2026 01:42:42 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2514f72c48efc6cebaa5f8b27cec937e7c5e52c075089c1508617a70148d4ca`  
		Last Modified: Tue, 17 Mar 2026 01:42:42 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:3e635614fa8749f828ba199d8964c21769075c637920b98c7f4662d7bd439ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6a8cf75547125fd4c5384a721e6f68b17d4bdb9e004a61069d50978a2365e8`

```dockerfile
```

-	Layers:
	-	`sha256:09808b4040fea29ed25f07212ce2fb378146a023923610b05181156c4ad98b6e`  
		Last Modified: Tue, 17 Mar 2026 01:42:41 GMT  
		Size: 4.3 MB (4281000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82457b23551bbbb53af580e69f54ce114e60459e75bc36e673ba808b176288b1`  
		Last Modified: Tue, 17 Mar 2026 01:42:41 GMT  
		Size: 31.7 KB (31653 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:4258e3b8c7fe2d7634440b995f1a51d77a82d088bd4e432c2373d3bbebdc6e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117047008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc517a24f5b6ff731506d15a18f5a52b8a53aed10f34cacdb51fda182084dcf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:02:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Mar 2026 09:02:45 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 09:02:45 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Mar 2026 09:02:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 09:02:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 09:02:46 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 09:02:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Mar 2026 09:02:46 GMT
ARG MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 09:02:46 GMT
ENV MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 09:02:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
# Tue, 17 Mar 2026 09:03:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Mar 2026 09:04:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Mar 2026 09:04:11 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Mar 2026 09:04:11 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Mar 2026 09:04:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 09:04:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 09:04:11 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Mar 2026 09:04:11 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3e9f0ac598eca4e14498b439afe700ee1c6f6ad559e5c088d8e7a313331d84`  
		Last Modified: Tue, 17 Mar 2026 09:03:51 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd371de8a5eba369d727dec51cbcdad80d077fe9b8c8e7a700802f9ed238648`  
		Last Modified: Tue, 17 Mar 2026 09:03:51 GMT  
		Size: 5.9 MB (5927347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4fd8870eac0f6c8ea95576bfe2060405f652fd02060b32b13491d73a4ce642`  
		Last Modified: Tue, 17 Mar 2026 09:03:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac002149d6568148c5f6c6840237e72eb7eba6901f7ca500d6717380a8be3138`  
		Last Modified: Tue, 17 Mar 2026 09:04:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebcc60494c8974282c98446d75fdba2e00f2dba05e84f2a13e1faa2abadc321`  
		Last Modified: Tue, 17 Mar 2026 09:04:47 GMT  
		Size: 76.8 MB (76795380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502490583d88ec7b46fbfba9d98a0a88b30b0b068a174c255671ea507b94e182`  
		Last Modified: Tue, 17 Mar 2026 09:04:44 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29369d68fe4611ce25a006a8e0c8404569388a4676f0c9dd563aec480026c41e`  
		Last Modified: Tue, 17 Mar 2026 09:04:44 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:3314ff38db52782e58dc5ad1ad3afc02183883f32bec8080ad41b4321e7ed0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b6e99b57358a874497c02614053e500b69973d56e9bc05ad8cb54b282b92e5`

```dockerfile
```

-	Layers:
	-	`sha256:6b0c7df2772a773d4ea2e94d662ae504fefd00ff4ddabc99fc216ef5a987f687`  
		Last Modified: Tue, 17 Mar 2026 09:04:45 GMT  
		Size: 4.3 MB (4281658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4427fee3dc55b3f109b92c91a06b45229be590111b6116de3786dfde6a0d2753`  
		Last Modified: Tue, 17 Mar 2026 09:04:44 GMT  
		Size: 31.5 KB (31517 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:123fe80ec3a9ab2aeff016422cca713737f891697e6d294591948d076a80dd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.2 MB (112211538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e6a64a1f74b1a7495c5f4f2c5da5e38559e211fb8e14eedd3adc2cfa4aaecf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:34 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 17 Mar 2026 02:34:52 GMT
ENV GOSU_VERSION=1.19
# Tue, 17 Mar 2026 02:34:52 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 17 Mar 2026 02:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 17 Mar 2026 02:34:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Mar 2026 02:34:52 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 02:34:52 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.2.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 17 Mar 2026 02:34:52 GMT
ARG MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 02:34:52 GMT
ENV MARIADB_VERSION=1:12.2.2+maria~ubu2404
# Tue, 17 Mar 2026 02:34:52 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
# Tue, 17 Mar 2026 02:35:29 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 17 Mar 2026 02:35:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.2.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.2.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 17 Mar 2026 02:35:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Mar 2026 02:35:44 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 17 Mar 2026 02:35:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 17 Mar 2026 02:35:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Mar 2026 02:35:44 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 17 Mar 2026 02:35:44 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414ac4daf3326a50b6ac078ce4f761470d5ea0b4c0e7eeb0cf2d383be614dce1`  
		Last Modified: Tue, 17 Mar 2026 02:35:30 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87634c8077a4cef954bd991ca6d3305283f09240004ab288d0c1ce2658fbaf5`  
		Last Modified: Tue, 17 Mar 2026 02:35:30 GMT  
		Size: 5.4 MB (5443692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92914b34f52e84f0bc55ca2bae4c0ddff62e3556476dbe01d3eb26142395c78c`  
		Last Modified: Tue, 17 Mar 2026 02:35:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3b3ebdf3498ae8b1717faf9b92a48af3d8e79815be9995f8ed47bb74901d10`  
		Last Modified: Tue, 17 Mar 2026 02:36:10 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95407bb484bc1b963ed53c41c20dcdd225dbce9b78d21e5f643ba4f29039eea7`  
		Last Modified: Tue, 17 Mar 2026 02:36:12 GMT  
		Size: 76.8 MB (76843239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3a1d14c831f80bf1fbaa534365b92f22a1d4a8e1d734e8483f6113332dd84d`  
		Last Modified: Tue, 17 Mar 2026 02:36:10 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614cd55902c3ef3b33e051e513b1ff3b4524d021acde4db99a78b7738f864d96`  
		Last Modified: Tue, 17 Mar 2026 02:36:11 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:683efe012f8f74e9da960ff2e24bb758f1b967ec5701ed7ff5cfc9e117c8eac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d93668dd966895869fa2402310b1ffa8d83a02381235bb597989a01bb9f860bb`

```dockerfile
```

-	Layers:
	-	`sha256:bc44f53ee545f97c9d0fd581f4d09682000615e571c129b7a28518c91be2a45a`  
		Last Modified: Tue, 17 Mar 2026 02:36:11 GMT  
		Size: 4.3 MB (4275442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65b2a3c6b3f8f42330714355c169d09eabcbe3b0518e8847f022365fd07d2c6e`  
		Last Modified: Tue, 17 Mar 2026 02:36:10 GMT  
		Size: 31.4 KB (31441 bytes)  
		MIME: application/vnd.in-toto+json
