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
$ docker pull mysql@sha256:c8f68301981a7224cc9c063fc7a97b6ef13cfc4142b4871d1a35c95777ce96f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:cac49b06d95908bde09e2dcdadb4fa915c3fb3b0228e4e79e44f67b4024eb571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05311a87aeb4d7f98b2726c39d4d29d6a174d20953a6d1ceaa236bfa177f5fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Mar 2022 08:06:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:53 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:54 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f242378e320c364d16b6d056493d7a6d02ccb0d0214cd43a092c09c2d196a89`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65503c01868a3fb0c4046bd568e0753952da09a77ee7b6babd5adf12c762ce`  
		Last Modified: Fri, 18 Mar 2022 08:09:14 GMT  
		Size: 108.6 MB (108637241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8944d50437c0d3db8b41c6f67af3c5a2fabccea9da92b293f4bbff80e5ca95`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597d59a9a4245232eb602d93945953ad5217c782e5f3f62b4501905e68d54fdf`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:c8f68301981a7224cc9c063fc7a97b6ef13cfc4142b4871d1a35c95777ce96f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cac49b06d95908bde09e2dcdadb4fa915c3fb3b0228e4e79e44f67b4024eb571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05311a87aeb4d7f98b2726c39d4d29d6a174d20953a6d1ceaa236bfa177f5fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Mar 2022 08:06:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:53 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:54 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f242378e320c364d16b6d056493d7a6d02ccb0d0214cd43a092c09c2d196a89`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65503c01868a3fb0c4046bd568e0753952da09a77ee7b6babd5adf12c762ce`  
		Last Modified: Fri, 18 Mar 2022 08:09:14 GMT  
		Size: 108.6 MB (108637241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8944d50437c0d3db8b41c6f67af3c5a2fabccea9da92b293f4bbff80e5ca95`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597d59a9a4245232eb602d93945953ad5217c782e5f3f62b4501905e68d54fdf`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:6a7a8a0c15fa4ca0d9ec85ac3fda70b4749e52fd13c9ca4d5eb0d16efc192e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:847a9c4e83c6bd9fe737e8fb841a2d6197d1407a4657ddb810060a9fff475e76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63e577980bf587f2bafeea4ae79d9eb41c5744cde8f9d24501a7c3a806a23da`
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
# Tue, 08 Mar 2022 19:26:31 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 08 Mar 2022 19:27:03 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Tue, 08 Mar 2022 19:27:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:27:18 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:27:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:27:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Tue, 08 Mar 2022 19:27:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:27:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:27:38 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:27:38 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:27:38 GMT
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
	-	`sha256:93b5fb768db2157c6bdb3a1bcac58e3652bf1543d39f8a81f3ee8be220b3a712`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 3.7 MB (3708422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd86b448d395b76436c8bbfc3b07df034056a757f7420243eb4e4c8783d9503`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856e87d733fdb342899ec85fff5eb1f64b798a865fa1cda8a2aea57ec9c6f31`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78d167e47009381ea4d0fe0033d991f03d879159801424084ffca52ed2a075`  
		Last Modified: Tue, 08 Mar 2022 19:29:50 GMT  
		Size: 25.4 MB (25445899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23017b8e617195316dee8808ceb16ecb9c4e1da4e8230a88af69a9070c077f`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e418ba1e823bddac09c2b166a2d7cbcc06166878249d85ad07119637d8d4a`  
		Last Modified: Tue, 08 Mar 2022 19:29:54 GMT  
		Size: 46.4 MB (46354930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d661b191f612f8741ee6366a28d4f6231833fed59ccf3b145a95c68fd49bcfbf`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:c8f68301981a7224cc9c063fc7a97b6ef13cfc4142b4871d1a35c95777ce96f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:cac49b06d95908bde09e2dcdadb4fa915c3fb3b0228e4e79e44f67b4024eb571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05311a87aeb4d7f98b2726c39d4d29d6a174d20953a6d1ceaa236bfa177f5fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Mar 2022 08:06:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:53 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:54 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f242378e320c364d16b6d056493d7a6d02ccb0d0214cd43a092c09c2d196a89`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65503c01868a3fb0c4046bd568e0753952da09a77ee7b6babd5adf12c762ce`  
		Last Modified: Fri, 18 Mar 2022 08:09:14 GMT  
		Size: 108.6 MB (108637241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8944d50437c0d3db8b41c6f67af3c5a2fabccea9da92b293f4bbff80e5ca95`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597d59a9a4245232eb602d93945953ad5217c782e5f3f62b4501905e68d54fdf`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:c8f68301981a7224cc9c063fc7a97b6ef13cfc4142b4871d1a35c95777ce96f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cac49b06d95908bde09e2dcdadb4fa915c3fb3b0228e4e79e44f67b4024eb571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05311a87aeb4d7f98b2726c39d4d29d6a174d20953a6d1ceaa236bfa177f5fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Mar 2022 08:06:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:53 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:54 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f242378e320c364d16b6d056493d7a6d02ccb0d0214cd43a092c09c2d196a89`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65503c01868a3fb0c4046bd568e0753952da09a77ee7b6babd5adf12c762ce`  
		Last Modified: Fri, 18 Mar 2022 08:09:14 GMT  
		Size: 108.6 MB (108637241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8944d50437c0d3db8b41c6f67af3c5a2fabccea9da92b293f4bbff80e5ca95`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597d59a9a4245232eb602d93945953ad5217c782e5f3f62b4501905e68d54fdf`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:6a7a8a0c15fa4ca0d9ec85ac3fda70b4749e52fd13c9ca4d5eb0d16efc192e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:847a9c4e83c6bd9fe737e8fb841a2d6197d1407a4657ddb810060a9fff475e76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63e577980bf587f2bafeea4ae79d9eb41c5744cde8f9d24501a7c3a806a23da`
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
# Tue, 08 Mar 2022 19:26:31 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 08 Mar 2022 19:27:03 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Tue, 08 Mar 2022 19:27:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:27:18 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:27:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:27:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Tue, 08 Mar 2022 19:27:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:27:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:27:38 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:27:38 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:27:38 GMT
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
	-	`sha256:93b5fb768db2157c6bdb3a1bcac58e3652bf1543d39f8a81f3ee8be220b3a712`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 3.7 MB (3708422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd86b448d395b76436c8bbfc3b07df034056a757f7420243eb4e4c8783d9503`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856e87d733fdb342899ec85fff5eb1f64b798a865fa1cda8a2aea57ec9c6f31`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78d167e47009381ea4d0fe0033d991f03d879159801424084ffca52ed2a075`  
		Last Modified: Tue, 08 Mar 2022 19:29:50 GMT  
		Size: 25.4 MB (25445899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23017b8e617195316dee8808ceb16ecb9c4e1da4e8230a88af69a9070c077f`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e418ba1e823bddac09c2b166a2d7cbcc06166878249d85ad07119637d8d4a`  
		Last Modified: Tue, 08 Mar 2022 19:29:54 GMT  
		Size: 46.4 MB (46354930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d661b191f612f8741ee6366a28d4f6231833fed59ccf3b145a95c68fd49bcfbf`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37`

```console
$ docker pull mysql@sha256:c8f68301981a7224cc9c063fc7a97b6ef13cfc4142b4871d1a35c95777ce96f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37` - linux; amd64

```console
$ docker pull mysql@sha256:cac49b06d95908bde09e2dcdadb4fa915c3fb3b0228e4e79e44f67b4024eb571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05311a87aeb4d7f98b2726c39d4d29d6a174d20953a6d1ceaa236bfa177f5fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Mar 2022 08:06:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:53 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:54 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f242378e320c364d16b6d056493d7a6d02ccb0d0214cd43a092c09c2d196a89`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65503c01868a3fb0c4046bd568e0753952da09a77ee7b6babd5adf12c762ce`  
		Last Modified: Fri, 18 Mar 2022 08:09:14 GMT  
		Size: 108.6 MB (108637241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8944d50437c0d3db8b41c6f67af3c5a2fabccea9da92b293f4bbff80e5ca95`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597d59a9a4245232eb602d93945953ad5217c782e5f3f62b4501905e68d54fdf`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-debian`

```console
$ docker pull mysql@sha256:c8f68301981a7224cc9c063fc7a97b6ef13cfc4142b4871d1a35c95777ce96f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cac49b06d95908bde09e2dcdadb4fa915c3fb3b0228e4e79e44f67b4024eb571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155419411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05311a87aeb4d7f98b2726c39d4d29d6a174d20953a6d1ceaa236bfa177f5fb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Mar 2022 08:06:24 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Mar 2022 08:06:25 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:53 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:53 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:54 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f242378e320c364d16b6d056493d7a6d02ccb0d0214cd43a092c09c2d196a89`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc65503c01868a3fb0c4046bd568e0753952da09a77ee7b6babd5adf12c762ce`  
		Last Modified: Fri, 18 Mar 2022 08:09:14 GMT  
		Size: 108.6 MB (108637241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8944d50437c0d3db8b41c6f67af3c5a2fabccea9da92b293f4bbff80e5ca95`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 5.1 KB (5138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597d59a9a4245232eb602d93945953ad5217c782e5f3f62b4501905e68d54fdf`  
		Last Modified: Fri, 18 Mar 2022 08:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-oracle`

```console
$ docker pull mysql@sha256:6a7a8a0c15fa4ca0d9ec85ac3fda70b4749e52fd13c9ca4d5eb0d16efc192e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:847a9c4e83c6bd9fe737e8fb841a2d6197d1407a4657ddb810060a9fff475e76
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124779861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63e577980bf587f2bafeea4ae79d9eb41c5744cde8f9d24501a7c3a806a23da`
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
# Tue, 08 Mar 2022 19:26:31 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 08 Mar 2022 19:27:03 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 08 Mar 2022 19:27:03 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Tue, 08 Mar 2022 19:27:04 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 08 Mar 2022 19:27:18 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 08 Mar 2022 19:27:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 08 Mar 2022 19:27:19 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Tue, 08 Mar 2022 19:27:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 08 Mar 2022 19:27:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 08 Mar 2022 19:27:38 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Tue, 08 Mar 2022 19:27:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Mar 2022 19:27:38 GMT
EXPOSE 3306 33060
# Tue, 08 Mar 2022 19:27:38 GMT
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
	-	`sha256:93b5fb768db2157c6bdb3a1bcac58e3652bf1543d39f8a81f3ee8be220b3a712`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 3.7 MB (3708422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd86b448d395b76436c8bbfc3b07df034056a757f7420243eb4e4c8783d9503`  
		Last Modified: Tue, 08 Mar 2022 19:29:48 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856e87d733fdb342899ec85fff5eb1f64b798a865fa1cda8a2aea57ec9c6f31`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af78d167e47009381ea4d0fe0033d991f03d879159801424084ffca52ed2a075`  
		Last Modified: Tue, 08 Mar 2022 19:29:50 GMT  
		Size: 25.4 MB (25445899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f23017b8e617195316dee8808ceb16ecb9c4e1da4e8230a88af69a9070c077f`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3e418ba1e823bddac09c2b166a2d7cbcc06166878249d85ad07119637d8d4a`  
		Last Modified: Tue, 08 Mar 2022 19:29:54 GMT  
		Size: 46.4 MB (46354930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d661b191f612f8741ee6366a28d4f6231833fed59ccf3b145a95c68fd49bcfbf`  
		Last Modified: Tue, 08 Mar 2022 19:29:45 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:8c2d1f30f6734998339eb461ba194daf2e305626707d89e1eb59ef8e23f53b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7e0deebd9fdf8e46d830911a8c8975a00462147f7d923d7aa7773221eafe5534
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133155232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fb8170f15f6d079a63ed552de428861e093873629a97b5cde83ddf86af5d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 08:02:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:02:48 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:02:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:03:25 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 18 Mar 2022 08:04:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Mar 2022 08:04:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Mar 2022 08:04:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Mar 2022 08:04:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:57 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Mar 2022 08:04:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:04:58 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:04:58 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:04:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1824cb7e97fbcfc5c6ffea667f8e19cee765d015fef1b8ad70f96252d9713c95`  
		Last Modified: Fri, 18 Mar 2022 05:24:44 GMT  
		Size: 42.1 MB (42110196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5603b74046dbdf928d0641abd36690bf5ef09bec61a2131c3ec7eb4b4c6d8ba4`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c5d7fe8298ed20bcb5c7adbbe025eef7a9de9e5b1e3447936ed9d02b09b7f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc1f1a8427b3e502f4f25dd7acf037e2a2d35927b3201d2711442516c32591b`  
		Last Modified: Fri, 18 Mar 2022 08:07:32 GMT  
		Size: 4.6 MB (4552961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c348d46c25eeb80c794020883a39367c3db1dae41fc9a79aa6fda96d43a51d`  
		Last Modified: Fri, 18 Mar 2022 08:07:31 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2658193beeb76b4b398b4ee7ecc71ebfd580ecf8925d131c8e84598f7c3182`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3694176cd71ffaa30adad12882db7b497d0e83d860f4cbfbdf559213d1fcbb1b`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 47.3 MB (47269558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32d4e62ce97c09e1c91dcf712a5bec3c227e2edcbbc4947ffaf2a7f7acddfb4`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3b55b1e47e4fb94d7b16d8d2d6c298bf1b155b21feed7e8eb3b50060ce91fd`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 38.3 MB (38284179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b3ad406f04dc3a6b8a318c6bf53f8868d1b65941fd2aaf608d5e9a9f4dc33e`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9b456391b4bb798292b6a959f0d3a992911fc1f9c21cb1bee563096d9015f6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141172027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b353a72fcab60e6c13412fdafe5840a37e7dad38f5c36f7374eff8b8321151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:35:35 GMT
ADD file:b16af05882bd38ac02b1f1cba2cc7e80bfbe467ce57f3cf35f1f5a551cee90fa in / 
# Fri, 18 Mar 2022 00:35:36 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 14:48:31 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 14:48:32 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 14:48:35 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 14:49:02 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 19 Mar 2022 14:49:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 19 Mar 2022 14:49:47 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 19 Mar 2022 14:49:48 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:49:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 19 Mar 2022 14:50:17 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:50:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 19 Mar 2022 14:50:46 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 14:50:48 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Sat, 19 Mar 2022 14:50:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 14:50:49 GMT
EXPOSE 3306 33060
# Sat, 19 Mar 2022 14:50:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f8e506fd7c6683f24250871efec36e3fe21cc71090a2f5c59dccdcdfeed2311`  
		Last Modified: Fri, 18 Mar 2022 00:36:38 GMT  
		Size: 42.0 MB (42017883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2e303329ed7fcb9aeb4e6a5e5e8ff70c5ecaca6b4004efe7c5538f98ae073e`  
		Last Modified: Sat, 19 Mar 2022 14:51:14 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43a54926eb5a7901c559b6766eb23666ade02e931708faf2888edadac9e1851`  
		Last Modified: Sat, 19 Mar 2022 14:51:13 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0039e24d8493013955f1061869d44fbdb472434d801986ac8140f0b1846bf4a`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 4.4 MB (4376516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d112a79f85ef077e50966e6ff296393952c4e854cabca838a2ae8ea52346dd`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a816874cae3d0e7af62a465c20b10528a92dedfae97f28912f66a1e05d2eb35`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf3e7c1e5610eed17336f2c459440bddfc67726e3c7fb87fafa6d6b69621d5`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 53.4 MB (53429849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2d8bfe6537a1ff984d2f0af8a1ca0efeb31774cec4a12f966f708d51cb479`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380e2f8b0a3606c651c20ab98460614d53fb50d4b9a9f7b33eff69eebc508ab1`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 40.5 MB (40481210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9d4712db09dae7f88b55a0497883dc40d43f805f6a22a8c289b92a5a6a5398`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:8c2d1f30f6734998339eb461ba194daf2e305626707d89e1eb59ef8e23f53b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7e0deebd9fdf8e46d830911a8c8975a00462147f7d923d7aa7773221eafe5534
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133155232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fb8170f15f6d079a63ed552de428861e093873629a97b5cde83ddf86af5d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 08:02:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:02:48 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:02:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:03:25 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 18 Mar 2022 08:04:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Mar 2022 08:04:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Mar 2022 08:04:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Mar 2022 08:04:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:57 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Mar 2022 08:04:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:04:58 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:04:58 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:04:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1824cb7e97fbcfc5c6ffea667f8e19cee765d015fef1b8ad70f96252d9713c95`  
		Last Modified: Fri, 18 Mar 2022 05:24:44 GMT  
		Size: 42.1 MB (42110196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5603b74046dbdf928d0641abd36690bf5ef09bec61a2131c3ec7eb4b4c6d8ba4`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c5d7fe8298ed20bcb5c7adbbe025eef7a9de9e5b1e3447936ed9d02b09b7f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc1f1a8427b3e502f4f25dd7acf037e2a2d35927b3201d2711442516c32591b`  
		Last Modified: Fri, 18 Mar 2022 08:07:32 GMT  
		Size: 4.6 MB (4552961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c348d46c25eeb80c794020883a39367c3db1dae41fc9a79aa6fda96d43a51d`  
		Last Modified: Fri, 18 Mar 2022 08:07:31 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2658193beeb76b4b398b4ee7ecc71ebfd580ecf8925d131c8e84598f7c3182`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3694176cd71ffaa30adad12882db7b497d0e83d860f4cbfbdf559213d1fcbb1b`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 47.3 MB (47269558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32d4e62ce97c09e1c91dcf712a5bec3c227e2edcbbc4947ffaf2a7f7acddfb4`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3b55b1e47e4fb94d7b16d8d2d6c298bf1b155b21feed7e8eb3b50060ce91fd`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 38.3 MB (38284179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b3ad406f04dc3a6b8a318c6bf53f8868d1b65941fd2aaf608d5e9a9f4dc33e`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9b456391b4bb798292b6a959f0d3a992911fc1f9c21cb1bee563096d9015f6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141172027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b353a72fcab60e6c13412fdafe5840a37e7dad38f5c36f7374eff8b8321151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:35:35 GMT
ADD file:b16af05882bd38ac02b1f1cba2cc7e80bfbe467ce57f3cf35f1f5a551cee90fa in / 
# Fri, 18 Mar 2022 00:35:36 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 14:48:31 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 14:48:32 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 14:48:35 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 14:49:02 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 19 Mar 2022 14:49:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 19 Mar 2022 14:49:47 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 19 Mar 2022 14:49:48 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:49:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 19 Mar 2022 14:50:17 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:50:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 19 Mar 2022 14:50:46 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 14:50:48 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Sat, 19 Mar 2022 14:50:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 14:50:49 GMT
EXPOSE 3306 33060
# Sat, 19 Mar 2022 14:50:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f8e506fd7c6683f24250871efec36e3fe21cc71090a2f5c59dccdcdfeed2311`  
		Last Modified: Fri, 18 Mar 2022 00:36:38 GMT  
		Size: 42.0 MB (42017883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2e303329ed7fcb9aeb4e6a5e5e8ff70c5ecaca6b4004efe7c5538f98ae073e`  
		Last Modified: Sat, 19 Mar 2022 14:51:14 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43a54926eb5a7901c559b6766eb23666ade02e931708faf2888edadac9e1851`  
		Last Modified: Sat, 19 Mar 2022 14:51:13 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0039e24d8493013955f1061869d44fbdb472434d801986ac8140f0b1846bf4a`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 4.4 MB (4376516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d112a79f85ef077e50966e6ff296393952c4e854cabca838a2ae8ea52346dd`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a816874cae3d0e7af62a465c20b10528a92dedfae97f28912f66a1e05d2eb35`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf3e7c1e5610eed17336f2c459440bddfc67726e3c7fb87fafa6d6b69621d5`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 53.4 MB (53429849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2d8bfe6537a1ff984d2f0af8a1ca0efeb31774cec4a12f966f708d51cb479`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380e2f8b0a3606c651c20ab98460614d53fb50d4b9a9f7b33eff69eebc508ab1`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 40.5 MB (40481210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9d4712db09dae7f88b55a0497883dc40d43f805f6a22a8c289b92a5a6a5398`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-debian`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28-debian` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-oracle`

```console
$ docker pull mysql@sha256:8c2d1f30f6734998339eb461ba194daf2e305626707d89e1eb59ef8e23f53b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.28-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7e0deebd9fdf8e46d830911a8c8975a00462147f7d923d7aa7773221eafe5534
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133155232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fb8170f15f6d079a63ed552de428861e093873629a97b5cde83ddf86af5d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 08:02:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:02:48 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:02:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:03:25 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 18 Mar 2022 08:04:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Mar 2022 08:04:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Mar 2022 08:04:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Mar 2022 08:04:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:57 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Mar 2022 08:04:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:04:58 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:04:58 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:04:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1824cb7e97fbcfc5c6ffea667f8e19cee765d015fef1b8ad70f96252d9713c95`  
		Last Modified: Fri, 18 Mar 2022 05:24:44 GMT  
		Size: 42.1 MB (42110196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5603b74046dbdf928d0641abd36690bf5ef09bec61a2131c3ec7eb4b4c6d8ba4`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c5d7fe8298ed20bcb5c7adbbe025eef7a9de9e5b1e3447936ed9d02b09b7f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc1f1a8427b3e502f4f25dd7acf037e2a2d35927b3201d2711442516c32591b`  
		Last Modified: Fri, 18 Mar 2022 08:07:32 GMT  
		Size: 4.6 MB (4552961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c348d46c25eeb80c794020883a39367c3db1dae41fc9a79aa6fda96d43a51d`  
		Last Modified: Fri, 18 Mar 2022 08:07:31 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2658193beeb76b4b398b4ee7ecc71ebfd580ecf8925d131c8e84598f7c3182`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3694176cd71ffaa30adad12882db7b497d0e83d860f4cbfbdf559213d1fcbb1b`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 47.3 MB (47269558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32d4e62ce97c09e1c91dcf712a5bec3c227e2edcbbc4947ffaf2a7f7acddfb4`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3b55b1e47e4fb94d7b16d8d2d6c298bf1b155b21feed7e8eb3b50060ce91fd`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 38.3 MB (38284179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b3ad406f04dc3a6b8a318c6bf53f8868d1b65941fd2aaf608d5e9a9f4dc33e`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.28-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9b456391b4bb798292b6a959f0d3a992911fc1f9c21cb1bee563096d9015f6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141172027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b353a72fcab60e6c13412fdafe5840a37e7dad38f5c36f7374eff8b8321151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:35:35 GMT
ADD file:b16af05882bd38ac02b1f1cba2cc7e80bfbe467ce57f3cf35f1f5a551cee90fa in / 
# Fri, 18 Mar 2022 00:35:36 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 14:48:31 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 14:48:32 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 14:48:35 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 14:49:02 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 19 Mar 2022 14:49:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 19 Mar 2022 14:49:47 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 19 Mar 2022 14:49:48 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:49:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 19 Mar 2022 14:50:17 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:50:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 19 Mar 2022 14:50:46 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 14:50:48 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Sat, 19 Mar 2022 14:50:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 14:50:49 GMT
EXPOSE 3306 33060
# Sat, 19 Mar 2022 14:50:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f8e506fd7c6683f24250871efec36e3fe21cc71090a2f5c59dccdcdfeed2311`  
		Last Modified: Fri, 18 Mar 2022 00:36:38 GMT  
		Size: 42.0 MB (42017883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2e303329ed7fcb9aeb4e6a5e5e8ff70c5ecaca6b4004efe7c5538f98ae073e`  
		Last Modified: Sat, 19 Mar 2022 14:51:14 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43a54926eb5a7901c559b6766eb23666ade02e931708faf2888edadac9e1851`  
		Last Modified: Sat, 19 Mar 2022 14:51:13 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0039e24d8493013955f1061869d44fbdb472434d801986ac8140f0b1846bf4a`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 4.4 MB (4376516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d112a79f85ef077e50966e6ff296393952c4e854cabca838a2ae8ea52346dd`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a816874cae3d0e7af62a465c20b10528a92dedfae97f28912f66a1e05d2eb35`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf3e7c1e5610eed17336f2c459440bddfc67726e3c7fb87fafa6d6b69621d5`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 53.4 MB (53429849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2d8bfe6537a1ff984d2f0af8a1ca0efeb31774cec4a12f966f708d51cb479`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380e2f8b0a3606c651c20ab98460614d53fb50d4b9a9f7b33eff69eebc508ab1`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 40.5 MB (40481210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9d4712db09dae7f88b55a0497883dc40d43f805f6a22a8c289b92a5a6a5398`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:b2ae0f527005d99bacdf3a220958ed171e1eb0676377174f0323e0a10912408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:00f9eb474bf3c508d79292234abc60dae082290445f44e38d9fcd844c2cd3372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154588164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c9bc24a0883226e994aabbd09fcb5621a4eadb510df749bc6dac40fa991e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:05:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 18 Mar 2022 08:05:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:17 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:05:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:05:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:05:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:05:46 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:05:47 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Mar 2022 08:05:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Mar 2022 08:06:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Mar 2022 08:06:12 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:06:12 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Mar 2022 08:06:12 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:06:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Mar 2022 08:06:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:06:14 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:06:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b610d88fd99d32cc566df2799696e4c382585071097a00051274edd5aba2a2`  
		Last Modified: Fri, 18 Mar 2022 08:08:01 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38567843b438528aec2e445daf0b2f45d468e92718c73612926e8b6c8f2ebe10`  
		Last Modified: Fri, 18 Mar 2022 08:08:02 GMT  
		Size: 4.2 MB (4179316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc423bf9558fc1c7102977e94d1f95331ff2b7e2e5e02e0a32346e1217ce4b3`  
		Last Modified: Fri, 18 Mar 2022 08:08:00 GMT  
		Size: 1.4 MB (1386669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8241dfe8280a8f86bacace41eda0644b04ee0696bd32e9a6b95bafd2d48f8b`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc662311610e8df5f42ff626b5db6d179f9c894c73ab0cccf719dd7848d5222a`  
		Last Modified: Fri, 18 Mar 2022 08:08:04 GMT  
		Size: 14.1 MB (14052414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832d1192cf2fe8622425e18f9f868f2efbe0e78fe3724d999f3521ff2da8363`  
		Last Modified: Fri, 18 Mar 2022 08:07:59 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2aa1710465f892ce62ad802679f4052567ab6da737d520da7f8a01f6251774d`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2d5722b8f34e9bf522099069d23bfbccfdb49063febf5d440f242fa89e57b0`  
		Last Modified: Fri, 18 Mar 2022 08:08:22 GMT  
		Size: 107.8 MB (107805152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a246e8d7cac973ac8c6dbf8a9d2c7c15c95ee700602d152f56194331e8a2a8f`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f834692d7cccae00681493349f623ffc62226e8a4af1e6ce0b08799e4a8b670`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 5.1 KB (5137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374095680229f498cd512f25bc465fe563353f70ea395cc9eb4709f0177e5f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:57 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:8c2d1f30f6734998339eb461ba194daf2e305626707d89e1eb59ef8e23f53b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7e0deebd9fdf8e46d830911a8c8975a00462147f7d923d7aa7773221eafe5534
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133155232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7fb8170f15f6d079a63ed552de428861e093873629a97b5cde83ddf86af5d78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 05:23:28 GMT
ADD file:09b0bc8af49fa3558fb3e8d50daa682180e194cb11ca332d03ca65059e615dfd in / 
# Fri, 18 Mar 2022 05:23:29 GMT
CMD ["/bin/bash"]
# Fri, 18 Mar 2022 08:02:48 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Mar 2022 08:02:48 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Mar 2022 08:02:53 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Mar 2022 08:03:25 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 18 Mar 2022 08:04:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Mar 2022 08:04:01 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Mar 2022 08:04:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Mar 2022 08:04:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Mar 2022 08:04:28 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Mar 2022 08:04:57 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Mar 2022 08:04:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Mar 2022 08:04:58 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Fri, 18 Mar 2022 08:04:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Mar 2022 08:04:58 GMT
EXPOSE 3306 33060
# Fri, 18 Mar 2022 08:04:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1824cb7e97fbcfc5c6ffea667f8e19cee765d015fef1b8ad70f96252d9713c95`  
		Last Modified: Fri, 18 Mar 2022 05:24:44 GMT  
		Size: 42.1 MB (42110196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5603b74046dbdf928d0641abd36690bf5ef09bec61a2131c3ec7eb4b4c6d8ba4`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c5d7fe8298ed20bcb5c7adbbe025eef7a9de9e5b1e3447936ed9d02b09b7f1`  
		Last Modified: Fri, 18 Mar 2022 08:07:37 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc1f1a8427b3e502f4f25dd7acf037e2a2d35927b3201d2711442516c32591b`  
		Last Modified: Fri, 18 Mar 2022 08:07:32 GMT  
		Size: 4.6 MB (4552961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c348d46c25eeb80c794020883a39367c3db1dae41fc9a79aa6fda96d43a51d`  
		Last Modified: Fri, 18 Mar 2022 08:07:31 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2658193beeb76b4b398b4ee7ecc71ebfd580ecf8925d131c8e84598f7c3182`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3694176cd71ffaa30adad12882db7b497d0e83d860f4cbfbdf559213d1fcbb1b`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 47.3 MB (47269558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32d4e62ce97c09e1c91dcf712a5bec3c227e2edcbbc4947ffaf2a7f7acddfb4`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3b55b1e47e4fb94d7b16d8d2d6c298bf1b155b21feed7e8eb3b50060ce91fd`  
		Last Modified: Fri, 18 Mar 2022 08:07:41 GMT  
		Size: 38.3 MB (38284179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b3ad406f04dc3a6b8a318c6bf53f8868d1b65941fd2aaf608d5e9a9f4dc33e`  
		Last Modified: Fri, 18 Mar 2022 08:07:28 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:e9b456391b4bb798292b6a959f0d3a992911fc1f9c21cb1bee563096d9015f6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141172027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b353a72fcab60e6c13412fdafe5840a37e7dad38f5c36f7374eff8b8321151`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 18 Mar 2022 00:35:35 GMT
ADD file:b16af05882bd38ac02b1f1cba2cc7e80bfbe467ce57f3cf35f1f5a551cee90fa in / 
# Fri, 18 Mar 2022 00:35:36 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 14:48:31 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Sat, 19 Mar 2022 14:48:32 GMT
ENV GOSU_VERSION=1.14
# Sat, 19 Mar 2022 14:48:35 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 19 Mar 2022 14:49:02 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 19 Mar 2022 14:49:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 19 Mar 2022 14:49:47 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 19 Mar 2022 14:49:48 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:49:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Sat, 19 Mar 2022 14:50:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 19 Mar 2022 14:50:17 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Sat, 19 Mar 2022 14:50:46 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 19 Mar 2022 14:50:46 GMT
VOLUME [/var/lib/mysql]
# Sat, 19 Mar 2022 14:50:48 GMT
COPY file:e9a583a365264f0f565259ffd0f19e5199ef4351d098f75af32f633c0d6cbe73 in /usr/local/bin/ 
# Sat, 19 Mar 2022 14:50:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 19 Mar 2022 14:50:49 GMT
EXPOSE 3306 33060
# Sat, 19 Mar 2022 14:50:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2f8e506fd7c6683f24250871efec36e3fe21cc71090a2f5c59dccdcdfeed2311`  
		Last Modified: Fri, 18 Mar 2022 00:36:38 GMT  
		Size: 42.0 MB (42017883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2e303329ed7fcb9aeb4e6a5e5e8ff70c5ecaca6b4004efe7c5538f98ae073e`  
		Last Modified: Sat, 19 Mar 2022 14:51:14 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43a54926eb5a7901c559b6766eb23666ade02e931708faf2888edadac9e1851`  
		Last Modified: Sat, 19 Mar 2022 14:51:13 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0039e24d8493013955f1061869d44fbdb472434d801986ac8140f0b1846bf4a`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 4.4 MB (4376516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d112a79f85ef077e50966e6ff296393952c4e854cabca838a2ae8ea52346dd`  
		Last Modified: Sat, 19 Mar 2022 14:51:12 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a816874cae3d0e7af62a465c20b10528a92dedfae97f28912f66a1e05d2eb35`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cf3e7c1e5610eed17336f2c459440bddfc67726e3c7fb87fafa6d6b69621d5`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 53.4 MB (53429849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2d8bfe6537a1ff984d2f0af8a1ca0efeb31774cec4a12f966f708d51cb479`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380e2f8b0a3606c651c20ab98460614d53fb50d4b9a9f7b33eff69eebc508ab1`  
		Last Modified: Sat, 19 Mar 2022 14:51:17 GMT  
		Size: 40.5 MB (40481210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9d4712db09dae7f88b55a0497883dc40d43f805f6a22a8c289b92a5a6a5398`  
		Last Modified: Sat, 19 Mar 2022 14:51:10 GMT  
		Size: 5.1 KB (5142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
