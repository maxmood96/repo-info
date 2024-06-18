## `mariadb:11-noble`

```console
$ docker pull mariadb@sha256:e59ba8783bf7bc02a4779f103bb0d8751ac0e10f9471089709608377eded7aa8
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

### `mariadb:11-noble` - unknown; unknown

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

### `mariadb:11-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:d772844a71b9682194d9adffd17b194689688f47624968e91de7045655a95190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.1 MB (120146236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2313083ebb3ca1fde006294f4d4d04032d992466bd677337d2fb96b47219eea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
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
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4ffd57e0533519955c7536d5e861aa90342d45fbce84f0bebec566fae70897`  
		Last Modified: Tue, 18 Jun 2024 00:27:40 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c957fe3312e7b0c842457b0afb02f5237aefb5926448bb41cf639bfac8bccf1`  
		Last Modified: Tue, 18 Jun 2024 00:27:41 GMT  
		Size: 5.1 MB (5129609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4899d66f413ce935102c2ed2838431bf95fba5b037e95df7f7ba489f6d0055c6`  
		Last Modified: Tue, 18 Jun 2024 00:27:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb019725fb14cdab7ed6c2eec6664a86aef99d44eea7302f1018465278db01e`  
		Last Modified: Tue, 18 Jun 2024 00:51:58 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fe81485ea8052e4474524d62ff5fcf39d594906722186e5cbd4e91fb0a5403`  
		Last Modified: Tue, 18 Jun 2024 00:52:01 GMT  
		Size: 86.2 MB (86159960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194c73d14556b3fbe02108d15719ebde29dec01f20263bdc978fd00d13e934d2`  
		Last Modified: Tue, 18 Jun 2024 00:51:59 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5a0156c39980c18348ae79a86790cd16d1157466506f5b140fb7b8a3fb9730`  
		Last Modified: Tue, 18 Jun 2024 00:51:59 GMT  
		Size: 8.4 KB (8381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:8f88e62c21d98ca5d96e1aaf45bffd26d1a7a5aa5660e72344db0c6e8ff34eed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad3c158f640a8a0d4d4e3d3dd1238af681f041c2e11ad0ab9bbf060649e37e9`

```dockerfile
```

-	Layers:
	-	`sha256:dfce4a4775d262d784ffdadbb16d1228b85d136e79efa3bbe599a97c06515171`  
		Last Modified: Tue, 18 Jun 2024 00:51:59 GMT  
		Size: 4.0 MB (4031850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b15fe2b9d2ef5e8b95f7498fc8087db5fda7da65aaf320b3de57daf2428967ea`  
		Last Modified: Tue, 18 Jun 2024 00:51:58 GMT  
		Size: 32.0 KB (31979 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:11-noble` - linux; ppc64le

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

### `mariadb:11-noble` - unknown; unknown

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

### `mariadb:11-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:3af38083c53ea90d6bec2e69244c583cb7287759fc3d9cbaa60d79a3c7be1be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128791698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b2cb8c44237881a8d763ba0764b1695441181594bcb5eca823f4ac27f65c71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:41 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:41 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:43 GMT
ADD file:25fd4d5892ebbc4a423c330fe39c4ea6e82588ffbcb191cf41477a4446e164e0 in / 
# Fri, 07 Jun 2024 12:00:43 GMT
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
	-	`sha256:a6125d8d1f1ce7b6b64fd8488df6bfb6b16e2bc511182f295d85af07d68cb191`  
		Last Modified: Fri, 07 Jun 2024 12:11:52 GMT  
		Size: 30.0 MB (30045689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f1db406da16dbc3bb64eec0c566be8d83675b1ae46cd32cfc3da42e8d28554`  
		Last Modified: Mon, 17 Jun 2024 23:53:33 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811bb1b1c77068864262232e82ece4e89f38558434d078b3ec66848fe3551bed`  
		Last Modified: Mon, 17 Jun 2024 23:53:34 GMT  
		Size: 5.5 MB (5524906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38b9db14751f5c918ed8d821b9ba8064317f0023802596e6b4cedefdf374348`  
		Last Modified: Mon, 17 Jun 2024 23:53:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587a1549f66144b2ce7b4284ca192ddf6f3a1d1bf13eca3179d8a982a9e51f5f`  
		Last Modified: Mon, 17 Jun 2024 23:54:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1155f2dd5784d7a8d3a91f4c4a4827247693aec70f106340b6cf025a17aa0b`  
		Last Modified: Mon, 17 Jun 2024 23:54:41 GMT  
		Size: 93.2 MB (93207483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019cc9591fc90a5d6673b5c42f4b5255863b12eced62e43888c9bdbe60d57278`  
		Last Modified: Mon, 17 Jun 2024 23:54:39 GMT  
		Size: 3.6 KB (3632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b59063b21bf28bbbaedd67038ff7066df966230a7b913df2f51cfba3a44e7c`  
		Last Modified: Mon, 17 Jun 2024 23:54:39 GMT  
		Size: 8.4 KB (8379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:11-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:88d5d15a4fed44e609ba62183632e8413c3c6b2d1ff4deda9e798b8467fd83b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e183f6a302d9068777ec923ccd0cac6832fc65f0a3011a6562798efbf20defbd`

```dockerfile
```

-	Layers:
	-	`sha256:b2dfba2ccec4cf6da43e9b4571273ec66da98f7d7cf31654cecef634a8e0450c`  
		Last Modified: Mon, 17 Jun 2024 23:54:39 GMT  
		Size: 4.0 MB (4026275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57b4d8f9ce8176604d84e61bb4bf12c12d8e91518c760237e8cebc527100a31a`  
		Last Modified: Mon, 17 Jun 2024 23:54:39 GMT  
		Size: 31.6 KB (31606 bytes)  
		MIME: application/vnd.in-toto+json
