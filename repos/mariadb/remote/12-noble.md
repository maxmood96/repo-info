## `mariadb:12-noble`

```console
$ docker pull mariadb@sha256:607835cd628b78e2876f6a586d0ec37b296c47683b31ef750002d3d17d3d8f7a
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

### `mariadb:12-noble` - linux; amd64

```console
$ docker pull mariadb@sha256:1c84068c7b5ca8520b1393098459bd39e91dcde84246dfe1fa5f6df860c8038e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105475718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4993dba27de422f8a3e17161c4572adf3b32da19d6aa5b475f4f3dae938aeae3`
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
# Thu, 13 Nov 2025 23:29:40 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:29:40 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 13 Nov 2025 23:29:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:29:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:29:40 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:29:40 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 13 Nov 2025 23:29:40 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Thu, 13 Nov 2025 23:29:40 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Thu, 13 Nov 2025 23:29:40 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Thu, 13 Nov 2025 23:29:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 13 Nov 2025 23:29:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 13 Nov 2025 23:29:56 GMT
VOLUME [/var/lib/mysql]
# Thu, 13 Nov 2025 23:29:56 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 13 Nov 2025 23:29:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:56 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 13 Nov 2025 23:29:56 GMT
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
	-	`sha256:4a3db27d125ab890a74a1ae572c5dbb730a03fda53a488f92cd69e8c602c160c`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 5.3 MB (5287982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac04ba1e5c3e335bc67e65722de0039389832a3c243c553e4a0031f363ad732`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ac905c2366abf63421e3a98212084bd000916046dd3ee21e5df336687c9c86`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5769b646debf3b07ede6dee3e90b775139bb6fd4b193852f0439b3133aa5bd6`  
		Last Modified: Thu, 13 Nov 2025 23:30:30 GMT  
		Size: 70.4 MB (70448821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c335bd5f0034168d4477dcabc2000a159a36aff296fbb7776fc19e2c8bde2f08`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a96bd3ecc9e15b456508d5bb49ee575c2c7682c9ba76bf15d2161fd6833ecd`  
		Last Modified: Thu, 13 Nov 2025 23:30:18 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:87a6f6e0b7e5c7b875e704fef6a110cc3c17766b45cd1dcc49379d1c1b5a6b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1279d389feaea10db73d77c33ae1b6894d834ff58e642b372c5c1592528185a4`

```dockerfile
```

-	Layers:
	-	`sha256:0aefa1ef12df6443180dd4459ada4b64596ed31a2dbed71770d2251ff8ffbabf`  
		Last Modified: Fri, 14 Nov 2025 01:37:34 GMT  
		Size: 4.3 MB (4272129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c5c27023c44f9e0233fc2ddebfde3ceb4dea7f301d1dcb61562462b2586b988`  
		Last Modified: Fri, 14 Nov 2025 01:37:35 GMT  
		Size: 31.4 KB (31441 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1513c5354bc9c049ea05f6af42b8561d32205fdaa855f929b72ce127d128ed07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103436637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d80ec225ce9d378c7e2bc2cc33c371c4f699f7b3acb1f2bb89dbe000d4282a18`
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
# Thu, 13 Nov 2025 23:28:28 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 13 Nov 2025 23:28:46 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:28:46 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 13 Nov 2025 23:28:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:28:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:28:46 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:28:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 13 Nov 2025 23:28:46 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Thu, 13 Nov 2025 23:28:46 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Thu, 13 Nov 2025 23:28:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Thu, 13 Nov 2025 23:28:46 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 13 Nov 2025 23:29:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 13 Nov 2025 23:29:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 13 Nov 2025 23:29:00 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 13 Nov 2025 23:29:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:29:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:29:00 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 13 Nov 2025 23:29:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d329cd861962f663d05e9a07dc9e70fe9a107a7332a19e0864f821d60e744ee`  
		Last Modified: Thu, 13 Nov 2025 23:29:23 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3feccb4eb78663e55c08cd19458503383b8704477f2e64cc6783b4877725cffb`  
		Last Modified: Thu, 13 Nov 2025 23:29:23 GMT  
		Size: 5.1 MB (5097404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c2c4c5871a29f79e4e6d7d41eaed34614da4dace501142745350c571e6203`  
		Last Modified: Thu, 13 Nov 2025 23:29:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72b4e4765ccff4e199c503b5ba512908438242b7172b84f41e432ac5629ff5e`  
		Last Modified: Thu, 13 Nov 2025 23:29:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0818611904fad1741a2fe8bb7d6ea6263477ab74bc692f825bb27fc9d24f94c7`  
		Last Modified: Thu, 13 Nov 2025 23:29:36 GMT  
		Size: 69.5 MB (69463045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a87ed30f7121db802e8599d5cc6dc92d4c4405af1c2dd11d45041d11df17317`  
		Last Modified: Thu, 13 Nov 2025 23:29:23 GMT  
		Size: 4.0 KB (4040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd30753608fdea6bb6e5fe2d2b3b45418d307037b23511656b78c5cc00a148`  
		Last Modified: Thu, 13 Nov 2025 23:29:23 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:f34369eab520a5ba137761908df8dda464e0d96d6844648aebd6ea41541f6974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60a6b92e59e783974ebb9ea355080a759d099356000f6d8c214f21b1a84e85b`

```dockerfile
```

-	Layers:
	-	`sha256:f96a59da0964f836bd1b94588c15a2bc16d16ecb9a00afbb5a6f70a7e4465245`  
		Last Modified: Fri, 14 Nov 2025 01:37:40 GMT  
		Size: 4.3 MB (4279406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b5c38fcd699575fff03b9e6926f51a9a89b8af7147908181ee1b61675cce0c1`  
		Last Modified: Fri, 14 Nov 2025 01:37:41 GMT  
		Size: 31.7 KB (31653 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:55c0c47a7f38df9340f8816dee5ef4d67da2e50605675eb48c84e1454458fef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115687527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69582485c138920f88c2d2b4da94db2590d6975649b0cd8896ebdd638068a5ff`
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 14 Nov 2025 00:13:22 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 14 Nov 2025 00:13:22 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 14 Nov 2025 00:13:22 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 14 Nov 2025 00:14:54 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 14 Nov 2025 00:15:21 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 14 Nov 2025 00:15:21 GMT
VOLUME [/var/lib/mysql]
# Fri, 14 Nov 2025 00:15:21 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 14 Nov 2025 00:15:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 14 Nov 2025 00:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Nov 2025 00:15:22 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 14 Nov 2025 00:15:22 GMT
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
	-	`sha256:cb8b7fca202b30549a7dc328b0124409d033d3fe0b4ac4a2f1d2e7a459b5837e`  
		Last Modified: Fri, 14 Nov 2025 00:16:05 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460d0dad45b8aaadf37cb57d01e35bb331c340732c36a7ea6a05644080cc4d4`  
		Last Modified: Fri, 14 Nov 2025 00:16:15 GMT  
		Size: 75.4 MB (75441572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62498e81ae3f381f868f433f4316ac18ca1b103a43e8cc34e97462c1b4a623e9`  
		Last Modified: Fri, 14 Nov 2025 00:16:05 GMT  
		Size: 4.0 KB (4042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11ab19cf8b777b26c70241522694fcea1b780a71b47da39a09b34350542d25c`  
		Last Modified: Fri, 14 Nov 2025 00:16:05 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:5727a29fe80720c2c9e4c378680e6ac965fea4c37808ac4f741cacfd564b6956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4920170b21e5ed129336d922dcff8534661e17b963afdffb310c9105e8c1a754`

```dockerfile
```

-	Layers:
	-	`sha256:433d553ef21c59478120706fb3323ec7ec0665a2b104c87ba3ae485b61275753`  
		Last Modified: Fri, 14 Nov 2025 01:37:45 GMT  
		Size: 4.3 MB (4280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b4c358f8f265b658312e8d3c7030645c0acaed69a94739cf9b2a529fcbe74c`  
		Last Modified: Fri, 14 Nov 2025 01:37:46 GMT  
		Size: 31.5 KB (31517 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:89eb1f7476bcd44681d0e74ef6ab057d94505b88b61b56a692b6f9708a6a7ac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110878759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d9ae2fc903339f410fe676da215604d6240029bc312d328b83d2c413a6cee6`
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
# Thu, 13 Nov 2025 23:22:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Thu, 13 Nov 2025 23:22:44 GMT
ENV GOSU_VERSION=1.19
# Thu, 13 Nov 2025 23:22:44 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 13 Nov 2025 23:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 13 Nov 2025 23:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:22:44 GMT
ENV LANG=C.UTF-8
# Thu, 13 Nov 2025 23:22:44 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 13 Nov 2025 23:22:44 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Thu, 13 Nov 2025 23:22:44 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Thu, 13 Nov 2025 23:22:44 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Thu, 13 Nov 2025 23:22:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 13 Nov 2025 23:23:26 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 13 Nov 2025 23:23:26 GMT
VOLUME [/var/lib/mysql]
# Thu, 13 Nov 2025 23:23:26 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 13 Nov 2025 23:23:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Nov 2025 23:23:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Nov 2025 23:23:26 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 13 Nov 2025 23:23:26 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7d5b0205a5ff16c2b58f20a113b5eb9a80393a644df077beab5d90635153dc66`  
		Last Modified: Thu, 16 Oct 2025 21:17:39 GMT  
		Size: 29.9 MB (29907597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd39e11293c9f818f559757651d060f46d6e0da64eb419f0cff94a70ff280597`  
		Last Modified: Thu, 13 Nov 2025 23:23:44 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a829c7700ebc710d9c07557f1bdd681ebadc05b7ac150d77f0862fdb90184972`  
		Last Modified: Thu, 13 Nov 2025 23:23:45 GMT  
		Size: 5.4 MB (5443789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae738bde1163ebb2cfcf4af0e845a2c687fdb451767bb155520f041b9f8e50d`  
		Last Modified: Thu, 13 Nov 2025 23:23:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7fa2963010edf515853b4d0388a7b38600a14486ee5527ed963b719b801259`  
		Last Modified: Thu, 13 Nov 2025 23:23:56 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6faf438a7ac815961d6183ff1ab022a472b8b8d912e80828f82f3225404126`  
		Last Modified: Thu, 13 Nov 2025 23:24:05 GMT  
		Size: 75.5 MB (75513145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112bccc65996e53fd47cd81e7003415e436e153577cafc22432223160bf9d890`  
		Last Modified: Thu, 13 Nov 2025 23:23:57 GMT  
		Size: 4.0 KB (4041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def311eec7df1628bcf57958654fd680ea41d08404e9ec11462b02106c424a32`  
		Last Modified: Thu, 13 Nov 2025 23:23:57 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:73d030dcfba9bc632db89358f511d51502004f4906b506d4e144024d825f0e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1170218f1c9b50fc26255ae3e8f19c61c620f6423e7a11e503c92d50103d9a6c`

```dockerfile
```

-	Layers:
	-	`sha256:aed10bb0ee1b91476c901f808552f1850f84dd7a3b5b55fa3ce215aebea41095`  
		Last Modified: Fri, 14 Nov 2025 01:37:51 GMT  
		Size: 4.3 MB (4273848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88b755898c7b076d382d8cbb752d9274b1d18046f0bcd7d834b77a9953e3a47a`  
		Last Modified: Fri, 14 Nov 2025 01:37:52 GMT  
		Size: 31.4 KB (31439 bytes)  
		MIME: application/vnd.in-toto+json
