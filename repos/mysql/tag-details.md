<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.38`](#mysql5738)
-	[`mysql:5.7.38-debian`](#mysql5738-debian)
-	[`mysql:5.7.38-oracle`](#mysql5738-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.29`](#mysql8029)
-	[`mysql:8.0.29-debian`](#mysql8029-debian)
-	[`mysql:8.0.29-oracle`](#mysql8029-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:e767595ba3408fbb2dda493be3594b9a148178df58325fafe8b0363662935624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:9519054fe27aa84758d6303f66a6059c47f4bfbfc9d2ce32e4f6fed63cf93a8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa4b5ffb001f0092b491bdd8a48a83cb2ab2b721646db139d4cda64dea93600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:20:28 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Wed, 27 Apr 2022 22:20:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:20:47 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:20:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:47 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:48 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c4c43adf52f5de087a3de9cbbe44961b77501325a167b6e276b1beb16e0f1d`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cab33e8f91f2158824d485f04855550f65a994841cdea4496d0a7faf0d299f`  
		Last Modified: Wed, 27 Apr 2022 22:22:57 GMT  
		Size: 115.7 MB (115675703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c4f2c43f66ed8d87c2d72149baa14bd693f2decdd241b1df1ae5bb1d84632`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ee322af488c94e1fa00b5d075340197f93a00fdbae2e3ac5b9ff68fe8d502`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:e767595ba3408fbb2dda493be3594b9a148178df58325fafe8b0363662935624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9519054fe27aa84758d6303f66a6059c47f4bfbfc9d2ce32e4f6fed63cf93a8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa4b5ffb001f0092b491bdd8a48a83cb2ab2b721646db139d4cda64dea93600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:20:28 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Wed, 27 Apr 2022 22:20:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:20:47 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:20:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:47 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:48 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c4c43adf52f5de087a3de9cbbe44961b77501325a167b6e276b1beb16e0f1d`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cab33e8f91f2158824d485f04855550f65a994841cdea4496d0a7faf0d299f`  
		Last Modified: Wed, 27 Apr 2022 22:22:57 GMT  
		Size: 115.7 MB (115675703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c4f2c43f66ed8d87c2d72149baa14bd693f2decdd241b1df1ae5bb1d84632`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ee322af488c94e1fa00b5d075340197f93a00fdbae2e3ac5b9ff68fe8d502`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:30a1708538c16b5487f559af0b223bd2d1391355c8e1d2d4bed39807ecb9bd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1a41c43ec1d524c4b66c1901b27a438da21eadfbafe3616bda8ea75302098b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126893712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7619c1a0561f44994c5527d453687ac411749a02708aae7e966ce8407ad7a2b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:12:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:12:23 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:12:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:12:36 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 31 Mar 2022 02:12:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:19:48 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Wed, 27 Apr 2022 22:19:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:20:03 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:20:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:20:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Wed, 27 Apr 2022 22:20:22 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:20:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:23 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:23 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1268f9b69b4d2dfc0086f5426266fd97bb99c37e0dc2db707e3e7a5667bba3c`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1084d021338c13d9afc0d3fa5ab8ff753ddd7d97abc2a81074b6fff0807a96`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ad34fb0ede94774c93b333cbdc752915f8d0b45eda981588615248b8fbad9e`  
		Last Modified: Thu, 31 Mar 2022 02:14:12 GMT  
		Size: 3.8 MB (3755164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341499385aec2522efd754b4ba03c458add9de6802a7834b941209fb793dc0f`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50a4a291c85ddcce0931530fad6656dbf111a0b9e320a939a69a55aedb3c6c8`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396321ba07427f51923e3a3dd9aae2ee975d943cd39407d5c1557dc5f457e5d0`  
		Last Modified: Wed, 27 Apr 2022 22:22:24 GMT  
		Size: 25.5 MB (25473337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3992ab4878ba76eec5124d91b386fd2e3c35db49932c8eec13e0511a1996e21`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7881d745f09807de84ae1a7e0e09556a2c31831776461cc55e6b531d5e73bf3c`  
		Last Modified: Wed, 27 Apr 2022 22:22:29 GMT  
		Size: 48.0 MB (47967990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17c44fe903a44a0e1f059dcb92b1bea5ce893982a0644e310ce3527cfd68f64`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:e767595ba3408fbb2dda493be3594b9a148178df58325fafe8b0363662935624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:9519054fe27aa84758d6303f66a6059c47f4bfbfc9d2ce32e4f6fed63cf93a8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa4b5ffb001f0092b491bdd8a48a83cb2ab2b721646db139d4cda64dea93600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:20:28 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Wed, 27 Apr 2022 22:20:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:20:47 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:20:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:47 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:48 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c4c43adf52f5de087a3de9cbbe44961b77501325a167b6e276b1beb16e0f1d`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cab33e8f91f2158824d485f04855550f65a994841cdea4496d0a7faf0d299f`  
		Last Modified: Wed, 27 Apr 2022 22:22:57 GMT  
		Size: 115.7 MB (115675703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c4f2c43f66ed8d87c2d72149baa14bd693f2decdd241b1df1ae5bb1d84632`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ee322af488c94e1fa00b5d075340197f93a00fdbae2e3ac5b9ff68fe8d502`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:e767595ba3408fbb2dda493be3594b9a148178df58325fafe8b0363662935624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9519054fe27aa84758d6303f66a6059c47f4bfbfc9d2ce32e4f6fed63cf93a8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa4b5ffb001f0092b491bdd8a48a83cb2ab2b721646db139d4cda64dea93600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:20:28 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Wed, 27 Apr 2022 22:20:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:20:47 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:20:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:47 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:48 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c4c43adf52f5de087a3de9cbbe44961b77501325a167b6e276b1beb16e0f1d`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cab33e8f91f2158824d485f04855550f65a994841cdea4496d0a7faf0d299f`  
		Last Modified: Wed, 27 Apr 2022 22:22:57 GMT  
		Size: 115.7 MB (115675703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c4f2c43f66ed8d87c2d72149baa14bd693f2decdd241b1df1ae5bb1d84632`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ee322af488c94e1fa00b5d075340197f93a00fdbae2e3ac5b9ff68fe8d502`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:30a1708538c16b5487f559af0b223bd2d1391355c8e1d2d4bed39807ecb9bd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1a41c43ec1d524c4b66c1901b27a438da21eadfbafe3616bda8ea75302098b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126893712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7619c1a0561f44994c5527d453687ac411749a02708aae7e966ce8407ad7a2b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:12:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:12:23 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:12:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:12:36 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 31 Mar 2022 02:12:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:19:48 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Wed, 27 Apr 2022 22:19:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:20:03 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:20:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:20:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Wed, 27 Apr 2022 22:20:22 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:20:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:23 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:23 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1268f9b69b4d2dfc0086f5426266fd97bb99c37e0dc2db707e3e7a5667bba3c`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1084d021338c13d9afc0d3fa5ab8ff753ddd7d97abc2a81074b6fff0807a96`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ad34fb0ede94774c93b333cbdc752915f8d0b45eda981588615248b8fbad9e`  
		Last Modified: Thu, 31 Mar 2022 02:14:12 GMT  
		Size: 3.8 MB (3755164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341499385aec2522efd754b4ba03c458add9de6802a7834b941209fb793dc0f`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50a4a291c85ddcce0931530fad6656dbf111a0b9e320a939a69a55aedb3c6c8`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396321ba07427f51923e3a3dd9aae2ee975d943cd39407d5c1557dc5f457e5d0`  
		Last Modified: Wed, 27 Apr 2022 22:22:24 GMT  
		Size: 25.5 MB (25473337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3992ab4878ba76eec5124d91b386fd2e3c35db49932c8eec13e0511a1996e21`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7881d745f09807de84ae1a7e0e09556a2c31831776461cc55e6b531d5e73bf3c`  
		Last Modified: Wed, 27 Apr 2022 22:22:29 GMT  
		Size: 48.0 MB (47967990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17c44fe903a44a0e1f059dcb92b1bea5ce893982a0644e310ce3527cfd68f64`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38`

```console
$ docker pull mysql@sha256:e767595ba3408fbb2dda493be3594b9a148178df58325fafe8b0363662935624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38` - linux; amd64

```console
$ docker pull mysql@sha256:9519054fe27aa84758d6303f66a6059c47f4bfbfc9d2ce32e4f6fed63cf93a8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa4b5ffb001f0092b491bdd8a48a83cb2ab2b721646db139d4cda64dea93600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:20:28 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Wed, 27 Apr 2022 22:20:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:20:47 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:20:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:47 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:48 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c4c43adf52f5de087a3de9cbbe44961b77501325a167b6e276b1beb16e0f1d`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cab33e8f91f2158824d485f04855550f65a994841cdea4496d0a7faf0d299f`  
		Last Modified: Wed, 27 Apr 2022 22:22:57 GMT  
		Size: 115.7 MB (115675703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c4f2c43f66ed8d87c2d72149baa14bd693f2decdd241b1df1ae5bb1d84632`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ee322af488c94e1fa00b5d075340197f93a00fdbae2e3ac5b9ff68fe8d502`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-debian`

```console
$ docker pull mysql@sha256:e767595ba3408fbb2dda493be3594b9a148178df58325fafe8b0363662935624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9519054fe27aa84758d6303f66a6059c47f4bfbfc9d2ce32e4f6fed63cf93a8c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa4b5ffb001f0092b491bdd8a48a83cb2ab2b721646db139d4cda64dea93600`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:05:20 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:20:28 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Wed, 27 Apr 2022 22:20:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:20:47 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:20:47 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:47 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:20:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:48 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c4c43adf52f5de087a3de9cbbe44961b77501325a167b6e276b1beb16e0f1d`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cab33e8f91f2158824d485f04855550f65a994841cdea4496d0a7faf0d299f`  
		Last Modified: Wed, 27 Apr 2022 22:22:57 GMT  
		Size: 115.7 MB (115675703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1c4f2c43f66ed8d87c2d72149baa14bd693f2decdd241b1df1ae5bb1d84632`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5ee322af488c94e1fa00b5d075340197f93a00fdbae2e3ac5b9ff68fe8d502`  
		Last Modified: Wed, 27 Apr 2022 22:22:42 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-oracle`

```console
$ docker pull mysql@sha256:30a1708538c16b5487f559af0b223bd2d1391355c8e1d2d4bed39807ecb9bd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1a41c43ec1d524c4b66c1901b27a438da21eadfbafe3616bda8ea75302098b8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126893712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7619c1a0561f44994c5527d453687ac411749a02708aae7e966ce8407ad7a2b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:36:11 GMT
ADD file:b0df42f2bb614be48861be26e670ab6a81c1549d24e64b5e355980adcf0074be in / 
# Tue, 29 Mar 2022 18:36:11 GMT
CMD ["/bin/bash"]
# Thu, 31 Mar 2022 02:12:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 31 Mar 2022 02:12:23 GMT
ENV GOSU_VERSION=1.14
# Thu, 31 Mar 2022 02:12:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 31 Mar 2022 02:12:36 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 31 Mar 2022 02:12:37 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 31 Mar 2022 02:12:37 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 27 Apr 2022 22:19:48 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Wed, 27 Apr 2022 22:19:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:20:03 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:20:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:20:04 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Wed, 27 Apr 2022 22:20:22 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:20:23 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:20:23 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:20:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:20:23 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:20:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9347a8f0b30748522f1f50b679f9f2d0c3eea2bb49da98bb4f38a8c8619b7bf8`  
		Last Modified: Tue, 29 Mar 2022 18:37:31 GMT  
		Size: 48.8 MB (48757483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1268f9b69b4d2dfc0086f5426266fd97bb99c37e0dc2db707e3e7a5667bba3c`  
		Last Modified: Thu, 31 Mar 2022 02:14:13 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1084d021338c13d9afc0d3fa5ab8ff753ddd7d97abc2a81074b6fff0807a96`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ad34fb0ede94774c93b333cbdc752915f8d0b45eda981588615248b8fbad9e`  
		Last Modified: Thu, 31 Mar 2022 02:14:12 GMT  
		Size: 3.8 MB (3755164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e341499385aec2522efd754b4ba03c458add9de6802a7834b941209fb793dc0f`  
		Last Modified: Thu, 31 Mar 2022 02:14:11 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50a4a291c85ddcce0931530fad6656dbf111a0b9e320a939a69a55aedb3c6c8`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396321ba07427f51923e3a3dd9aae2ee975d943cd39407d5c1557dc5f457e5d0`  
		Last Modified: Wed, 27 Apr 2022 22:22:24 GMT  
		Size: 25.5 MB (25473337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3992ab4878ba76eec5124d91b386fd2e3c35db49932c8eec13e0511a1996e21`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7881d745f09807de84ae1a7e0e09556a2c31831776461cc55e6b531d5e73bf3c`  
		Last Modified: Wed, 27 Apr 2022 22:22:29 GMT  
		Size: 48.0 MB (47967990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17c44fe903a44a0e1f059dcb92b1bea5ce893982a0644e310ce3527cfd68f64`  
		Last Modified: Wed, 27 Apr 2022 22:22:20 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:fc78703c40e5e3927fb7f175d80cb86101b8cad21be0bc739151534027cc5adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e2e3ac9e2e250f5a732aa19e7abbecaddd8b6ca0062219639b63d712cc896101
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134826957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb7e0211b3307d63627318adc7ded02adf2f286fcd01a9a9eb29d497dff9325`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:18:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 27 Apr 2022 22:18:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 27 Apr 2022 22:18:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 27 Apr 2022 22:18:28 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:18:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:18:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:18:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:19:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:19:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:24 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:24 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfb98692c91e41758cca49b67e9d047a2b0b9330b7b72fbff20a4c50865e5b5`  
		Last Modified: Wed, 27 Apr 2022 22:21:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12707a593559027a9ae6ecf82c947caf83dea80b0bb7dd42c59fd1b95f8701d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e11d97b12251011247579c13626ff8dfb07b0e6dd8eb90e7abc3553bedc04d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 4.6 MB (4558301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9923677ea4133dd45c8ca78f72f6f375732f0dd79e314ad3b1f0cc120d59010`  
		Last Modified: Wed, 27 Apr 2022 22:21:15 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ea275311cdcc42db37cacafb4c63481f6341e971dc3a8b6bef67cca06a82d`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b618919e74db0e4a09bddba62fdc562d4955d20b32bc23c4414416b64f92dc61`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 47.3 MB (47267824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7481ce0984d0580224176c0926e2797d941accba91da8b98b343294be1ad66ec`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d98e5de332ce6dd030a782b4f0945f0b6b19b02b04f9a5aca1799524549cc85`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 39.9 MB (39948341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798d9de77592cc395f2d2034b096fc1cdeb02ebc88dcbfd336b3c1ed30bfcc66`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:fc78703c40e5e3927fb7f175d80cb86101b8cad21be0bc739151534027cc5adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e2e3ac9e2e250f5a732aa19e7abbecaddd8b6ca0062219639b63d712cc896101
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134826957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb7e0211b3307d63627318adc7ded02adf2f286fcd01a9a9eb29d497dff9325`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:18:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 27 Apr 2022 22:18:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 27 Apr 2022 22:18:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 27 Apr 2022 22:18:28 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:18:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:18:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:18:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:19:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:19:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:24 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:24 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfb98692c91e41758cca49b67e9d047a2b0b9330b7b72fbff20a4c50865e5b5`  
		Last Modified: Wed, 27 Apr 2022 22:21:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12707a593559027a9ae6ecf82c947caf83dea80b0bb7dd42c59fd1b95f8701d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e11d97b12251011247579c13626ff8dfb07b0e6dd8eb90e7abc3553bedc04d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 4.6 MB (4558301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9923677ea4133dd45c8ca78f72f6f375732f0dd79e314ad3b1f0cc120d59010`  
		Last Modified: Wed, 27 Apr 2022 22:21:15 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ea275311cdcc42db37cacafb4c63481f6341e971dc3a8b6bef67cca06a82d`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b618919e74db0e4a09bddba62fdc562d4955d20b32bc23c4414416b64f92dc61`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 47.3 MB (47267824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7481ce0984d0580224176c0926e2797d941accba91da8b98b343294be1ad66ec`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d98e5de332ce6dd030a782b4f0945f0b6b19b02b04f9a5aca1799524549cc85`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 39.9 MB (39948341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798d9de77592cc395f2d2034b096fc1cdeb02ebc88dcbfd336b3c1ed30bfcc66`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-debian`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29-debian` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-oracle`

```console
$ docker pull mysql@sha256:1016c4f84331f19a49ed684eee6a10a8fa87216624542cbb1af9a617dae4e66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e2e3ac9e2e250f5a732aa19e7abbecaddd8b6ca0062219639b63d712cc896101
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134826957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb7e0211b3307d63627318adc7ded02adf2f286fcd01a9a9eb29d497dff9325`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:18:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 27 Apr 2022 22:18:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 27 Apr 2022 22:18:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 27 Apr 2022 22:18:28 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:18:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:18:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:18:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:19:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:19:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:24 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:24 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfb98692c91e41758cca49b67e9d047a2b0b9330b7b72fbff20a4c50865e5b5`  
		Last Modified: Wed, 27 Apr 2022 22:21:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12707a593559027a9ae6ecf82c947caf83dea80b0bb7dd42c59fd1b95f8701d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e11d97b12251011247579c13626ff8dfb07b0e6dd8eb90e7abc3553bedc04d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 4.6 MB (4558301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9923677ea4133dd45c8ca78f72f6f375732f0dd79e314ad3b1f0cc120d59010`  
		Last Modified: Wed, 27 Apr 2022 22:21:15 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ea275311cdcc42db37cacafb4c63481f6341e971dc3a8b6bef67cca06a82d`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b618919e74db0e4a09bddba62fdc562d4955d20b32bc23c4414416b64f92dc61`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 47.3 MB (47267824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7481ce0984d0580224176c0926e2797d941accba91da8b98b343294be1ad66ec`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d98e5de332ce6dd030a782b4f0945f0b6b19b02b04f9a5aca1799524549cc85`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 39.9 MB (39948341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798d9de77592cc395f2d2034b096fc1cdeb02ebc88dcbfd336b3c1ed30bfcc66`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:2dafe3f044f140ec6c07716d34f0b317b98f8e251435abd347951699f7aa3904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:6e866f4e8bf7e83d8c605fe0252e53219c23e4052cb22f7f23353d5bf800de63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155885274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d0eae5ed6069320a16ec1029b7378e330c31473bb7ba3027578c7c582c0076`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 20 Apr 2022 04:43:48 GMT
ADD file:011a43ee23214c201afb7f3b5be592f374b89a4c71aea82ca66146bbbc31b959 in / 
# Wed, 20 Apr 2022 04:43:48 GMT
CMD ["bash"]
# Wed, 20 Apr 2022 10:04:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 20 Apr 2022 10:04:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:36 GMT
ENV GOSU_VERSION=1.14
# Wed, 20 Apr 2022 10:04:45 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 20 Apr 2022 10:04:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 20 Apr 2022 10:04:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Apr 2022 10:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 20 Apr 2022 10:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:19:28 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Wed, 27 Apr 2022 22:19:28 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 27 Apr 2022 22:19:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 27 Apr 2022 22:19:43 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:43 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 27 Apr 2022 22:19:44 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 27 Apr 2022 22:19:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:44 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4be315f6562fccf08fd6c749557e31e45ab6d987370e20e2c4933ddb04ddd5ff`  
		Last Modified: Wed, 20 Apr 2022 04:49:15 GMT  
		Size: 27.1 MB (27140664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e2eb237a1b01f5f7102bf13d4d92bc60937a8f75fcfd4bea0d6f37f29e36ad`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa3ac85066b123f51dc3116666eaa90f904194f8ccbbb38edef3f75382bde5a`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 4.2 MB (4179280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e524f6c89f7c75ef7a9ad752e344967db67ebf0a0a1248a2e40c120290bf8`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a88631064fc8f7cd0d269d71800a9fe2768e1bf3c32ffd10489e620ab52b32`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15bb3ec3ff50c5b6a064dd106f3ece814edc88c72e3d9672434e1c014784585e`  
		Last Modified: Wed, 20 Apr 2022 10:06:12 GMT  
		Size: 14.1 MB (14064336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae65dc337dcb723acc14fda695c58c87adbf9e0c85b631185c6158f9c447a0df`  
		Last Modified: Wed, 20 Apr 2022 10:06:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573c3c7fa18d22ec13ab3d6c5117206fb39696cafa18e4d3aff9745699d7f9e3`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10771b98b8c94d2d2abf3f498ff6358162b8e01118188d1a4fc5fe59fed973`  
		Last Modified: Wed, 27 Apr 2022 22:21:52 GMT  
		Size: 109.1 MB (109103563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8ef442614b5e3860c987592f78592e7aa9c791fd76d8745877c05e25df821e`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc17a6cea2677755e08ed163a46d098e7e5f1c89b9bb52d19f3df8975acb3ac`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752752efdaeae5b119214a83fbc73c7509e3bc3750f395ac96c900f7a562a0a2`  
		Last Modified: Wed, 27 Apr 2022 22:21:36 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:fc78703c40e5e3927fb7f175d80cb86101b8cad21be0bc739151534027cc5adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e2e3ac9e2e250f5a732aa19e7abbecaddd8b6ca0062219639b63d712cc896101
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134826957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb7e0211b3307d63627318adc7ded02adf2f286fcd01a9a9eb29d497dff9325`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 22:18:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 27 Apr 2022 22:18:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 27 Apr 2022 22:18:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 27 Apr 2022 22:18:28 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 27 Apr 2022 22:18:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:18:29 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 27 Apr 2022 22:18:54 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 27 Apr 2022 22:18:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 27 Apr 2022 22:18:55 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Wed, 27 Apr 2022 22:19:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 27 Apr 2022 22:19:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 27 Apr 2022 22:19:24 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 27 Apr 2022 22:19:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Apr 2022 22:19:24 GMT
EXPOSE 3306 33060
# Wed, 27 Apr 2022 22:19:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bfb98692c91e41758cca49b67e9d047a2b0b9330b7b72fbff20a4c50865e5b5`  
		Last Modified: Wed, 27 Apr 2022 22:21:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12707a593559027a9ae6ecf82c947caf83dea80b0bb7dd42c59fd1b95f8701d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e11d97b12251011247579c13626ff8dfb07b0e6dd8eb90e7abc3553bedc04d4`  
		Last Modified: Wed, 27 Apr 2022 22:21:16 GMT  
		Size: 4.6 MB (4558301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9923677ea4133dd45c8ca78f72f6f375732f0dd79e314ad3b1f0cc120d59010`  
		Last Modified: Wed, 27 Apr 2022 22:21:15 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890ea275311cdcc42db37cacafb4c63481f6341e971dc3a8b6bef67cca06a82d`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b618919e74db0e4a09bddba62fdc562d4955d20b32bc23c4414416b64f92dc61`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 47.3 MB (47267824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7481ce0984d0580224176c0926e2797d941accba91da8b98b343294be1ad66ec`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d98e5de332ce6dd030a782b4f0945f0b6b19b02b04f9a5aca1799524549cc85`  
		Last Modified: Wed, 27 Apr 2022 22:21:21 GMT  
		Size: 39.9 MB (39948341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798d9de77592cc395f2d2034b096fc1cdeb02ebc88dcbfd336b3c1ed30bfcc66`  
		Last Modified: Wed, 27 Apr 2022 22:21:13 GMT  
		Size: 5.1 KB (5140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a84c40eb932fc324b1232320a83a91bdd0e25292400e44690c956fc036a5826
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3f4a2767a37c46e2f5424f1f0e8e79ace6fad52400c3220a6b7f7092b52aff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 19:36:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Wed, 30 Mar 2022 19:36:27 GMT
ENV GOSU_VERSION=1.14
# Wed, 30 Mar 2022 19:36:30 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 30 Mar 2022 19:36:52 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 30 Mar 2022 19:36:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 30 Mar 2022 19:36:55 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 30 Mar 2022 19:36:56 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:36:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 30 Mar 2022 19:37:21 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 30 Mar 2022 19:37:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 30 Mar 2022 19:37:22 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 30 Mar 2022 19:37:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 30 Mar 2022 19:37:51 GMT
VOLUME [/var/lib/mysql]
# Wed, 30 Mar 2022 19:37:52 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Wed, 30 Mar 2022 19:37:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Mar 2022 19:37:53 GMT
EXPOSE 3306 33060
# Wed, 30 Mar 2022 19:37:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab860100fd06bf966bba43e945a81bc929141ededd09d9ac425c6f84f6e3e03`  
		Last Modified: Wed, 30 Mar 2022 19:38:24 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beca8ba6c49cf952f7d2a549637ac71b887bba93a5e30f8e8cf1858369fb67d`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c660f342d4fc90e2cae9584677828102e44965aac6e26780916a1e8ef2ff18ee`  
		Last Modified: Wed, 30 Mar 2022 19:38:22 GMT  
		Size: 4.4 MB (4378770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ff8141a9459038f2bc38cd3ded605c6f405d4daf7d56cf6b4f52dd9a2cb5dd`  
		Last Modified: Wed, 30 Mar 2022 19:38:21 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81de35ab51f9a083208854e695dc8879ecf7b9820ef90d9c2c356219ba2651fc`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd10c0fb45dc51fe4815d510ad7c71fef44e80dd9393308f7ad1a475c465c`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 53.4 MB (53429900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42744cc7790693010c1abb7779bc759b995d9e50d8904bd37afebaf941dcf12b`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cc9d0d65fd6d9afa6e8bcca9941cd6fdaab5a37ee45ce68ea4def7528d673a`  
		Last Modified: Wed, 30 Mar 2022 19:38:27 GMT  
		Size: 40.5 MB (40479681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18f188c7be958b84ecc16d325c13dd32543ff1e126d9fe14bec3b8397ec173c`  
		Last Modified: Wed, 30 Mar 2022 19:38:19 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
