## `mariadb:12-noble`

```console
$ docker pull mariadb@sha256:b30cc65b57a11a2e791ad5c06284e599fe9f1bf3fe9081a88d85bcf36389be4a
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
$ docker pull mariadb@sha256:f85578448fc01b193932701c22c6fefcc161f575949c8520d5dce5033d4356d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105534437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300929c28ab758f3322f12273e9e8b0f2233d8af06050bd1b9e17133cc5beb1a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 06:51:00 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:51:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:51:00 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:51:02 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Wed, 30 Jul 2025 06:51:03 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d05662ac2dcea9531520029c8d5a91b544a42d1a561c712a1d86914a0a4f1c`  
		Last Modified: Tue, 12 Aug 2025 18:03:50 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637be8612834e5d8c919ab6458ec07bc460abd71e89671b7e5f70367ba847b13`  
		Last Modified: Tue, 12 Aug 2025 18:03:54 GMT  
		Size: 5.3 MB (5349615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd08ae2b55f20c8ed216dea68306840a060a150ea036df68feb56dd08529983`  
		Last Modified: Tue, 12 Aug 2025 18:03:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd82d392121c13439003f22e4278814bbb43d2ac52584f54105cf198fcb652c`  
		Last Modified: Tue, 12 Aug 2025 18:03:46 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162fcbecc8c809e6861e9a81556e2c2c0a55daa6b83e5672f02d34de5ef85d09`  
		Last Modified: Tue, 12 Aug 2025 18:03:51 GMT  
		Size: 70.4 MB (70447383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3409c89ba295e2c4618974a71988fdd8e7bdf2dab2909460d867478a8804b4f8`  
		Last Modified: Tue, 12 Aug 2025 18:03:46 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8057d4c0a8e3ebb798355b0cd4d15c40058ecbd1d4f954950aa014bba95d86d4`  
		Last Modified: Tue, 12 Aug 2025 18:03:47 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:eb21447585dfa16247d83012954e14034a0232a34cfd9cdfb798e728442de4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4294855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6555556755729555c124ab327825ffdb1022759f33f76c166fd0971af1dcba1f`

```dockerfile
```

-	Layers:
	-	`sha256:d2be9c4ef95bb12751b6a649a707a01253f594fd12a9e9c68d670016e3d1aa6a`  
		Last Modified: Tue, 12 Aug 2025 18:38:07 GMT  
		Size: 4.3 MB (4263643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:220fb88b1d9c4aed93f62d76f95b7e9c4c183778efd40072c655e27265987901`  
		Last Modified: Tue, 12 Aug 2025 18:38:08 GMT  
		Size: 31.2 KB (31212 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:4b0f16d9c3bb45a96fc52eb4fc6477d0602efbc6f51633f60b28726c4db8f007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103467897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01411b052a68c985570ded84623166ff4eb8f99b9c0f2c92cd91fc6d8d409b85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 07:00:50 GMT
ARG RELEASE
# Wed, 30 Jul 2025 07:00:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 07:00:50 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 07:00:53 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Wed, 30 Jul 2025 07:00:53 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c338cf0a6fdd14a75116b56eb64dcda609dc691d5fbacedfb5e14b9f08c06a8`  
		Last Modified: Tue, 12 Aug 2025 20:23:09 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2493992af1cc5296fc9b659b101cbdd16fbebd330e70d4a0256c031f4d9f9c30`  
		Last Modified: Tue, 12 Aug 2025 20:23:11 GMT  
		Size: 5.1 MB (5130793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8a4983bbff6ec6f8888f0b865864a42c82168d8327000596df30b4cc02321d`  
		Last Modified: Tue, 12 Aug 2025 20:23:10 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01177262941838f9b20b0b48d0cbfc24a63b84e29b47e2263934c61f6fabba1c`  
		Last Modified: Tue, 12 Aug 2025 20:23:53 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02204cc5844b3e5007a75a32edb253656738e4bbc1864c69dd94cb62df7caf35`  
		Last Modified: Tue, 12 Aug 2025 20:24:07 GMT  
		Size: 69.5 MB (69462492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3dec5de06599d3abd986ab8f85477a6a9d178867c9e27071c6736daa9ee0d`  
		Last Modified: Tue, 12 Aug 2025 20:23:55 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5bc966d2b8a74b272c90eddd8e7a320471397aab0ce13ad84a79f10f4a677a`  
		Last Modified: Tue, 12 Aug 2025 20:23:55 GMT  
		Size: 8.4 KB (8401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:854990c6e0f05a1e242160b9827d9293589e262f6244a401d2010ac9350c154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b44392c8f5a0b290e25b2f2574ce02f68bcba16afe44b16c8b52d462455e4c`

```dockerfile
```

-	Layers:
	-	`sha256:b960301d69a1d20d938a741c5a5aab72277ba0cb82168e137d623276472dff08`  
		Last Modified: Tue, 12 Aug 2025 21:36:24 GMT  
		Size: 4.3 MB (4270918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06021e618f0d773639276ff4e2d79f1f58b800791cd04dcd88c2dee99852f86`  
		Last Modified: Tue, 12 Aug 2025 21:36:25 GMT  
		Size: 31.4 KB (31424 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:7ad0f9200a86d7dee01f428e60960f8cf0b4f82080c7e7b86dbeddda4f06a58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115698341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf10e321073de2b7f9cfdcbc4afa35686cfaf029cb1d084253b8866a9855eb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 06:57:25 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:57:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:57:25 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:57:28 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Wed, 30 Jul 2025 06:57:29 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd7a5e760d320843c285acd261810983b19225ee585ab95584ac7dd3841d9b6`  
		Last Modified: Tue, 12 Aug 2025 18:27:32 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdf5b6b96f834a6dfd4a6c7e3f82b7821d4d9631f26926c4613c3e0079cc218`  
		Last Modified: Tue, 12 Aug 2025 18:27:34 GMT  
		Size: 5.9 MB (5914109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746d698fe66e8d3d776c1a4f7890fb400866e428f705aba6f3d7a5ce6e65c964`  
		Last Modified: Tue, 12 Aug 2025 18:27:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34258d4ab85ad60bd94f852c9895e319c6a9c67a5a63c907b6f1ab0e5e593c61`  
		Last Modified: Wed, 13 Aug 2025 04:34:42 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c145b8e7a8a24fec01d196992ef44147345ea6204626e8560102a41784ce7b3b`  
		Last Modified: Wed, 13 Aug 2025 06:39:48 GMT  
		Size: 75.4 MB (75440359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd6380919fb9131dd96514d8339995ad9b5fc8e00a29dd13b14a21b5ba38a8d`  
		Last Modified: Wed, 13 Aug 2025 04:34:45 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b631cad8373c6b7fc9c32b50127853b24860c785ceef5d32711b4d450a0627ba`  
		Last Modified: Wed, 13 Aug 2025 04:34:48 GMT  
		Size: 8.4 KB (8396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:8dfb35166a5964f969571855f3daf7f4e5a9729e4ab358c51a6bde508f15190d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1682675c780145ffd47834b291e56d4cfaf7efce74eacd907abfcc43e6a945`

```dockerfile
```

-	Layers:
	-	`sha256:bafaca40dd0e013c8c28ec97a98b68a4bc3b493640a89a267c0a756e72fa9f38`  
		Last Modified: Wed, 13 Aug 2025 06:35:54 GMT  
		Size: 4.3 MB (4271564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6066887f296f9fafb94582620daa535b6ab5188b8771e42c80223639aa977dce`  
		Last Modified: Wed, 13 Aug 2025 06:35:55 GMT  
		Size: 31.3 KB (31288 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:12-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:03e6aefe6acfbc39bf7d016c6444a5c362729e69480ea3e0cddb2fa119bb4942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.9 MB (110942742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f63b3093045aadf059e02d8e3854246926878b2725e90120f418fb17a977942`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 30 Jul 2025 06:55:11 GMT
ARG RELEASE
# Wed, 30 Jul 2025 06:55:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 30 Jul 2025 06:55:11 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 30 Jul 2025 06:55:12 GMT
ADD file:f751959e6b8dae58a35017dc82c7271708f085c111710b59527373699b0784b5 in / 
# Wed, 30 Jul 2025 06:55:12 GMT
CMD ["/bin/bash"]
# Fri, 08 Aug 2025 08:15:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV GOSU_VERSION=1.17
# Fri, 08 Aug 2025 08:15:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 08:15:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=12.0.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 08 Aug 2025 08:15:27 GMT
ARG MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ENV MARIADB_VERSION=1:12.0.2+maria~ubu2404
# Fri, 08 Aug 2025 08:15:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:12.0.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-12.0.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 08 Aug 2025 08:15:27 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 08:15:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 08 Aug 2025 08:15:27 GMT
EXPOSE map[3306/tcp:{}]
# Fri, 08 Aug 2025 08:15:27 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:1c5d0b18c745fadd2e177b54d4df793f25b01437577bc09c72ae52a0f3f9aeb3`  
		Last Modified: Wed, 30 Jul 2025 11:30:49 GMT  
		Size: 29.9 MB (29932680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481159fd28f90c963174b1eefac3032c0b6ae27e002b93a43032b7766eedbf7f`  
		Last Modified: Tue, 12 Aug 2025 18:35:15 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ee83d9c1373e20c8e34d888e290185b305abedbaa9c48240420c94411cedaa`  
		Last Modified: Tue, 12 Aug 2025 18:42:12 GMT  
		Size: 5.5 MB (5483382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db3ac951f35780017e1e72f2bd2d213fea050d3691d574025c973b4706b1ba9`  
		Last Modified: Tue, 12 Aug 2025 18:35:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9850b5dfe95e11bb83914167b3bd1e35a11a34102a04bb3df585ba50e5c8092`  
		Last Modified: Tue, 12 Aug 2025 18:35:36 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32cccbd0a03c8a71a4e0f0276f64436267b9e553db4fe59c1f286e976af6a404`  
		Last Modified: Tue, 12 Aug 2025 18:42:31 GMT  
		Size: 75.5 MB (75512451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd6b601dffbd4716d145749f1d13ec6e8cf8c86972d81d0643953e13ea3f907`  
		Last Modified: Tue, 12 Aug 2025 18:35:40 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a6a72882a317e474c6460d2f3ee7a598760179c10ebbc0b9cab1264baf8fbe`  
		Last Modified: Tue, 12 Aug 2025 18:35:43 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:12-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:0a829a67701e8c8b45d0e2702658c6dbe448d88b01acc67fa447ef7046dc12c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f8d73192591f9996fefaab513c1283386facb87268b330097258c1370627f9`

```dockerfile
```

-	Layers:
	-	`sha256:5c1d2d20570db8ba9e5711ccd7e93631a80dabc86feac0203e5d719909fe48eb`  
		Last Modified: Tue, 12 Aug 2025 18:38:13 GMT  
		Size: 4.3 MB (4265364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:272e8b6dbe67965bb9091c340be7aac081b4f17b06afc843c5d7dd120dde0ad4`  
		Last Modified: Tue, 12 Aug 2025 18:38:14 GMT  
		Size: 31.2 KB (31211 bytes)  
		MIME: application/vnd.in-toto+json
