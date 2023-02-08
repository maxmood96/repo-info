<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.41`](#mysql5741)
-	[`mysql:5.7.41-debian`](#mysql5741-debian)
-	[`mysql:5.7.41-oracle`](#mysql5741-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.32`](#mysql8032)
-	[`mysql:8.0.32-debian`](#mysql8032-debian)
-	[`mysql:8.0.32-oracle`](#mysql8032-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:1e637483dfa9e3f2027357f1e8fc566f5c01b7c0a7da1f2408a8b2e8661c785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:ce9f3f34ced66d8f1134cae332db346b99eac57fe98151b66d332273ad37e0a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162697008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098b17901f722f8abb61238c31204b90b65986117f25b494725bb3a580346a0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:48:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Feb 2023 14:48:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:48:28 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 14:48:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 14:48:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 14:48:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:48:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 14:48:45 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 04 Feb 2023 14:48:45 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Sat, 04 Feb 2023 14:48:46 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Feb 2023 14:49:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 04 Feb 2023 14:49:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Feb 2023 14:49:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:49:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 14:49:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:49:06 GMT
EXPOSE 3306 33060
# Sat, 04 Feb 2023 14:49:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa52c08f6d64c27c8bbc7f78f8368224b99c37b48e8343a9d0364d33d779de21`  
		Last Modified: Sat, 04 Feb 2023 14:50:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f717ed1938dd429e6bf1387feb8f1365db34cc1e17ae307ed79d89cfef28f8`  
		Last Modified: Sat, 04 Feb 2023 14:50:12 GMT  
		Size: 4.2 MB (4182319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a135a3b62b02e7b6e0becd2e51dab4b8d1c0c0fc1d8bfb45dba78e63e5c9bd4`  
		Last Modified: Sat, 04 Feb 2023 14:50:12 GMT  
		Size: 1.4 MB (1441725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd96155287dc7fa118c3ef4c5b929337571a489a4e01a879313dd1e53c25612`  
		Last Modified: Sat, 04 Feb 2023 14:50:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139136d0303f40fe184d71465c0d8eaad987d48ceb1dba15bd99d77d8e1a11ad`  
		Last Modified: Sat, 04 Feb 2023 14:50:14 GMT  
		Size: 14.1 MB (14089433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eaaf4eeed62dee382967f65959afb060a8e0ed386be7ad8038a98548075ece`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277fa21096ee1963f0dbd04bedb91574e4eb14db48230f23b6158828b685575`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a4d032701adf22ae19c0ca5e82bd887758807d9557541db8039a699b120ca0`  
		Last Modified: Sat, 04 Feb 2023 14:50:25 GMT  
		Size: 115.8 MB (115832990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4f39afc4d329d98aa5f9d8c441455b653db63f99e280f36a58363618988837`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b6afcd59994a6e603ab93368f70455a849f21899602cd7f2fab9292be534b6`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:1e637483dfa9e3f2027357f1e8fc566f5c01b7c0a7da1f2408a8b2e8661c785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:ce9f3f34ced66d8f1134cae332db346b99eac57fe98151b66d332273ad37e0a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162697008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098b17901f722f8abb61238c31204b90b65986117f25b494725bb3a580346a0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:48:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Feb 2023 14:48:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:48:28 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 14:48:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 14:48:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 14:48:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:48:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 14:48:45 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 04 Feb 2023 14:48:45 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Sat, 04 Feb 2023 14:48:46 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Feb 2023 14:49:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 04 Feb 2023 14:49:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Feb 2023 14:49:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:49:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 14:49:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:49:06 GMT
EXPOSE 3306 33060
# Sat, 04 Feb 2023 14:49:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa52c08f6d64c27c8bbc7f78f8368224b99c37b48e8343a9d0364d33d779de21`  
		Last Modified: Sat, 04 Feb 2023 14:50:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f717ed1938dd429e6bf1387feb8f1365db34cc1e17ae307ed79d89cfef28f8`  
		Last Modified: Sat, 04 Feb 2023 14:50:12 GMT  
		Size: 4.2 MB (4182319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a135a3b62b02e7b6e0becd2e51dab4b8d1c0c0fc1d8bfb45dba78e63e5c9bd4`  
		Last Modified: Sat, 04 Feb 2023 14:50:12 GMT  
		Size: 1.4 MB (1441725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd96155287dc7fa118c3ef4c5b929337571a489a4e01a879313dd1e53c25612`  
		Last Modified: Sat, 04 Feb 2023 14:50:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139136d0303f40fe184d71465c0d8eaad987d48ceb1dba15bd99d77d8e1a11ad`  
		Last Modified: Sat, 04 Feb 2023 14:50:14 GMT  
		Size: 14.1 MB (14089433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eaaf4eeed62dee382967f65959afb060a8e0ed386be7ad8038a98548075ece`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277fa21096ee1963f0dbd04bedb91574e4eb14db48230f23b6158828b685575`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a4d032701adf22ae19c0ca5e82bd887758807d9557541db8039a699b120ca0`  
		Last Modified: Sat, 04 Feb 2023 14:50:25 GMT  
		Size: 115.8 MB (115832990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4f39afc4d329d98aa5f9d8c441455b653db63f99e280f36a58363618988837`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b6afcd59994a6e603ab93368f70455a849f21899602cd7f2fab9292be534b6`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-debian`

```console
$ docker pull mysql@sha256:1e637483dfa9e3f2027357f1e8fc566f5c01b7c0a7da1f2408a8b2e8661c785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:ce9f3f34ced66d8f1134cae332db346b99eac57fe98151b66d332273ad37e0a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162697008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098b17901f722f8abb61238c31204b90b65986117f25b494725bb3a580346a0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Feb 2023 06:52:07 GMT
ADD file:4fbe1e3712cf37c85529cc81e0d03c82085203de00d64b0d669b5996e975925a in / 
# Sat, 04 Feb 2023 06:52:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:48:23 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Feb 2023 14:48:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:48:28 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 14:48:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 14:48:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 14:48:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:48:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 14:48:45 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 04 Feb 2023 14:48:45 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Sat, 04 Feb 2023 14:48:46 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Feb 2023 14:49:04 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 04 Feb 2023 14:49:05 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Feb 2023 14:49:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:49:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 14:49:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:49:06 GMT
EXPOSE 3306 33060
# Sat, 04 Feb 2023 14:49:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0cf508b37688dca559387b506062329202aaf08b48be5f55f9278b2a818ad2c9`  
		Last Modified: Sat, 04 Feb 2023 06:56:58 GMT  
		Size: 27.1 MB (27140353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa52c08f6d64c27c8bbc7f78f8368224b99c37b48e8343a9d0364d33d779de21`  
		Last Modified: Sat, 04 Feb 2023 14:50:13 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47f717ed1938dd429e6bf1387feb8f1365db34cc1e17ae307ed79d89cfef28f8`  
		Last Modified: Sat, 04 Feb 2023 14:50:12 GMT  
		Size: 4.2 MB (4182319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a135a3b62b02e7b6e0becd2e51dab4b8d1c0c0fc1d8bfb45dba78e63e5c9bd4`  
		Last Modified: Sat, 04 Feb 2023 14:50:12 GMT  
		Size: 1.4 MB (1441725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd96155287dc7fa118c3ef4c5b929337571a489a4e01a879313dd1e53c25612`  
		Last Modified: Sat, 04 Feb 2023 14:50:11 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139136d0303f40fe184d71465c0d8eaad987d48ceb1dba15bd99d77d8e1a11ad`  
		Last Modified: Sat, 04 Feb 2023 14:50:14 GMT  
		Size: 14.1 MB (14089433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eaaf4eeed62dee382967f65959afb060a8e0ed386be7ad8038a98548075ece`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277fa21096ee1963f0dbd04bedb91574e4eb14db48230f23b6158828b685575`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a4d032701adf22ae19c0ca5e82bd887758807d9557541db8039a699b120ca0`  
		Last Modified: Sat, 04 Feb 2023 14:50:25 GMT  
		Size: 115.8 MB (115832990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4f39afc4d329d98aa5f9d8c441455b653db63f99e280f36a58363618988837`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b6afcd59994a6e603ab93368f70455a849f21899602cd7f2fab9292be534b6`  
		Last Modified: Sat, 04 Feb 2023 14:50:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-oracle`

```console
$ docker pull mysql@sha256:8cf035b14977b26f4a47d98e85949a7dd35e641f88fc24aa4b466b36beecf9d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:6b5917f3cfc5920881d728c19f5e3a035a06257cf5f983b1203962327d21ac66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129975079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be16cf2d832a9a54ce42144e25f5ae7cc66bccf0e003837e7b5eb1a455dc742b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 27 Jan 2023 23:36:36 GMT
ADD file:eefc8abcbb6ec3141573da12cc99f3d9592d5a0bd105bb189e0e1db15c0d1bf5 in / 
# Fri, 27 Jan 2023 23:36:37 GMT
CMD ["/bin/bash"]
# Sat, 28 Jan 2023 00:06:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 01 Feb 2023 04:23:51 GMT
ENV GOSU_VERSION=1.16
# Wed, 01 Feb 2023 04:23:54 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 01 Feb 2023 04:24:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 01 Feb 2023 04:24:13 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 01 Feb 2023 04:24:13 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Wed, 01 Feb 2023 04:24:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 01 Feb 2023 04:24:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 01 Feb 2023 04:24:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 01 Feb 2023 04:24:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Wed, 01 Feb 2023 04:24:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 01 Feb 2023 04:24:57 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 Feb 2023 04:24:57 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 01 Feb 2023 04:24:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 01 Feb 2023 04:24:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Feb 2023 04:24:58 GMT
EXPOSE 3306 33060
# Wed, 01 Feb 2023 04:24:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e048d0a387420acfdb05a1ec44ed79aa01be81adcd731b3100359277ca89d08b`  
		Last Modified: Fri, 27 Jan 2023 23:38:26 GMT  
		Size: 50.5 MB (50466577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7847c8a41cb8230f06f790ec1f0ed987fa4b9fea784840951ddc7adda2efe08`  
		Last Modified: Sat, 28 Jan 2023 00:08:54 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:351a550f260d7de0e214367bed3a1660746ddbf80330881ee0aeba5b5505c2cb`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 983.7 KB (983714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce196d9d34faa9d0fd3ee95a6db615d2dcf9a01d641373b50ca9060f41c6750`  
		Last Modified: Wed, 01 Feb 2023 04:27:17 GMT  
		Size: 4.5 MB (4542168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17febb6f203083f20aed59a57deb5f1a5e7b24b21166912e82c41686608ae27f`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4e426841fb4f39098843fbfe51841e7325df410b6abbe5141f6db916832ab7b`  
		Last Modified: Wed, 01 Feb 2023 04:27:16 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda41038b9f8db87281de8e62ff6f6a99413d17be72234806465069152c30296`  
		Last Modified: Wed, 01 Feb 2023 04:27:18 GMT  
		Size: 25.5 MB (25525352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47aac56b41be2f4420a90abd519b0642d7dc0f15ae013f05eb049265312d039`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a90c36973704783547f014c19a92adebbfe0af84a414eb94123a40ae0a8986`  
		Last Modified: Wed, 01 Feb 2023 04:27:23 GMT  
		Size: 48.4 MB (48447571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97091252395b2a7d7d6abfe03cee67308af5b10836f6d1a1d9a290086369e8cf`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84fac29d61e98e5bb41d2e3b7897427e7a66ff35d3ecd3cbee0e41d3d8ae142f`  
		Last Modified: Wed, 01 Feb 2023 04:27:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:3cebdc40926f61eaac83b5ea26388f8fa770e7636c2ea930421cc5604a41a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3463914132e73c14c172cd4a94da9c66d0baa1a315b16161f462921193e36aa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177751835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20690ccd77820231956c3b7385b477bcd57afe216412e84b5c0166e04cab52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:47:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Feb 2023 14:47:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:38 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 14:47:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 14:47:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 14:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Sat, 04 Feb 2023 14:47:54 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Feb 2023 14:48:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 04 Feb 2023 14:48:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Feb 2023 14:48:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 04 Feb 2023 14:48:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:48:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 14:48:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:48:11 GMT
EXPOSE 3306 33060
# Sat, 04 Feb 2023 14:48:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4957656d4d97b158dafcf9f7ea1e52ce85827e65d97a1fce33f22b024e0d659f`  
		Last Modified: Sat, 04 Feb 2023 14:49:37 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6013719e001ed5ce0cbc7cdff4ae1f79c141597caa27a8006e92a6326e53345a`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 4.4 MB (4414927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa6814d598d5914d9926ec0a5a04fcc6e790afabc91f4766372af106c17acd2`  
		Last Modified: Sat, 04 Feb 2023 14:49:36 GMT  
		Size: 1.5 MB (1471342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c8eaab45d1b1d84217a009b1ed704b791e724afbf410b70e19cccba16330e7`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f646a9bb01ef05b95b959b0aa365de8bfd5b41ee6f963d2f9f053a176ac2d`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f77555863007461c120a08bff5a4064950f9480c943803faeab52ce0195ecd`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f26b2b4e771728df08c074cb278d9d41dd87e6048ec1eccfb1206e01d5e4f8f`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587ff3b05d9015e5d9471aceedbbdff6e371c2b9ae923af273addce00abfbd1`  
		Last Modified: Sat, 04 Feb 2023 14:49:53 GMT  
		Size: 127.8 MB (127795588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f0c92d7ddeafcc2949667f9fbf63dfaff447ad17cff156957fe4e38ca45aac`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5690a3da4b66efa9e50222b88182474283b4dda3ddd5e7bfee83568005657562`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b8d1d871af097f1efb61a6f8f1c623aa6b6201969f6367182c8d03aab0186e`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:3cebdc40926f61eaac83b5ea26388f8fa770e7636c2ea930421cc5604a41a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3463914132e73c14c172cd4a94da9c66d0baa1a315b16161f462921193e36aa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177751835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20690ccd77820231956c3b7385b477bcd57afe216412e84b5c0166e04cab52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:47:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Feb 2023 14:47:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:38 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 14:47:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 14:47:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 14:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Sat, 04 Feb 2023 14:47:54 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Feb 2023 14:48:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 04 Feb 2023 14:48:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Feb 2023 14:48:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 04 Feb 2023 14:48:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:48:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 14:48:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:48:11 GMT
EXPOSE 3306 33060
# Sat, 04 Feb 2023 14:48:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4957656d4d97b158dafcf9f7ea1e52ce85827e65d97a1fce33f22b024e0d659f`  
		Last Modified: Sat, 04 Feb 2023 14:49:37 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6013719e001ed5ce0cbc7cdff4ae1f79c141597caa27a8006e92a6326e53345a`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 4.4 MB (4414927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa6814d598d5914d9926ec0a5a04fcc6e790afabc91f4766372af106c17acd2`  
		Last Modified: Sat, 04 Feb 2023 14:49:36 GMT  
		Size: 1.5 MB (1471342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c8eaab45d1b1d84217a009b1ed704b791e724afbf410b70e19cccba16330e7`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f646a9bb01ef05b95b959b0aa365de8bfd5b41ee6f963d2f9f053a176ac2d`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f77555863007461c120a08bff5a4064950f9480c943803faeab52ce0195ecd`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f26b2b4e771728df08c074cb278d9d41dd87e6048ec1eccfb1206e01d5e4f8f`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587ff3b05d9015e5d9471aceedbbdff6e371c2b9ae923af273addce00abfbd1`  
		Last Modified: Sat, 04 Feb 2023 14:49:53 GMT  
		Size: 127.8 MB (127795588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f0c92d7ddeafcc2949667f9fbf63dfaff447ad17cff156957fe4e38ca45aac`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5690a3da4b66efa9e50222b88182474283b4dda3ddd5e7bfee83568005657562`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b8d1d871af097f1efb61a6f8f1c623aa6b6201969f6367182c8d03aab0186e`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-debian`

```console
$ docker pull mysql@sha256:3cebdc40926f61eaac83b5ea26388f8fa770e7636c2ea930421cc5604a41a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.32-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3463914132e73c14c172cd4a94da9c66d0baa1a315b16161f462921193e36aa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177751835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20690ccd77820231956c3b7385b477bcd57afe216412e84b5c0166e04cab52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:47:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Feb 2023 14:47:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:38 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 14:47:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 14:47:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 14:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Sat, 04 Feb 2023 14:47:54 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Feb 2023 14:48:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 04 Feb 2023 14:48:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Feb 2023 14:48:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 04 Feb 2023 14:48:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:48:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 14:48:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:48:11 GMT
EXPOSE 3306 33060
# Sat, 04 Feb 2023 14:48:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4957656d4d97b158dafcf9f7ea1e52ce85827e65d97a1fce33f22b024e0d659f`  
		Last Modified: Sat, 04 Feb 2023 14:49:37 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6013719e001ed5ce0cbc7cdff4ae1f79c141597caa27a8006e92a6326e53345a`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 4.4 MB (4414927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa6814d598d5914d9926ec0a5a04fcc6e790afabc91f4766372af106c17acd2`  
		Last Modified: Sat, 04 Feb 2023 14:49:36 GMT  
		Size: 1.5 MB (1471342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c8eaab45d1b1d84217a009b1ed704b791e724afbf410b70e19cccba16330e7`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f646a9bb01ef05b95b959b0aa365de8bfd5b41ee6f963d2f9f053a176ac2d`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f77555863007461c120a08bff5a4064950f9480c943803faeab52ce0195ecd`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f26b2b4e771728df08c074cb278d9d41dd87e6048ec1eccfb1206e01d5e4f8f`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587ff3b05d9015e5d9471aceedbbdff6e371c2b9ae923af273addce00abfbd1`  
		Last Modified: Sat, 04 Feb 2023 14:49:53 GMT  
		Size: 127.8 MB (127795588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f0c92d7ddeafcc2949667f9fbf63dfaff447ad17cff156957fe4e38ca45aac`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5690a3da4b66efa9e50222b88182474283b4dda3ddd5e7bfee83568005657562`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b8d1d871af097f1efb61a6f8f1c623aa6b6201969f6367182c8d03aab0186e`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-oracle`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:3cebdc40926f61eaac83b5ea26388f8fa770e7636c2ea930421cc5604a41a247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:3463914132e73c14c172cd4a94da9c66d0baa1a315b16161f462921193e36aa6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177751835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf20690ccd77820231956c3b7385b477bcd57afe216412e84b5c0166e04cab52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:41 GMT
ADD file:1d256392bb7afe6942d157db84ca62774ac4114f8a3816fd50bace8d73130b57 in / 
# Sat, 04 Feb 2023 06:51:41 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 14:47:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 04 Feb 2023 14:47:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:38 GMT
ENV GOSU_VERSION=1.16
# Sat, 04 Feb 2023 14:47:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 04 Feb 2023 14:47:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 04 Feb 2023 14:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 14:47:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 04 Feb 2023 14:47:53 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Sat, 04 Feb 2023 14:47:54 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 04 Feb 2023 14:48:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 04 Feb 2023 14:48:10 GMT
VOLUME [/var/lib/mysql]
# Sat, 04 Feb 2023 14:48:10 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 04 Feb 2023 14:48:10 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 04 Feb 2023 14:48:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 04 Feb 2023 14:48:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 14:48:11 GMT
EXPOSE 3306 33060
# Sat, 04 Feb 2023 14:48:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:01b5b2efb836d74b8b49da819514eca52e25290d1688db59420ffb9c6b65a03c`  
		Last Modified: Sat, 04 Feb 2023 06:56:17 GMT  
		Size: 31.4 MB (31396919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4957656d4d97b158dafcf9f7ea1e52ce85827e65d97a1fce33f22b024e0d659f`  
		Last Modified: Sat, 04 Feb 2023 14:49:37 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6013719e001ed5ce0cbc7cdff4ae1f79c141597caa27a8006e92a6326e53345a`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 4.4 MB (4414927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa6814d598d5914d9926ec0a5a04fcc6e790afabc91f4766372af106c17acd2`  
		Last Modified: Sat, 04 Feb 2023 14:49:36 GMT  
		Size: 1.5 MB (1471342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c8eaab45d1b1d84217a009b1ed704b791e724afbf410b70e19cccba16330e7`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf5f646a9bb01ef05b95b959b0aa365de8bfd5b41ee6f963d2f9f053a176ac2d`  
		Last Modified: Sat, 04 Feb 2023 14:49:38 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f77555863007461c120a08bff5a4064950f9480c943803faeab52ce0195ecd`  
		Last Modified: Sat, 04 Feb 2023 14:49:35 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f26b2b4e771728df08c074cb278d9d41dd87e6048ec1eccfb1206e01d5e4f8f`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587ff3b05d9015e5d9471aceedbbdff6e371c2b9ae923af273addce00abfbd1`  
		Last Modified: Sat, 04 Feb 2023 14:49:53 GMT  
		Size: 127.8 MB (127795588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f0c92d7ddeafcc2949667f9fbf63dfaff447ad17cff156957fe4e38ca45aac`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5690a3da4b66efa9e50222b88182474283b4dda3ddd5e7bfee83568005657562`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b8d1d871af097f1efb61a6f8f1c623aa6b6201969f6367182c8d03aab0186e`  
		Last Modified: Sat, 04 Feb 2023 14:49:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:8653a170e0b0df19ea95055267def2615fc53c62df529e3750817c1a886485f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:41932716f7d57462d4f017d8334b60dfb2af5ec973db22e262619c16bd5048e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152727852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57da161f45ac3835bc872dcb50f0cde87f65661ba8f50a5a0835dee7e262703f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:27:31 GMT
ADD file:6a3fb962576ab4237e9335cfcf419249f08417e28cfbb633d7cc6f26f1f85287 in / 
# Wed, 08 Feb 2023 19:27:32 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 19:59:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 19:59:58 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:00:02 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:00:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:00:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:00:28 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:00:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:01:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:01:02 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:01:38 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:01:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:01:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:01:39 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:01:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:197c1adcd755131915cd019bdd58658d44445b3638f65449932c18ee39b6047c`  
		Last Modified: Wed, 08 Feb 2023 19:29:00 GMT  
		Size: 44.6 MB (44555906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f2e353f7d21bc5254906ef1805f61a38d92d477cd26f230488c3db848a109e`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ec6ece42ef02148a547fdb4301418736fe52385681cc85b5f6179760e8d3b3`  
		Last Modified: Wed, 08 Feb 2023 20:02:21 GMT  
		Size: 982.8 KB (982818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa4d9a7b88e583fc9dc29d203ffe164ce01a52512bacb66f6e874150cb12f79`  
		Last Modified: Wed, 08 Feb 2023 20:02:20 GMT  
		Size: 4.6 MB (4619215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cab5858b1d710687ed4a1f05f78b386dca532ea81607ec2d8ea1b2760ffe30`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 2.6 KB (2628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fcd248d9826df8366b03d21a9844394daebd50e645f83487c789464cc386c7`  
		Last Modified: Wed, 08 Feb 2023 20:02:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88635e83312d6f7e9b2bcef9b8689dd22826178b1179c392941b885701403ac3`  
		Last Modified: Wed, 08 Feb 2023 20:02:31 GMT  
		Size: 56.2 MB (56216798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f0427259d9f937d080c42fb75a91d03eb70747ef7a58a4e607c28834ab1572`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79828698a290770756545ab1dc57437faa574f41f08babf9ae72ac9e5cacbec8`  
		Last Modified: Wed, 08 Feb 2023 20:02:26 GMT  
		Size: 46.3 MB (46343438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8854781893ed4f3fa4ea06ad7b928b23e95ddf0c4083efefc634c8932ac4ff6`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8bdf3091d9b3f16eaf8fdbc6055cda47933a21e8b28800b7ca988874f05dba`  
		Last Modified: Wed, 08 Feb 2023 20:02:17 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6499d4392110bbcd65518b96cb64d67110dd191bb462c2f77a81a4c01e4c52eb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.6 MB (151601578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2846b2a84d49c55c6f417ce26161d7cae4ebb0cca9cc123669e739dccb0be989`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 08 Feb 2023 19:44:57 GMT
ADD file:b0d30d32b82572c00d83e2fd97813f8b9ff4c6a92efcd3696df1120df4c1065f in / 
# Wed, 08 Feb 2023 19:44:58 GMT
CMD ["/bin/bash"]
# Wed, 08 Feb 2023 20:01:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 08 Feb 2023 20:01:26 GMT
ENV GOSU_VERSION=1.16
# Wed, 08 Feb 2023 20:01:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 08 Feb 2023 20:01:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 08 Feb 2023 20:01:55 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:01:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 08 Feb 2023 20:02:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Wed, 08 Feb 2023 20:02:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 08 Feb 2023 20:02:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Wed, 08 Feb 2023 20:02:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 08 Feb 2023 20:02:53 GMT
VOLUME [/var/lib/mysql]
# Wed, 08 Feb 2023 20:02:53 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 08 Feb 2023 20:02:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 08 Feb 2023 20:02:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Feb 2023 20:02:53 GMT
EXPOSE 3306 33060
# Wed, 08 Feb 2023 20:02:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7d4ed4ca78bc8f807025d2f2a491ee60099ed37ad040ce330257955d319a347f`  
		Last Modified: Wed, 08 Feb 2023 19:46:11 GMT  
		Size: 43.5 MB (43456591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657a7ca448ac4a06dafad5de62f7753976220cc4f0f4dc519c213be6a7555e4d`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bd78ce95ca0f620cabfb111458e24ddb94a0d6ce9472e1f1c81366116ff9ba`  
		Last Modified: Wed, 08 Feb 2023 20:03:18 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e937b70acc8f194df1b8e96520025950d8d0bbc37443bb7d779b3d0a9514d5`  
		Last Modified: Wed, 08 Feb 2023 20:03:17 GMT  
		Size: 4.4 MB (4448682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bf3d14eb5e577cb1de4158ce1507c412a06d9d68fe20a2c15d96ec4a07b064`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f675b4a4ac08d09f567ff71b9a6addb67614a72f426e6c66f0c8bcaaefece6b`  
		Last Modified: Wed, 08 Feb 2023 20:03:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53482ccac7faf615f7623bd55ff437727b25430d58d569a60f9e456b22218df9`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 55.6 MB (55604368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:828f282108718fdb3be37ba68321d9cf8705e037984d387b85fed2265d41db62`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db57577e20b500fc8c3cd0df79ab20f2898b5f79128727e4129c076a77f99f1`  
		Last Modified: Wed, 08 Feb 2023 20:03:21 GMT  
		Size: 47.2 MB (47169267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:314e3cb90a9a258b0b5c4026555b07c10f129673c1c766e92d98a5b51dec3236`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408e09447dc645e2f39214984dc111b3187cf80ee79c8bcae84049f61fec9044`  
		Last Modified: Wed, 08 Feb 2023 20:03:14 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
