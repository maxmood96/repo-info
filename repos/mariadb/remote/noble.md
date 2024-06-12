## `mariadb:noble`

```console
$ docker pull mariadb@sha256:396146c0a2e703ddebcf51f26abb28bf5590991d1d830c35c1d802034d140352
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
$ docker pull mariadb@sha256:36dfc3e71d54063523874845f7b616e1e48323b390dd67022473f5c4f0ec5f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122068131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d08fd2bbace4fd8221c9eb276e484946c5a95ced0cdac29ce31534934aa72044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 06:04:00 GMT
ARG RELEASE
# Thu, 30 May 2024 06:04:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:04:00 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:04:02 GMT
ADD file:7f5ee17de6aff2b67213e3ad424185b6eed94293669c5ab7cb155108c8df0e9e in / 
# Thu, 30 May 2024 06:04:02 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:00d679a470c495ef7d52e70bcd7a008f4983530b67653e63e9d3cd27fade63d7`  
		Last Modified: Thu, 30 May 2024 06:26:08 GMT  
		Size: 28.9 MB (28872332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381fb89d9026ab7e5d9f82dc23a74762e88573a1dd1863934be111dea40f5de3`  
		Last Modified: Tue, 11 Jun 2024 23:54:03 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd042176e576ff51f4279c616b99d98f1d38130a10565e8856ac1f0e86b2084c`  
		Last Modified: Tue, 11 Jun 2024 23:54:03 GMT  
		Size: 5.4 MB (5350640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b21b96f832d4aac9fb6948b9c1044929eb3a210c1ca23f0f162eb9c9666882`  
		Last Modified: Tue, 11 Jun 2024 23:54:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:310e39ef046da0643075343d34fb33570a80973519f1dd6c253b54f63d419a2b`  
		Last Modified: Tue, 11 Jun 2024 23:54:03 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e41361440255cf5980dd24671539742817ee3dcfc76bf6dc0c7560f6a9c5fa1`  
		Last Modified: Tue, 11 Jun 2024 23:54:06 GMT  
		Size: 87.8 MB (87831546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187e9145a80cc9c95a6906f0c45a747eecf4c9eb063f11ad9a17ba3ad9190c7`  
		Last Modified: Tue, 11 Jun 2024 23:54:04 GMT  
		Size: 3.6 KB (3631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8cfc1ced4583b76c762bbe006830db8ac6930c99cd9763f7353ded7ff488f2`  
		Last Modified: Tue, 11 Jun 2024 23:54:04 GMT  
		Size: 8.4 KB (8377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:1d9e27f807a8ecd573405b88e3549fb249517369908f2a80cb8b456057357580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc9e5fca7db454f56ebfd37b8adcf972debeeca142aeb4570ed2aae5163c801`

```dockerfile
```

-	Layers:
	-	`sha256:0d131306063d82d08c266a95e86100bbca33c06cf4fb772419030a8fb1de1ca0`  
		Last Modified: Tue, 11 Jun 2024 23:54:03 GMT  
		Size: 4.0 MB (4023713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd3f63391522099e3530b90534379879ef7c90e4f8241727eb149ef2f58c8a87`  
		Last Modified: Tue, 11 Jun 2024 23:54:03 GMT  
		Size: 31.6 KB (31606 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9e015817a69353a1912840d04e900ac8123e7129b9421c862ed2480e43e1a816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120183301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d6b3f858a26e8c8e1ee5b32b57fc13055a407bbf8d0d3db18e1a245e39e53`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:aa21f24e1940b1a682fe8effed3c9dcce0642450f7b085da08ebf725f3b70f1c`  
		Last Modified: Thu, 30 May 2024 06:26:14 GMT  
		Size: 28.0 MB (28018664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb291409c171c62fc068fd4b8a02acd33582f9f659cea2ca295c74a29947dd1`  
		Last Modified: Wed, 05 Jun 2024 16:13:35 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ab25513b917adf3e93a167a8fe0294c0c18c2d4c6b9b18a6ea3e5780b7d633`  
		Last Modified: Wed, 05 Jun 2024 16:13:36 GMT  
		Size: 5.1 MB (5131776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd997aaf9e3a3fc37228d055b04976f47865eeca24ae74db12a44962537b0f7`  
		Last Modified: Wed, 05 Jun 2024 16:13:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586af169321482fd7bc973f0dde35415a0bc08a457d1b2f9aeac5347d7e16ba0`  
		Last Modified: Wed, 05 Jun 2024 16:14:26 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac3a7174875b38d476e6d5bfc2c21f48dd0b3064273d44e05c6657bba32db68`  
		Last Modified: Wed, 05 Jun 2024 16:14:29 GMT  
		Size: 87.0 MB (87019247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0deeb7c2184236fa293626f9eb4b2f74c5ae7360c44db77a6fbcea9235cb6a`  
		Last Modified: Tue, 11 Jun 2024 23:57:01 GMT  
		Size: 3.6 KB (3629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b3bc9adcb1f1dd0c5090d322cab14facf66b4f8ae06686e8ac451b455b0b60`  
		Last Modified: Tue, 11 Jun 2024 23:57:01 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:070e23f5748f92e17e6328898253991fcb1951a2544de723d32cceab40f8cf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b2148cfc37928bf66f97f4cd64546a3d2fbed32387f3142b325b5e855b3c16`

```dockerfile
```

-	Layers:
	-	`sha256:e4fe897ca0a963222d513a02a070a3eb80d7e8f9aaef8b8691d935436e0cf444`  
		Last Modified: Tue, 11 Jun 2024 23:57:01 GMT  
		Size: 4.0 MB (4031015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dcd815339206222ddef3f2fe9842ebfe2ce2643fcedab27d67cbc2b3815b124`  
		Last Modified: Tue, 11 Jun 2024 23:57:01 GMT  
		Size: 32.0 KB (31979 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:516849d2e61b73bb8c9a5bd8155df943c2e7c76efe3f113a4368ed0bc03e2018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132843650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01395af6a49dd86bacde8a185daa2ce2bcd56e673c195087b52173f2075e223e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:059424863d1c38263ac74ee9c9b4b5d5df9febb81b7b0cd7ad14f5b351708678`  
		Last Modified: Thu, 30 May 2024 06:26:26 GMT  
		Size: 33.5 MB (33492344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443536062d915962a54bdf7885024c3f459391a879e298aab440754abaac9695`  
		Last Modified: Wed, 05 Jun 2024 14:25:54 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5b52d8357de6fbdd30b1cb05edc1654f599bd0e0413bb937735608317ceeb1`  
		Last Modified: Wed, 05 Jun 2024 14:25:55 GMT  
		Size: 5.9 MB (5945701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa03906778b7f66cc2839b95573d24ed00b0df012faef8b7da41cc92d6d489dd`  
		Last Modified: Wed, 05 Jun 2024 14:25:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297e00ca29b269bec9d4777166d738f82a54a14d2628ab4f218577f04c2fa6d2`  
		Last Modified: Wed, 05 Jun 2024 14:27:15 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a06ce5698630e002e4dfb231fdc004d2de3eef84707a8cd7d36ad394e2db28`  
		Last Modified: Wed, 05 Jun 2024 14:27:19 GMT  
		Size: 93.4 MB (93391991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632c81da18d112f34311fb1f0ba802c3615dd23de00a61a35a45c90588b2981e`  
		Last Modified: Wed, 12 Jun 2024 00:00:31 GMT  
		Size: 3.6 KB (3631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d54efc736222a03c7b7a7e4e244bfb7e847025551c172b206c2fe978235bd7`  
		Last Modified: Wed, 12 Jun 2024 00:00:31 GMT  
		Size: 8.4 KB (8379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:6f908bdcf8fbc87addaed7d6f74c25e3085d6ece7e4f4c1a826852b7ea15e998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7dcc4f5317b4a7599e73ba5ea84fcb153dcbf1a71c3cc375430589c48ef96c`

```dockerfile
```

-	Layers:
	-	`sha256:314304adf2c94691280b77f9f304705f333f661492e68c5ed82a920e2a709088`  
		Last Modified: Wed, 12 Jun 2024 00:00:31 GMT  
		Size: 4.0 MB (4031468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd0518939cb52fe0e40779685b4d7aa91b99f0ae28506586ebfcefd44b3d9b7`  
		Last Modified: Wed, 12 Jun 2024 00:00:31 GMT  
		Size: 31.7 KB (31688 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:noble` - linux; s390x

```console
$ docker pull mariadb@sha256:8d9b4114b5297e3c06ffdc3190f1e6555a67ee88883d7e19d5963b9c5ee847c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128828011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:909fe598289cb77b8f0b29ec769bdadc8c3f7489c1488510099e4d2fb7dde309`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Thu, 30 May 2024 06:02:59 GMT
ARG RELEASE
# Thu, 30 May 2024 06:02:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:02:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:02 GMT
ADD file:86f095e5ef79ee7d8fd4d38b4387a592e42b8c601012de015a295a8d2e2bca0c in / 
# Thu, 30 May 2024 06:03:02 GMT
CMD ["/bin/bash"]
# Tue, 11 Jun 2024 02:37:24 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV GOSU_VERSION=1.17
# Tue, 11 Jun 2024 02:37:24 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENV LANG=C.UTF-8
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 11 Jun 2024 02:37:24 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 02:37:24 GMT
EXPOSE map[3306/tcp:{}]
# Tue, 11 Jun 2024 02:37:24 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:dfeef248fc5b7b7a6c3c4f71a30ae3f5c8fc461af91cee39c368079dbaa3351a`  
		Last Modified: Thu, 30 May 2024 06:26:32 GMT  
		Size: 29.2 MB (29167835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b904e8e532582c582cd07e605f12fa03fda5f491f67edca5a3523d581df3abce`  
		Last Modified: Wed, 05 Jun 2024 07:48:31 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442098e59eb6057e9e1cd7fdf3b2d311534207d8a5098ac68eed931995478064`  
		Last Modified: Wed, 05 Jun 2024 07:48:31 GMT  
		Size: 5.5 MB (5528448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7096711287895ea34ff1fee80629c7cdc0911e50460a7219c8496e079aeba744`  
		Last Modified: Wed, 05 Jun 2024 07:48:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a9061d1b0721f8d8f6fce5a3caa4d2502fd7eba368ebdbd20437901a29f923`  
		Last Modified: Wed, 05 Jun 2024 07:49:38 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70ddbfda31476b90d652334ea207dbacc1e39325eb7c173ed859b0ff4412ca6e`  
		Last Modified: Wed, 05 Jun 2024 07:49:40 GMT  
		Size: 94.1 MB (94118104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d2a8e5b3887fb3a0894d7db8e70773147f4145b2f0a1cd26bc08fc66c9162a`  
		Last Modified: Tue, 11 Jun 2024 23:58:17 GMT  
		Size: 3.6 KB (3632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe64ec798a3fea6f0f4b9491a51eb1c0a3108b8dcff95d33874d779923d76c13`  
		Last Modified: Tue, 11 Jun 2024 23:58:17 GMT  
		Size: 8.4 KB (8380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:ff280735c19e3b374bb5ad6420c3e51707d43d10d227705b58d737cfcdd8ff60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766b3307382e75cf45c7cb9502d9c5ac7d533ccde981bac47ef5b6ba1a17a6a2`

```dockerfile
```

-	Layers:
	-	`sha256:0dfaae17d8d2854265218b33207d4d47b2a40c60e8214d7b02fae734841aae27`  
		Last Modified: Tue, 11 Jun 2024 23:58:17 GMT  
		Size: 4.0 MB (4025442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91ab0c12f797e57a492eb869bb3e04d3edebe64831f2ee5e7d23187dbaa4f610`  
		Last Modified: Tue, 11 Jun 2024 23:58:17 GMT  
		Size: 31.6 KB (31606 bytes)  
		MIME: application/vnd.in-toto+json
