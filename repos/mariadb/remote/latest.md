## `mariadb:latest`

```console
$ docker pull mariadb@sha256:7c6a4b7716e0c6f0455d81f41f4db8d2687273deed19e9c9b7a09f5830e1453b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:latest` - linux; amd64

```console
$ docker pull mariadb@sha256:ffdd06c9e58c8222d8bbbb426f347dbe1cb13c1c8494cbf98074a032da142d81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123138450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd537a872d20b231a4bb77b2b87be1f78373e915111932423bfc5fe0045fcf05`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 18:27:16 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Jul 2023 18:27:16 GMT
ENV GOSU_VERSION=1.14
# Tue, 04 Jul 2023 18:27:16 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 04 Jul 2023 18:27:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 18:27:38 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 18:27:39 GMT
ENV LANG=C.UTF-8
# Tue, 15 Aug 2023 01:20:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 15 Aug 2023 01:20:17 GMT
ARG MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:20:17 GMT
ENV MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:20:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
# Tue, 15 Aug 2023 01:20:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 15 Aug 2023 01:20:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 15 Aug 2023 01:20:35 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Aug 2023 01:20:35 GMT
COPY file:1980cab2a8b7fba7431710370aad263c40d659a4885e66510adf2002b57ddf4c in /usr/local/bin/healthcheck.sh 
# Tue, 15 Aug 2023 01:20:35 GMT
COPY file:41cd6c305128c82d238b47cc775ecf2262c7b95806428fa87026c43a3d858b56 in /usr/local/bin/ 
# Tue, 15 Aug 2023 01:20:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Aug 2023 01:20:35 GMT
EXPOSE 3306
# Tue, 15 Aug 2023 01:20:35 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718e898a86ffe915c46f60c599bc87928aa5e7e3a9434cbf52066b49651d3a1f`  
		Last Modified: Tue, 04 Jul 2023 18:32:00 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bd7a143a6c5d92cccbae0a38df554277f44cb4dbfcb668436dc5ed3398144a`  
		Last Modified: Tue, 04 Jul 2023 18:32:01 GMT  
		Size: 5.6 MB (5592713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80cdf483b70a4a08d0db0ff26cb8dbdc933588954a3bf91fce2f2544b7be37b8`  
		Last Modified: Tue, 04 Jul 2023 18:31:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde42c81159069286fe433515d8530d1cf95736560e681a410dc5178f9693a2b`  
		Last Modified: Tue, 15 Aug 2023 01:23:59 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7201941f79f4c384a98b87a6d3c2d5f0fa5ed04c1ac7c7fc5b106e31fc697ec`  
		Last Modified: Tue, 15 Aug 2023 01:24:11 GMT  
		Size: 87.1 MB (87101151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50e82e19b04daa9c4cdf8531bb75408ede9bfdff6b9ea392098cd9ce3b323500`  
		Last Modified: Tue, 15 Aug 2023 01:23:59 GMT  
		Size: 3.6 KB (3564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da2bc800ee928bb1b25eb087ca712b2b2e2c37b81f715b816a9e9631e2c502c`  
		Last Modified: Tue, 15 Aug 2023 01:23:59 GMT  
		Size: 7.6 KB (7567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:9f8f6eac045a3111de6aafaa4ece257ad70305d24b2eceed6236a5945ce76dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117636432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1b0653e1b48ebe69d1ad153d10d7eda72c4d6314257a1187b1cb3f4881f14d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 28 Jun 2023 08:42:48 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:42:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:42:48 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:42:50 GMT
ADD file:262490f82459c14632f5c9a6d6a5cf6c07b4f307e8fd380fa764662cda46e88f in / 
# Wed, 28 Jun 2023 08:42:50 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 15:48:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Jul 2023 15:48:55 GMT
ENV GOSU_VERSION=1.14
# Tue, 04 Jul 2023 15:48:56 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 04 Jul 2023 15:49:11 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 15:49:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Tue, 15 Aug 2023 01:09:23 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 15 Aug 2023 01:09:23 GMT
ARG MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:09:23 GMT
ENV MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:09:23 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
# Tue, 15 Aug 2023 01:09:24 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 15 Aug 2023 01:09:40 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 15 Aug 2023 01:09:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Aug 2023 01:09:42 GMT
COPY file:1980cab2a8b7fba7431710370aad263c40d659a4885e66510adf2002b57ddf4c in /usr/local/bin/healthcheck.sh 
# Tue, 15 Aug 2023 01:09:42 GMT
COPY file:41cd6c305128c82d238b47cc775ecf2262c7b95806428fa87026c43a3d858b56 in /usr/local/bin/ 
# Tue, 15 Aug 2023 01:09:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Aug 2023 01:09:42 GMT
EXPOSE 3306
# Tue, 15 Aug 2023 01:09:42 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ac34a2e0269ced3acc355be706239ee0f3f1e73a035c40dd2fac74827164ee53`  
		Last Modified: Wed, 28 Jun 2023 23:23:40 GMT  
		Size: 28.4 MB (28391011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f226d4d968a5322b60d61898c78418afeeb62f9a8613d9939d2546229a59ed0`  
		Last Modified: Tue, 04 Jul 2023 15:53:12 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a718d9544847f819e9859244c57b1093e55eb4bbd1d50066804d9ddd24d9c2c`  
		Last Modified: Tue, 04 Jul 2023 15:53:12 GMT  
		Size: 5.4 MB (5406735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad17cece0015293005bd369ad4550b0faa2ef78f55de897f35a48e5b101b83c8`  
		Last Modified: Tue, 04 Jul 2023 15:53:10 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742348862e7261bf7ef0286a7d5ae7dd0188a155cdc468e0f900433c6680eccc`  
		Last Modified: Tue, 15 Aug 2023 01:13:07 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1191150133085bfddabdffe017d28fda26ceadaeb36a46a5cb7d60d3bf44ce4f`  
		Last Modified: Tue, 15 Aug 2023 01:13:17 GMT  
		Size: 83.8 MB (83825315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e50cfa945140ebd9804c46e48c0b1fb797db304d67b30609e87de9ec491467`  
		Last Modified: Tue, 15 Aug 2023 01:13:07 GMT  
		Size: 3.6 KB (3565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813c65d70660d19712bcfb867bf0782b381ec5336f9d254a564b903979282c26`  
		Last Modified: Tue, 15 Aug 2023 01:13:07 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; ppc64le

```console
$ docker pull mariadb@sha256:3992ba4cd5ae6a5e4e560509d3251377c7109885ae92414ab1ccdaa16cb48ec8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131524103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19da6debc3f90943d998c15c4828fa7683f864659de51cf7223891f422a6b9e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 05 Jul 2023 01:06:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 05 Jul 2023 01:06:57 GMT
ENV GOSU_VERSION=1.14
# Wed, 05 Jul 2023 01:06:57 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Wed, 05 Jul 2023 01:07:34 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 05 Jul 2023 01:07:36 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 05 Jul 2023 01:07:36 GMT
ENV LANG=C.UTF-8
# Tue, 15 Aug 2023 01:07:05 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 15 Aug 2023 01:07:06 GMT
ARG MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:07:06 GMT
ENV MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:07:06 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
# Tue, 15 Aug 2023 01:07:08 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 15 Aug 2023 01:07:58 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 15 Aug 2023 01:08:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Aug 2023 01:08:03 GMT
COPY file:1980cab2a8b7fba7431710370aad263c40d659a4885e66510adf2002b57ddf4c in /usr/local/bin/healthcheck.sh 
# Tue, 15 Aug 2023 01:08:03 GMT
COPY file:41cd6c305128c82d238b47cc775ecf2262c7b95806428fa87026c43a3d858b56 in /usr/local/bin/ 
# Tue, 15 Aug 2023 01:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Aug 2023 01:08:04 GMT
EXPOSE 3306
# Tue, 15 Aug 2023 01:08:05 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af03c7013049bbb43a9d70711423a0aa0933ad63d557a33679e987f9f4552c2`  
		Last Modified: Wed, 05 Jul 2023 01:19:30 GMT  
		Size: 1.8 KB (1752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fae131e82b0a7c398eb2a917463894a99192198e537fa4a742953dfdec5d9a5`  
		Last Modified: Wed, 05 Jul 2023 01:19:32 GMT  
		Size: 6.0 MB (6017861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c002ce052617f5efe1f7afc4ec819f1f45b350c5956b79ee09c9bd522fe18736`  
		Last Modified: Wed, 05 Jul 2023 01:19:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebeb68280a5a79d2ba6868c49a7271bc85d0f0ce8944231f7746c0bca97046e`  
		Last Modified: Tue, 15 Aug 2023 01:16:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c918e2bee05c446858876cc31df7848ea249f78c3ec0f8d478771cc53042ddbe`  
		Last Modified: Tue, 15 Aug 2023 01:16:41 GMT  
		Size: 89.8 MB (89781414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcea5fb973f50ce18d355bb0acb6317d0b9ce031184515469f414c19727c09c`  
		Last Modified: Tue, 15 Aug 2023 01:16:16 GMT  
		Size: 3.6 KB (3563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4847ca930a7fb623ab19b0b4b6901144a93f8ef3bab1c27623ae93bcf95dd8de`  
		Last Modified: Tue, 15 Aug 2023 01:16:16 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:latest` - linux; s390x

```console
$ docker pull mariadb@sha256:0197121449cd52a4de8371ce1f0e916ea6c2be16f6c93e947dab258a367d01fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121603180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c694c0bcb8117bcbd49c11d7889aa83ef49002a7fb86da9ece254b2dce1d6f46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 28 Jun 2023 08:53:20 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:53:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:53:20 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:53:22 GMT
ADD file:fa0aef35be7808c8fd6751a52bdec4dd81057e2fcaa075c547a1db53640dae9a in / 
# Wed, 28 Jun 2023 08:53:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 16:55:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Jul 2023 16:55:27 GMT
ENV GOSU_VERSION=1.14
# Tue, 04 Jul 2023 16:55:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Tue, 04 Jul 2023 16:55:43 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 16:55:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 16:55:44 GMT
ENV LANG=C.UTF-8
# Tue, 15 Aug 2023 01:04:17 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=11.0.3 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 15 Aug 2023 01:04:17 GMT
ARG MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:04:17 GMT
ENV MARIADB_VERSION=1:11.0.3+maria~ubu2204
# Tue, 15 Aug 2023 01:04:17 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
# Tue, 15 Aug 2023 01:04:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 15 Aug 2023 01:04:33 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-11.0.3/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mariadb_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 15 Aug 2023 01:04:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Aug 2023 01:04:39 GMT
COPY file:1980cab2a8b7fba7431710370aad263c40d659a4885e66510adf2002b57ddf4c in /usr/local/bin/healthcheck.sh 
# Tue, 15 Aug 2023 01:04:39 GMT
COPY file:41cd6c305128c82d238b47cc775ecf2262c7b95806428fa87026c43a3d858b56 in /usr/local/bin/ 
# Tue, 15 Aug 2023 01:04:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Aug 2023 01:04:39 GMT
EXPOSE 3306
# Tue, 15 Aug 2023 01:04:39 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:ce02ee0330980398d6a84a50abfa1a8c4d1cba27cbd7442b79f4aa1b1a14020d`  
		Last Modified: Tue, 04 Jul 2023 13:08:30 GMT  
		Size: 28.6 MB (28645696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fb1ab422c0ae864df4333ba064fd3a16ef9b10862dca7b3320a9fb32c7e0bd`  
		Last Modified: Tue, 04 Jul 2023 17:00:17 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be60fdd8cf07af19113cd853d2f0ebedd02fc5cb31582325b43c0d50a323535`  
		Last Modified: Tue, 04 Jul 2023 17:00:18 GMT  
		Size: 5.5 MB (5470782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1374c790d73360e41f53f0d1a2d9cbaef5dd6c371a1ab7c58c7e20e71945704`  
		Last Modified: Tue, 04 Jul 2023 17:00:16 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46e6bf7058a41f3c469f223b205d4cf0117ff90a46243c845af4186cf4a2f35`  
		Last Modified: Tue, 15 Aug 2023 01:08:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f4159eddd74872cb3c56fbbe3c25576f612d8063f9437c6bceea27d0c77680`  
		Last Modified: Tue, 15 Aug 2023 01:08:26 GMT  
		Size: 87.5 MB (87473336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b717e16faf4735fa639f52916ac0e68de8562e0a29e440094e58588854afe4a`  
		Last Modified: Tue, 15 Aug 2023 01:08:13 GMT  
		Size: 3.6 KB (3563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03268fbb87c181f1f871ab28573358c91b95a89de3698b8fd5907743ab5481b5`  
		Last Modified: Tue, 15 Aug 2023 01:08:13 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
