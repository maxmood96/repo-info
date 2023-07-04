## `mariadb:lts-jammy`

```console
$ docker pull mariadb@sha256:ecf047d90b1978d9274192b093db307e2883040ce621ff1381521c4cf35d675f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:lts-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:4b6b625ae683588d99507ac01b042863d4311b6e15f81d653be6892762637375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123105947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b77d250201f61f86a2a98c7e07d5bd77f96b4a345f40f8ce53593c2ffca84d`
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
# Tue, 04 Jul 2023 18:28:38 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 04 Jul 2023 18:28:38 GMT
ARG MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Tue, 04 Jul 2023 18:28:38 GMT
ENV MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Tue, 04 Jul 2023 18:28:38 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
# Tue, 04 Jul 2023 18:28:39 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 04 Jul 2023 18:28:56 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 04 Jul 2023 18:28:57 GMT
VOLUME [/var/lib/mysql]
# Tue, 04 Jul 2023 18:28:57 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Tue, 04 Jul 2023 18:28:57 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Tue, 04 Jul 2023 18:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 18:28:57 GMT
EXPOSE 3306
# Tue, 04 Jul 2023 18:28:58 GMT
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
	-	`sha256:fa9531173fe68dc54682bc25ac9b4c270ed5772c4ba6b47daef52a3d4e70af77`  
		Last Modified: Tue, 04 Jul 2023 18:32:56 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7375440478980efc7a168e77a3f085cd056c5f722e11d17a5ef922de66c95f45`  
		Last Modified: Tue, 04 Jul 2023 18:33:09 GMT  
		Size: 87.1 MB (87068650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe8be80cd3b8009d3f30675bf4b5402c953d8dfaae942c2fb610a1fab9f826c3`  
		Last Modified: Tue, 04 Jul 2023 18:32:56 GMT  
		Size: 3.6 KB (3565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2384dd133a6708cc48561cd0773fb9abe3b23eae32323d644c2b8c57c8148f3`  
		Last Modified: Tue, 04 Jul 2023 18:32:56 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:33e8f9991a22fd6678ef20bf31b2bcecc6fc7c7bea5c62b0144ba4df243ff107
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.6 MB (117618140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc7fccd2af985a12c6a6c0d2decd2a77618a858164ee12eb905621a5e02e6dc`
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
# Tue, 04 Jul 2023 15:50:06 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 04 Jul 2023 15:50:07 GMT
ARG MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Tue, 04 Jul 2023 15:50:07 GMT
ENV MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Tue, 04 Jul 2023 15:50:07 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
# Tue, 04 Jul 2023 15:50:07 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 04 Jul 2023 15:50:22 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 04 Jul 2023 15:50:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 04 Jul 2023 15:50:24 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Tue, 04 Jul 2023 15:50:24 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Tue, 04 Jul 2023 15:50:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 15:50:24 GMT
EXPOSE 3306
# Tue, 04 Jul 2023 15:50:24 GMT
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
	-	`sha256:8210aced70ef3e24a46799929c24c1213867224b74ac675905ac218d01442f43`  
		Last Modified: Tue, 04 Jul 2023 15:54:02 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cb7b8053f2d91dc92f88f643e2865478be6d9ff1a66c023d0c46ac4354ee4b`  
		Last Modified: Tue, 04 Jul 2023 15:54:11 GMT  
		Size: 83.8 MB (83807029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449424199d1167824fde06f204297c2ba55b2095c8bfd15d6a77aa93b09c7e4b`  
		Last Modified: Tue, 04 Jul 2023 15:54:01 GMT  
		Size: 3.6 KB (3565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3ad0253591ba73c469a1fb8a855ae6c9f69b8c1c7c16163e792da830111d9f`  
		Last Modified: Tue, 04 Jul 2023 15:54:02 GMT  
		Size: 7.6 KB (7568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:abefb9c20018d8628753214a97d6d476fb3fe347c533eca3638f4c3def14a12f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131775418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a62d588a167c571dfb99610c61917af2611b3036f1982623214bcc1607769cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Mon, 05 Jun 2023 17:01:00 GMT
ARG RELEASE
# Mon, 05 Jun 2023 17:01:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 05 Jun 2023 17:01:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 05 Jun 2023 17:01:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 05 Jun 2023 17:01:03 GMT
ADD file:00c4f44b35b683caef54d5b8b0e0b1e68872f45eae17dd7543adaf6c54512447 in / 
# Mon, 05 Jun 2023 17:01:04 GMT
CMD ["/bin/bash"]
# Fri, 16 Jun 2023 01:42:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 16 Jun 2023 01:42:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 16 Jun 2023 01:42:10 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 16 Jun 2023 01:42:49 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 16 Jun 2023 01:42:51 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 16 Jun 2023 01:42:51 GMT
ENV LANG=C.UTF-8
# Fri, 16 Jun 2023 01:45:13 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 16 Jun 2023 01:45:14 GMT
ARG MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 16 Jun 2023 01:45:14 GMT
ENV MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Fri, 16 Jun 2023 01:45:15 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
# Fri, 16 Jun 2023 01:45:16 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 27 Jun 2023 02:01:12 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 27 Jun 2023 02:01:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 27 Jun 2023 02:01:16 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Tue, 27 Jun 2023 02:01:17 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Tue, 27 Jun 2023 02:01:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Jun 2023 02:01:17 GMT
EXPOSE 3306
# Tue, 27 Jun 2023 02:01:18 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:a02dd69d9a8a1e6f4fc2ccb509fb8efd6014b00ff932a757d23b4b012a2bec49`  
		Last Modified: Fri, 16 Jun 2023 00:44:52 GMT  
		Size: 35.7 MB (35711397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ef2f0de58dc6b86ab230fc24fdea7663e7c4036eaecb5cfaa5ca13d0538e76`  
		Last Modified: Fri, 16 Jun 2023 01:55:23 GMT  
		Size: 1.7 KB (1746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527730925c9b9eea7a40aa0f642c5ecb732e3ffe1537b1481481e867ece7fc5b`  
		Last Modified: Fri, 16 Jun 2023 01:55:25 GMT  
		Size: 6.0 MB (6017949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b6ffe59959eb8b4ce9b862df0bc5e9542904c81ae9b29b3bb640e9df667043`  
		Last Modified: Fri, 16 Jun 2023 01:55:21 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ee680c9d760e2a0bf4493724c809bd0e81a429896ce65611874b0a8b39e853`  
		Last Modified: Fri, 16 Jun 2023 01:56:45 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad12c1ff2b7ed204ad307029a65c7a6302e18faa30b9e594fe3b2b15acb346b`  
		Last Modified: Tue, 27 Jun 2023 02:09:08 GMT  
		Size: 90.0 MB (90032718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd6913e176e443dc6db74f903551921f935132b966e0af0e5bd9d4dbdd57ce3`  
		Last Modified: Tue, 27 Jun 2023 02:08:44 GMT  
		Size: 3.6 KB (3566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526e257e0463308da28036dff80424b33bf333912d2a3b534c6866cc239e08b5`  
		Last Modified: Tue, 27 Jun 2023 02:08:44 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:lts-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:2b727f34069c4b59da2e9dae7fa9f907e91d2bce79801c4bdc33012d4cbe038f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121580518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378fece5fccb2954bad0c49ec6a7ed1c913335d61542c2a7db9cddf4df77e3d5`
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
# Tue, 04 Jul 2023 16:56:57 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.4 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Tue, 04 Jul 2023 16:56:57 GMT
ARG MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Tue, 04 Jul 2023 16:56:57 GMT
ENV MARIADB_VERSION=1:10.11.4+maria~ubu2204
# Tue, 04 Jul 2023 16:56:57 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
# Tue, 04 Jul 2023 16:56:57 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Tue, 04 Jul 2023 16:57:13 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.4/repo/ubuntu/ jammy main
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Tue, 04 Jul 2023 16:57:18 GMT
VOLUME [/var/lib/mysql]
# Tue, 04 Jul 2023 16:57:18 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Tue, 04 Jul 2023 16:57:18 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Tue, 04 Jul 2023 16:57:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 16:57:18 GMT
EXPOSE 3306
# Tue, 04 Jul 2023 16:57:18 GMT
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
	-	`sha256:e27e7e4b86fecdc32e5bd05e78321e6746840e6a0544d4bedbbdf1c2754a5d72`  
		Last Modified: Tue, 04 Jul 2023 17:01:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0090bfea6877acf7ee51c046ee6600b616e08ac7ee48d3fdc628a0167e130e3`  
		Last Modified: Tue, 04 Jul 2023 17:01:18 GMT  
		Size: 87.5 MB (87450671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093cd65cb7e5e05be6911f64a423e13b6109f3d369f8ac17e7e2584cbe74d8a5`  
		Last Modified: Tue, 04 Jul 2023 17:01:05 GMT  
		Size: 3.6 KB (3568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3082833c7ebee98976c11b8826ef88fa09fa5b139d6b6830488e0ed2a7144e3`  
		Last Modified: Tue, 04 Jul 2023 17:01:05 GMT  
		Size: 7.6 KB (7570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
