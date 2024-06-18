## `mariadb:lts`

```console
$ docker pull mariadb@sha256:f9d00f880657a6ec4645e727181411e8c6826b29fc2ca9ee5e22c8cdee001bed
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
$ docker pull mariadb@sha256:fdc72e8f2960d758aa77ebac9ea65028ca195d4cba854a14e4afae703f5f6a22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.0 MB (122028062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4486d64c9c3b538b6dee6bcd5ea0ac5f74ea5e3cafc71181a54ec678ae0370aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
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
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f7f3c9a7412f9c52b77cdfa3ea4c45f541c95f9819e959dab2cba4200a0e6c`  
		Last Modified: Mon, 17 Jun 2024 22:49:31 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c034108521826c8ff2e6ed440ed2eeda9817a783c1c0f707d6e4496354b484`  
		Last Modified: Mon, 17 Jun 2024 22:49:32 GMT  
		Size: 5.3 MB (5348306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50366979c20a723076928e483f24034f6003f2f64ba0c566dd6bbf14eeb3cfbe`  
		Last Modified: Mon, 17 Jun 2024 22:49:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0221331af5c08ed2caeeca2a04e9b8cc074a68706a3da3744017f51aa8487093`  
		Last Modified: Mon, 17 Jun 2024 22:49:32 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c4d1c9d9cbdf9ea9685f5485710d4134001c65eda60fe34227f92208696a40`  
		Last Modified: Mon, 17 Jun 2024 22:49:35 GMT  
		Size: 87.0 MB (86960986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef7a8467f9894ed17342c4b3c9f113a0ce78fabddcd5e85f3c8ff190cc09475`  
		Last Modified: Mon, 17 Jun 2024 22:49:33 GMT  
		Size: 3.6 KB (3632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c15bb5bb031dc77bf55ee64652dcf5ae2e2eceb45aa5e31b3c38f2adfe7ee2`  
		Last Modified: Mon, 17 Jun 2024 22:49:33 GMT  
		Size: 8.4 KB (8380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:fcd449d112ed53008fc24e5f0abe4276aa3cb1b99e9972225344ccd8666d6a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eeed453db6466101ee2616dfe848275cdf2395de848d09ee0d14c462e04e1d4`

```dockerfile
```

-	Layers:
	-	`sha256:8a66b0a4b050cda5d188b7f1425fc0853c57599eaedddc5f1428d746139b9e7b`  
		Last Modified: Mon, 17 Jun 2024 22:49:32 GMT  
		Size: 4.0 MB (4024547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6a9d714b2b3a5e6a823bb5e5a58fa78f22715037ddac3255c74859222bf1254`  
		Last Modified: Mon, 17 Jun 2024 22:49:31 GMT  
		Size: 31.6 KB (31606 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; arm64 variant v8

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

### `mariadb:lts` - unknown; unknown

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

### `mariadb:lts` - linux; ppc64le

```console
$ docker pull mariadb@sha256:05de170690b750d28b7dfa7a98f520c49372debbe6d4fa15833d1bc72c0e938f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132816091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4bd79b7d68ee18467749098fb93b290e00549231dc8821983e709059084267`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
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
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09adda1317e6826b5d983ce456b705ac15a158737ed13cbed308f6f76454e180`  
		Last Modified: Mon, 17 Jun 2024 23:19:37 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c601a19205f49c7c789f708015bb87ad1eefaaa3ceb9f40659b9a3c3fbec2d`  
		Last Modified: Mon, 17 Jun 2024 23:19:38 GMT  
		Size: 5.9 MB (5943653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152889e72928cb809f2fe6769f7ab0a1c85e5b041d69e3aed543b65615270834`  
		Last Modified: Mon, 17 Jun 2024 23:19:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8ac4ee725fff29845300841de9438610af751b71979449b6d3d231b24fd2a5`  
		Last Modified: Mon, 17 Jun 2024 23:37:06 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc208a256557596195beb471e50836cee8d399d4dd85f370565011b163834657`  
		Last Modified: Mon, 17 Jun 2024 23:37:09 GMT  
		Size: 92.4 MB (92352792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e32d5cede26412c970178043be8206cad60905b2479574eebede5ca179c5ef5`  
		Last Modified: Mon, 17 Jun 2024 23:37:07 GMT  
		Size: 3.6 KB (3631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42414d6ea5ba44d90ee8d107432523ddb405ecfcbab5a27b5e26633d6df54f66`  
		Last Modified: Mon, 17 Jun 2024 23:37:07 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts` - unknown; unknown

```console
$ docker pull mariadb@sha256:3888f9cd313355c3bc365511f4f2c434d2045d78f3bc18e744ca836b1569e3df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf87b15b783a22b9c20a131104a7f895c1af5065b05ca0fc53c504d860c576e0`

```dockerfile
```

-	Layers:
	-	`sha256:3e7ea97a34e249ab175020c68def208f767a444e11adff1b83261d87603ad9bd`  
		Last Modified: Mon, 17 Jun 2024 23:37:07 GMT  
		Size: 4.0 MB (4032307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57ce3909b2c2c398a95cfcdf79310c2182d21e596b44a30798cac49a3644b0b`  
		Last Modified: Mon, 17 Jun 2024 23:37:06 GMT  
		Size: 31.7 KB (31688 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts` - linux; s390x

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

### `mariadb:lts` - unknown; unknown

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
