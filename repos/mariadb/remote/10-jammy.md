## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:197ed4890f934423f7095a460d58e93383d626f04e91cc25f7a64f44dd8bd880
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
$ docker pull mariadb@sha256:3f111eec639eeb22518b22566e9241f08bf13dcd5269472d79083b9dc39d7a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.6 MB (122566414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccf0a9f80dfdcc0e72f246f2cec86250bce2d33e916c712fc1711ec182a1a9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 11 Jun 2024 02:37:24 GMT
ARG RELEASE
# Tue, 11 Jun 2024 02:37:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 11 Jun 2024 02:37:24 GMT
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ed4502c671debee7e2b20b2c956e4ccd76832f6b70e99cb8b091002f758519`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccee233ae035d32fba3ddfb41a5edd77678a8b2091d0f28e507f22de07ac3504`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 5.6 MB (5647737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d32e878297621c1fa86b100f55357db81b92e4db48891e8b52e0c9162a035`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257a4184da5c351b40a184935703db59151c9e4a56cc95be5076e30a8f287e81`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079eb852aa15acc53e4181ec562c41a37e260ec0f569a71a96482f787c644cbb`  
		Last Modified: Tue, 02 Jul 2024 03:04:09 GMT  
		Size: 87.4 MB (87370502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6414a516a991dcf3104acd9fc67db2734c04f5455c650df3051367127f23f`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96faa6efb673ef390f8e2c6315e9528843fe4b90f9383da85caacd482bf29b8b`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 8.3 KB (8340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:e4812fc59f0e53d41b516a635fb4582a02020cb33421838774bd0ed057975933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4582591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7358ab4b88688e4d86963bc72aba75362c452b3757cb747ebb45630684625fd`

```dockerfile
```

-	Layers:
	-	`sha256:1edf2fd91ae2d6c6407f3ece9b1535eeec69e571fc0d5305c2c5a17d18dd115f`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 4.6 MB (4552165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcf4fa95e2b1697a48395c1c23722cb8f790eb1fc99cd008ed12c14b011188ef`  
		Last Modified: Tue, 02 Jul 2024 03:04:07 GMT  
		Size: 30.4 KB (30426 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:e5ff77af80530b7f30a2b17678ea6efc92514552a700826f3c80649e1773513c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.0 MB (117012638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81a86fb8106734e436e03292262a749843cf1cc21335adc721a30a9ea71e31fa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331be689e5be1cbce31535ffbf720385fb4f71ee3823c42972ec48179d84d78f`  
		Last Modified: Wed, 05 Jun 2024 16:15:54 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6bbb859570f6acfcb7882965b2b530064d726df12e949a4712c5034115af6e`  
		Last Modified: Wed, 05 Jun 2024 16:15:55 GMT  
		Size: 5.5 MB (5462658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73d9b054a673883441c0d2daf29033f084d0bace77a3d63e8deaefb9c4467cd`  
		Last Modified: Wed, 05 Jun 2024 16:15:55 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41019807b3c9e914c39cd394a47ac1dda186421244cd945fb37d0979bfa8dddc`  
		Last Modified: Wed, 05 Jun 2024 16:17:42 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c9aaf48af4ccb90561506ee59b47d6ec1025fd7a9488cea72e985603214b10`  
		Last Modified: Wed, 05 Jun 2024 16:17:44 GMT  
		Size: 84.2 MB (84174059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b3ef3d99d583eabaa4f20377045ac71c033e1734345adce040b4f6ffd5405d`  
		Last Modified: Wed, 05 Jun 2024 16:17:42 GMT  
		Size: 3.6 KB (3616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7271026b1c97a3ba27f15df07f333abcbff601b26e40e7eec9ada160ca7e8d0e`  
		Last Modified: Wed, 12 Jun 2024 00:00:25 GMT  
		Size: 8.3 KB (8343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:499bb03937ae949a79affb1730b5b4a707c42d0f4f02ea0a2089e0528078d801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4589357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13409f45a02fbe94dc2d110c6117f95d1fc48f73eb45bc022a756654f24ac8f`

```dockerfile
```

-	Layers:
	-	`sha256:b2d50b5d47abb1664a658cdf79d017f52a4a32db5fa19bbfcb95c54f1f067a60`  
		Last Modified: Wed, 12 Jun 2024 00:00:25 GMT  
		Size: 4.6 MB (4558605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82df36718fcbce6d216d4824bd7d716e2fe1ecbe3b0e3c9284d22e832200c92`  
		Last Modified: Wed, 12 Jun 2024 00:00:25 GMT  
		Size: 30.8 KB (30752 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:8685cbaba4989b6ca9eb8ec2d87068f89c6da91136f0c7f07fe5e8dafe788e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130626834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237d7b2c752cb8ba114c9001204c80c6414c565e6a71943950196ea771686216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 11 Jun 2024 02:37:24 GMT
ARG RELEASE
# Tue, 11 Jun 2024 02:37:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Tue, 11 Jun 2024 02:37:24 GMT
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14434a7b1478c550cf7d089ce2cf67c0d046d7d2d67b5229e31eaf6de0cca113`  
		Last Modified: Tue, 02 Jul 2024 10:54:38 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f1fe207177f74d50f11f346325676b2722a78eb101820adce13494e001732e`  
		Last Modified: Tue, 02 Jul 2024 10:54:38 GMT  
		Size: 6.1 MB (6079549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08434d05a602005203b3c1aff405c608ead4ea6b632b86bf2fc46ed00dd4cf5`  
		Last Modified: Tue, 02 Jul 2024 10:54:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760dfce355e3685f640043d6f3aa4dd197642cab86b36c085fc1329ed2053915`  
		Last Modified: Tue, 02 Jul 2024 10:57:19 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7e201dae016fb629eefb7556fd92bbfc8117dd38baf83e1ca9313012ac21502`  
		Last Modified: Tue, 02 Jul 2024 10:57:22 GMT  
		Size: 90.1 MB (90072076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46f32fdb3372f559f0a7254403146d42427e04715126e5eb70f38c2d0c65d62`  
		Last Modified: Tue, 02 Jul 2024 10:57:19 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52dd6dca21a4f5e635ac78fd75cac077161ed87a01c2e34cdfa59de0f24f557`  
		Last Modified: Tue, 02 Jul 2024 10:57:19 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:54b14ac2d3a9993287c8de04db40b1176d899fe6a4ef0f46ab5d39d534a8cce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df6cbbe47f10747586c7796b0062afec72b4d103d5f2a6fc2bfc9df3bd7c8331`

```dockerfile
```

-	Layers:
	-	`sha256:ec0a024e917f94b94ceeb0c88d32e8162f20bb2af92381af974d5ef349fc51ab`  
		Last Modified: Tue, 02 Jul 2024 10:57:20 GMT  
		Size: 4.6 MB (4559796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e09521d9d65fb1321005ed3fabff70a34b07c5a6fb017714576b09fe0dab6a9`  
		Last Modified: Tue, 02 Jul 2024 10:57:20 GMT  
		Size: 30.5 KB (30485 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:f0a9f58d8d2f2cea4b266eb3428be9ae50e38710b85225b9fe62f2e7383774c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.5 MB (121546344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1889fc3d4713df6efba9ffaa193dc64bc4abc0242139a326e6e9498b9be84b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Tue, 11 Jun 2024 02:37:24 GMT
ARG RELEASE
# Tue, 11 Jun 2024 02:37:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 11 Jun 2024 02:37:24 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 11 Jun 2024 02:37:24 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Tue, 11 Jun 2024 02:37:24 GMT
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
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.8 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 11 Jun 2024 02:37:24 GMT
ARG MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ENV MARIADB_VERSION=1:10.11.8+maria~ubu2204
# Tue, 11 Jun 2024 02:37:24 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Tue, 11 Jun 2024 02:37:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:10.11.8+maria~ubu2204 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.8/repo/ubuntu/ jammy main main/debug
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
	-	`sha256:bc95fae2023d2ac4f35628ab3a262084bf2801462adfa6e7304b2b4e70ff4ab1`  
		Last Modified: Thu, 27 Jun 2024 20:18:52 GMT  
		Size: 28.0 MB (28000540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccd589ea21dffa20b237a73c265074d402d13a17068b6c00e3f87e251dfd79e`  
		Last Modified: Tue, 02 Jul 2024 06:12:15 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73cdc94364be122e4d5b8a375e6f8a0895efb584f6a2b9b6aeec366959ef462e`  
		Last Modified: Tue, 02 Jul 2024 06:12:16 GMT  
		Size: 5.5 MB (5532149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b59c85e5b9a6a82e884be6177a609e9017a73f566d539674f9d1dc9f7c802`  
		Last Modified: Tue, 02 Jul 2024 06:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39604e11cd8db17e64d654e3ce4cc67f486eeb54f7c2ad63cc6c9c2aab3c39c8`  
		Last Modified: Tue, 02 Jul 2024 06:14:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6182c951b06f0d7d1f26ae705413c1cd0671cf28ae836dd970e444968e537f5e`  
		Last Modified: Tue, 02 Jul 2024 06:14:26 GMT  
		Size: 88.0 MB (87999521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a898118851dc70b94d1b215a5751e0c649599b3de4f39c000a11b50471b8c4`  
		Last Modified: Tue, 02 Jul 2024 06:14:17 GMT  
		Size: 3.6 KB (3613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebcd893bae50e7f4abe71da62feaed47dcefa094e63c1973cfdc5494902fcf4a`  
		Last Modified: Tue, 02 Jul 2024 06:14:17 GMT  
		Size: 8.3 KB (8342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:10-jammy` - unknown; unknown

```console
$ docker pull mariadb@sha256:abce39a4dc7635020131e285b373226d8148960baeeef24a660fb059609b6eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4582920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6570c655fb7d46df0423b224b24c42ae26cbc34bbfe69ab6630831043a7a0f0`

```dockerfile
```

-	Layers:
	-	`sha256:f6b30efbd5ac8b324723d49db749ad8f0b9fc09b4276d92af49277a4716bbbeb`  
		Last Modified: Tue, 02 Jul 2024 06:14:17 GMT  
		Size: 4.6 MB (4552493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b917889614494c40d62a52e821433802e724b3f11b9628e248539ca813e175ca`  
		Last Modified: Tue, 02 Jul 2024 06:14:16 GMT  
		Size: 30.4 KB (30427 bytes)  
		MIME: application/vnd.in-toto+json
