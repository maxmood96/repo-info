## `mariadb:lts-noble`

```console
$ docker pull mariadb@sha256:934277de8883c061e32a21d01c64973b28272b441a3f797faf189c045a7c0a51
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

### `mariadb:lts-noble` - linux; amd64

```console
$ docker pull mariadb@sha256:c678f9437a4bd2a89e68479b3799749f81845376d923d4b9512e4426ed6bbdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.1 MB (122068119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b177ae28b69f91e08b55e74a625068ce055e9a9276a51e063affe9755c068cc`
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
# Thu, 30 May 2024 07:51:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 07:51:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 07:51:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 07:51:53 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 30 May 2024 07:51:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 07:51:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 07:51:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 07:51:53 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 07:51:53 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:00d679a470c495ef7d52e70bcd7a008f4983530b67653e63e9d3cd27fade63d7`  
		Last Modified: Thu, 30 May 2024 06:26:08 GMT  
		Size: 28.9 MB (28872332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eddd2b094bc662391a8b8aa561e06eabad810891f1a483e9533915098192c60`  
		Last Modified: Wed, 05 Jun 2024 02:20:33 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bae458de01504976e754ad7c59420e13d336d0a0f53fe2e27367c97c947fd0`  
		Last Modified: Wed, 05 Jun 2024 02:20:33 GMT  
		Size: 5.4 MB (5350635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fd58cc8d1b823bf83f30d31814a963bd094c022ebf0ebc05140a0bdcbb443d`  
		Last Modified: Wed, 05 Jun 2024 02:20:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44b62991c05630ffe5ff77bfea1ac2dd9d6879eda395d059d7a254118d32015`  
		Last Modified: Wed, 05 Jun 2024 02:20:34 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dedb1c2846b9c5c1c703b24da36ca29dc619e02b5fcae5ff9375f8f6895c8c`  
		Last Modified: Wed, 05 Jun 2024 02:20:36 GMT  
		Size: 87.8 MB (87831594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa481306a939b5d7aa9e4f9c31afb28e26a84089377d73c008ef319a682a3dbe`  
		Last Modified: Wed, 05 Jun 2024 02:20:34 GMT  
		Size: 3.6 KB (3614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689797659655f2d0a1bcd3e1ddf168f767d319552165ea3115b3fcada10dd8e5`  
		Last Modified: Wed, 05 Jun 2024 02:20:35 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:1610f660f315085b84dc6af253b491854e6f40da3ed75b24e884520fd3ca25c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab95cfc20d00c5c6922b0f2b4c98c43f5ea95721a02c15e632004fe697e301f`

```dockerfile
```

-	Layers:
	-	`sha256:3eb1e2f5bd230a0b5f0cbb3dca111ffe914686789bc992dfd082ae170c7d8e72`  
		Last Modified: Wed, 05 Jun 2024 02:20:34 GMT  
		Size: 4.0 MB (4023713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae18a75d17fba62a22a34141fdbf95632d830323c5a89703c70b6a190c96c2f`  
		Last Modified: Wed, 05 Jun 2024 02:20:33 GMT  
		Size: 31.6 KB (31557 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:690b7077d4804705682b4b9af4ed7c18d4f38d368e3d3fa10106c4883f1cde38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120183246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f078f838f28b0db4602499c2b85ab9c5a31b875830890356b9a8c445554d712a`
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
# Thu, 30 May 2024 07:51:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 07:51:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 07:51:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 07:51:53 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 30 May 2024 07:51:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 07:51:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 07:51:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 07:51:53 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 07:51:53 GMT
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
	-	`sha256:482c0462aebebd004c7e014a13d31f2039ea2738262d246b50f9d05f24b62e19`  
		Last Modified: Wed, 05 Jun 2024 16:14:26 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ce8ab27d58b32ab45dc8155677f279c9f3d318638e2010b8aea338b7883daf`  
		Last Modified: Wed, 05 Jun 2024 16:14:27 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:772d141b3927e887def08e35585809c29a212575ddb0e898a895f689dca154e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0bcd86d1688c1fa61e37bcdb1fc2f4787c4de7703a4f3aa7b1931efea38de62`

```dockerfile
```

-	Layers:
	-	`sha256:b7307c73c8380876f8b61f5e46ecb1b5f8ca09e5e5f6b600b1ca2920c224b675`  
		Last Modified: Wed, 05 Jun 2024 16:14:27 GMT  
		Size: 4.0 MB (4031015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9feafe3b60155820aad95f00e2bf51b40476cdf31d5cfcd79b1e31313bfd7945`  
		Last Modified: Wed, 05 Jun 2024 16:14:26 GMT  
		Size: 31.9 KB (31930 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:c2d11f3ce22ea2a351d993d77cf06e4b7c1a9f5ce0c703cbdb4e0f5a9096847a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132843596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6959c1bdfaaebbcde70bdcc00af2c17486f1f2a2d7ff06ec2b1438d22bcd3a2`
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
# Thu, 30 May 2024 07:51:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 07:51:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 07:51:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 07:51:53 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 30 May 2024 07:51:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 07:51:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 07:51:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 07:51:53 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 07:51:53 GMT
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
	-	`sha256:3d8910fb1f2fa03cbfa785045f6ba5f57e0e08ce727528dc0a6435d479eff0e9`  
		Last Modified: Wed, 05 Jun 2024 14:27:16 GMT  
		Size: 3.6 KB (3616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf1b7fef353b669a4df1a9fbccf35c7e8cd49110a81d1ed402ec25234b0a9b1`  
		Last Modified: Wed, 05 Jun 2024 14:27:16 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:7151001387b0f23de8e584e311547e1ae51d779f69e13a225b6be8404aac25a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46080de5b4be276605a5f29b4ffed8fd58958d95bf2118395f084a1d7b84219`

```dockerfile
```

-	Layers:
	-	`sha256:2d7651326e57e0a7aacb599a00d80f5841a175f7e45ab3b6cac881a7d010d8c6`  
		Last Modified: Wed, 05 Jun 2024 14:27:16 GMT  
		Size: 4.0 MB (4031468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0912840009cef2105a48746a0b21977a254225f8492a28a55e8c640a00098044`  
		Last Modified: Wed, 05 Jun 2024 14:27:15 GMT  
		Size: 31.6 KB (31639 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:0e3d17f1856d690f0a32cec4ab6d62428bf377347ebb2e038c8c1a5ce64b963c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128827957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29264caf9c1e74c497f2ba552b835348b64eb10009f9526eb1d0e98c4b49c6e4`
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
# Thu, 30 May 2024 07:51:53 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV GOSU_VERSION=1.17
# Thu, 30 May 2024 07:51:53 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENV LANG=C.UTF-8
# Thu, 30 May 2024 07:51:53 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.4.2 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Thu, 30 May 2024 07:51:53 GMT
ARG MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ENV MARIADB_VERSION=1:11.4.2+maria~ubu2404
# Thu, 30 May 2024 07:51:53 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Thu, 30 May 2024 07:51:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.4.2+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.4.2/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Thu, 30 May 2024 07:51:53 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 May 2024 07:51:53 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Thu, 30 May 2024 07:51:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 30 May 2024 07:51:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 May 2024 07:51:53 GMT
EXPOSE map[3306/tcp:{}]
# Thu, 30 May 2024 07:51:53 GMT
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
	-	`sha256:07d284a30a4d92f9528dd08ba60b1c5ce16b19984e87b3e4d88d285148deaf7d`  
		Last Modified: Wed, 05 Jun 2024 07:49:38 GMT  
		Size: 3.6 KB (3616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22b8018e9394f765b7b67f28255fb1e290ce8d218cf8b1dbc37e49b3f79c0ce`  
		Last Modified: Wed, 05 Jun 2024 07:49:38 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:d6d4ae595aaac24862c884d8c6a3e84a979b5dd5cf4ef47467c49d398b53e601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e26f91b9073ebeb2e282402c098aff28be203df9f1383dbe78a8cd94c00770c`

```dockerfile
```

-	Layers:
	-	`sha256:725ada04b10ac21d45f084d944d897bb55b1b5923db8ac6139ac1d401250eb63`  
		Last Modified: Wed, 05 Jun 2024 07:49:38 GMT  
		Size: 4.0 MB (4025442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30ecdaa0795cc05dbbd1dfe3b88f9edb0e66b40d677a47fa2de2378d30e2a54`  
		Last Modified: Wed, 05 Jun 2024 07:49:38 GMT  
		Size: 31.6 KB (31556 bytes)  
		MIME: application/vnd.in-toto+json
