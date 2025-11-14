## `mariadb:lts`

```console
$ docker pull mariadb@sha256:6b848cb24fbbd87429917f6c4422ac53c343e85692eb0fef86553e99e4f422f3
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
$ docker pull mariadb@sha256:b8fbd3fdd76230d10d81362778b34ad1aabb7363664e8354f4195a9ef6407eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.2 MB (106218642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70745dd8f1d0426395bc6d6d615274f4e25d6cf7519bbcf81fce2baa2f1a289b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:29:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:29:39 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 13 Nov 2025 23:29:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:29:39 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:29:39 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 13 Nov 2025 23:29:39 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Thu, 13 Nov 2025 23:29:39 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Thu, 13 Nov 2025 23:29:39 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Thu, 13 Nov 2025 23:29:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 13 Nov 2025 23:29:55 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 13 Nov 2025 23:29:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 13 Nov 2025 23:29:55 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 13 Nov 2025 23:29:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:55 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 13 Nov 2025 23:29:55 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8341999369d455e7646409ca849875da2ad117b1240cba639d750a3b5da17e`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062bc720a64ab5c41b4059aaeaa48d8c7a494afc41cb7002a30624651a9f1d3b`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 5.3 MB (5288013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a2b82d2744edad79f165d2b0ac9cca8ab1752724018ca1703586fce3d1361a`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd78a7741960934b5ec45b536589ab39c527e34f8d6fdea99996d8f533355d6`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8730d4da5144d33e331de839cff5800f9778d6eb775d5e95b7a7dc11fe2fdf76`  
		Last Modified: Thu, 13 Nov 2025 23:30:28 GMT  
		Size: 71.2 MB (71191708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56107a3cd80f0e14edf6c13719e2bc4b41d2f40be1ec14791878c315446225e4`  
		Last Modified: Thu, 13 Nov 2025 23:30:19 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe728ae2aa2a7d50d671b0a38e481c7bebd973c75890d9fd01e7f90b8393678`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:9cf4b017b070f918def6585d848a12a3d984ae735a126080c0985a090a487b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c26e886283b0e2e44712745ed5ed46db5e0a3a27c5f3b4eeee21ea03460167d`

```dockerfile
```

-	Layers:
	-	`sha256:d7748589b5739648a66ec7fe7494b05ee6df1117c91df3e74060d4a6a5629092`  
		Last Modified: Fri, 14 Nov 2025 01:36:35 GMT  
		Size: 4.3 MB (4273709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d26497b90bcc74cccef602b88f5dda8c9f3a6f549e5b5de36fd5ab3c88e08f`  
		Last Modified: Fri, 14 Nov 2025 01:36:36 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:77b510f08688b49b9c9662a78ded3fc330e1b423b38d5c53488c74b55a1fa34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104124947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c42974091237fd2a537c88ccd9908ea8e6414b27f8e3d0af838de2761f7f63`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:29:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 13 Nov 2025 23:29:17 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:29:17 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 13 Nov 2025 23:29:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:29:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:29:17 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:29:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 13 Nov 2025 23:29:17 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Thu, 13 Nov 2025 23:29:17 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Thu, 13 Nov 2025 23:29:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Thu, 13 Nov 2025 23:29:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 13 Nov 2025 23:29:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 13 Nov 2025 23:29:33 GMT
VOLUME [/var/lib/mysql]
# Thu, 13 Nov 2025 23:29:33 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 13 Nov 2025 23:29:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:34 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 13 Nov 2025 23:29:34 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f050d23b387f9b5c412517b202337bcaab831950003e3d4cb03f39a2984678`  
		Last Modified: Thu, 13 Nov 2025 23:29:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e08f0c13bccf494a5793dada2fcf472b5793fdc07c14cba888aa774343a2ca`  
		Last Modified: Thu, 13 Nov 2025 23:29:57 GMT  
		Size: 5.1 MB (5097448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106504999b297c330db83cd95b0bb52937d3dab8d7a297341ce4be16832679a0`  
		Last Modified: Thu, 13 Nov 2025 23:29:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed50140a83c8d22eb9c4d5ae5e1a54d429a642869cd9ce194ec6256b708dc5d3`  
		Last Modified: Thu, 13 Nov 2025 23:29:57 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3a9841fe10e8249860e52638a963fdd2c58acc23532e2254d91f146c3d24e7`  
		Last Modified: Thu, 13 Nov 2025 23:30:04 GMT  
		Size: 70.2 MB (70151302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f825a578a67d4a4afd0b52ba6610eea93b9d1262ac176e3a6c7a39c4929b7`  
		Last Modified: Thu, 13 Nov 2025 23:29:57 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf00162704f91d2a7c3742e475c6b009ec6313e9d12e54728e53f348d0ec543`  
		Last Modified: Thu, 13 Nov 2025 23:29:57 GMT  
		Size: 8.4 KB (8402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:771547c438fbd6d2191a53eb16e48da3adbe5a148daee05df59753bee63926dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4312653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eff291934d7a45144317eb49dc9d79207d28cc47461372e81057f9c08a7e8dc`

```dockerfile
```

-	Layers:
	-	`sha256:4c2f7b7777a6dcbda29a039954f146c8e30775b8c5899f80b45371b3db8c85ce`  
		Last Modified: Fri, 14 Nov 2025 01:36:41 GMT  
		Size: 4.3 MB (4280986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2461dcf56920aa27ad9709560c8c3859d7b77c781903377d33f3db2a1611bd75`  
		Last Modified: Fri, 14 Nov 2025 01:36:41 GMT  
		Size: 31.7 KB (31667 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:b66827c03ea99a15c5dcb4ca2e5845749330e7afa0b43fbf5cc22ea0e58518a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.4 MB (116402069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e671f7ac014f60441e7750e4106d302e0c81caf68c367ce8a1be90f46d2be106`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 00:12:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 14 Nov 2025 00:13:21 GMT
ENV GOSU_VERSION=1.19
# Fri, 14 Nov 2025 00:13:21 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 14 Nov 2025 00:13:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 14 Nov 2025 00:13:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 14 Nov 2025 00:13:22 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 00:13:22 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 00:13:22 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Fri, 14 Nov 2025 00:13:22 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Fri, 14 Nov 2025 00:13:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Fri, 14 Nov 2025 00:16:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Nov 2025 00:16:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Nov 2025 00:16:56 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Nov 2025 00:16:57 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Nov 2025 00:16:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 00:16:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:16:57 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Nov 2025 00:16:57 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aff447ebd9eaab46e933b5b095d7f167289cfb347cf30a92e5b3050d7a7eae`  
		Last Modified: Fri, 14 Nov 2025 00:14:44 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747f705fa4d9f87bff178e6df9cacc66527c13b014f33fa344f6b1ca0404c8a6`  
		Last Modified: Fri, 14 Nov 2025 00:14:45 GMT  
		Size: 5.9 MB (5927290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25615154a46e8abf12ba721c170c1c732a02479c56ec2e5955f0576b7bd43e3`  
		Last Modified: Fri, 14 Nov 2025 00:14:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2e151bc9940fc113c7133bc6350ced9edffbdb060779daa332bb9bff21ddb4`  
		Last Modified: Fri, 14 Nov 2025 00:17:40 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821409051c4f84dd45b5a88f133d5e663e821282aa7832c51e79fa2429c7112f`  
		Last Modified: Fri, 14 Nov 2025 00:17:47 GMT  
		Size: 76.2 MB (76156116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f54b75a8c23dc795bf6a3e29c1d9bcc3e7440c7c2fd0653c0f3119a61d207ae`  
		Last Modified: Fri, 14 Nov 2025 00:17:40 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ebc074b3ada8a23e9b4e336805a18ad6af18f48b487ecb3e9f2ad957f74ab0`  
		Last Modified: Fri, 14 Nov 2025 00:17:40 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:1a8efdb3cec0447f94216555ac01ff0ec18e6121aa2e9090df44bc4dbbadc47e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa710363d4f29b02e48f844dbd29366e83a5101ea16943cc3d8bafe5264ddb8`

```dockerfile
```

-	Layers:
	-	`sha256:f7faec6bd7d0831d530c007bcd4a82a4397124364196a923eb892317b19b957b`  
		Last Modified: Fri, 14 Nov 2025 01:36:46 GMT  
		Size: 4.3 MB (4281644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0edc904b6d227a02e22060423fc95107fd776120a7c78837c4fc8704dbe54559`  
		Last Modified: Fri, 14 Nov 2025 01:36:47 GMT  
		Size: 31.5 KB (31528 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:4ab6e9974e21eaac1d2c0b0b008319298c6e0b517c6da8bbd5a8e54048089fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111614034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14bbccf72b340b9c0f38183cf6e39cc4bdf6bbc1de28428c5ac2620a810cdb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:14 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:14 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:16 GMT
ADD file:f7335d462150d31c3c91b13ccd3e927bc9a1b9c6664fa8905ccf68bbe3d86cd3 in / 
# Thu, 16 Oct 2025 19:25:16 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:21:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 13 Nov 2025 23:21:53 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:21:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 13 Nov 2025 23:21:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:21:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:21:53 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:21:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 13 Nov 2025 23:21:53 GMT
ARG MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Thu, 13 Nov 2025 23:21:53 GMT
ENV MARIADB_VERSION=1:11.8.4+maria~ubu2404
# Thu, 13 Nov 2025 23:21:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
# Thu, 13 Nov 2025 23:22:41 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 13 Nov 2025 23:23:32 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.4+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.4/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 13 Nov 2025 23:23:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 13 Nov 2025 23:23:32 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 13 Nov 2025 23:23:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:23:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:32 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 13 Nov 2025 23:23:32 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c7d697026502bd6e5c5f140b6c646a5d33fc3104c02fddd15b0c84b64268b5`  
		Last Modified: Thu, 13 Nov 2025 23:22:35 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3a7ba1b6f0eee66809c5821f2ef1b98f5e44fc0b00e8a2c76faafee41e62a3`  
		Last Modified: Thu, 13 Nov 2025 23:22:36 GMT  
		Size: 5.4 MB (5443768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dada8ad46dc78110d50fb57cf63f46aa7e0a4ca820909af42dccc8a61e28cbb5`  
		Last Modified: Thu, 13 Nov 2025 23:22:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127aca24960652d795004d87fa3c5c3357caa46ce4b7145d8f54c3da0406a5c6`  
		Last Modified: Thu, 13 Nov 2025 23:24:02 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2203348afb0c7f8fae5d37774622ae0a5a0cf1d70ef1369a6a5a405b988ef0f`  
		Last Modified: Thu, 13 Nov 2025 23:24:09 GMT  
		Size: 76.2 MB (76248437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03af72a654b58b088f5505d218d585e15fa049ff98cd8a426e84dfb2b90ecf23`  
		Last Modified: Thu, 13 Nov 2025 23:24:02 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7147807d6ebdc9e1c71b4a06e136c77783b7e6eb99c59713e15efe9c7a4ab8d`  
		Last Modified: Thu, 13 Nov 2025 23:24:01 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:7ebf6a0ebe13ae56a5064f57b1e03bb8e8ceb792e55edafa56546eda2a160443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4306883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fb01bab90097ccf966903945e6d9ee617b8dcf43a0aaebd2a5c168f72d5702`

```dockerfile
```

-	Layers:
	-	`sha256:97939047559dcc3b1c36dc67ed0bda228773fc8ffee905c0f40a483eefaa011a`  
		Last Modified: Fri, 14 Nov 2025 01:36:52 GMT  
		Size: 4.3 MB (4275428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099c25d1c47c1c4446fec206d5da026044895849e536a47f6797800e88c098dc`  
		Last Modified: Fri, 14 Nov 2025 01:36:53 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json
