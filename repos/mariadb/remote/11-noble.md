## `mariadb:11-noble`

```console
$ docker pull mariadb@sha256:12244ee83e3c6e934c15c71b7b6028fc4a4413e74dbecbb36a6982417e0d2361
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

### `mariadb:11-noble` - linux; amd64

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

### `mariadb:11-noble` - unknown; unknown

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

### `mariadb:11-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:71f09a2a5748e14b27c69017a1316a8f69c4bb3034bfda291556064efd61a435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122396526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6847f0c2eeaf6eb0eead5f4e3da1fd7c820cdd4cd84dec672c9b7dfa0efba181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
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
	-	`sha256:9502885e1cbc0555698020a32dea91a7124302b31e46e81699f8eb0752cdf706`  
		Last Modified: Mon, 29 Apr 2024 17:08:50 GMT  
		Size: 28.0 MB (28015067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8530a8229b642bc201d79a9bc30ce581afa71086f34589791d88a5067e18cc04`  
		Last Modified: Fri, 31 May 2024 16:23:54 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972416b068932f26c6c375e8254dc3d880cdea4db8699a1fd0b5e309b62b9dd5`  
		Last Modified: Fri, 31 May 2024 16:23:55 GMT  
		Size: 7.4 MB (7350045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cc607c0c1576532265b0047dd07922e90a798127a9565f9b17fca1e78c9449`  
		Last Modified: Fri, 31 May 2024 16:23:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445b0c7913576d9592706635c9c34353c26a128f9423df55cbb1e30264081a73`  
		Last Modified: Fri, 31 May 2024 16:26:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108e71d2783c43822f2075017c0238045912d9b4e18a2ca656c2754322faec68`  
		Last Modified: Fri, 31 May 2024 16:26:59 GMT  
		Size: 87.0 MB (87017851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2ce2727898dd4d4e3113563b0edef8bdcd0359cf2f30049e2567d42a6402b6`  
		Last Modified: Fri, 31 May 2024 16:26:56 GMT  
		Size: 3.6 KB (3615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34c9af6c129b248d5069debbd1fba671e3c197d6269e916570d453cb6687abf`  
		Last Modified: Fri, 31 May 2024 16:26:56 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:00ddc88f196310ba8771679f128c3cc79036f82ab3ebd3587ea53be25622e374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5aa7609baedb81ba505c7d7a60cf6a6f0be6460cdc528429c7635e77227dd9f`

```dockerfile
```

-	Layers:
	-	`sha256:f1828bc09c406985646b525d9e80e55b2c3e19f2f24029f70f1c274b7e504a4a`  
		Last Modified: Fri, 31 May 2024 16:26:56 GMT  
		Size: 4.0 MB (4031011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b220fc276bb6f082b11358cb6f5882ff5a5f087cfb3e5383d07895198b6d1809`  
		Last Modified: Fri, 31 May 2024 16:26:57 GMT  
		Size: 31.9 KB (31930 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:af0f50dc28d2fd64239c0f09c0dd98759f74eae1afc6423e2d90fd0bc44f45ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135507839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142fa47e0bbacd9a792ea8c53ca1b35756d892f4d953e14a3f88cfaa2b755c7d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 29 Apr 2024 16:36:39 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:36:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:36:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:36:42 GMT
ADD file:c915ac180ad59faba89e9e3f73473adedd3ac5b7024bea2fe61b266b3efc1267 in / 
# Mon, 29 Apr 2024 16:36:42 GMT
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
	-	`sha256:a4196a9eeb6a07a3ef4f5885f4695a8ed06afbcd1291fc4128f9e405aaab821f`  
		Last Modified: Mon, 29 Apr 2024 17:09:03 GMT  
		Size: 33.5 MB (33493549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7fce08dc181d1ca2f6f9c52dc061715d04bbe457a5498c456d06bfe734fddf0`  
		Last Modified: Fri, 31 May 2024 01:31:58 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff5646a747caeff03e2d6d2661fcb8c1f7f39d3e42b65ceb7b4fb98efa1733e`  
		Last Modified: Fri, 31 May 2024 01:31:59 GMT  
		Size: 8.6 MB (8608818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e83ae90f0bedfc807cebb2ef0949e9fc0ca9f7c8106949719c2daad57d8aee3`  
		Last Modified: Fri, 31 May 2024 01:31:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780d78e40386237c130080f3a77369176b55f709a4d43d06763c57540e40baaa`  
		Last Modified: Fri, 31 May 2024 01:35:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4229072915e6fddf8d6497a343b5c621748c905eb2f3410ee6e77de07995b5`  
		Last Modified: Fri, 31 May 2024 01:35:15 GMT  
		Size: 93.4 MB (93391908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0fec261ee5b383605976a7ddc9ccaadf77a02168eb0be5153483585c2b6902`  
		Last Modified: Fri, 31 May 2024 01:35:12 GMT  
		Size: 3.6 KB (3616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6258663e70b48ee2789b18a128e6ad0fc3b7868c003c5dc6fde279dff714a985`  
		Last Modified: Fri, 31 May 2024 01:35:12 GMT  
		Size: 8.3 KB (8341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:aa99fe1e914433dcaa7cbe98fbbb8ec8fe4e7bfce8ddb89cd32efe0d28107a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13374ad519d7c7d1fb6dcd4aaa811777ca9f4f32a2b9393c6f0df5a652de567a`

```dockerfile
```

-	Layers:
	-	`sha256:a8703bd80375ea2bcecb885eac41f26c98b4415542875bc7ef6c99e6e70e8955`  
		Last Modified: Fri, 31 May 2024 01:35:12 GMT  
		Size: 4.0 MB (4031464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:167b2e2160044fa879b18a67a7f8f7db6756781289d6b19e0fe93adf4dea4849`  
		Last Modified: Fri, 31 May 2024 01:35:12 GMT  
		Size: 31.6 KB (31639 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:af5aa493aaddf47956ce6261a022ce68ddc87898fe69d0fa3650161bf64ce517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.0 MB (130955087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169d6a779f1a10d475c001edafdb58a86f1b233747ca4873fe53d069b21c1401`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:11 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:11 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:13 GMT
ADD file:09121ba3a412b610ce92684a3218535826bd353b73e98bc8efe44ad9b4233d0d in / 
# Mon, 29 Apr 2024 16:38:14 GMT
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
	-	`sha256:d450eb1572800c4118ae87f5fd5ee2a6fa067b00be1e578fcfee7725ca35a70e`  
		Last Modified: Mon, 29 Apr 2024 17:09:10 GMT  
		Size: 29.2 MB (29165121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a6425756d98485020a2b7992761b21821615e5e8075babe8e9dff9260da4a5`  
		Last Modified: Fri, 31 May 2024 02:19:49 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be8b14ed3a77d5b6feb7d7380a4b1861b67750af9dc08231acc7948f893cabb`  
		Last Modified: Fri, 31 May 2024 02:19:50 GMT  
		Size: 7.7 MB (7658595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28058b63d0fea7dbbb755debcbcf5a2ac7f10f857788623b2f542128e1bf336`  
		Last Modified: Fri, 31 May 2024 02:19:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9384849b24d50ae697e767ae4b14be9e3d6c88286181a24cd4595803781d308`  
		Last Modified: Fri, 31 May 2024 02:22:07 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e0cb0fe09e4ff671fe3877fdada17c68ae7603deaf9e428755bf465b0fe98`  
		Last Modified: Fri, 31 May 2024 02:22:09 GMT  
		Size: 94.1 MB (94117807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867040e6e095a1504d414a58f5bfff1a30a513d2d994adae7034b73281d53e1d`  
		Last Modified: Fri, 31 May 2024 02:22:07 GMT  
		Size: 3.6 KB (3616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9891dd4ecd0ddec03b2d8e9c8788def337c9c6e52048befe16dfffecec8a5e2a`  
		Last Modified: Fri, 31 May 2024 02:22:07 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:63bd2d3544e031cdcc3e716aebd04a8a84f1cf4021d73a63dddad1cb76e85855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262ecbf3ef27dfbfcd350ddb12e3ecc4d1de0654a378539176c72ada17a2eb2e`

```dockerfile
```

-	Layers:
	-	`sha256:1ed19aa0d5b547d7cfae67d0ffb497595a0ef8674ef16336bfa0572b6830b3a8`  
		Last Modified: Fri, 31 May 2024 02:22:07 GMT  
		Size: 4.0 MB (4025438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7f1cdf3655a1b65f77248e157da415026da1ee0dbc629af6f5b97e04b4a19a`  
		Last Modified: Fri, 31 May 2024 02:22:06 GMT  
		Size: 31.6 KB (31557 bytes)  
		MIME: application/vnd.in-toto+json
