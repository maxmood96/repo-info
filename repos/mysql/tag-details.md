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
$ docker pull mysql@sha256:7e99b2b8d5bca914ef31059858210f57b009c40375d647f0d4d65ecd01d6b1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:06c614dfc9720ccc0177acf700d0e0794f0efe3a032e78ea5318c30886ce62c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0961b7de03c7b11afd13fec09d0d30992b6e0b4f947a4aba4273723778ed95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Sat, 28 May 2022 05:33:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:34:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:34:17 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:34:17 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:34:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:34:17 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:34:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe6daf23954caa3d837bbd8317dcde57ad466ad3ca6e0c4b8f0f3c61ee451b`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf426818fd53d690090f3e6029160dec25694793d6b77a52e80ff70d7651e2`  
		Last Modified: Sat, 28 May 2022 05:35:45 GMT  
		Size: 115.7 MB (115675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b838b06054d3f3b54fea8f73531a1908182330b6571c08f5453c78aa879901`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b606c4f93dfd881271b87ffd349ff0467a9fe1354d461f8d1a54934a1457c37`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:7e99b2b8d5bca914ef31059858210f57b009c40375d647f0d4d65ecd01d6b1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:06c614dfc9720ccc0177acf700d0e0794f0efe3a032e78ea5318c30886ce62c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0961b7de03c7b11afd13fec09d0d30992b6e0b4f947a4aba4273723778ed95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Sat, 28 May 2022 05:33:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:34:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:34:17 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:34:17 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:34:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:34:17 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:34:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe6daf23954caa3d837bbd8317dcde57ad466ad3ca6e0c4b8f0f3c61ee451b`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf426818fd53d690090f3e6029160dec25694793d6b77a52e80ff70d7651e2`  
		Last Modified: Sat, 28 May 2022 05:35:45 GMT  
		Size: 115.7 MB (115675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b838b06054d3f3b54fea8f73531a1908182330b6571c08f5453c78aa879901`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b606c4f93dfd881271b87ffd349ff0467a9fe1354d461f8d1a54934a1457c37`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:8d14ae9dc8e1b1c4cbae95d16ec7f01014394fdee514536a6ead00d353c58aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2194c27c2d52ab3df2a9056fb3cf0fa3eb8f88e7d5212bbdcdfc4afe63c698bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126910152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8eb106578751bc1f63e6663e8e08019d56e20e7c02e2fe71cf4d2c540dd07d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 May 2022 18:21:17 GMT
ADD file:60c2a17c0433d95caf7d6bac5520da02174f48bf0c50f6f369b00bf8f9774f82 in / 
# Thu, 19 May 2022 18:21:17 GMT
CMD ["/bin/bash"]
# Thu, 19 May 2022 18:47:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 19 May 2022 18:47:44 GMT
ENV GOSU_VERSION=1.14
# Thu, 19 May 2022 18:47:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 19 May 2022 18:47:58 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 19 May 2022 18:47:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 19 May 2022 18:47:59 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 19 May 2022 18:47:59 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Thu, 19 May 2022 18:47:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 19 May 2022 18:48:13 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 19 May 2022 18:48:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 19 May 2022 18:48:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Thu, 19 May 2022 18:48:32 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 19 May 2022 18:48:33 GMT
VOLUME [/var/lib/mysql]
# Mon, 23 May 2022 23:37:56 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 23 May 2022 23:37:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:37:56 GMT
EXPOSE 3306 33060
# Mon, 23 May 2022 23:37:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f0182e2fe516824cf8f93b207b7c4b65d05c48db476f53312b17b5cd952bfcc3`  
		Last Modified: Thu, 19 May 2022 18:22:04 GMT  
		Size: 48.8 MB (48757934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5e90eb10a94a478f939d07381938536ef8d0e34f1ebf62e9ae46d9f9a1b98`  
		Last Modified: Thu, 19 May 2022 18:49:15 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918efb5a19fdff32ebbd33154bbbd84a4dbffd235322accd6ab8aa71ca2d3bbc`  
		Last Modified: Thu, 19 May 2022 18:49:13 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62093a3d9873d04c95dac16a1f5351ec06126d2b0b2eee3d719a9054f192cd80`  
		Last Modified: Thu, 19 May 2022 18:49:13 GMT  
		Size: 3.8 MB (3760687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50893e22eb52afb36426bb228d1d140d9983f8f5738cd6a138af4732de54ddc0`  
		Last Modified: Thu, 19 May 2022 18:49:12 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5b859cc25c9ac85939eb1e97b5ee0adf65f53b10f4394372726142dda05cac`  
		Last Modified: Thu, 19 May 2022 18:49:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea71ed17aba2bf2c4cccc50c9e2a525dd3073ef1ed8dee89553c7de243265a9`  
		Last Modified: Thu, 19 May 2022 18:49:14 GMT  
		Size: 25.5 MB (25476871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde64eb02cf9d89a916ca0031cdef2c5f77a8437ca8726ff2445924977b24d36`  
		Last Modified: Thu, 19 May 2022 18:49:10 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fd1907b83f9d8971dfeebcbacd4f9009fb58e15722673546f13ec17f617629`  
		Last Modified: Thu, 19 May 2022 18:49:19 GMT  
		Size: 48.0 MB (47974906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8be39ae35ba9bcbfd684644265cb3613a39aec1f11a65ed53f7ced3fd6de0d`  
		Last Modified: Mon, 23 May 2022 23:39:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:7e99b2b8d5bca914ef31059858210f57b009c40375d647f0d4d65ecd01d6b1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:06c614dfc9720ccc0177acf700d0e0794f0efe3a032e78ea5318c30886ce62c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0961b7de03c7b11afd13fec09d0d30992b6e0b4f947a4aba4273723778ed95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Sat, 28 May 2022 05:33:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:34:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:34:17 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:34:17 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:34:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:34:17 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:34:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe6daf23954caa3d837bbd8317dcde57ad466ad3ca6e0c4b8f0f3c61ee451b`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf426818fd53d690090f3e6029160dec25694793d6b77a52e80ff70d7651e2`  
		Last Modified: Sat, 28 May 2022 05:35:45 GMT  
		Size: 115.7 MB (115675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b838b06054d3f3b54fea8f73531a1908182330b6571c08f5453c78aa879901`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b606c4f93dfd881271b87ffd349ff0467a9fe1354d461f8d1a54934a1457c37`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:7e99b2b8d5bca914ef31059858210f57b009c40375d647f0d4d65ecd01d6b1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:06c614dfc9720ccc0177acf700d0e0794f0efe3a032e78ea5318c30886ce62c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0961b7de03c7b11afd13fec09d0d30992b6e0b4f947a4aba4273723778ed95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Sat, 28 May 2022 05:33:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:34:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:34:17 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:34:17 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:34:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:34:17 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:34:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe6daf23954caa3d837bbd8317dcde57ad466ad3ca6e0c4b8f0f3c61ee451b`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf426818fd53d690090f3e6029160dec25694793d6b77a52e80ff70d7651e2`  
		Last Modified: Sat, 28 May 2022 05:35:45 GMT  
		Size: 115.7 MB (115675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b838b06054d3f3b54fea8f73531a1908182330b6571c08f5453c78aa879901`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b606c4f93dfd881271b87ffd349ff0467a9fe1354d461f8d1a54934a1457c37`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:8d14ae9dc8e1b1c4cbae95d16ec7f01014394fdee514536a6ead00d353c58aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2194c27c2d52ab3df2a9056fb3cf0fa3eb8f88e7d5212bbdcdfc4afe63c698bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126910152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8eb106578751bc1f63e6663e8e08019d56e20e7c02e2fe71cf4d2c540dd07d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 May 2022 18:21:17 GMT
ADD file:60c2a17c0433d95caf7d6bac5520da02174f48bf0c50f6f369b00bf8f9774f82 in / 
# Thu, 19 May 2022 18:21:17 GMT
CMD ["/bin/bash"]
# Thu, 19 May 2022 18:47:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 19 May 2022 18:47:44 GMT
ENV GOSU_VERSION=1.14
# Thu, 19 May 2022 18:47:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 19 May 2022 18:47:58 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 19 May 2022 18:47:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 19 May 2022 18:47:59 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 19 May 2022 18:47:59 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Thu, 19 May 2022 18:47:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 19 May 2022 18:48:13 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 19 May 2022 18:48:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 19 May 2022 18:48:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Thu, 19 May 2022 18:48:32 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 19 May 2022 18:48:33 GMT
VOLUME [/var/lib/mysql]
# Mon, 23 May 2022 23:37:56 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 23 May 2022 23:37:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:37:56 GMT
EXPOSE 3306 33060
# Mon, 23 May 2022 23:37:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f0182e2fe516824cf8f93b207b7c4b65d05c48db476f53312b17b5cd952bfcc3`  
		Last Modified: Thu, 19 May 2022 18:22:04 GMT  
		Size: 48.8 MB (48757934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5e90eb10a94a478f939d07381938536ef8d0e34f1ebf62e9ae46d9f9a1b98`  
		Last Modified: Thu, 19 May 2022 18:49:15 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918efb5a19fdff32ebbd33154bbbd84a4dbffd235322accd6ab8aa71ca2d3bbc`  
		Last Modified: Thu, 19 May 2022 18:49:13 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62093a3d9873d04c95dac16a1f5351ec06126d2b0b2eee3d719a9054f192cd80`  
		Last Modified: Thu, 19 May 2022 18:49:13 GMT  
		Size: 3.8 MB (3760687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50893e22eb52afb36426bb228d1d140d9983f8f5738cd6a138af4732de54ddc0`  
		Last Modified: Thu, 19 May 2022 18:49:12 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5b859cc25c9ac85939eb1e97b5ee0adf65f53b10f4394372726142dda05cac`  
		Last Modified: Thu, 19 May 2022 18:49:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea71ed17aba2bf2c4cccc50c9e2a525dd3073ef1ed8dee89553c7de243265a9`  
		Last Modified: Thu, 19 May 2022 18:49:14 GMT  
		Size: 25.5 MB (25476871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde64eb02cf9d89a916ca0031cdef2c5f77a8437ca8726ff2445924977b24d36`  
		Last Modified: Thu, 19 May 2022 18:49:10 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fd1907b83f9d8971dfeebcbacd4f9009fb58e15722673546f13ec17f617629`  
		Last Modified: Thu, 19 May 2022 18:49:19 GMT  
		Size: 48.0 MB (47974906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8be39ae35ba9bcbfd684644265cb3613a39aec1f11a65ed53f7ced3fd6de0d`  
		Last Modified: Mon, 23 May 2022 23:39:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38`

```console
$ docker pull mysql@sha256:7e99b2b8d5bca914ef31059858210f57b009c40375d647f0d4d65ecd01d6b1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38` - linux; amd64

```console
$ docker pull mysql@sha256:06c614dfc9720ccc0177acf700d0e0794f0efe3a032e78ea5318c30886ce62c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0961b7de03c7b11afd13fec09d0d30992b6e0b4f947a4aba4273723778ed95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Sat, 28 May 2022 05:33:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:34:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:34:17 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:34:17 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:34:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:34:17 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:34:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe6daf23954caa3d837bbd8317dcde57ad466ad3ca6e0c4b8f0f3c61ee451b`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf426818fd53d690090f3e6029160dec25694793d6b77a52e80ff70d7651e2`  
		Last Modified: Sat, 28 May 2022 05:35:45 GMT  
		Size: 115.7 MB (115675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b838b06054d3f3b54fea8f73531a1908182330b6571c08f5453c78aa879901`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b606c4f93dfd881271b87ffd349ff0467a9fe1354d461f8d1a54934a1457c37`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-debian`

```console
$ docker pull mysql@sha256:7e99b2b8d5bca914ef31059858210f57b009c40375d647f0d4d65ecd01d6b1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-debian` - linux; amd64

```console
$ docker pull mysql@sha256:06c614dfc9720ccc0177acf700d0e0794f0efe3a032e78ea5318c30886ce62c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162456143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0961b7de03c7b11afd13fec09d0d30992b6e0b4f947a4aba4273723778ed95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 May 2022 05:33:57 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Sat, 28 May 2022 05:33:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:34:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:34:17 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:34:17 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:34:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:34:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:34:17 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:34:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81fe6daf23954caa3d837bbd8317dcde57ad466ad3ca6e0c4b8f0f3c61ee451b`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ccf426818fd53d690090f3e6029160dec25694793d6b77a52e80ff70d7651e2`  
		Last Modified: Sat, 28 May 2022 05:35:45 GMT  
		Size: 115.7 MB (115675662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b838b06054d3f3b54fea8f73531a1908182330b6571c08f5453c78aa879901`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b606c4f93dfd881271b87ffd349ff0467a9fe1354d461f8d1a54934a1457c37`  
		Last Modified: Sat, 28 May 2022 05:35:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-oracle`

```console
$ docker pull mysql@sha256:8d14ae9dc8e1b1c4cbae95d16ec7f01014394fdee514536a6ead00d353c58aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2194c27c2d52ab3df2a9056fb3cf0fa3eb8f88e7d5212bbdcdfc4afe63c698bd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126910152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8eb106578751bc1f63e6663e8e08019d56e20e7c02e2fe71cf4d2c540dd07d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 19 May 2022 18:21:17 GMT
ADD file:60c2a17c0433d95caf7d6bac5520da02174f48bf0c50f6f369b00bf8f9774f82 in / 
# Thu, 19 May 2022 18:21:17 GMT
CMD ["/bin/bash"]
# Thu, 19 May 2022 18:47:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 19 May 2022 18:47:44 GMT
ENV GOSU_VERSION=1.14
# Thu, 19 May 2022 18:47:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 19 May 2022 18:47:58 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 19 May 2022 18:47:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 19 May 2022 18:47:59 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 19 May 2022 18:47:59 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Thu, 19 May 2022 18:47:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 19 May 2022 18:48:13 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 19 May 2022 18:48:14 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 19 May 2022 18:48:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Thu, 19 May 2022 18:48:32 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 19 May 2022 18:48:33 GMT
VOLUME [/var/lib/mysql]
# Mon, 23 May 2022 23:37:56 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 23 May 2022 23:37:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:37:56 GMT
EXPOSE 3306 33060
# Mon, 23 May 2022 23:37:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f0182e2fe516824cf8f93b207b7c4b65d05c48db476f53312b17b5cd952bfcc3`  
		Last Modified: Thu, 19 May 2022 18:22:04 GMT  
		Size: 48.8 MB (48757934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee5e90eb10a94a478f939d07381938536ef8d0e34f1ebf62e9ae46d9f9a1b98`  
		Last Modified: Thu, 19 May 2022 18:49:15 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918efb5a19fdff32ebbd33154bbbd84a4dbffd235322accd6ab8aa71ca2d3bbc`  
		Last Modified: Thu, 19 May 2022 18:49:13 GMT  
		Size: 930.2 KB (930229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62093a3d9873d04c95dac16a1f5351ec06126d2b0b2eee3d719a9054f192cd80`  
		Last Modified: Thu, 19 May 2022 18:49:13 GMT  
		Size: 3.8 MB (3760687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50893e22eb52afb36426bb228d1d140d9983f8f5738cd6a138af4732de54ddc0`  
		Last Modified: Thu, 19 May 2022 18:49:12 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5b859cc25c9ac85939eb1e97b5ee0adf65f53b10f4394372726142dda05cac`  
		Last Modified: Thu, 19 May 2022 18:49:10 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea71ed17aba2bf2c4cccc50c9e2a525dd3073ef1ed8dee89553c7de243265a9`  
		Last Modified: Thu, 19 May 2022 18:49:14 GMT  
		Size: 25.5 MB (25476871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde64eb02cf9d89a916ca0031cdef2c5f77a8437ca8726ff2445924977b24d36`  
		Last Modified: Thu, 19 May 2022 18:49:10 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fd1907b83f9d8971dfeebcbacd4f9009fb58e15722673546f13ec17f617629`  
		Last Modified: Thu, 19 May 2022 18:49:19 GMT  
		Size: 48.0 MB (47974906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8be39ae35ba9bcbfd684644265cb3613a39aec1f11a65ed53f7ced3fd6de0d`  
		Last Modified: Mon, 23 May 2022 23:39:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:b3c6816133f60df2c3721361b343308cfcae82b6e29d7e7c3f26388f608aa5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1fe1c2a3ee560d25f4b30139fb2d1859803e9dbd00cd42da7eaff6351993bea9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131645654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6664c768aba77eb6ce3f153206310293143f0d37113badc147d9f014d642bbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:41:42 GMT
ADD file:bbaf69bdffd0f506e447fbc52dca450a8966d950b8fa9aebd3a1bd5bd98f8b28 in / 
# Tue, 17 May 2022 22:41:42 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:10:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:10:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:10:42 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:10:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:11:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:11:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:11:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:11:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 23 May 2022 23:37:48 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 23 May 2022 23:37:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:37:49 GMT
EXPOSE 3306 33060
# Mon, 23 May 2022 23:37:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:90a00d516db16c568d3da8e0a7a5a78fa6fef5a39f3d688f831d254b77791565`  
		Last Modified: Tue, 17 May 2022 22:42:38 GMT  
		Size: 39.2 MB (39220501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec380701a2aab4173cf5a055f74c99227ae7c4fddf87803362ac984b3cbfa8ef`  
		Last Modified: Tue, 17 May 2022 23:12:28 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c639d40d7782dd181799bc0e030b8269850fa3ad5bb3bbdeb511ea1c782e33c6`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2e5b74a30bdb2c55f39992bb2ae64d81e0b737541ad217123841bd41bda53`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 4.5 MB (4536235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bce381d3796288927fc508cdc11bdca5a6c3d0dca64c13c2fc51035851ab296`  
		Last Modified: Tue, 17 May 2022 23:12:25 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e5b79d5c8e16d050f0a02cf0d1214f77e2a4e272b88299488b054d7c95f711`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858b3b51a1f97d5a72794a4cde78e9130b00620b922db41c2bc3ac79a55e8f58`  
		Last Modified: Tue, 17 May 2022 23:12:30 GMT  
		Size: 47.2 MB (47242274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2171f9f10a16c77335db5f61043051469c24c5080d9f80f87d5778f96b2bbc1c`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0fa78a73ac6ced6b681d9255b9345f3f8ab04aec0f08aa1fa0533dc37f055e`  
		Last Modified: Tue, 17 May 2022 23:12:31 GMT  
		Size: 39.7 MB (39708291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf8a962e18cf2513ce6e3370ba61fea0d9bb052a28a2c55aa0550cd0f11f125`  
		Last Modified: Mon, 23 May 2022 23:38:23 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:afc6503454a50cb7c6e0f15679f78f28a69c64ef9c13ab250b03868327d22964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138552519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d55b4cff902af2f58c08c9cb28ec9ec7ea498734d9e2b29b8211cab1399a0e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:09:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:09:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:09:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:09:26 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:09:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:09:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:09:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:09:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:09:56 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:10:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 May 2022 00:06:13 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 24 May 2022 00:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 00:06:14 GMT
EXPOSE 3306 33060
# Tue, 24 May 2022 00:06:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db29b0b5a771d422a5f85337ad705ae13b90861da7c4ae8a2d3020b42d0d4892`  
		Last Modified: Tue, 17 May 2022 23:10:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3855c850e40abd0de4601587237af854d07522e10e3bb9ee0e8c66b40ae49911`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a57b88152cf6fe699baa66b60fd8c2f07daef18b1931fae4dfc7c92d5d48ae5`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 4.3 MB (4342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac9375febdd7998b9cc129e95d554b5b9d024f9ecf3053d3e7156a31279923f`  
		Last Modified: Tue, 17 May 2022 23:10:55 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199a4e720f0e82bafd1852cdf3a57870a449bcb60c197daf349869c4d332bb3`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebac76248d98ab600a56814d6569f0e4f4799aceb8bc8d8999f1b88938873e6`  
		Last Modified: Tue, 17 May 2022 23:11:00 GMT  
		Size: 53.3 MB (53299522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6eb52402d98a9e93f419ca2bc248862a3b2b7e0c0fc6800cadd1622dc46e9`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5d943dd79edceeeeb858d6e3e80aa85a14a1f402e70156d2fd61d6e5f60a4`  
		Last Modified: Tue, 17 May 2022 23:11:01 GMT  
		Size: 42.0 MB (42030739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd8fe16828e527c9aa77b2da2af6a7ac4b797b59113d833c84b4400434b2012`  
		Last Modified: Tue, 24 May 2022 00:06:32 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:b3c6816133f60df2c3721361b343308cfcae82b6e29d7e7c3f26388f608aa5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1fe1c2a3ee560d25f4b30139fb2d1859803e9dbd00cd42da7eaff6351993bea9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131645654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6664c768aba77eb6ce3f153206310293143f0d37113badc147d9f014d642bbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:41:42 GMT
ADD file:bbaf69bdffd0f506e447fbc52dca450a8966d950b8fa9aebd3a1bd5bd98f8b28 in / 
# Tue, 17 May 2022 22:41:42 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:10:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:10:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:10:42 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:10:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:11:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:11:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:11:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:11:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 23 May 2022 23:37:48 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 23 May 2022 23:37:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:37:49 GMT
EXPOSE 3306 33060
# Mon, 23 May 2022 23:37:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:90a00d516db16c568d3da8e0a7a5a78fa6fef5a39f3d688f831d254b77791565`  
		Last Modified: Tue, 17 May 2022 22:42:38 GMT  
		Size: 39.2 MB (39220501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec380701a2aab4173cf5a055f74c99227ae7c4fddf87803362ac984b3cbfa8ef`  
		Last Modified: Tue, 17 May 2022 23:12:28 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c639d40d7782dd181799bc0e030b8269850fa3ad5bb3bbdeb511ea1c782e33c6`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2e5b74a30bdb2c55f39992bb2ae64d81e0b737541ad217123841bd41bda53`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 4.5 MB (4536235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bce381d3796288927fc508cdc11bdca5a6c3d0dca64c13c2fc51035851ab296`  
		Last Modified: Tue, 17 May 2022 23:12:25 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e5b79d5c8e16d050f0a02cf0d1214f77e2a4e272b88299488b054d7c95f711`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858b3b51a1f97d5a72794a4cde78e9130b00620b922db41c2bc3ac79a55e8f58`  
		Last Modified: Tue, 17 May 2022 23:12:30 GMT  
		Size: 47.2 MB (47242274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2171f9f10a16c77335db5f61043051469c24c5080d9f80f87d5778f96b2bbc1c`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0fa78a73ac6ced6b681d9255b9345f3f8ab04aec0f08aa1fa0533dc37f055e`  
		Last Modified: Tue, 17 May 2022 23:12:31 GMT  
		Size: 39.7 MB (39708291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf8a962e18cf2513ce6e3370ba61fea0d9bb052a28a2c55aa0550cd0f11f125`  
		Last Modified: Mon, 23 May 2022 23:38:23 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:afc6503454a50cb7c6e0f15679f78f28a69c64ef9c13ab250b03868327d22964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138552519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d55b4cff902af2f58c08c9cb28ec9ec7ea498734d9e2b29b8211cab1399a0e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:09:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:09:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:09:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:09:26 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:09:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:09:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:09:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:09:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:09:56 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:10:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 May 2022 00:06:13 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 24 May 2022 00:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 00:06:14 GMT
EXPOSE 3306 33060
# Tue, 24 May 2022 00:06:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db29b0b5a771d422a5f85337ad705ae13b90861da7c4ae8a2d3020b42d0d4892`  
		Last Modified: Tue, 17 May 2022 23:10:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3855c850e40abd0de4601587237af854d07522e10e3bb9ee0e8c66b40ae49911`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a57b88152cf6fe699baa66b60fd8c2f07daef18b1931fae4dfc7c92d5d48ae5`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 4.3 MB (4342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac9375febdd7998b9cc129e95d554b5b9d024f9ecf3053d3e7156a31279923f`  
		Last Modified: Tue, 17 May 2022 23:10:55 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199a4e720f0e82bafd1852cdf3a57870a449bcb60c197daf349869c4d332bb3`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebac76248d98ab600a56814d6569f0e4f4799aceb8bc8d8999f1b88938873e6`  
		Last Modified: Tue, 17 May 2022 23:11:00 GMT  
		Size: 53.3 MB (53299522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6eb52402d98a9e93f419ca2bc248862a3b2b7e0c0fc6800cadd1622dc46e9`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5d943dd79edceeeeb858d6e3e80aa85a14a1f402e70156d2fd61d6e5f60a4`  
		Last Modified: Tue, 17 May 2022 23:11:01 GMT  
		Size: 42.0 MB (42030739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd8fe16828e527c9aa77b2da2af6a7ac4b797b59113d833c84b4400434b2012`  
		Last Modified: Tue, 24 May 2022 00:06:32 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-debian`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-oracle`

```console
$ docker pull mysql@sha256:b3c6816133f60df2c3721361b343308cfcae82b6e29d7e7c3f26388f608aa5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.29-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1fe1c2a3ee560d25f4b30139fb2d1859803e9dbd00cd42da7eaff6351993bea9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131645654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6664c768aba77eb6ce3f153206310293143f0d37113badc147d9f014d642bbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:41:42 GMT
ADD file:bbaf69bdffd0f506e447fbc52dca450a8966d950b8fa9aebd3a1bd5bd98f8b28 in / 
# Tue, 17 May 2022 22:41:42 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:10:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:10:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:10:42 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:10:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:11:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:11:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:11:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:11:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 23 May 2022 23:37:48 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 23 May 2022 23:37:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:37:49 GMT
EXPOSE 3306 33060
# Mon, 23 May 2022 23:37:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:90a00d516db16c568d3da8e0a7a5a78fa6fef5a39f3d688f831d254b77791565`  
		Last Modified: Tue, 17 May 2022 22:42:38 GMT  
		Size: 39.2 MB (39220501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec380701a2aab4173cf5a055f74c99227ae7c4fddf87803362ac984b3cbfa8ef`  
		Last Modified: Tue, 17 May 2022 23:12:28 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c639d40d7782dd181799bc0e030b8269850fa3ad5bb3bbdeb511ea1c782e33c6`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2e5b74a30bdb2c55f39992bb2ae64d81e0b737541ad217123841bd41bda53`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 4.5 MB (4536235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bce381d3796288927fc508cdc11bdca5a6c3d0dca64c13c2fc51035851ab296`  
		Last Modified: Tue, 17 May 2022 23:12:25 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e5b79d5c8e16d050f0a02cf0d1214f77e2a4e272b88299488b054d7c95f711`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858b3b51a1f97d5a72794a4cde78e9130b00620b922db41c2bc3ac79a55e8f58`  
		Last Modified: Tue, 17 May 2022 23:12:30 GMT  
		Size: 47.2 MB (47242274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2171f9f10a16c77335db5f61043051469c24c5080d9f80f87d5778f96b2bbc1c`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0fa78a73ac6ced6b681d9255b9345f3f8ab04aec0f08aa1fa0533dc37f055e`  
		Last Modified: Tue, 17 May 2022 23:12:31 GMT  
		Size: 39.7 MB (39708291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf8a962e18cf2513ce6e3370ba61fea0d9bb052a28a2c55aa0550cd0f11f125`  
		Last Modified: Mon, 23 May 2022 23:38:23 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.29-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:afc6503454a50cb7c6e0f15679f78f28a69c64ef9c13ab250b03868327d22964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138552519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d55b4cff902af2f58c08c9cb28ec9ec7ea498734d9e2b29b8211cab1399a0e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:09:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:09:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:09:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:09:26 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:09:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:09:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:09:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:09:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:09:56 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:10:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 May 2022 00:06:13 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 24 May 2022 00:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 00:06:14 GMT
EXPOSE 3306 33060
# Tue, 24 May 2022 00:06:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db29b0b5a771d422a5f85337ad705ae13b90861da7c4ae8a2d3020b42d0d4892`  
		Last Modified: Tue, 17 May 2022 23:10:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3855c850e40abd0de4601587237af854d07522e10e3bb9ee0e8c66b40ae49911`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a57b88152cf6fe699baa66b60fd8c2f07daef18b1931fae4dfc7c92d5d48ae5`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 4.3 MB (4342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac9375febdd7998b9cc129e95d554b5b9d024f9ecf3053d3e7156a31279923f`  
		Last Modified: Tue, 17 May 2022 23:10:55 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199a4e720f0e82bafd1852cdf3a57870a449bcb60c197daf349869c4d332bb3`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebac76248d98ab600a56814d6569f0e4f4799aceb8bc8d8999f1b88938873e6`  
		Last Modified: Tue, 17 May 2022 23:11:00 GMT  
		Size: 53.3 MB (53299522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6eb52402d98a9e93f419ca2bc248862a3b2b7e0c0fc6800cadd1622dc46e9`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5d943dd79edceeeeb858d6e3e80aa85a14a1f402e70156d2fd61d6e5f60a4`  
		Last Modified: Tue, 17 May 2022 23:11:01 GMT  
		Size: 42.0 MB (42030739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd8fe16828e527c9aa77b2da2af6a7ac4b797b59113d833c84b4400434b2012`  
		Last Modified: Tue, 24 May 2022 00:06:32 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:b3c6816133f60df2c3721361b343308cfcae82b6e29d7e7c3f26388f608aa5cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1fe1c2a3ee560d25f4b30139fb2d1859803e9dbd00cd42da7eaff6351993bea9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131645654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6664c768aba77eb6ce3f153206310293143f0d37113badc147d9f014d642bbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:41:42 GMT
ADD file:bbaf69bdffd0f506e447fbc52dca450a8966d950b8fa9aebd3a1bd5bd98f8b28 in / 
# Tue, 17 May 2022 22:41:42 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:10:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:10:18 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:10:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:10:42 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:10:43 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:10:43 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:11:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:11:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:11:11 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:11:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:11:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 23 May 2022 23:37:48 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 23 May 2022 23:37:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:37:49 GMT
EXPOSE 3306 33060
# Mon, 23 May 2022 23:37:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:90a00d516db16c568d3da8e0a7a5a78fa6fef5a39f3d688f831d254b77791565`  
		Last Modified: Tue, 17 May 2022 22:42:38 GMT  
		Size: 39.2 MB (39220501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec380701a2aab4173cf5a055f74c99227ae7c4fddf87803362ac984b3cbfa8ef`  
		Last Modified: Tue, 17 May 2022 23:12:28 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c639d40d7782dd181799bc0e030b8269850fa3ad5bb3bbdeb511ea1c782e33c6`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 928.8 KB (928834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba2e5b74a30bdb2c55f39992bb2ae64d81e0b737541ad217123841bd41bda53`  
		Last Modified: Tue, 17 May 2022 23:12:26 GMT  
		Size: 4.5 MB (4536235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bce381d3796288927fc508cdc11bdca5a6c3d0dca64c13c2fc51035851ab296`  
		Last Modified: Tue, 17 May 2022 23:12:25 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e5b79d5c8e16d050f0a02cf0d1214f77e2a4e272b88299488b054d7c95f711`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858b3b51a1f97d5a72794a4cde78e9130b00620b922db41c2bc3ac79a55e8f58`  
		Last Modified: Tue, 17 May 2022 23:12:30 GMT  
		Size: 47.2 MB (47242274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2171f9f10a16c77335db5f61043051469c24c5080d9f80f87d5778f96b2bbc1c`  
		Last Modified: Tue, 17 May 2022 23:12:23 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0fa78a73ac6ced6b681d9255b9345f3f8ab04aec0f08aa1fa0533dc37f055e`  
		Last Modified: Tue, 17 May 2022 23:12:31 GMT  
		Size: 39.7 MB (39708291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf8a962e18cf2513ce6e3370ba61fea0d9bb052a28a2c55aa0550cd0f11f125`  
		Last Modified: Mon, 23 May 2022 23:38:23 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:afc6503454a50cb7c6e0f15679f78f28a69c64ef9c13ab250b03868327d22964
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138552519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d55b4cff902af2f58c08c9cb28ec9ec7ea498734d9e2b29b8211cab1399a0e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 May 2022 22:52:38 GMT
ADD file:263fe8ce0663428b324fa2909814084a77bf17118d772058d41546b804a4b968 in / 
# Tue, 17 May 2022 22:52:39 GMT
CMD ["/bin/bash"]
# Tue, 17 May 2022 23:09:01 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 17 May 2022 23:09:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 17 May 2022 23:09:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 May 2022 23:09:26 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 17 May 2022 23:09:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 17 May 2022 23:09:29 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 May 2022 23:09:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:09:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 17 May 2022 23:09:55 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 May 2022 23:09:56 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 17 May 2022 23:10:23 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 May 2022 23:10:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 24 May 2022 00:06:13 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 24 May 2022 00:06:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 May 2022 00:06:14 GMT
EXPOSE 3306 33060
# Tue, 24 May 2022 00:06:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0dbddf5847a3e154a061766ddebe6a3cae471c97cabb3be2871f6d91f265d137`  
		Last Modified: Tue, 17 May 2022 22:53:43 GMT  
		Size: 38.0 MB (38012703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db29b0b5a771d422a5f85337ad705ae13b90861da7c4ae8a2d3020b42d0d4892`  
		Last Modified: Tue, 17 May 2022 23:10:58 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3855c850e40abd0de4601587237af854d07522e10e3bb9ee0e8c66b40ae49911`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a57b88152cf6fe699baa66b60fd8c2f07daef18b1931fae4dfc7c92d5d48ae5`  
		Last Modified: Tue, 17 May 2022 23:10:56 GMT  
		Size: 4.3 MB (4342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ac9375febdd7998b9cc129e95d554b5b9d024f9ecf3053d3e7156a31279923f`  
		Last Modified: Tue, 17 May 2022 23:10:55 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a199a4e720f0e82bafd1852cdf3a57870a449bcb60c197daf349869c4d332bb3`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebac76248d98ab600a56814d6569f0e4f4799aceb8bc8d8999f1b88938873e6`  
		Last Modified: Tue, 17 May 2022 23:11:00 GMT  
		Size: 53.3 MB (53299522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b6eb52402d98a9e93f419ca2bc248862a3b2b7e0c0fc6800cadd1622dc46e9`  
		Last Modified: Tue, 17 May 2022 23:10:53 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5d943dd79edceeeeb858d6e3e80aa85a14a1f402e70156d2fd61d6e5f60a4`  
		Last Modified: Tue, 17 May 2022 23:11:01 GMT  
		Size: 42.0 MB (42030739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd8fe16828e527c9aa77b2da2af6a7ac4b797b59113d833c84b4400434b2012`  
		Last Modified: Tue, 24 May 2022 00:06:32 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
