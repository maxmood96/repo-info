## `mariadb:lts-noble`

```console
$ docker pull mariadb@sha256:78185355dd49b54dd6909072531ce8d7e06aa0eccd7aa5b23c93ebb7e34c5aaa
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
$ docker pull mariadb@sha256:c902499e9661a96c8151301746c7141c5462f9b766ed188cf1c495fa238f961a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103843333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd3e6e3af27dfb3fa12eb467205d9fafab29fa1c180ade7fc458aa063bfa73b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 18:35:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 20 May 2026 18:35:35 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 18:35:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 20 May 2026 18:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 18:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 18:35:35 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:35:35 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 20 May 2026 18:35:35 GMT
ARG MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:35:35 GMT
ENV MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:35:35 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
# Wed, 20 May 2026 18:35:35 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:35:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:35:48 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:35:48 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:35:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:35:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:48 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:35:48 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734a30f8b69cc167b07c5f7829bc9f29fd0b0275aa8898097b86ce503dc4e4d9`  
		Last Modified: Wed, 20 May 2026 18:36:02 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199691a65f0d1f67cc38f7d1249ac06d7cba8390e1ef3d4430a1a8412e0143d`  
		Last Modified: Wed, 20 May 2026 18:36:03 GMT  
		Size: 5.3 MB (5288056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9231a5d302adfc0db8d642c1bfd5b688d1c53d65c678a2d57d34d5802d600d9b`  
		Last Modified: Wed, 20 May 2026 18:36:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1c9d2d4f5b95705dfb409b73b412a1c2d4b6415ab04939bcc5d1fe09b247ad`  
		Last Modified: Wed, 20 May 2026 18:36:03 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac86d2b31a8a903325eb7ca0390f589afadb932f9f2fe758d26c30d18e7d3657`  
		Last Modified: Wed, 20 May 2026 18:36:06 GMT  
		Size: 68.8 MB (68808051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c1013d260b749c8db9bc1a5d65503cef552fdda3180ed48cf666df68897317`  
		Last Modified: Wed, 20 May 2026 18:36:04 GMT  
		Size: 4.0 KB (4038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019d8b2da7a8b24072a16f040fa81a9d83918df3962dff207b09955b24ee0181`  
		Last Modified: Wed, 20 May 2026 18:36:04 GMT  
		Size: 8.4 KB (8414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:6e105c419b572270bff5e79b8924bdf489f143fdd3b02afded542f676edb5851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53ce5c0a4b8521765b290591dd468d301c5772afcc6e137a777dd32b760fb63`

```dockerfile
```

-	Layers:
	-	`sha256:c0010fd12bf845d608adbb16434c4df02d6e530920e79e1be38779949fcd58d2`  
		Last Modified: Wed, 20 May 2026 18:36:03 GMT  
		Size: 4.3 MB (4274514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:330c68d9ff3477c28356383530a9a85eda3d47d0dea177f8492ea94718659cfc`  
		Last Modified: Wed, 20 May 2026 18:36:02 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:5086c7ad7f09d1b284bb7c81c767838572d03d65b8142dcf4508245260995bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101977991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f4cd29f3a55f7ad078e95f9ec71af356ad784796323c5e688854e420f1ccf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 18:35:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 20 May 2026 18:35:27 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 18:35:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 20 May 2026 18:35:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 18:35:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 18:35:27 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:35:27 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 20 May 2026 18:35:27 GMT
ARG MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:35:27 GMT
ENV MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:35:27 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
# Wed, 20 May 2026 18:35:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:35:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:35:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:35:43 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:35:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:35:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:43 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:35:43 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5748f55ea6c1bc2033907c4c86f663a94e0bd60e5eb5c35a6e291cbd228aa5ac`  
		Last Modified: Wed, 20 May 2026 18:35:59 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6080ded722c13840f0c3bf816ee5cc41a6f603afe97c20679a7bfd88c3c4c83`  
		Last Modified: Wed, 20 May 2026 18:35:59 GMT  
		Size: 5.1 MB (5098564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cca3838c89f20a4d942fafdef28f5f46a620738503650cb0894a96eddda2ec`  
		Last Modified: Wed, 20 May 2026 18:35:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b0f7c22970170dd43335f81bbd4a6e1a3aed05ecaf16ce551b611a011192d`  
		Last Modified: Wed, 20 May 2026 18:35:59 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ee291eb87e2d135004f7b921a6123f58204d7d74ade733b08136a1b4778232`  
		Last Modified: Wed, 20 May 2026 18:36:02 GMT  
		Size: 68.0 MB (67989407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7ef227d8b39b202827362bff48bc16d935907202378a131c98032160fb2d7f`  
		Last Modified: Wed, 20 May 2026 18:36:00 GMT  
		Size: 4.0 KB (4034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e04e573e65103729862e215125317de04cd179d160c2c31297df51d57f154d6`  
		Last Modified: Wed, 20 May 2026 18:36:00 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:d30a7272d5a4681fa2824177d185a23b000d482065d93d070114ca5df15d51ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c00a6346986ed4027111202ee6babd3e4620b35dadc54ea008da06160f69f4a2`

```dockerfile
```

-	Layers:
	-	`sha256:182f1179e2716b88847e15ba645f84ad5029b61f254c4fd51344a02c4a964461`  
		Last Modified: Wed, 20 May 2026 18:35:59 GMT  
		Size: 4.3 MB (4281791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e647092537e16ceb94c9e61ac537230055ce1b6b297cfa9aaafc395e1f2c506b`  
		Last Modified: Wed, 20 May 2026 18:35:59 GMT  
		Size: 31.7 KB (31665 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; ppc64le

```console
$ docker pull mariadb@sha256:82aefbf794b0870c2753e1c36e6b66fc358e508385a44b2e1126eb0d127449a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113764561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cc7ef993278e7b7fd126ada2ad4ea4a929f48ebc3ea3bd352fb0d4565e47d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 18:32:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 20 May 2026 18:34:14 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 18:34:14 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 20 May 2026 18:34:14 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 18:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 18:34:15 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:34:15 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 20 May 2026 18:34:15 GMT
ARG MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:34:15 GMT
ENV MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:34:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
# Wed, 20 May 2026 18:34:15 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:35:00 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:35:00 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:35:00 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:35:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:35:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:35:00 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:35:00 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ab6ca40b38a1b6ad029a23b02c6f38d37acddd780bccad2fe6a872da77e42c`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4183776bb3052cb352302661ff638d9d3fa37fbb73f2d193344662bca766db0`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 5.9 MB (5927651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cf481b7143192448683cac79bacf443d90e1285b373d223a51197aaac8272a`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4337ed89914f2d6afbc89d4e23b1bb220bbf5981a184ef3877fa61ad38299b0d`  
		Last Modified: Wed, 20 May 2026 18:35:30 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceed2ed11499603d62c07f84281e53a28fd2e85e05e658111ddecaddc36af14`  
		Last Modified: Wed, 20 May 2026 18:35:37 GMT  
		Size: 73.5 MB (73508489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4caa8e08dfbe4c08bb7e15795c4bb98aa124d7c3e147baa25737dfdacbe3c282`  
		Last Modified: Wed, 20 May 2026 18:35:32 GMT  
		Size: 4.0 KB (4036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca59b5903c7d06bcfd7cdaed9b76a4feb00639ef2aff4af3777ceae607dba7e6`  
		Last Modified: Wed, 20 May 2026 18:35:33 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:728d5db2d30132d9e60753ef677ab22b6eb0069c0f21f3cf26a5357168785205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4313980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a7f3f1239102a1b6e6b0d45a06e6f8985012271de87d4ce8c0e17683741eb1`

```dockerfile
```

-	Layers:
	-	`sha256:5eca64affe4f663895213884baca44a641e26b8b2c2239fd78592b353db998ec`  
		Last Modified: Wed, 20 May 2026 18:35:31 GMT  
		Size: 4.3 MB (4282449 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea56727c7410cd43fee53e37f875fbf4217d4c97ee86d7c99393c549c0606f2a`  
		Last Modified: Wed, 20 May 2026 18:35:30 GMT  
		Size: 31.5 KB (31531 bytes)  
		MIME: application/vnd.in-toto+json

### `mariadb:lts-noble` - linux; s390x

```console
$ docker pull mariadb@sha256:51b3d747e21ba608d7d4e07254c5d30763edaf1494dac5150f30920cdb1fac40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.1 MB (108149057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6a0ed622b3027fa7fc5fc1716c26ab2c0b7aa0d98206d06a296f0cc0a4a9b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Fri, 10 Apr 2026 06:50:27 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:50:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:50:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:50:29 GMT
ADD file:41defd98c44eed6fc946fd94496a94164879f2ad4f63d66a5c1e213cc2259ad1 in / 
# Fri, 10 Apr 2026 06:50:29 GMT
CMD ["/bin/bash"]
# Wed, 20 May 2026 18:34:29 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql --home-dir /var/lib/mysql && userdel --remove ubuntu # buildkit
# Wed, 20 May 2026 18:37:59 GMT
ENV GOSU_VERSION=1.19
# Wed, 20 May 2026 18:37:59 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 20 May 2026 18:37:59 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		libtcmalloc-minimal4t64 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 20 May 2026 18:38:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 20 May 2026 18:38:03 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 18:38:03 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:noble org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.8.7 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Wed, 20 May 2026 18:38:03 GMT
ARG MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:38:03 GMT
ENV MARIADB_VERSION=1:11.8.7+maria~ubu2404
# Wed, 20 May 2026 18:38:03 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
# Wed, 20 May 2026 18:49:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb # buildkit
# Wed, 20 May 2026 18:52:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 MARIADB_VERSION=1:11.8.7+maria~ubu2404 REPOSITORY=http://archive.mariadb.org/mariadb-11.8.7/repo/ubuntu/ noble main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /run/mysqld; 	chmod 1777 /run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi # buildkit
# Wed, 20 May 2026 18:52:58 GMT
VOLUME [/var/lib/mysql]
# Wed, 20 May 2026 18:53:01 GMT
COPY healthcheck.sh /usr/local/bin/healthcheck.sh # buildkit
# Wed, 20 May 2026 18:53:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 18:53:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 18:53:03 GMT
EXPOSE map[3306/tcp:{}]
# Wed, 20 May 2026 18:53:03 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ef1c26d09a5f9962879f732e212c4246a41e8473f6120efb435886357c85dd5a`  
		Last Modified: Fri, 10 Apr 2026 09:34:53 GMT  
		Size: 29.9 MB (29912147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1543cb0e690fa7db79bd58210bca3981df64f82ce3afa221d0f70bbdf98cb501`  
		Last Modified: Wed, 20 May 2026 18:46:11 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a588d47471ea77816b14a3b784226e4ec92fb840ec38ecabfb422718af40cc`  
		Last Modified: Wed, 20 May 2026 18:46:14 GMT  
		Size: 5.4 MB (5444548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f1a559dc1b9745625f2b36b9decd35a0811f54381d60cf6d8227170052906b`  
		Last Modified: Wed, 20 May 2026 18:46:12 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a52df36550402da40f5e12ef69125f271a252fa777ca30b2ca808b665482d6`  
		Last Modified: Wed, 20 May 2026 18:54:07 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38f9887ed948c8ed9dc9bba3aeee517bff2e69bb4423df47a3a9b49d3e92d92`  
		Last Modified: Wed, 20 May 2026 18:54:13 GMT  
		Size: 72.8 MB (72778105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72db68d21dc043f859e4e5aea5150af1cbb698367e0e58b5f4b35025318ef14`  
		Last Modified: Wed, 20 May 2026 18:54:07 GMT  
		Size: 4.0 KB (4035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd9d9b462503f3ce98a0be631b69aa4655b7fbc3d74bf0e5e254916bb045815`  
		Last Modified: Wed, 20 May 2026 18:54:06 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mariadb:lts-noble` - unknown; unknown

```console
$ docker pull mariadb@sha256:6fab9d72f1389d98f49d2355d11f3ec5565bb87aff601a5bb1a2670cadfee475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4307688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2232408ddcb0f0d95343e22d7e150f7aad8041feff552ac39c3c8c84ebdfa555`

```dockerfile
```

-	Layers:
	-	`sha256:641961ffbe95c982f81b3bc8a3b017e1fa97eb118744f75d03b945c7759ce57b`  
		Last Modified: Wed, 20 May 2026 18:54:08 GMT  
		Size: 4.3 MB (4276233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c86a21750c7a9a0b58a71079a6b9209914b0f7177253081dcf83d2d1f33c30af`  
		Last Modified: Wed, 20 May 2026 18:54:06 GMT  
		Size: 31.5 KB (31455 bytes)  
		MIME: application/vnd.in-toto+json
