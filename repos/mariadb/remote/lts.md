## `mariadb:lts`

```console
$ docker pull mariadb@sha256:1d18f91deb21136d1881705720071d1b474a9904ecca827058bf1c0fc64d3118
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
$ docker pull mariadb@sha256:1a8a2e7db2ecbcf102639546c2ca9e6a850ba4f84a323ea3e8023a0911fc68db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104534492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6cf2f4d23299885d5677dfe3574acc7b95dff096e7bb40ee9d2f046999b3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 21 May 2025 23:31:53 GMT
ARG RELEASE
# Wed, 21 May 2025 23:31:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 21 May 2025 23:31:53 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 21 May 2025 23:31:53 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302baf52b0511bb487f41f83a51e78d1cfe2f194c21a4d670fcf061210b4ba4`  
		Last Modified: Tue, 03 Jun 2025 13:30:24 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bab579fe2a59dfc5c036cb55ba6c02da5472ea4d79b8a90242a390cb83a60e`  
		Last Modified: Tue, 03 Jun 2025 13:30:24 GMT  
		Size: 5.3 MB (5349771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321dc82d3936069cfdf7e90e923c1c5b3998bfdcba4eae76e3428a0664744ad`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5083331da3752f8fe33c2d174f88da318dd75d5d9201aa757c8cac76ae3454a8`  
		Last Modified: Tue, 03 Jun 2025 13:30:24 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc70a241ff368c6ce38ec8a24761d1a6036e4b9904890ccedc25600610cd923`  
		Last Modified: Tue, 03 Jun 2025 13:30:34 GMT  
		Size: 69.5 MB (69455158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357e05a3616882a031ff35711550b5829471ad42d7f91ab8f4b3cc392d3ccc97`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9946569e436f81aca24bcd8238e1b012eb14fd993bf903ed4c16a67c5829dd8`  
		Last Modified: Tue, 03 Jun 2025 13:30:26 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:6f4b5a900f7f0d99113943da4b9284fe3ddd3fcb3c59832471c006746711b3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86fc3398aaab973863880c1764f7de20137f6caab8960f2e7929cb884b47e95`

```dockerfile
```

-	Layers:
	-	`sha256:1b520036aa8640760bb0a73ba56437ef03331fac1ccd4d2550dc44280e4c001d`  
		Last Modified: Tue, 03 Jun 2025 13:32:31 GMT  
		Size: 4.1 MB (4106996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c225bd1b7cb17cc42a8ba91ec919dcf6c154363e1ac81991b9ecfafc2b1b3734`  
		Last Modified: Tue, 03 Jun 2025 13:32:33 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:98ee8fa9516db36ae13b671af74b73643bed683f68615d4e41c47f5ee83efdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102526091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f192c42450f576c34d2753854ccfb4cc79f7d83d5c8d01d469b4b4c570c7425c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 21 May 2025 23:31:53 GMT
ARG RELEASE
# Wed, 21 May 2025 23:31:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 21 May 2025 23:31:53 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 21 May 2025 23:31:53 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a585ea2a801a7e852a88607392a2682abe6163f7c62138bc8d2d7387ea51501`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986b7028e52e39fadc4122e969e818c2b9a57ad0d041026ea995dd6310da15be`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 5.1 MB (5130694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0665a0c3d191cb19d9f0027302e47db304a8c37fc255b0e842ff49df3fb83`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cecca58a85f9175912d5dbaa5a6bfd1fad6a303d13329c51fe71e50f6c14ee3`  
		Last Modified: Tue, 03 Jun 2025 13:32:37 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2093c49330f9ff046e4c426ebb86fa9d83d23b7424c2d15ae321d19484aa1c6`  
		Last Modified: Tue, 03 Jun 2025 13:32:59 GMT  
		Size: 68.5 MB (68529274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d43a5390d05f229b563dd7549ba2543e1b0b8aaea5ffbe716b52851318e27c`  
		Last Modified: Tue, 03 Jun 2025 13:33:00 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ce864a354f958024d53e605ee6487f4de19e887f4a9acb90efe0c1fc868ec9`  
		Last Modified: Tue, 03 Jun 2025 13:33:02 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:d98abae7c36c56392c162ee3170d42a5038c1e0ce496f7d88415d16d372bc725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4145066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424d3eb8544ce5aeff0f107f9e5401db5df05a3d6b4eb846a7bfe8317ded7197`

```dockerfile
```

-	Layers:
	-	`sha256:6403c7d254de15e732b1f964b709bd507258daa4d72186bef68343cbcaddd7f2`  
		Last Modified: Tue, 03 Jun 2025 13:33:08 GMT  
		Size: 4.1 MB (4114244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c4b4b6b3d76048bd3c14f3191bddc4c79f81a8ae3c7238cfea22dd9e9998c38`  
		Last Modified: Tue, 03 Jun 2025 13:33:10 GMT  
		Size: 30.8 KB (30822 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:e1111af309e0332f10133050681fb8eb7aef6a23236f6ab5acc42da077f3413e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114566364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119ec9a2e89057565c91e812c4dd5c81417f9af78372708f6edbb9eb22098330`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 21 May 2025 23:31:53 GMT
ARG RELEASE
# Wed, 21 May 2025 23:31:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 21 May 2025 23:31:53 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 21 May 2025 23:31:53 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aec2f93beb092fd508654d6b65008daccc70c648b327c0a15b2c30625a1adf`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d65edb66daa513260a7a1438a1a6f3265ff07b0f1a6e7e043855431f352db2b`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 5.9 MB (5913654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1082ff111e81d8c4c7c6533f02f800be6c3a27ee393fc4f48a96a584eb32bd08`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367eb33e92948e16a0b36c4f09f83550bad0ebea905b573e81e519697bdaa745`  
		Last Modified: Tue, 03 Jun 2025 13:33:14 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053b975896d3dbf91ec0335350fa8547342839cefef8693f74c03e2d5386f75c`  
		Last Modified: Tue, 03 Jun 2025 13:33:21 GMT  
		Size: 74.3 MB (74313269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b278fcdb8a9403e05844ed3ae3adabd9e18a3fbbd6ac3f7243b46d6ad6bda`  
		Last Modified: Tue, 03 Jun 2025 13:33:22 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66d0bf1bcb597611f9d766447173cbf6f6b9abc4c34108268883073d9c620ee`  
		Last Modified: Tue, 03 Jun 2025 13:33:25 GMT  
		Size: 8.4 KB (8397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:3075f3813868c9545d8a6040b343580933bbc62cca1d7b142faa12181564296e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4145580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70bfb82a1ca0d538070dfe47a739a37c833d21116850336a58c018b6495f627c`

```dockerfile
```

-	Layers:
	-	`sha256:64e6aeb4925bc919eeeb5c7c6c184f86410ef770257ec196b077ec997fc15767`  
		Last Modified: Tue, 03 Jun 2025 13:33:30 GMT  
		Size: 4.1 MB (4114882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5894a2345cddf2889cc274796c400b2f7c7007762cfa2e8215ad42025f64117`  
		Last Modified: Tue, 03 Jun 2025 13:33:31 GMT  
		Size: 30.7 KB (30698 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

```console
$ docker pull mariadb@sha256:c2aa70fcdc2f703cc5a7107f6d8bab70f746ba8aaa6c375d568b72a614ba3dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.7 MB (109732238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b00fa85e9f3d3569e42329661ee1f422d6588c4cbb65971013da3b4a3ea6eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 21 May 2025 23:31:53 GMT
ARG RELEASE
# Wed, 21 May 2025 23:31:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 21 May 2025 23:31:53 GMT
ADD file:b6b8557b3fef6c06eb943ce735f649cf7033ab3925e70e6b43901f1f29b4d5e9 in / 
# Wed, 21 May 2025 23:31:53 GMT
CMD ["/bin/bash"]
# Wed, 21 May 2025 23:31:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV GOSU_VERSION=1.17
# Wed, 21 May 2025 23:31:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENV LANG=C.UTF-8
# Wed, 21 May 2025 23:31:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 21 May 2025 23:31:53 GMT
ARG MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ENV MARIADB_VERSION=1:11.4.7+maria~ubu2404
# Wed, 21 May 2025 23:31:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 21 May 2025 23:31:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 21 May 2025 23:31:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 21 May 2025 23:31:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 21 May 2025 23:31:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 May 2025 23:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 May 2025 23:31:53 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 21 May 2025 23:31:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7fa55ab2f467363da0197dee4a8e5af9e7ba7ef5686c6f0951bc509c387b765c`  
		Last Modified: Tue, 03 Jun 2025 13:31:43 GMT  
		Size: 29.9 MB (29930056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804a13623bce625679e864774fe2b261ed02034b35ff8b2583c726c56d9ea4e8`  
		Last Modified: Tue, 03 Jun 2025 13:31:46 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f15a2b0453944ed71ea96d071142918aa6a2624ccbb26cb62fdd998dadf4bd`  
		Last Modified: Tue, 03 Jun 2025 13:31:48 GMT  
		Size: 5.5 MB (5483127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b417049e11f5879de3bc012d1d14f690887697020f55619030293ab9ee75f08`  
		Last Modified: Tue, 03 Jun 2025 13:31:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e400a476cbc29d6b87b683327379f59826cee4a94dddc986b19f9a08baca25e`  
		Last Modified: Tue, 03 Jun 2025 13:33:36 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9379efe367b17fcce4ad4773ef9ccd3e21835a45b677595431ae678d3009f8b`  
		Last Modified: Tue, 03 Jun 2025 13:33:43 GMT  
		Size: 74.3 MB (74304826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879da734a22e0cbc420cc95b4513095c0c3f43504298a8aa40f27a6adc0b0c89`  
		Last Modified: Tue, 03 Jun 2025 13:33:45 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba8ff219216ede44610078c96fc2e802d065d738f9c6b2e7efbab93234c641a`  
		Last Modified: Tue, 03 Jun 2025 13:33:47 GMT  
		Size: 8.4 KB (8400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:cb279389cae4180f3db868fdc51f01ebf06700dbc776abd1fd25a2dae2dfafda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4139354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3781a6fc6cba7e68bf62602744131533229139cac1bbb84a9380201e449a6a26`

```dockerfile
```

-	Layers:
	-	`sha256:42a0c65f52ae9f6857a47d62d7132d9b6129d7d291fbf245e98bca5918cd1055`  
		Last Modified: Tue, 03 Jun 2025 13:33:53 GMT  
		Size: 4.1 MB (4108720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061bcaa526ff7d9e64e8332dec30b3e5dd49d8bd385f7cdad433e5e96809bcff`  
		Last Modified: Tue, 03 Jun 2025 13:33:55 GMT  
		Size: 30.6 KB (30634 bytes)  
		MIME: application/vnd.in-toto+json
