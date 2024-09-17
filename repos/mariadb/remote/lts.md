## `mariadb:lts`

```console
$ docker pull mariadb@sha256:6be1a7bcd68d19ddef1d05eb0bbcccc4d22069ef75b0071ee261fb530dcafdc2
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
$ docker pull mariadb@sha256:92b5b7f09a2196801459901deadf442c86345212dc6f7b24866ea9d7b39a7b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.6 MB (124647457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5989c279833583ac3757805b5d4fa5fcf85652dcd708f5c04ff701b4286ae09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b825f2f598edb7aad0813d643be08fd79c5b3756bb89b95a53b42ccd203384`  
		Last Modified: Tue, 17 Sep 2024 00:59:27 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fbab539cba71f7a7a01deea8d8d7ab5157dd78f2f96fdefd53d158b175b329`  
		Last Modified: Tue, 17 Sep 2024 00:59:27 GMT  
		Size: 7.8 MB (7755585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e093b2f3a650549515bb7cc6ca79dff1168b5e29406381d16b15ab39040f1e38`  
		Last Modified: Tue, 17 Sep 2024 00:59:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eda8ef6cc46d35914e73abafe1d24cbbe474fe97d829dbff232d40f207c7a0a`  
		Last Modified: Tue, 17 Sep 2024 00:59:27 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f9eb534a6502944f297f1605355f15df76980d96accc17d08484d37dcc1e8e`  
		Last Modified: Tue, 17 Sep 2024 00:59:31 GMT  
		Size: 87.1 MB (87127859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b6ad6ca6cefcb73d8341784aee0055e6c1470093c679fbd1e6ece1d82a53e9`  
		Last Modified: Tue, 17 Sep 2024 00:59:28 GMT  
		Size: 4.0 KB (3977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaaa8c72e7e483b8f3cf4d16638eedc78e7effdf026fb45d41b8f383cc5a919`  
		Last Modified: Tue, 17 Sep 2024 00:59:28 GMT  
		Size: 8.4 KB (8421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:cba763461edaf536689fc0b8e514575eec324467af43444de612b6401eb88c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e9e1d40543c11023f236a91c6991552d526607d4b20b7f87e328375546ed69`

```dockerfile
```

-	Layers:
	-	`sha256:c2b9aae66f642c3a6426a8470238db00334d4ae295585a9c3383a12f0d0d94cd`  
		Last Modified: Tue, 17 Sep 2024 00:59:27 GMT  
		Size: 4.1 MB (4061991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1751316b2f3e39094d6e73ad38fac44f649a15158b19964b7e13f9dff87d964a`  
		Last Modified: Tue, 17 Sep 2024 00:59:27 GMT  
		Size: 30.4 KB (30380 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:2f0975bf78c12f81b5a6f65386934ec2b317e701c49dcb826177c477cfff4156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120239244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816a9ea3107335e5533ba055ce0f96edbee623baa625f56d23ba6198b5c96b7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 01 Aug 2024 15:33:35 GMT
ARG RELEASE
# Thu, 01 Aug 2024 15:33:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 15:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 15:33:36 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 15:33:38 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 01 Aug 2024 15:33:38 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3291cf9bba67c91822cecd3b5d419bcd936d852c4dc5aaff76a738e732e9b49`  
		Last Modified: Sat, 17 Aug 2024 03:10:16 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3969bcb710ce8552dea9c7e3618233b26b0c230eaab39c5156ff724dac851c`  
		Last Modified: Sat, 17 Aug 2024 03:10:17 GMT  
		Size: 5.1 MB (5129577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a948c6a0af0cb95e3f26ce3ba4e7832d8149d7d99eb58c32a79321f5a5c4ecdf`  
		Last Modified: Sat, 17 Aug 2024 03:10:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f622f011c91ee772ce62cdd01d016111997539d2501f381e911ef0c385a7011c`  
		Last Modified: Sat, 17 Aug 2024 03:12:04 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac5bf87c0c814e7eee8f4d2d3d6c586d5f716bd0854dfe514c37145be10af20`  
		Last Modified: Sat, 17 Aug 2024 03:12:07 GMT  
		Size: 86.3 MB (86251789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89327d032910e9f12c68048e8049ca29f872d3f9629562053340373afa2732`  
		Last Modified: Tue, 03 Sep 2024 19:00:20 GMT  
		Size: 4.0 KB (3977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55044a584ebdf19dc29afe7e81dec26534f28f200e547d0d666f15f40d2b738a`  
		Last Modified: Tue, 03 Sep 2024 19:00:20 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:28f3190474670bf878dde6a38213e2af5069ddc55c0102b4fbe1cfcc932039f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4097401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b824918449eb01e2e2706dd717057b6401159db4d1d9aaf6782295820c97153`

```dockerfile
```

-	Layers:
	-	`sha256:479a45a5cbf32ca0b5958422268b9d18c4bbb3098b253eba5219e67ef4b74304`  
		Last Modified: Tue, 03 Sep 2024 19:00:20 GMT  
		Size: 4.1 MB (4066696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff49a28cea39666f0d7c0def08a5c8fcdcff80b6636694e58bdd1ee580b4840f`  
		Last Modified: Tue, 03 Sep 2024 19:00:20 GMT  
		Size: 30.7 KB (30705 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c7dcb54e13ad7de5091c09ff612ac522079083bf395076632712d61158cc2b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135451789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0475d3da07d30538b33292d4470767c90be175aead64560afc1d58a022a2df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acf3d3aea23d3ca827d3c9c02b6bbceefd98b17cd3b5d74128e605f9a4bbd8a`  
		Last Modified: Tue, 17 Sep 2024 01:37:05 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f1909086bf4104f7007c5f7c0be887fb573b5554ea0ee0293fb9c4d2ff50ab5`  
		Last Modified: Tue, 17 Sep 2024 01:37:06 GMT  
		Size: 8.6 MB (8563087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:269d1f5fa1bfae1678bdabf19ec94a6e15241630591de537b6c6c3ff46a461ea`  
		Last Modified: Tue, 17 Sep 2024 01:37:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f4ebde8c7e0dc44dec11741cad99addd6250dc173a16472f3f548fdd99ba80`  
		Last Modified: Tue, 17 Sep 2024 01:39:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e08d0f88029fa09559ee1fdf38f1638cae481faae428bbc2a59bfacfab9e3d7`  
		Last Modified: Tue, 17 Sep 2024 01:39:54 GMT  
		Size: 92.5 MB (92482158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fded52d738cb88297101a84a3e996aa385c6769518fae212a029e7b7796dd71f`  
		Last Modified: Tue, 17 Sep 2024 01:39:51 GMT  
		Size: 4.0 KB (3978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ec2a88b22e49688cf8c35be1af6261aeb6d19a51f0a8ee42f9de843056481c`  
		Last Modified: Tue, 17 Sep 2024 01:39:51 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:fa2b4f396645f4eb0e6e9c6b3ef2722b83193ebd9e1b66454ecfb52fcb2497db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4100165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925d5023a725432f0fb770f9da3a5cefec186543f0daff86ea20a7c62213504d`

```dockerfile
```

-	Layers:
	-	`sha256:e37a5d1ee4531d676e22a77ea451fe0f902b069d645599b30b6c420514c6543a`  
		Last Modified: Tue, 17 Sep 2024 01:39:52 GMT  
		Size: 4.1 MB (4069727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b76e55140a8bd3b0d97ef9dd366003736780adb13a685fb06cfd7bc2e5e7cef`  
		Last Modified: Tue, 17 Sep 2024 01:39:51 GMT  
		Size: 30.4 KB (30438 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:38814b72c1ffb000cb951444413356f59623e0f87ce549cfa8434868f304a994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130985659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115cc660b1647afc6b41ca634cff68baa57cb048ab2958ffe209784810635e68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:05 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:08 GMT
ADD file:55ce2834630c73439274688061a6b2ad0d6952c2435dc51250026e14f139275d in / 
# Tue, 27 Aug 2024 15:55:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Sep 2024 02:17:54 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV GOSU_VERSION=1.17
# Tue, 03 Sep 2024 02:17:54 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENV LANG=C.UTF-8
# Tue, 03 Sep 2024 02:17:54 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 03 Sep 2024 02:17:54 GMT
ARG MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ENV MARIADB_VERSION=1:11.4.3+maria~ubu2404
# Tue, 03 Sep 2024 02:17:54 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.3+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.3/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Sep 2024 02:17:54 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 02:17:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 02:17:54 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 03 Sep 2024 02:17:54 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:43b981c5954bdfa7626a4bec06cf075f7bb2df6698b5c0b42b5b5770109637c6`  
		Last Modified: Tue, 27 Aug 2024 17:08:36 GMT  
		Size: 30.0 MB (30024629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2712ca6f3873c2145d1a291b0d408a68add66fd54ae0a978612a1c3562c8e17e`  
		Last Modified: Tue, 17 Sep 2024 02:16:56 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e5b99e7ca48946c95b0839303199b77c809240d369b1c44d6bef242276016c`  
		Last Modified: Tue, 17 Sep 2024 02:16:56 GMT  
		Size: 7.6 MB (7599715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ce2b4ac53e38de73d1f4dd5b15c3bfe0383e1338bbd31b3db09535d4095eae`  
		Last Modified: Tue, 17 Sep 2024 02:16:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3fe6114834cdb39eca8be1ee03a25d2ef19cc8383ea2a410c999a16dd6879`  
		Last Modified: Tue, 17 Sep 2024 02:19:22 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68efefe1484e4b8f2e6d7fbe27a6b82be5b9d3c39d3299c43f4b31a49266dcda`  
		Last Modified: Tue, 17 Sep 2024 02:19:23 GMT  
		Size: 93.3 MB (93347115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43962b76b280bc7055e31d25a5dd773ca96c8d9ecb487caf8afaf7a0a70747d3`  
		Last Modified: Tue, 17 Sep 2024 02:19:22 GMT  
		Size: 4.0 KB (3980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7452f2cb5504d2621f1c0d9b3a0f966d36de76b58cafdd4c745600ca46cd58a1`  
		Last Modified: Tue, 17 Sep 2024 02:19:22 GMT  
		Size: 8.4 KB (8427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:3dd0d353afdaee69c76dda78a674b0740552e53e98c01a46da2afb934b048e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4094099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae93e8859c35d6bfd567fa9acdba10bd03cec58b44448c6663fa5cd4347d0fc`

```dockerfile
```

-	Layers:
	-	`sha256:1ce1559056a26de3048b5aa44d57af572e5f5c09f602c3376a77056690409883`  
		Last Modified: Tue, 17 Sep 2024 02:19:22 GMT  
		Size: 4.1 MB (4063719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106b5d24a1b5b9979ea42c66185c3e6fa86e79e44d816b8e35799df9bd49cf06`  
		Last Modified: Tue, 17 Sep 2024 02:19:22 GMT  
		Size: 30.4 KB (30380 bytes)  
		MIME: application/vnd.in-toto+json
