## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:e1980e8fa806278c0a04f9372ffded67756768f0a510f9643bcf84a64f19436a
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
$ docker pull mariadb@sha256:b252c09a2ffe51d7c27fe198c0ade3db76c4695ca3ac08e0e7364ea083edda0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122672097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68a2ddacd8eeb337bf0de665d2cab81beccc589deaeb4e346cb8267a8682e73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 04:29:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 15 Aug 2024 04:29:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV LANG=C.UTF-8
# Thu, 15 Aug 2024 04:29:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Aug 2024 04:29:43 GMT
ARG MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ENV MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Aug 2024 04:29:43 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 04:29:43 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Aug 2024 04:29:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b7a73818199a667cf1f87c208ab13356637adb73ec93155bf5354a7f9f81cd`  
		Last Modified: Thu, 15 Aug 2024 17:59:16 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077830b27b2da552553fc2a020764a7ccce888337a6f7febb6c58228e48be1fd`  
		Last Modified: Thu, 15 Aug 2024 17:59:17 GMT  
		Size: 5.6 MB (5648067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5236d9c82d23d4129100030d31c45592e3be1d9ca25c93dac240b052d16a83ad`  
		Last Modified: Thu, 15 Aug 2024 17:59:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46cda49702d6da853633586a518dfa5da73d22f081519a22df5b96f74708d4`  
		Last Modified: Thu, 15 Aug 2024 17:59:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e0315938cb0e5f53df58fe3caa4a91da4c558bf29160b6c69bf3c592affca0`  
		Last Modified: Thu, 15 Aug 2024 17:59:20 GMT  
		Size: 87.5 MB (87475586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264f0c0a09cb60e053d249cc5eb6236b3b69cd6a774be5d43b3aacd38cf2d056`  
		Last Modified: Thu, 15 Aug 2024 17:59:17 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ff63f81d7632d9fc83bd5e0740b46eb66737d9f57eb2fe47b54d2ac2b6da4f`  
		Last Modified: Thu, 15 Aug 2024 17:59:17 GMT  
		Size: 8.4 KB (8377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:bbdf4b3630c2b72f6eddcc8da7ee57cd406569925073a3b4b5f26dce624453f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4621266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdc6966c14d7e355353b8b49ba2d7ba3b4e25571a2ceabd5f3e6328c5d075e4`

```dockerfile
```

-	Layers:
	-	`sha256:afb706008833e6cbdb31f3ae01cc66128830582351d5c3b188f445cd02304bee`  
		Last Modified: Thu, 15 Aug 2024 17:59:17 GMT  
		Size: 4.6 MB (4590839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5af3b187ad9205a4845216e10067c6cd981c51eb11bb9f0eab8248d828a3d7fb`  
		Last Modified: Thu, 15 Aug 2024 17:59:16 GMT  
		Size: 30.4 KB (30427 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:538a4cc4fc509e8513800be01cd4fe23e9b7a5bebe9b5e4fd76441e2810ec728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.1 MB (117089860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7219bfac7529d64e8530b6ee72b93cb6a3e107adb22cbee0ae0b999246f2f8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 04:29:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 15 Aug 2024 04:29:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV LANG=C.UTF-8
# Thu, 15 Aug 2024 04:29:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Aug 2024 04:29:43 GMT
ARG MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ENV MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Aug 2024 04:29:43 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 04:29:43 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Aug 2024 04:29:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a772fa2d99bc1716f63fc1a42b8ed67415df81199e710d07c1732f618eb8838`  
		Last Modified: Mon, 12 Aug 2024 17:05:01 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ef21b649a46aaef30881a18a430f81fbb8b54f6845c8dd451a7c1f2b1baa3`  
		Last Modified: Thu, 15 Aug 2024 18:27:31 GMT  
		Size: 5.5 MB (5461420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3494322cc5e08941689a3e6f8b544946704e9e0fe555c314a8bcc5cd5ffcc8b`  
		Last Modified: Thu, 15 Aug 2024 18:27:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b325b69266ffea604887b246945969ea4b38c83546b3138f1676250f1ad75f`  
		Last Modified: Thu, 15 Aug 2024 18:30:24 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10dd9151d3123ff1d959f4910701f7c89ace008a113cad9323e83fdce323b0d3`  
		Last Modified: Thu, 15 Aug 2024 18:30:27 GMT  
		Size: 84.3 MB (84254028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739fda6f79fb607caea67fab9a557f1d8bd4d768503e4a4b19a80f08f8ab2980`  
		Last Modified: Thu, 15 Aug 2024 18:30:24 GMT  
		Size: 3.8 KB (3840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ccbaa5c2c1f098a61553302c81770aaf324fae5d27e21fd48c3f46c1db4231`  
		Last Modified: Thu, 15 Aug 2024 18:30:24 GMT  
		Size: 8.4 KB (8377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:4e5ffbf24a937c376232b0082bb64e0d2fd9aca9a8f1a9aa42802f8e88222bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4628031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c941f8167b15b7f1d18d50a8352da0b85dbcdee2324b595469499592d4f55add`

```dockerfile
```

-	Layers:
	-	`sha256:824ac0a59a94591a79a14ad0135fea26715e48575cdf9c68135ee0f185a7bb19`  
		Last Modified: Thu, 15 Aug 2024 18:30:25 GMT  
		Size: 4.6 MB (4597280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d935b83c2e0fa436c71eba2c6630547ab8820825eb252e704d1208662c2c904`  
		Last Modified: Thu, 15 Aug 2024 18:30:24 GMT  
		Size: 30.8 KB (30751 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:5ae6ca38f063cad2ce2a276d35e8ded52bb667d1ca35827ebc4ddade56cf30da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130740539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6abf5c13908f953da43a9827fc82cc1e9290b032e1eb1a56e605081fd38e2f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 04:29:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 15 Aug 2024 04:29:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV LANG=C.UTF-8
# Thu, 15 Aug 2024 04:29:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Aug 2024 04:29:43 GMT
ARG MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ENV MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Aug 2024 04:29:43 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 04:29:43 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Aug 2024 04:29:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a68de480ee27a13b745474f0f1c9c0022c8ba4329cc29257b341c9497431e1`  
		Last Modified: Mon, 12 Aug 2024 17:08:02 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6298948b05aa623e5c6973178b72def44c03d6172d1c8a389b9109b8361b32`  
		Last Modified: Mon, 12 Aug 2024 17:08:03 GMT  
		Size: 6.1 MB (6079892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1177f2bb34a0d3850674762fa77b2099e6908330b7dbe419455e344e3da19aef`  
		Last Modified: Thu, 15 Aug 2024 18:33:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bf2054b1ba18793309835eb3d7abd319cbd8e0de513fedea30bca95d32a0aa`  
		Last Modified: Thu, 15 Aug 2024 18:37:49 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555898464e19cf108acc379834c7d1393565a7cce3500462b1a76600480cab1b`  
		Last Modified: Thu, 15 Aug 2024 18:37:52 GMT  
		Size: 90.2 MB (90185171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff43689e99a9f9c094f0ad9b8611615e1e2fe4dc93b0fb6fe616023736bd53`  
		Last Modified: Thu, 15 Aug 2024 18:37:49 GMT  
		Size: 3.8 KB (3843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bea51bb44e9ecd1be41e08e3c29f14d108dca3af029b0cb2b6b0a274c3e9ff`  
		Last Modified: Thu, 15 Aug 2024 18:37:49 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:3a5ce7eccff1823f81e80599b2025b9b8d8abb88585f13cf3a5381bf773d20a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4628955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865e9239c57ff1f392b256a25cf197b9135416c5f415e243bafa1b7dd5fac0af`

```dockerfile
```

-	Layers:
	-	`sha256:14dafb59a61658176aab1c6b11ee50efeb20be40be57516ad57191ce5a9f60aa`  
		Last Modified: Thu, 15 Aug 2024 18:37:50 GMT  
		Size: 4.6 MB (4598470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:538c24540a1e546212103f9b6e4d66e2746344cc568be936a55b739ffd9cf690`  
		Last Modified: Thu, 15 Aug 2024 18:37:49 GMT  
		Size: 30.5 KB (30485 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:29161df23994ccf65f9cfe53b6d89c73674816301606679570cb494ba0e328ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121619038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c406f8d1642d43c1a904e28c85781e6296a4a73668c55412981d2b460248279`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 27 Jun 2024 19:26:47 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:26:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:26:47 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:26:50 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 19:26:50 GMT
CMD ["/bin/bash"]
# Thu, 15 Aug 2024 04:29:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV GOSU_VERSION=1.17
# Thu, 15 Aug 2024 04:29:43 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENV LANG=C.UTF-8
# Thu, 15 Aug 2024 04:29:43 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.9 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 15 Aug 2024 04:29:43 GMT
ARG MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ENV MARIADB_VERSION=1:10.11.9+maria~ubu2204
# Thu, 15 Aug 2024 04:29:43 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.9+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.9/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
VOLUME [/var/lib/mysql]
# Thu, 15 Aug 2024 04:29:43 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 15 Aug 2024 04:29:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Aug 2024 04:29:43 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 15 Aug 2024 04:29:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf9db3289e1abffa2c6251d35396624b52fe9c32bcef50002b7e17d4e1f8169`  
		Last Modified: Mon, 12 Aug 2024 17:08:48 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420d235fac9f80ba2d1252cfc18b2b0f115075fe7c16b01e3f4c6613fc0cfaef`  
		Last Modified: Thu, 15 Aug 2024 18:32:10 GMT  
		Size: 5.5 MB (5532711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98cb797a3de7c03fc77fb73935b9627dd4a3247ee9deb1c4eae2eeb5cc2c4f7f`  
		Last Modified: Thu, 15 Aug 2024 18:32:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb901cb0d5756406c2fc6a1368c36b970ab5ba8d64e9cb907f5f11319372070`  
		Last Modified: Thu, 15 Aug 2024 18:37:15 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bd311d389a3d47a7c05db93ec940724ae4319370e014019bcf5cf5127d3136`  
		Last Modified: Thu, 15 Aug 2024 18:37:21 GMT  
		Size: 88.1 MB (88071392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0ca96621fc1be19a09374f82b05d2db692cceaaf676c229422440d81abbae4`  
		Last Modified: Thu, 15 Aug 2024 18:37:15 GMT  
		Size: 3.8 KB (3841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbf204be90da3fbd2335d480b2479691a9d7a9b2e9014ba5bd3a796821b7035`  
		Last Modified: Thu, 15 Aug 2024 18:37:15 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:f06a25a71ef0bca7ae48c625caa3bd4b42aee0aa994494be3871e4535cc7a596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4621594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b1ee8d95cfd4cb1aa88c105627c5feeb56190734b49c1a3bcabbed5f4cf555`

```dockerfile
```

-	Layers:
	-	`sha256:fccd515632ca5f3c1c813189f182f0d6c588aba92c0a19cadb41bb14c710c244`  
		Last Modified: Thu, 15 Aug 2024 18:37:15 GMT  
		Size: 4.6 MB (4591167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3da09abac694e3d87397e177bc782b131dbea5edba2298126b0e0df3c6edb509`  
		Last Modified: Thu, 15 Aug 2024 18:37:15 GMT  
		Size: 30.4 KB (30427 bytes)  
		MIME: application/vnd.in-toto+json
