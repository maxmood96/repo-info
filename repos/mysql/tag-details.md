<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.37`](#mysql5737)
-	[`mysql:5.7.37-debian`](#mysql5737-debian)
-	[`mysql:5.7.37-oracle`](#mysql5737-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.28`](#mysql8028)
-	[`mysql:8.0.28-debian`](#mysql8028-debian)
-	[`mysql:8.0.28-oracle`](#mysql8028-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:372af24c361a5466db159b7a2b9726762473b9a8f097fe66d3df43ba0df51743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:661be71bb5bbf896a4d897bb89965cb39129fe9aa62245e5923523463e397788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae552624b4bdd1ada7c727321df1a9266fdf55315f877cfa9264939813357f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 01 Mar 2022 13:50:03 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:50:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:50:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:50:27 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:50:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:50:28 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a924e739fa391e619d7c43a6b71ecb21a681c775ae0c85c0e6a7072795718f3e`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd08908162d4584521f888c9c1c4300289e06b818874a265e1e4579d06da9f8`  
		Last Modified: Tue, 01 Mar 2022 13:52:20 GMT  
		Size: 108.6 MB (108636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a8f23ce674bbb479ce961eeb7253ca352f8ece074d60f0f6da52df4cddd10d`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72260a38e18a2c9ed8a4d291dbf8659c2b84fc154e906207de7a14b32648af7`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:372af24c361a5466db159b7a2b9726762473b9a8f097fe66d3df43ba0df51743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:661be71bb5bbf896a4d897bb89965cb39129fe9aa62245e5923523463e397788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae552624b4bdd1ada7c727321df1a9266fdf55315f877cfa9264939813357f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 01 Mar 2022 13:50:03 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:50:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:50:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:50:27 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:50:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:50:28 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a924e739fa391e619d7c43a6b71ecb21a681c775ae0c85c0e6a7072795718f3e`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd08908162d4584521f888c9c1c4300289e06b818874a265e1e4579d06da9f8`  
		Last Modified: Tue, 01 Mar 2022 13:52:20 GMT  
		Size: 108.6 MB (108636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a8f23ce674bbb479ce961eeb7253ca352f8ece074d60f0f6da52df4cddd10d`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72260a38e18a2c9ed8a4d291dbf8659c2b84fc154e906207de7a14b32648af7`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:5fca31d24116ab727cdcb8cb8f0b581ba26f9257d2343e4b12a6de47c66ad3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:47092e3dd85d585b6ebcf3a8d665ba37c524fb2e9ea2b6cba630ca2c468b7ed9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124772454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2549c657f5970cfeed1e30074b83ae065d7c04e15708612f74c7d53f79e9708`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 02:33:18 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 	; 	yum clean all
# Sat, 26 Feb 2022 02:33:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 02:33:54 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 26 Feb 2022 02:33:54 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Sat, 26 Feb 2022 02:33:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 02:34:14 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 02:34:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 02:34:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Sat, 26 Feb 2022 02:34:33 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 02:34:34 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 02:34:34 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 02:34:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 02:34:35 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 02:34:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d3bca8464f8e48d13da175628bf452f777f119cdbd09b067cdcc93133ef08f`  
		Last Modified: Sat, 26 Feb 2022 02:35:40 GMT  
		Size: 3.7 MB (3711625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518b04e30279fb2321a66e4ab61a0e10fba0b7f6dd033f9f9f1cc067ac213661`  
		Last Modified: Sat, 26 Feb 2022 02:35:39 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a682d24e4a47e47913cc3061c0f6b0a7ff035cb2f3987df557a7b85bd4b811b1`  
		Last Modified: Sat, 26 Feb 2022 02:35:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c0faeb2d4f17e0aa5422653dfccde10762667e946c7a6467564fa5abbeb345`  
		Last Modified: Sat, 26 Feb 2022 02:35:41 GMT  
		Size: 25.4 MB (25434060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76d2a24e41cb6651bef1fdd04c19ec05f9921971120256559f5d4dfc0174e47`  
		Last Modified: Sat, 26 Feb 2022 02:35:37 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dce0835ec0040ee6a890b755517e33ca40d036e26056e40b8c6b0792536d58`  
		Last Modified: Sat, 26 Feb 2022 02:35:46 GMT  
		Size: 46.4 MB (46356342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c9e91e4d59e02df36a3fdda04f62cda3325737aef115a8f63260a330eacd7`  
		Last Modified: Sat, 26 Feb 2022 02:35:36 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:372af24c361a5466db159b7a2b9726762473b9a8f097fe66d3df43ba0df51743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:661be71bb5bbf896a4d897bb89965cb39129fe9aa62245e5923523463e397788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae552624b4bdd1ada7c727321df1a9266fdf55315f877cfa9264939813357f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 01 Mar 2022 13:50:03 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:50:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:50:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:50:27 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:50:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:50:28 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a924e739fa391e619d7c43a6b71ecb21a681c775ae0c85c0e6a7072795718f3e`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd08908162d4584521f888c9c1c4300289e06b818874a265e1e4579d06da9f8`  
		Last Modified: Tue, 01 Mar 2022 13:52:20 GMT  
		Size: 108.6 MB (108636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a8f23ce674bbb479ce961eeb7253ca352f8ece074d60f0f6da52df4cddd10d`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72260a38e18a2c9ed8a4d291dbf8659c2b84fc154e906207de7a14b32648af7`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:372af24c361a5466db159b7a2b9726762473b9a8f097fe66d3df43ba0df51743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:661be71bb5bbf896a4d897bb89965cb39129fe9aa62245e5923523463e397788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae552624b4bdd1ada7c727321df1a9266fdf55315f877cfa9264939813357f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 01 Mar 2022 13:50:03 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:50:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:50:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:50:27 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:50:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:50:28 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a924e739fa391e619d7c43a6b71ecb21a681c775ae0c85c0e6a7072795718f3e`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd08908162d4584521f888c9c1c4300289e06b818874a265e1e4579d06da9f8`  
		Last Modified: Tue, 01 Mar 2022 13:52:20 GMT  
		Size: 108.6 MB (108636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a8f23ce674bbb479ce961eeb7253ca352f8ece074d60f0f6da52df4cddd10d`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72260a38e18a2c9ed8a4d291dbf8659c2b84fc154e906207de7a14b32648af7`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:5fca31d24116ab727cdcb8cb8f0b581ba26f9257d2343e4b12a6de47c66ad3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:47092e3dd85d585b6ebcf3a8d665ba37c524fb2e9ea2b6cba630ca2c468b7ed9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124772454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2549c657f5970cfeed1e30074b83ae065d7c04e15708612f74c7d53f79e9708`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 02:33:18 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 	; 	yum clean all
# Sat, 26 Feb 2022 02:33:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 02:33:54 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 26 Feb 2022 02:33:54 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Sat, 26 Feb 2022 02:33:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 02:34:14 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 02:34:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 02:34:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Sat, 26 Feb 2022 02:34:33 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 02:34:34 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 02:34:34 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 02:34:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 02:34:35 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 02:34:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d3bca8464f8e48d13da175628bf452f777f119cdbd09b067cdcc93133ef08f`  
		Last Modified: Sat, 26 Feb 2022 02:35:40 GMT  
		Size: 3.7 MB (3711625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518b04e30279fb2321a66e4ab61a0e10fba0b7f6dd033f9f9f1cc067ac213661`  
		Last Modified: Sat, 26 Feb 2022 02:35:39 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a682d24e4a47e47913cc3061c0f6b0a7ff035cb2f3987df557a7b85bd4b811b1`  
		Last Modified: Sat, 26 Feb 2022 02:35:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c0faeb2d4f17e0aa5422653dfccde10762667e946c7a6467564fa5abbeb345`  
		Last Modified: Sat, 26 Feb 2022 02:35:41 GMT  
		Size: 25.4 MB (25434060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76d2a24e41cb6651bef1fdd04c19ec05f9921971120256559f5d4dfc0174e47`  
		Last Modified: Sat, 26 Feb 2022 02:35:37 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dce0835ec0040ee6a890b755517e33ca40d036e26056e40b8c6b0792536d58`  
		Last Modified: Sat, 26 Feb 2022 02:35:46 GMT  
		Size: 46.4 MB (46356342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c9e91e4d59e02df36a3fdda04f62cda3325737aef115a8f63260a330eacd7`  
		Last Modified: Sat, 26 Feb 2022 02:35:36 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37`

```console
$ docker pull mysql@sha256:372af24c361a5466db159b7a2b9726762473b9a8f097fe66d3df43ba0df51743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37` - linux; amd64

```console
$ docker pull mysql@sha256:661be71bb5bbf896a4d897bb89965cb39129fe9aa62245e5923523463e397788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae552624b4bdd1ada7c727321df1a9266fdf55315f877cfa9264939813357f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 01 Mar 2022 13:50:03 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:50:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:50:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:50:27 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:50:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:50:28 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a924e739fa391e619d7c43a6b71ecb21a681c775ae0c85c0e6a7072795718f3e`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd08908162d4584521f888c9c1c4300289e06b818874a265e1e4579d06da9f8`  
		Last Modified: Tue, 01 Mar 2022 13:52:20 GMT  
		Size: 108.6 MB (108636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a8f23ce674bbb479ce961eeb7253ca352f8ece074d60f0f6da52df4cddd10d`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72260a38e18a2c9ed8a4d291dbf8659c2b84fc154e906207de7a14b32648af7`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-debian`

```console
$ docker pull mysql@sha256:372af24c361a5466db159b7a2b9726762473b9a8f097fe66d3df43ba0df51743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:661be71bb5bbf896a4d897bb89965cb39129fe9aa62245e5923523463e397788
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154804577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae552624b4bdd1ada7c727321df1a9266fdf55315f877cfa9264939813357f7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 01 Mar 2022 13:50:03 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Tue, 01 Mar 2022 13:50:03 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:50:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:50:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:50:27 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:50:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:50:28 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:50:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a924e739fa391e619d7c43a6b71ecb21a681c775ae0c85c0e6a7072795718f3e`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd08908162d4584521f888c9c1c4300289e06b818874a265e1e4579d06da9f8`  
		Last Modified: Tue, 01 Mar 2022 13:52:20 GMT  
		Size: 108.6 MB (108636653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a8f23ce674bbb479ce961eeb7253ca352f8ece074d60f0f6da52df4cddd10d`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72260a38e18a2c9ed8a4d291dbf8659c2b84fc154e906207de7a14b32648af7`  
		Last Modified: Tue, 01 Mar 2022 13:52:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-oracle`

```console
$ docker pull mysql@sha256:5fca31d24116ab727cdcb8cb8f0b581ba26f9257d2343e4b12a6de47c66ad3c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:47092e3dd85d585b6ebcf3a8d665ba37c524fb2e9ea2b6cba630ca2c468b7ed9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124772454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2549c657f5970cfeed1e30074b83ae065d7c04e15708612f74c7d53f79e9708`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:48 GMT
ADD file:91284124cb9327f41cef52acd3563b18b3470a9c4354f2e2ecdf45e23330437f in / 
# Fri, 25 Feb 2022 02:07:49 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:33:55 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:33:55 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:33:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 02:33:18 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 	; 	yum clean all
# Sat, 26 Feb 2022 02:33:54 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 02:33:54 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 26 Feb 2022 02:33:54 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Sat, 26 Feb 2022 02:33:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 02:34:14 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 02:34:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 02:34:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Sat, 26 Feb 2022 02:34:33 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 02:34:34 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 02:34:34 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 02:34:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 02:34:35 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 02:34:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:564e69ebc2e04e046f0b9f0d3a96822dabef192300736d02dc92c3f23e3fd084`  
		Last Modified: Fri, 25 Feb 2022 02:09:09 GMT  
		Size: 48.3 MB (48330862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4915557694f2e99ba4f3c31018dd343c5dd684cc17dfc82bc6907c0ad8b7c7be`  
		Last Modified: Fri, 25 Feb 2022 03:36:26 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda14bdaa732132cfb0a98e28a5372b750b07f7c701dd3f23b27209d91359dd0`  
		Last Modified: Fri, 25 Feb 2022 03:36:23 GMT  
		Size: 930.2 KB (930235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d3bca8464f8e48d13da175628bf452f777f119cdbd09b067cdcc93133ef08f`  
		Last Modified: Sat, 26 Feb 2022 02:35:40 GMT  
		Size: 3.7 MB (3711625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518b04e30279fb2321a66e4ab61a0e10fba0b7f6dd033f9f9f1cc067ac213661`  
		Last Modified: Sat, 26 Feb 2022 02:35:39 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a682d24e4a47e47913cc3061c0f6b0a7ff035cb2f3987df557a7b85bd4b811b1`  
		Last Modified: Sat, 26 Feb 2022 02:35:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c0faeb2d4f17e0aa5422653dfccde10762667e946c7a6467564fa5abbeb345`  
		Last Modified: Sat, 26 Feb 2022 02:35:41 GMT  
		Size: 25.4 MB (25434060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76d2a24e41cb6651bef1fdd04c19ec05f9921971120256559f5d4dfc0174e47`  
		Last Modified: Sat, 26 Feb 2022 02:35:37 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dce0835ec0040ee6a890b755517e33ca40d036e26056e40b8c6b0792536d58`  
		Last Modified: Sat, 26 Feb 2022 02:35:46 GMT  
		Size: 46.4 MB (46356342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c9e91e4d59e02df36a3fdda04f62cda3325737aef115a8f63260a330eacd7`  
		Last Modified: Sat, 26 Feb 2022 02:35:36 GMT  
		Size: 5.0 KB (4955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:c290ae4835977163f5e64f0097ca8e3e68b7bfe8e1be6eaf868cd2c784f49a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:597c5419f5b4979ca774c3a08b8cc720d4f6b91b931db53e1cb86e8d0a25762c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132231021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915bc1b56d7faf8dbed03ea6307819c2de218fe65cc4b0f01f1c2ba9c389399`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 02:31:13 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 02:31:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:31:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 02:32:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 02:32:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 02:32:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:32:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 02:32:44 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 02:32:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 02:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 02:32:45 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 02:32:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459aff8953013538dc5161aac0290e8bbe67052969efa2ab421fa3639f61956`  
		Last Modified: Sat, 26 Feb 2022 02:35:11 GMT  
		Size: 3.8 MB (3849261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193d82a8e1cea1608ed4d733010f06e490fd2fc76717106fff8824bc58cc33d1`  
		Last Modified: Sat, 26 Feb 2022 02:35:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed143356aa61b0171a452553374af4991efa3a035ab79617b7836b4bde902906`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0dcca74e88aacab22d3e1eaf2c07b52f21eab21515916480c11764bd982d6c`  
		Last Modified: Sat, 26 Feb 2022 02:35:17 GMT  
		Size: 47.3 MB (47261001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e90b9d1c34c4a1ebe12dc9910794d0a77b03e8ec2cfd3c101896f150d7c46`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e096125d73fe4740b24a4cd94e0d2ae6f171b2f0258bcf07a535419e7f7e9`  
		Last Modified: Sat, 26 Feb 2022 02:35:16 GMT  
		Size: 38.3 MB (38301334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b53604831c3b9b77bdba50ebf896f1a64947ce00f09e60a7bb2a8bc9874623`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 5.0 KB (4953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e005dcbd8ab96b15fe4937aba1cdac2ee332f9ac64844b43f0682c9e0ecd0dca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140761765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffe8c4711962405da726c2e9b7bd19521b8cb346cdedc97a2d49c093303da4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 16:44:31 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 16:45:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 16:45:13 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 16:45:14 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:45:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 16:45:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:46:02 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 16:46:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 16:46:04 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 16:46:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 16:46:05 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 16:46:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ed278df2509412e7b05f12e7320cb3f2614a831ec1ec894d7d39c9cb0ab6e5`  
		Last Modified: Sat, 26 Feb 2022 16:46:39 GMT  
		Size: 4.0 MB (4005620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93b01f7b04bed4054f1e9ba825f4a4bcb8cbfaaab21ab7e1bc7e4e5facbd34`  
		Last Modified: Sat, 26 Feb 2022 16:46:38 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a0806a1841064be108b7c204ea8cc39462f116525a4f7a044e8056cd9c5851`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc52d9a5079e1a0f43a9bc7f53334d0a9688c1327414e1eb1562ade8abfede7f`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 53.4 MB (53426463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb38734b87010a77486e57a23a05876bd81d3636d0dc8e0b1794cb9a9a9ad9`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e25dd4e90f4fc5e4eb6cc2e41e3e65e51486a69d8e7bd0de461f4c5e4db1ad`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 40.5 MB (40511442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142127aec3b22b34c28299004fabee9100ff4f610c0f205373e48e976bc0ca43`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:c290ae4835977163f5e64f0097ca8e3e68b7bfe8e1be6eaf868cd2c784f49a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:597c5419f5b4979ca774c3a08b8cc720d4f6b91b931db53e1cb86e8d0a25762c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132231021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915bc1b56d7faf8dbed03ea6307819c2de218fe65cc4b0f01f1c2ba9c389399`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 02:31:13 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 02:31:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:31:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 02:32:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 02:32:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 02:32:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:32:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 02:32:44 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 02:32:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 02:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 02:32:45 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 02:32:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459aff8953013538dc5161aac0290e8bbe67052969efa2ab421fa3639f61956`  
		Last Modified: Sat, 26 Feb 2022 02:35:11 GMT  
		Size: 3.8 MB (3849261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193d82a8e1cea1608ed4d733010f06e490fd2fc76717106fff8824bc58cc33d1`  
		Last Modified: Sat, 26 Feb 2022 02:35:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed143356aa61b0171a452553374af4991efa3a035ab79617b7836b4bde902906`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0dcca74e88aacab22d3e1eaf2c07b52f21eab21515916480c11764bd982d6c`  
		Last Modified: Sat, 26 Feb 2022 02:35:17 GMT  
		Size: 47.3 MB (47261001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e90b9d1c34c4a1ebe12dc9910794d0a77b03e8ec2cfd3c101896f150d7c46`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e096125d73fe4740b24a4cd94e0d2ae6f171b2f0258bcf07a535419e7f7e9`  
		Last Modified: Sat, 26 Feb 2022 02:35:16 GMT  
		Size: 38.3 MB (38301334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b53604831c3b9b77bdba50ebf896f1a64947ce00f09e60a7bb2a8bc9874623`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 5.0 KB (4953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e005dcbd8ab96b15fe4937aba1cdac2ee332f9ac64844b43f0682c9e0ecd0dca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140761765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffe8c4711962405da726c2e9b7bd19521b8cb346cdedc97a2d49c093303da4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 16:44:31 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 16:45:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 16:45:13 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 16:45:14 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:45:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 16:45:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:46:02 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 16:46:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 16:46:04 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 16:46:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 16:46:05 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 16:46:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ed278df2509412e7b05f12e7320cb3f2614a831ec1ec894d7d39c9cb0ab6e5`  
		Last Modified: Sat, 26 Feb 2022 16:46:39 GMT  
		Size: 4.0 MB (4005620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93b01f7b04bed4054f1e9ba825f4a4bcb8cbfaaab21ab7e1bc7e4e5facbd34`  
		Last Modified: Sat, 26 Feb 2022 16:46:38 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a0806a1841064be108b7c204ea8cc39462f116525a4f7a044e8056cd9c5851`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc52d9a5079e1a0f43a9bc7f53334d0a9688c1327414e1eb1562ade8abfede7f`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 53.4 MB (53426463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb38734b87010a77486e57a23a05876bd81d3636d0dc8e0b1794cb9a9a9ad9`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e25dd4e90f4fc5e4eb6cc2e41e3e65e51486a69d8e7bd0de461f4c5e4db1ad`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 40.5 MB (40511442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142127aec3b22b34c28299004fabee9100ff4f610c0f205373e48e976bc0ca43`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-debian`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28-debian` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-oracle`

```console
$ docker pull mysql@sha256:c290ae4835977163f5e64f0097ca8e3e68b7bfe8e1be6eaf868cd2c784f49a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.28-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:597c5419f5b4979ca774c3a08b8cc720d4f6b91b931db53e1cb86e8d0a25762c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132231021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915bc1b56d7faf8dbed03ea6307819c2de218fe65cc4b0f01f1c2ba9c389399`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 02:31:13 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 02:31:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:31:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 02:32:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 02:32:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 02:32:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:32:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 02:32:44 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 02:32:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 02:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 02:32:45 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 02:32:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459aff8953013538dc5161aac0290e8bbe67052969efa2ab421fa3639f61956`  
		Last Modified: Sat, 26 Feb 2022 02:35:11 GMT  
		Size: 3.8 MB (3849261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193d82a8e1cea1608ed4d733010f06e490fd2fc76717106fff8824bc58cc33d1`  
		Last Modified: Sat, 26 Feb 2022 02:35:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed143356aa61b0171a452553374af4991efa3a035ab79617b7836b4bde902906`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0dcca74e88aacab22d3e1eaf2c07b52f21eab21515916480c11764bd982d6c`  
		Last Modified: Sat, 26 Feb 2022 02:35:17 GMT  
		Size: 47.3 MB (47261001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e90b9d1c34c4a1ebe12dc9910794d0a77b03e8ec2cfd3c101896f150d7c46`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e096125d73fe4740b24a4cd94e0d2ae6f171b2f0258bcf07a535419e7f7e9`  
		Last Modified: Sat, 26 Feb 2022 02:35:16 GMT  
		Size: 38.3 MB (38301334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b53604831c3b9b77bdba50ebf896f1a64947ce00f09e60a7bb2a8bc9874623`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 5.0 KB (4953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.28-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e005dcbd8ab96b15fe4937aba1cdac2ee332f9ac64844b43f0682c9e0ecd0dca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140761765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffe8c4711962405da726c2e9b7bd19521b8cb346cdedc97a2d49c093303da4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 16:44:31 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 16:45:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 16:45:13 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 16:45:14 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:45:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 16:45:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:46:02 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 16:46:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 16:46:04 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 16:46:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 16:46:05 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 16:46:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ed278df2509412e7b05f12e7320cb3f2614a831ec1ec894d7d39c9cb0ab6e5`  
		Last Modified: Sat, 26 Feb 2022 16:46:39 GMT  
		Size: 4.0 MB (4005620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93b01f7b04bed4054f1e9ba825f4a4bcb8cbfaaab21ab7e1bc7e4e5facbd34`  
		Last Modified: Sat, 26 Feb 2022 16:46:38 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a0806a1841064be108b7c204ea8cc39462f116525a4f7a044e8056cd9c5851`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc52d9a5079e1a0f43a9bc7f53334d0a9688c1327414e1eb1562ade8abfede7f`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 53.4 MB (53426463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb38734b87010a77486e57a23a05876bd81d3636d0dc8e0b1794cb9a9a9ad9`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e25dd4e90f4fc5e4eb6cc2e41e3e65e51486a69d8e7bd0de461f4c5e4db1ad`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 40.5 MB (40511442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142127aec3b22b34c28299004fabee9100ff4f610c0f205373e48e976bc0ca43`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:6b8987c74b59b635abd3c5772f5ca0aa8cd9e27f08cb1274fcd1f7ba1489132e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:031e723e628c034205236c06cd1db16c30268f658c855cc1e42c1dcd31fdc589
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153973208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97615307ac32ac351df9260ac75dd1217345231a2c9a2c2f791fcd4c37ee2ebe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 13:48:38 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 01 Mar 2022 13:48:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:48:43 GMT
ENV GOSU_VERSION=1.14
# Tue, 01 Mar 2022 13:48:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 01 Mar 2022 13:48:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 01 Mar 2022 13:48:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 13:49:35 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 01 Mar 2022 13:49:35 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Tue, 01 Mar 2022 13:49:35 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 01 Mar 2022 13:49:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 01 Mar 2022 13:49:52 GMT
VOLUME [/var/lib/mysql]
# Tue, 01 Mar 2022 13:49:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 01 Mar 2022 13:49:53 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Tue, 01 Mar 2022 13:49:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 01 Mar 2022 13:49:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 13:49:55 GMT
EXPOSE 3306 33060
# Tue, 01 Mar 2022 13:49:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d733f6778b181d07e9ff21935ae00b45200f293a2039d0fc297849a64a367c14`  
		Last Modified: Tue, 01 Mar 2022 13:51:08 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc7a6c74a0458d6d543c4cfe6db10ee69e16eee46f187be2c97284327862cb2`  
		Last Modified: Tue, 01 Mar 2022 13:51:09 GMT  
		Size: 4.2 MB (4179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4364028a80547cb56664e863ad522f90961befd7c6198545f6961a8a01d8663`  
		Last Modified: Tue, 01 Mar 2022 13:51:06 GMT  
		Size: 1.4 MB (1386644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82887163f0f667b80bdfcbbd52a2c1022fea2d1abc1fdd698fb2cb021d8398d7`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097bfae26e7a301949e03362d9a3ddc221890b14bb30be32b1453a860ebc6d9f`  
		Last Modified: Tue, 01 Mar 2022 13:51:11 GMT  
		Size: 13.4 MB (13438515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b044d6a24fd39387e37c340f6f20c0d36e6560d80dd18be4ac8535faf92846`  
		Last Modified: Tue, 01 Mar 2022 13:51:05 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2978bd4d1242e8fa43c34e203a35aa5dc72d9057b1ee7ee80bfbb29bbc19e5`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bce5cc16774ef0b7cbe16c9586babd91bdf75b14fcbb194daf6d3127fee122`  
		Last Modified: Tue, 01 Mar 2022 13:51:29 GMT  
		Size: 107.8 MB (107804440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907b6d6957603b83f6a8a988e6425af07fc99f73ba02f118441d3eb0e2f3df79`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc290af3c07a4e422007149fc80aaea8100ec69155f2a7571ff43d91b7c454f3`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 5.0 KB (4950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3516da1e765ebf4ab4d80aff2cd302ab6f7f43385051b174934779ff683e737`  
		Last Modified: Tue, 01 Mar 2022 13:51:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c290ae4835977163f5e64f0097ca8e3e68b7bfe8e1be6eaf868cd2c784f49a61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:597c5419f5b4979ca774c3a08b8cc720d4f6b91b931db53e1cb86e8d0a25762c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132231021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6915bc1b56d7faf8dbed03ea6307819c2de218fe65cc4b0f01f1c2ba9c389399`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:b6480acd933244be4e731db5554fd5341361b4d26356e9dea6db584cea3e137c in / 
# Fri, 25 Feb 2022 02:07:20 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 03:31:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 03:31:44 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 03:31:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 02:31:13 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 02:31:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 02:31:49 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:31:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 02:32:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 02:32:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 02:32:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 02:32:43 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 02:32:44 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 02:32:44 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 02:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 02:32:45 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 02:32:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a2af32d411b4106f43f8ff56651eed59979576281483ccfb3b9f4a7cf1f5944b`  
		Last Modified: Fri, 25 Feb 2022 02:08:31 GMT  
		Size: 41.9 MB (41881280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5207ba089c5352dfd5cafa4419213f7e6c2dfb2a3d8301f9911ec66fc683c9`  
		Last Modified: Fri, 25 Feb 2022 03:36:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598adc979ae4bcf156eb841c681302fa8f44b58dea06ce95ccf11afb915fd3c2`  
		Last Modified: Fri, 25 Feb 2022 03:35:58 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3459aff8953013538dc5161aac0290e8bbe67052969efa2ab421fa3639f61956`  
		Last Modified: Sat, 26 Feb 2022 02:35:11 GMT  
		Size: 3.8 MB (3849261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193d82a8e1cea1608ed4d733010f06e490fd2fc76717106fff8824bc58cc33d1`  
		Last Modified: Sat, 26 Feb 2022 02:35:10 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed143356aa61b0171a452553374af4991efa3a035ab79617b7836b4bde902906`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0dcca74e88aacab22d3e1eaf2c07b52f21eab21515916480c11764bd982d6c`  
		Last Modified: Sat, 26 Feb 2022 02:35:17 GMT  
		Size: 47.3 MB (47261001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664e90b9d1c34c4a1ebe12dc9910794d0a77b03e8ec2cfd3c101896f150d7c46`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e096125d73fe4740b24a4cd94e0d2ae6f171b2f0258bcf07a535419e7f7e9`  
		Last Modified: Sat, 26 Feb 2022 02:35:16 GMT  
		Size: 38.3 MB (38301334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b53604831c3b9b77bdba50ebf896f1a64947ce00f09e60a7bb2a8bc9874623`  
		Last Modified: Sat, 26 Feb 2022 02:35:08 GMT  
		Size: 5.0 KB (4953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e005dcbd8ab96b15fe4937aba1cdac2ee332f9ac64844b43f0682c9e0ecd0dca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140761765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffe8c4711962405da726c2e9b7bd19521b8cb346cdedc97a2d49c093303da4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 25 Feb 2022 02:07:20 GMT
ADD file:99a87d6732159802bc46dd7fcfa5c22f7bcb1faacab59f6e5b8c5284bd3ab861 in / 
# Fri, 25 Feb 2022 02:07:21 GMT
CMD ["/bin/bash"]
# Fri, 25 Feb 2022 02:58:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 25 Feb 2022 02:58:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 25 Feb 2022 02:58:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 26 Feb 2022 16:44:31 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		findutils 	; 	microdnf clean all
# Sat, 26 Feb 2022 16:45:12 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 26 Feb 2022 16:45:13 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 26 Feb 2022 16:45:14 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:45:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 26 Feb 2022 16:45:37 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 26 Feb 2022 16:45:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 26 Feb 2022 16:46:02 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 26 Feb 2022 16:46:03 GMT
VOLUME [/var/lib/mysql]
# Sat, 26 Feb 2022 16:46:04 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Sat, 26 Feb 2022 16:46:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 26 Feb 2022 16:46:05 GMT
EXPOSE 3306 33060
# Sat, 26 Feb 2022 16:46:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63ea605e0f838cb587cea4b75125afc43e9d339ddc5233440e9a29b7c5ba12d5`  
		Last Modified: Fri, 25 Feb 2022 02:08:42 GMT  
		Size: 42.0 MB (41951862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8682e43073605675017fa1d3f45abfea0fa0d6b3f0dcc26eb29a4920adc5d49b`  
		Last Modified: Fri, 25 Feb 2022 03:00:57 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8811e76642f83f9e9101fd42b5f55528b93b5e1943f6d61006f71ee6291bcde0`  
		Last Modified: Fri, 25 Feb 2022 03:00:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ed278df2509412e7b05f12e7320cb3f2614a831ec1ec894d7d39c9cb0ab6e5`  
		Last Modified: Sat, 26 Feb 2022 16:46:39 GMT  
		Size: 4.0 MB (4005620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c93b01f7b04bed4054f1e9ba825f4a4bcb8cbfaaab21ab7e1bc7e4e5facbd34`  
		Last Modified: Sat, 26 Feb 2022 16:46:38 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a0806a1841064be108b7c204ea8cc39462f116525a4f7a044e8056cd9c5851`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc52d9a5079e1a0f43a9bc7f53334d0a9688c1327414e1eb1562ade8abfede7f`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 53.4 MB (53426463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efb38734b87010a77486e57a23a05876bd81d3636d0dc8e0b1794cb9a9a9ad9`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e25dd4e90f4fc5e4eb6cc2e41e3e65e51486a69d8e7bd0de461f4c5e4db1ad`  
		Last Modified: Sat, 26 Feb 2022 16:46:43 GMT  
		Size: 40.5 MB (40511442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:142127aec3b22b34c28299004fabee9100ff4f610c0f205373e48e976bc0ca43`  
		Last Modified: Sat, 26 Feb 2022 16:46:36 GMT  
		Size: 5.0 KB (4952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
