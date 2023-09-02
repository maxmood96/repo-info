## `mariadb:10-jammy`

```console
$ docker pull mariadb@sha256:3e8f15fd6328340f4024fcb7005cce0da1fa5065554b7c420626f803b67ddc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `mariadb:10-jammy` - linux; amd64

```console
$ docker pull mariadb@sha256:97e1303681ef1c14cd0d0abb836c9899283151622d2f766378095670c5244eba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123138891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58df8de36e1c36985cf8169464644ba84d6317d01afd7c234588531cee2ae9d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:59:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 02 Sep 2023 00:59:27 GMT
ENV GOSU_VERSION=1.14
# Sat, 02 Sep 2023 00:59:27 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 02 Sep 2023 00:59:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 02 Sep 2023 00:59:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 02 Sep 2023 00:59:48 GMT
ENV LANG=C.UTF-8
# Sat, 02 Sep 2023 01:01:01 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sat, 02 Sep 2023 01:01:01 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Sat, 02 Sep 2023 01:01:01 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Sat, 02 Sep 2023 01:01:01 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Sat, 02 Sep 2023 01:01:02 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 02 Sep 2023 01:01:19 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Sat, 02 Sep 2023 01:01:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 02 Sep 2023 01:01:19 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Sat, 02 Sep 2023 01:01:19 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Sat, 02 Sep 2023 01:01:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 01:01:20 GMT
EXPOSE 3306
# Sat, 02 Sep 2023 01:01:20 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b8223d0cb63605c13620c5faa1fed71bc203d748f9999eb6ee3f9363a496fb`  
		Last Modified: Sat, 02 Sep 2023 01:02:40 GMT  
		Size: 1.7 KB (1748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2696fb09d6dc7e92a790a154e7de9922d8ba322d22f8f44baae2020cfc15bb`  
		Last Modified: Sat, 02 Sep 2023 01:02:41 GMT  
		Size: 5.6 MB (5592652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae32c298a0dedd83348f175f9614d7e4a822c3668eeb94b9159783f0a926a9d`  
		Last Modified: Sat, 02 Sep 2023 01:02:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6034be6212cb6b0f7a1bfaaf7e1a8e39d1d0393fc13e864e53262295102d24b3`  
		Last Modified: Sat, 02 Sep 2023 01:03:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b3291610cc0026bdf01c9c912d424d98c509fce88bf4c82f07835a7f4190c9`  
		Last Modified: Sat, 02 Sep 2023 01:03:49 GMT  
		Size: 87.1 MB (87093902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c5aa74fb3b74ce00c45fe9677a3308fd7da909b2826a8220d6fef6116b4044`  
		Last Modified: Sat, 02 Sep 2023 01:03:37 GMT  
		Size: 3.6 KB (3561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0c77b78022d6730f126d13c398fc71297770877f5e905cdcd4f17d6479396d`  
		Last Modified: Sat, 02 Sep 2023 01:03:37 GMT  
		Size: 7.6 KB (7567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; arm64 variant v8

```console
$ docker pull mariadb@sha256:1f21a376582acb1dbda1b6934fbf7e994d73c7deaacda761d21d07b4b0e229b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117669332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8247131dbb3a52dab305e3aebce910f85e4798202ee45d9d43e783d58fe94e75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:18:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 02 Sep 2023 00:18:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 02 Sep 2023 00:18:35 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 02 Sep 2023 00:18:52 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 02 Sep 2023 00:18:53 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 02 Sep 2023 00:18:53 GMT
ENV LANG=C.UTF-8
# Sat, 02 Sep 2023 00:19:46 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sat, 02 Sep 2023 00:19:46 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Sat, 02 Sep 2023 00:19:46 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Sat, 02 Sep 2023 00:19:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Sat, 02 Sep 2023 00:19:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 02 Sep 2023 00:20:03 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Sat, 02 Sep 2023 00:20:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 02 Sep 2023 00:20:05 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Sat, 02 Sep 2023 00:20:05 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Sat, 02 Sep 2023 00:20:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 00:20:05 GMT
EXPOSE 3306
# Sat, 02 Sep 2023 00:20:05 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637aa2386c4210136c2f6d3d8f3e9b858d2d27c3bbc9dfa94dc5cae331da8201`  
		Last Modified: Sat, 02 Sep 2023 00:21:15 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98ae087d21ef31a0d78ef0bf285f78b23fc43171ab8df39d3218a21d1f3368a`  
		Last Modified: Sat, 02 Sep 2023 00:21:16 GMT  
		Size: 5.4 MB (5407667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e997ce2d52c993e098e3715c8f20a0c45c3df5f2ae35f4915881bb428708b`  
		Last Modified: Sat, 02 Sep 2023 00:21:13 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89f6bfc2c488751331b54c0f7b68a6b7d2587d21fc539143bcf5cfc17d73fbc2`  
		Last Modified: Sat, 02 Sep 2023 00:22:05 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9db50cd78356bce317fbccf2660d1727151ad4113eb739efbb6cc3f0195fe196`  
		Last Modified: Sat, 02 Sep 2023 00:22:15 GMT  
		Size: 83.9 MB (83855312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee96d67685adde5b0d4c8b346c20c14ce9766fd0288f6b3437071f1285179181`  
		Last Modified: Sat, 02 Sep 2023 00:22:05 GMT  
		Size: 3.6 KB (3565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13133f2e38908b91dcb5f338a7e35239438077abf96fc58fee5e177de8953681`  
		Last Modified: Sat, 02 Sep 2023 00:22:05 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; ppc64le

```console
$ docker pull mariadb@sha256:6694878c92969d959e13241939370adbcd6284d12972d4f6ef3de1699b500295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.5 MB (131541127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621d88baeb1b99899d292b23120b10d37ecf748359bdc6e348064aed30ddb8ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 16 Aug 2023 06:03:07 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:03:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:03:08 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:03:11 GMT
ADD file:632018deeaeb9e42f0026fb331dfb08381e46bd414b2b470b18ea22ac0653bf6 in / 
# Wed, 16 Aug 2023 06:03:11 GMT
CMD ["/bin/bash"]
# Sat, 02 Sep 2023 00:33:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 02 Sep 2023 00:33:07 GMT
ENV GOSU_VERSION=1.14
# Sat, 02 Sep 2023 00:33:07 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Sat, 02 Sep 2023 00:33:45 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 02 Sep 2023 00:33:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 02 Sep 2023 00:33:47 GMT
ENV LANG=C.UTF-8
# Sat, 02 Sep 2023 00:35:44 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Sat, 02 Sep 2023 00:35:45 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Sat, 02 Sep 2023 00:35:45 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Sat, 02 Sep 2023 00:35:46 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Sat, 02 Sep 2023 00:35:47 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Sat, 02 Sep 2023 00:36:44 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Sat, 02 Sep 2023 00:36:48 GMT
VOLUME [/var/lib/mysql]
# Sat, 02 Sep 2023 00:36:48 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Sat, 02 Sep 2023 00:36:49 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Sat, 02 Sep 2023 00:36:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 00:36:49 GMT
EXPOSE 3306
# Sat, 02 Sep 2023 00:36:50 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:5d4cfc5435802883c4aaa9fa4afcc1b07f40e20bee68f058f0671804ab6bc3a0`  
		Last Modified: Sat, 02 Sep 2023 00:08:58 GMT  
		Size: 35.7 MB (35705651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64345a8130199c27b93b6487b25d9cea93bae6da6ae510e28fac1549ee8c075`  
		Last Modified: Sat, 02 Sep 2023 00:39:42 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c39e0a45dd6e59e7000b5b47fd5e15e8db6844fe28ae4d4aaf8a3edc69ac3c9`  
		Last Modified: Sat, 02 Sep 2023 00:39:44 GMT  
		Size: 6.0 MB (6018083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab4af533d32a1188b7b4b99ee2cb857cf1e833a3edd0e96a459d47c69cf3282`  
		Last Modified: Sat, 02 Sep 2023 00:39:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9e115e84d2fea93b098b51be67b533cb6c24b09419315ce30b33b3ed23454cc`  
		Last Modified: Sat, 02 Sep 2023 00:41:18 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3cf9709be07b773de567bfac9feee7a34ec4760d0b4d47b3e054ae0d10b0f9`  
		Last Modified: Sat, 02 Sep 2023 00:41:42 GMT  
		Size: 89.8 MB (89804025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e78431660c6efcb15279e3c0f8a282e5635b1c872ebd562572422334a15c21`  
		Last Modified: Sat, 02 Sep 2023 00:41:18 GMT  
		Size: 3.6 KB (3562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78971370a79314531902d3244db70d83a2e8d4534e9f99370210a5e2719ee84`  
		Last Modified: Sat, 02 Sep 2023 00:41:18 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mariadb:10-jammy` - linux; s390x

```console
$ docker pull mariadb@sha256:064d7369c869c55f689a1e5b3d0bad092f0095354c911866f09225c6f4ce1f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.6 MB (121644293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b229d6b3a7fee596ba04548559f6f0285f11925e914022e7250dc21229de38f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mariadbd"]`

```dockerfile
# Wed, 16 Aug 2023 06:05:03 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:05:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:05:03 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:05:05 GMT
ADD file:58eccd685d73ff80ea235016d6e33d093e1063800d869935b67b59a1b8891344 in / 
# Wed, 16 Aug 2023 06:05:05 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:36:03 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 01 Sep 2023 23:36:03 GMT
ENV GOSU_VERSION=1.14
# Fri, 01 Sep 2023 23:36:03 GMT
ARG GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
# Fri, 01 Sep 2023 23:36:17 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN set -eux; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends 		ca-certificates 		gpg 		gpgv 		libjemalloc2 		pwgen 		tzdata 		xz-utils 		zstd ; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get install -y --no-install-recommends 		dirmngr 		gpg-agent 		wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -q -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -q -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	GNUPGHOME="$(mktemp -d)"; 	export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --export "$GPG_KEYS" > /etc/apt/trusted.gpg.d/mariadb.gpg; 	if command -v gpgconf >/dev/null; then 		gpgconf --kill all; 	fi; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] ||	apt-mark manual $savedAptMark >/dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 01 Sep 2023 23:36:18 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 01 Sep 2023 23:36:18 GMT
ENV LANG=C.UTF-8
# Fri, 01 Sep 2023 23:37:25 GMT
LABEL org.opencontainers.image.authors=MariaDB Community org.opencontainers.image.title=MariaDB Database org.opencontainers.image.description=MariaDB Database for relational SQL org.opencontainers.image.documentation=https://hub.docker.com/_/mariadb/ org.opencontainers.image.base.name=docker.io/library/ubuntu:jammy org.opencontainers.image.licenses=GPL-2.0 org.opencontainers.image.source=https://github.com/MariaDB/mariadb-docker org.opencontainers.image.vendor=MariaDB Community org.opencontainers.image.version=10.11.5 org.opencontainers.image.url=https://github.com/MariaDB/mariadb-docker
# Fri, 01 Sep 2023 23:37:26 GMT
ARG MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Fri, 01 Sep 2023 23:37:26 GMT
ENV MARIADB_VERSION=1:10.11.5+maria~ubu2204
# Fri, 01 Sep 2023 23:37:26 GMT
ARG REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
# Fri, 01 Sep 2023 23:37:27 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -e;	echo "deb ${REPOSITORY}" > /etc/apt/sources.list.d/mariadb.list; 	{ 		echo 'Package: *'; 		echo 'Pin: release o=MariaDB'; 		echo 'Pin-Priority: 999'; 	} > /etc/apt/preferences.d/mariadb
# Fri, 01 Sep 2023 23:37:48 GMT
# ARGS: GPG_KEYS=177F4010FE56CA3336300305F1656F24C74CD1D8 REPOSITORY=http://archive.mariadb.org/mariadb-10.11.5/repo/ubuntu/ jammy main main/debug
RUN set -ex; 	{ 		echo "mariadb-server" mysql-server/root_password password 'unused'; 		echo "mariadb-server" mysql-server/root_password_again password 'unused'; 	} | debconf-set-selections; 	apt-get update; 	mkdir -p /var/lib/mysql/mysql ; touch /var/lib/mysql/mysql/user.frm ; 	apt-get install -y --no-install-recommends mariadb-server="$MARIADB_VERSION" mariadb-backup socat 	; 	rm -rf /var/lib/apt/lists/*; 	rm -rf /var/lib/mysql /etc/mysql/mariadb.conf.d/50-mysqld_safe.cnf; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown -R mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 777 /var/run/mysqld; 	find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log|user\s)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log|user\s)/#&/'; 	printf "[mariadb]\nhost-cache-size=0\nskip-name-resolve\n" > /etc/mysql/mariadb.conf.d/05-skipcache.cnf; 	if [ -L /etc/mysql/my.cnf ]; then 		sed -i -e '/includedir/ {N;s/\(.*\)\n\(.*\)/\n\2\n\1/}' /etc/mysql/mariadb.cnf; 	fi
# Fri, 01 Sep 2023 23:37:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 01 Sep 2023 23:37:58 GMT
COPY file:60282e2c078282f09827dfb0926d431a7ad71f6de3495a21fc8a846430fc5fc9 in /usr/local/bin/healthcheck.sh 
# Fri, 01 Sep 2023 23:37:58 GMT
COPY file:704c6685e9d99f08306a2726e0468f5a764a4040cc2eb6138c1be72ac2529bbc in /usr/local/bin/ 
# Fri, 01 Sep 2023 23:37:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Sep 2023 23:37:58 GMT
EXPOSE 3306
# Fri, 01 Sep 2023 23:37:58 GMT
CMD ["mariadbd"]
```

-	Layers:
	-	`sha256:e19a32372cc8a39496c7cbc80d6c7213997c1b24d50309e770a59738f35c719d`  
		Last Modified: Fri, 01 Sep 2023 23:23:30 GMT  
		Size: 28.6 MB (28645834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d53e92c022e34838ccbb6145d433542c97b6d40318e7275f5ecf685e1f0613`  
		Last Modified: Fri, 01 Sep 2023 23:40:16 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b244984b5e04195b965b09a4c525cf1979b9d1a6dc3c878386967f6d83ceba70`  
		Last Modified: Fri, 01 Sep 2023 23:40:17 GMT  
		Size: 5.5 MB (5470797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cb60f89bc1665b91c42d3524b465dc6f87d19014bddf098a502aa3b951d263`  
		Last Modified: Fri, 01 Sep 2023 23:40:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5177d7a11cd07c2a089ea23275551b5d6a1c97604681bf57b6a99671a6befaa6`  
		Last Modified: Fri, 01 Sep 2023 23:41:03 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:452d057ee188073c1bb6f1a8ee7256b43cf77f1dfe623c1f8ef29871ffbe78fd`  
		Last Modified: Fri, 01 Sep 2023 23:41:16 GMT  
		Size: 87.5 MB (87514295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49a0ee86b5d48fa8b73578c4dc5fdccfcec1a2e4656212d6a313e203e16eeaf`  
		Last Modified: Fri, 01 Sep 2023 23:41:03 GMT  
		Size: 3.6 KB (3565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9a18fca7ff044a9eecaa302d052bd404b55e8a85a11d0db1b76c9feff2b531`  
		Last Modified: Fri, 01 Sep 2023 23:41:03 GMT  
		Size: 7.6 KB (7568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
