## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:825d203272f1e2d7653c386f343bd5d87affc89f09931c3ae5e58aeadce2fc0b
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
$ docker pull mariadb@sha256:035a8cfc114df536f5e4ba8f5bad2e148416ef61d903caad47176e03206bc2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105368914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f59ffd33b9af4a4e0c2d72effcfd1bb3b644c67b7778969edb1146be6b804d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 05:32:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:32:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:32:11 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:32:14 GMT
ADD file:598bb7ba54e5a576778e9ebe1f4e514188812bea30c08d00446f8d04c37053e6 in / 
# Wed, 30 Jul 2025 05:32:14 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a3be5d4ce40198dc77f17780f02720f55b1898a2368f701dd1619fc9f84aac86`  
		Last Modified: Wed, 30 Jul 2025 09:36:23 GMT  
		Size: 29.5 MB (29536993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1325cf3580b4f9a7ee83ee18d2ae9fa1d9abe3ed349e275c20054870c0834ec6`  
		Last Modified: Tue, 12 Aug 2025 18:05:03 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc467e10dbced6c1b530a273edaa17efdb4a4383dabf2f48970adc9203165db6`  
		Last Modified: Tue, 12 Aug 2025 18:05:05 GMT  
		Size: 5.7 MB (5659783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635d6c9a972b2b5c15cfd257483ab4d8f3356dba32a6d8a1ef562da2fe86373d`  
		Last Modified: Tue, 12 Aug 2025 18:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcf9d2992fb001b2439cdae94e486e282cf040910e8a26c9ddf7f7afe7954ba`  
		Last Modified: Tue, 12 Aug 2025 18:05:05 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8c711ea4e7481bdbf161058614524dd1bebd4e33151273d5e8534069a6a5f`  
		Last Modified: Tue, 12 Aug 2025 18:05:21 GMT  
		Size: 70.2 MB (70157579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1c495a6d0ac548476480e52e118524a576c04d926d8f06b761afb059b0749d`  
		Last Modified: Tue, 12 Aug 2025 18:05:06 GMT  
		Size: 4.0 KB (4020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf1baf166ba499abc3b194c71533040b5c972d7f573196d7991cf7807ff6d62`  
		Last Modified: Tue, 12 Aug 2025 18:05:06 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:4c70b13e60aaf23ca0a17ebdccd8d9500b68987e14466fd302e9b7cd6ad6eb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4823651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5401080a7ad316ad6cc646a3b39b3c98632bcad18747bf6871ec74dbee42323a`

```dockerfile
```

-	Layers:
	-	`sha256:68f02ff4fc017172a40d2dfec766d8df91d809e3792256071a28604289eb9f29`  
		Last Modified: Tue, 12 Aug 2025 18:35:27 GMT  
		Size: 4.8 MB (4792958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc40e0bf4b5297daf595f746c01d071c8f60f22635d16b8140c7cc8c0c9ed80`  
		Last Modified: Tue, 12 Aug 2025 18:35:28 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:c92117f14bf88157973405cbcb0be20f948b32be436e96c677cddec9dd290085
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99751262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f131fa45798fbedb20659126be2ec553e3d5b575374aa6e962d218144ec08e91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:14 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:14 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:17 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Wed, 30 Jul 2025 05:34:17 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6e54bcf042caff3c37ac61be625162df633f1fdf401246a4b4d8c6917eec36`  
		Last Modified: Tue, 12 Aug 2025 20:25:49 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ab79885e4e4c6faee7feff724f270c7e08393758695a4199b8941462d7fcc`  
		Last Modified: Tue, 12 Aug 2025 20:25:51 GMT  
		Size: 5.5 MB (5472353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274114066d4ab32e7e3b6891ee358f6d76301a6b87aae2529602f587ee1e0ee9`  
		Last Modified: Tue, 12 Aug 2025 20:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f90c934bad83752fe6366268b4365c3ffdc0222af79c3745639f1e6fedc2fe6`  
		Last Modified: Tue, 12 Aug 2025 20:25:49 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:433a340c36e10ded9ce094a30992a5c15a8b0b494ab87f5f98da38966c7f3431`  
		Last Modified: Tue, 12 Aug 2025 20:25:56 GMT  
		Size: 66.9 MB (66905106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25fdab656758860ed2872aa6ef79e59cbdd8ddd66f2ce5ca80cbbcde1699176a`  
		Last Modified: Tue, 12 Aug 2025 20:25:49 GMT  
		Size: 4.0 KB (4019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3020bb46439df679d85b2a77d7ed2254474db454cd77ffc020ddfdf3b374e475`  
		Last Modified: Tue, 12 Aug 2025 20:25:50 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:92aa930c70c048297eee1b8cf01fe2c6a5ab43300a6faa91a266d1e889c7b942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4830274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ac46a7371f7823439ee5fce599a4589e178b7492c32650ae5af8d968a9f70fa`

```dockerfile
```

-	Layers:
	-	`sha256:7ae08b67e584c23ccbd4cefcea1583f5a69234b617197db38b04df6e62bf4a53`  
		Last Modified: Tue, 12 Aug 2025 21:35:24 GMT  
		Size: 4.8 MB (4799394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19b8b25e6c6cdf574c3b8c34e053fe38691314fb06e83eef32f4cd2e0c392302`  
		Last Modified: Tue, 12 Aug 2025 21:35:25 GMT  
		Size: 30.9 KB (30880 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:45bb703341a2fbc4a9797c11f00f0b023f2255e9076b15bef1d347d30e87776f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.0 MB (113003547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ff15a30f3f6a1807ce98448ba4658d9a36e625c59a6cb517d7b8e553ba6a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 05:34:03 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:34:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:34:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:34:06 GMT
ADD file:8e490d6aa7e352ca02bf6249fe59c9445bd10be61e8a31e7d8219d7f34f3df1e in / 
# Wed, 30 Jul 2025 05:34:06 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9e0049f176947659afd8c14b3a33c239a7d2fb1bdcbab338270e4d28b95b3a1d`  
		Last Modified: Tue, 12 Aug 2025 17:03:41 GMT  
		Size: 34.4 MB (34443145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9eaf327ac6efff8b6ff0b4504dc17344137e72c508dd709aba9ce3bbfbf9aef`  
		Last Modified: Tue, 12 Aug 2025 21:36:46 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32541075a557d8213f7a0cea7e7957d31c0c9977f1cc107359a5ec23899dabda`  
		Last Modified: Tue, 12 Aug 2025 21:36:49 GMT  
		Size: 6.1 MB (6086428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0218196f5c352693b87294425a3f7645f165bdbbaf2f96cbc260231d2572ed5`  
		Last Modified: Tue, 12 Aug 2025 21:36:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b60e9c978eb29894c8bef431c0c43bcadd03f673665718a0472a44afdfb9fea`  
		Last Modified: Tue, 12 Aug 2025 21:36:38 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a993dfc49ab0bf19306bb026ef28ff612b3e48879bbe12c0544d86d5440f80dd`  
		Last Modified: Tue, 12 Aug 2025 21:36:39 GMT  
		Size: 72.5 MB (72459416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec68e0390203682cc7627dee1542a394719e615c6df3b6d044145e886286cb3`  
		Last Modified: Tue, 12 Aug 2025 21:36:36 GMT  
		Size: 4.0 KB (4020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45464b60880ed38bde413f11573734d21e7ff88564de6b813dc777aecf5e257`  
		Last Modified: Tue, 12 Aug 2025 21:36:36 GMT  
		Size: 8.4 KB (8368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:5cd5dbe40568c62fc7b697a9a83a5558b4bdaa8a15d8c8d2e4ce365644b6eff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4831509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02afca32702a17331b65b1db117e10eed8d8c974b08847d1bbdb2a34c528395e`

```dockerfile
```

-	Layers:
	-	`sha256:c7bcb6ef6b23e063283ceb632ef20f929d7e55072d4eb31d0efeb146e2bd6d17`  
		Last Modified: Wed, 13 Aug 2025 00:35:27 GMT  
		Size: 4.8 MB (4800752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4045a67da80809712b1bfdbbfd3090cc0fbb207bb14d394438bf2324728cc884`  
		Last Modified: Wed, 13 Aug 2025 00:35:29 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:438c067ed3cbfb3e2f92dd42b7056023f948e6aae3f6978c8a313ab2079f0745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103196531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2a6d7f7529f8ee91c64a0302e99be52c20765bd6d85b1f38bde7788ef98bf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 05:33:01 GMT
ARG RELEASE
# Wed, 30 Jul 2025 05:33:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 05:33:01 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 30 Jul 2025 05:33:02 GMT
ADD file:e0994d65dd44d220b4a55ce1033f7309688125fc54c99056866a92caff4bce78 in / 
# Wed, 30 Jul 2025 05:33:02 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 07:40:04 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 07:40:04 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 07:40:04 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.14 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 07:40:04 GMT
ARG MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ENV MARIADB_VERSION=1:10.11.14+maria~ubu2204
# Fri, 08 Aug 2025 07:40:04 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.14+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.14/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 07:40:04 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 07:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 07:40:04 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 07:40:04 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9c54d9d5bd2c16422a2ac0653717d2ef3d3e03f04fb894713d9682ff2fb1a339`  
		Last Modified: Tue, 12 Aug 2025 17:29:30 GMT  
		Size: 28.0 MB (28003219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcebcb5347c9d80f82fa37564b9aa9ddde2fc769d7af33825eb17b4eec56ff8`  
		Last Modified: Tue, 12 Aug 2025 18:11:56 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921458e5c5f91efef80d1e22cdeebd7545b4801b02da6a8e76ca5e05e21a0177`  
		Last Modified: Tue, 12 Aug 2025 18:11:57 GMT  
		Size: 5.5 MB (5541849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9407620b7f002f04cf445109507076e043a99e1875cc669d72ba1d570dae81`  
		Last Modified: Tue, 12 Aug 2025 18:11:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a740c74cc474fa8862fd68a95871ddf5d815b93474787e1351b264ca0dd3db`  
		Last Modified: Tue, 12 Aug 2025 18:11:57 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ce18ddefda79e5e6a1adff70516283866ccdaa411337f5e1883f8fb995a974`  
		Last Modified: Tue, 12 Aug 2025 18:12:03 GMT  
		Size: 69.6 MB (69636908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ef970575220ab3250347be75d244862a3350f4e3f580db4fa1b04d9718d844`  
		Last Modified: Tue, 12 Aug 2025 18:11:58 GMT  
		Size: 4.0 KB (4017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2cc982d0465b008a82d653f0ef54224dc2e150260e2699fd778a45b48c58373`  
		Last Modified: Tue, 12 Aug 2025 18:11:58 GMT  
		Size: 8.4 KB (8366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:16f5fb5baaa88c004ad03fb456af89cc9d0d6c7f620c16f6bcf1b7c15d6ab975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4823976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7097505838d31ba8c46b858f7cfe765dae8b9eaca40dbab71034d3c7de40bc6`

```dockerfile
```

-	Layers:
	-	`sha256:921311d307ebf6f90731d3c1d937a439e551517b6465b444e5fc4fb713b13c0a`  
		Last Modified: Tue, 12 Aug 2025 18:35:42 GMT  
		Size: 4.8 MB (4793283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c150ec6746ca9d95c8aa53a474b96118f090a5ffc73fdc3ac173e44183b60a4`  
		Last Modified: Tue, 12 Aug 2025 18:35:43 GMT  
		Size: 30.7 KB (30693 bytes)  
		MIME: application/vnd.in-toto+json
