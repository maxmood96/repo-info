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
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:64ef2a07763f7f7ec4e1acbac84d5dbdda5b4bf468194aaa5caa9bf4bf370a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b70e11f0a1d0d3018bf6ca3846d872e4e68c699cdf2dc25b46049327386db1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127806404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5958a947375b1e5db8071ec2f5332b72526229a8a0699d64078c3f7baf60687b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Jun 2022 01:38:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 16 Jun 2022 01:38:41 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Jun 2022 01:38:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Jun 2022 00:22:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 28 Jun 2022 00:22:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:22:16 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:22:16 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 28 Jun 2022 00:22:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 28 Jun 2022 00:22:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 28 Jun 2022 00:22:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 28 Jun 2022 00:22:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 28 Jun 2022 00:22:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 28 Jun 2022 00:22:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:22:56 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:22:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:22:57 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:22:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921fb508f1d1aecc5558b119c43c60ca99e2803d417ea98b5a55f94975ac5440`  
		Last Modified: Thu, 16 Jun 2022 01:40:10 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c722a284ecb6bbcc3803b2a9fb3df9e58ebd491e421507db7c73d8f4255cf0f4`  
		Last Modified: Thu, 16 Jun 2022 01:40:09 GMT  
		Size: 930.2 KB (930225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e2862fad6e07e82b31bcad70ede98d8fda30c834740a571945313fbb06c086`  
		Last Modified: Tue, 28 Jun 2022 00:25:07 GMT  
		Size: 4.5 MB (4545079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa0403847e0144a5edf870bb60a1c2ca163adcbec7f37754825f101361ed34b`  
		Last Modified: Tue, 28 Jun 2022 00:25:06 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e220d9807c0bd3630bf3d8257814277de6620028f9769b8a0936e8e41d9177`  
		Last Modified: Tue, 28 Jun 2022 00:25:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bf024001e30ab8d7eef404acdf647bd35eea8ba5dfc013f809f664595e3aeb`  
		Last Modified: Tue, 28 Jun 2022 00:25:07 GMT  
		Size: 25.5 MB (25481000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a565f071b7651737bb567cf6f527aa8d30e5acb1f050e1c1744bba9b5aa825`  
		Last Modified: Tue, 28 Jun 2022 00:25:04 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcac0569bb6d8155444f4dd08484dd7ef1ed644e3f69d80c0fa9018d18ed0e`  
		Last Modified: Tue, 28 Jun 2022 00:25:12 GMT  
		Size: 48.1 MB (48082637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def88f6fdde385c164a91c0e22b6c4c4ef9d6c8d38ca8e53c39079e6b0915b38`  
		Last Modified: Tue, 28 Jun 2022 00:25:03 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:64ef2a07763f7f7ec4e1acbac84d5dbdda5b4bf468194aaa5caa9bf4bf370a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b70e11f0a1d0d3018bf6ca3846d872e4e68c699cdf2dc25b46049327386db1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127806404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5958a947375b1e5db8071ec2f5332b72526229a8a0699d64078c3f7baf60687b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Jun 2022 01:38:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 16 Jun 2022 01:38:41 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Jun 2022 01:38:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Jun 2022 00:22:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 28 Jun 2022 00:22:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:22:16 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:22:16 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 28 Jun 2022 00:22:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 28 Jun 2022 00:22:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 28 Jun 2022 00:22:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 28 Jun 2022 00:22:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 28 Jun 2022 00:22:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 28 Jun 2022 00:22:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:22:56 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:22:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:22:57 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:22:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921fb508f1d1aecc5558b119c43c60ca99e2803d417ea98b5a55f94975ac5440`  
		Last Modified: Thu, 16 Jun 2022 01:40:10 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c722a284ecb6bbcc3803b2a9fb3df9e58ebd491e421507db7c73d8f4255cf0f4`  
		Last Modified: Thu, 16 Jun 2022 01:40:09 GMT  
		Size: 930.2 KB (930225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e2862fad6e07e82b31bcad70ede98d8fda30c834740a571945313fbb06c086`  
		Last Modified: Tue, 28 Jun 2022 00:25:07 GMT  
		Size: 4.5 MB (4545079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa0403847e0144a5edf870bb60a1c2ca163adcbec7f37754825f101361ed34b`  
		Last Modified: Tue, 28 Jun 2022 00:25:06 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e220d9807c0bd3630bf3d8257814277de6620028f9769b8a0936e8e41d9177`  
		Last Modified: Tue, 28 Jun 2022 00:25:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bf024001e30ab8d7eef404acdf647bd35eea8ba5dfc013f809f664595e3aeb`  
		Last Modified: Tue, 28 Jun 2022 00:25:07 GMT  
		Size: 25.5 MB (25481000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a565f071b7651737bb567cf6f527aa8d30e5acb1f050e1c1744bba9b5aa825`  
		Last Modified: Tue, 28 Jun 2022 00:25:04 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcac0569bb6d8155444f4dd08484dd7ef1ed644e3f69d80c0fa9018d18ed0e`  
		Last Modified: Tue, 28 Jun 2022 00:25:12 GMT  
		Size: 48.1 MB (48082637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def88f6fdde385c164a91c0e22b6c4c4ef9d6c8d38ca8e53c39079e6b0915b38`  
		Last Modified: Tue, 28 Jun 2022 00:25:03 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-debian`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-oracle`

```console
$ docker pull mysql@sha256:64ef2a07763f7f7ec4e1acbac84d5dbdda5b4bf468194aaa5caa9bf4bf370a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8b70e11f0a1d0d3018bf6ca3846d872e4e68c699cdf2dc25b46049327386db1c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127806404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5958a947375b1e5db8071ec2f5332b72526229a8a0699d64078c3f7baf60687b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 16 Jun 2022 01:20:22 GMT
ADD file:5e615d6d49ec50cba937fa86f5fb7d6a4a7e680b2b4f5b659e879b95304c0417 in / 
# Thu, 16 Jun 2022 01:20:22 GMT
CMD ["/bin/bash"]
# Thu, 16 Jun 2022 01:38:41 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 16 Jun 2022 01:38:41 GMT
ENV GOSU_VERSION=1.14
# Thu, 16 Jun 2022 01:38:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 28 Jun 2022 00:22:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 28 Jun 2022 00:22:16 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:22:16 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:22:16 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 28 Jun 2022 00:22:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 28 Jun 2022 00:22:34 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 28 Jun 2022 00:22:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 28 Jun 2022 00:22:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 28 Jun 2022 00:22:56 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 28 Jun 2022 00:22:56 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:22:56 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:22:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:22:57 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:22:57 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:63183c9b4598e16c4cef95f706d50ff6c928de41f391cd513495b27eaa27bf89`  
		Last Modified: Thu, 16 Jun 2022 01:21:08 GMT  
		Size: 48.8 MB (48757931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921fb508f1d1aecc5558b119c43c60ca99e2803d417ea98b5a55f94975ac5440`  
		Last Modified: Thu, 16 Jun 2022 01:40:10 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c722a284ecb6bbcc3803b2a9fb3df9e58ebd491e421507db7c73d8f4255cf0f4`  
		Last Modified: Thu, 16 Jun 2022 01:40:09 GMT  
		Size: 930.2 KB (930225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e2862fad6e07e82b31bcad70ede98d8fda30c834740a571945313fbb06c086`  
		Last Modified: Tue, 28 Jun 2022 00:25:07 GMT  
		Size: 4.5 MB (4545079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa0403847e0144a5edf870bb60a1c2ca163adcbec7f37754825f101361ed34b`  
		Last Modified: Tue, 28 Jun 2022 00:25:06 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e220d9807c0bd3630bf3d8257814277de6620028f9769b8a0936e8e41d9177`  
		Last Modified: Tue, 28 Jun 2022 00:25:03 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bf024001e30ab8d7eef404acdf647bd35eea8ba5dfc013f809f664595e3aeb`  
		Last Modified: Tue, 28 Jun 2022 00:25:07 GMT  
		Size: 25.5 MB (25481000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a565f071b7651737bb567cf6f527aa8d30e5acb1f050e1c1744bba9b5aa825`  
		Last Modified: Tue, 28 Jun 2022 00:25:04 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbcac0569bb6d8155444f4dd08484dd7ef1ed644e3f69d80c0fa9018d18ed0e`  
		Last Modified: Tue, 28 Jun 2022 00:25:12 GMT  
		Size: 48.1 MB (48082637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def88f6fdde385c164a91c0e22b6c4c4ef9d6c8d38ca8e53c39079e6b0915b38`  
		Last Modified: Tue, 28 Jun 2022 00:25:03 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:e9a9bb6104727e8936450b3c03a4b2b5256a302ad23f6ab3e5507b83f5f4b8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6996eea0ad2e2001832c8f6bdc6e6fc466abd0ec0729bd0fc7bcb40aa8fc01e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131792367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55abd4f24284f81521e19ffeea65f3def1b08b3f327b18717e6417288d52b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:20:45 GMT
ADD file:03d0377f5864198b250372de990ebf0ef7597cfdcc2e18421e8e0025394a7572 in / 
# Thu, 30 Jun 2022 17:20:46 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:53:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:53:27 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:53:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:53:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:53:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:53:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:54:20 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:54:21 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:54:21 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:54:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:54:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:54:51 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:54:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:54:51 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:54:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:337897a5aaf7b54e691e2ed305fbf00e0e8933d5a8a3c07d6fbb95f10b15c644`  
		Last Modified: Thu, 30 Jun 2022 17:21:37 GMT  
		Size: 39.2 MB (39221672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab90e5959941cb8c7347e011f5afce2db019e988ebb616b297bb4389b910919`  
		Last Modified: Thu, 30 Jun 2022 17:55:39 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3fb1d80e2666e97623c60a8e9e2612c1200ac9ae2ac744fd22a758ea33f928`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39c2294433bf6d9e7b4ce4b1dc9f9c6d4a4f68a81414b4e27657402b9b8d3e`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 4.6 MB (4589009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d4e890a7354b6d4c2e1edf68d5979a0679beaf651375c96f606d208f87656f`  
		Last Modified: Thu, 30 Jun 2022 17:55:35 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa3c9d5a27ed6886b4ee359d0344efda21b1e5c80b3a0beb6843b1a01cdbcbd`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be0cdbeeceabf204578c357347b23dedc24b300fab828884daf7c3a5095b51`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 47.3 MB (47255195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24746683571299c7c147954a14ef60aeffedb81f8f4c97b5ddc957632a566e9`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7fdf5b11390c4379d8e8d8133f2e4d3b01142992dc9a890a2289ee9b67b2ff`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 39.8 MB (39788136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca0a906ad0c589647da783239568c1e4d3bd2415efea7f87c60cce702cd2af`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:083fa211ffb5822bafff1d3d01602870b39e92a4cd1468bd9c3b2b85a3faff49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138689282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441f1a5091104473200f24f007d6b5109b23e02f532af1fd8a1ddb4e2b2b8fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:40:34 GMT
ADD file:deb746f3cc547a36a34f3bfe68510bbd6f8a3b2da72bcca3cce36dfe0e519e77 in / 
# Thu, 30 Jun 2022 17:40:35 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:56:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:56:58 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:57:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:57:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:57:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:57:29 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:57:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:57:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:57:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:57:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:57:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:58:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:58:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:58:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:58:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:58:48 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:58:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c7107c973a1b04b1f048e43f460fd4f030df5f2e53fce3dfb8a13dc7fefdb4b0`  
		Last Modified: Thu, 30 Jun 2022 17:41:32 GMT  
		Size: 38.0 MB (38023864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ff5b23e734a8eeec60c2eb90597cbda9fa27e065d2bec4707d3bfde16a8cf5`  
		Last Modified: Thu, 30 Jun 2022 17:59:25 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878d994e970dcf35ae3f8d4ef9773a6613db5aed1ad17cdf98d0e5c625be7f2`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d2f997a642573befc691f0bdb1a3e66bf8a71a222dd933ad82006f039335e`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 4.4 MB (4417810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193bd54370e31cecfe8f9b83d935d06583f681f633c3e793fb545007b2164329`  
		Last Modified: Thu, 30 Jun 2022 17:59:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094f87b4a3b8b06442f2861ab45eca2bd8b8601b12112e73c8ed1d7e1d22826`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b1f91367333d55f0b315ef7083b0023b753a211321de72fff5fb5b59b7f244`  
		Last Modified: Thu, 30 Jun 2022 17:59:31 GMT  
		Size: 53.3 MB (53317903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3979aa14f69006762d7da4d412945edaf43ac5171fa872adc9caeb7f6c36831`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a181020e9b88f14ae8b99a6bff5417d99f19f2647f7cd08bd39f2fb093fe`  
		Last Modified: Thu, 30 Jun 2022 17:59:28 GMT  
		Size: 42.1 MB (42063118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa33730fe72d9d90227f1756a89841ccb1a6ec991a4233831b2a6cde446ac45`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:e9a9bb6104727e8936450b3c03a4b2b5256a302ad23f6ab3e5507b83f5f4b8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6996eea0ad2e2001832c8f6bdc6e6fc466abd0ec0729bd0fc7bcb40aa8fc01e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131792367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55abd4f24284f81521e19ffeea65f3def1b08b3f327b18717e6417288d52b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:20:45 GMT
ADD file:03d0377f5864198b250372de990ebf0ef7597cfdcc2e18421e8e0025394a7572 in / 
# Thu, 30 Jun 2022 17:20:46 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:53:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:53:27 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:53:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:53:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:53:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:53:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:54:20 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:54:21 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:54:21 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:54:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:54:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:54:51 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:54:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:54:51 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:54:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:337897a5aaf7b54e691e2ed305fbf00e0e8933d5a8a3c07d6fbb95f10b15c644`  
		Last Modified: Thu, 30 Jun 2022 17:21:37 GMT  
		Size: 39.2 MB (39221672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab90e5959941cb8c7347e011f5afce2db019e988ebb616b297bb4389b910919`  
		Last Modified: Thu, 30 Jun 2022 17:55:39 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3fb1d80e2666e97623c60a8e9e2612c1200ac9ae2ac744fd22a758ea33f928`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39c2294433bf6d9e7b4ce4b1dc9f9c6d4a4f68a81414b4e27657402b9b8d3e`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 4.6 MB (4589009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d4e890a7354b6d4c2e1edf68d5979a0679beaf651375c96f606d208f87656f`  
		Last Modified: Thu, 30 Jun 2022 17:55:35 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa3c9d5a27ed6886b4ee359d0344efda21b1e5c80b3a0beb6843b1a01cdbcbd`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be0cdbeeceabf204578c357347b23dedc24b300fab828884daf7c3a5095b51`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 47.3 MB (47255195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24746683571299c7c147954a14ef60aeffedb81f8f4c97b5ddc957632a566e9`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7fdf5b11390c4379d8e8d8133f2e4d3b01142992dc9a890a2289ee9b67b2ff`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 39.8 MB (39788136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca0a906ad0c589647da783239568c1e4d3bd2415efea7f87c60cce702cd2af`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:083fa211ffb5822bafff1d3d01602870b39e92a4cd1468bd9c3b2b85a3faff49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138689282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441f1a5091104473200f24f007d6b5109b23e02f532af1fd8a1ddb4e2b2b8fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:40:34 GMT
ADD file:deb746f3cc547a36a34f3bfe68510bbd6f8a3b2da72bcca3cce36dfe0e519e77 in / 
# Thu, 30 Jun 2022 17:40:35 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:56:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:56:58 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:57:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:57:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:57:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:57:29 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:57:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:57:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:57:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:57:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:57:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:58:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:58:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:58:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:58:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:58:48 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:58:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c7107c973a1b04b1f048e43f460fd4f030df5f2e53fce3dfb8a13dc7fefdb4b0`  
		Last Modified: Thu, 30 Jun 2022 17:41:32 GMT  
		Size: 38.0 MB (38023864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ff5b23e734a8eeec60c2eb90597cbda9fa27e065d2bec4707d3bfde16a8cf5`  
		Last Modified: Thu, 30 Jun 2022 17:59:25 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878d994e970dcf35ae3f8d4ef9773a6613db5aed1ad17cdf98d0e5c625be7f2`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d2f997a642573befc691f0bdb1a3e66bf8a71a222dd933ad82006f039335e`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 4.4 MB (4417810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193bd54370e31cecfe8f9b83d935d06583f681f633c3e793fb545007b2164329`  
		Last Modified: Thu, 30 Jun 2022 17:59:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094f87b4a3b8b06442f2861ab45eca2bd8b8601b12112e73c8ed1d7e1d22826`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b1f91367333d55f0b315ef7083b0023b753a211321de72fff5fb5b59b7f244`  
		Last Modified: Thu, 30 Jun 2022 17:59:31 GMT  
		Size: 53.3 MB (53317903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3979aa14f69006762d7da4d412945edaf43ac5171fa872adc9caeb7f6c36831`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a181020e9b88f14ae8b99a6bff5417d99f19f2647f7cd08bd39f2fb093fe`  
		Last Modified: Thu, 30 Jun 2022 17:59:28 GMT  
		Size: 42.1 MB (42063118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa33730fe72d9d90227f1756a89841ccb1a6ec991a4233831b2a6cde446ac45`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-debian`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-oracle`

```console
$ docker pull mysql@sha256:e9a9bb6104727e8936450b3c03a4b2b5256a302ad23f6ab3e5507b83f5f4b8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.29-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6996eea0ad2e2001832c8f6bdc6e6fc466abd0ec0729bd0fc7bcb40aa8fc01e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131792367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55abd4f24284f81521e19ffeea65f3def1b08b3f327b18717e6417288d52b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:20:45 GMT
ADD file:03d0377f5864198b250372de990ebf0ef7597cfdcc2e18421e8e0025394a7572 in / 
# Thu, 30 Jun 2022 17:20:46 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:53:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:53:27 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:53:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:53:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:53:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:53:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:54:20 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:54:21 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:54:21 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:54:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:54:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:54:51 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:54:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:54:51 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:54:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:337897a5aaf7b54e691e2ed305fbf00e0e8933d5a8a3c07d6fbb95f10b15c644`  
		Last Modified: Thu, 30 Jun 2022 17:21:37 GMT  
		Size: 39.2 MB (39221672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab90e5959941cb8c7347e011f5afce2db019e988ebb616b297bb4389b910919`  
		Last Modified: Thu, 30 Jun 2022 17:55:39 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3fb1d80e2666e97623c60a8e9e2612c1200ac9ae2ac744fd22a758ea33f928`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39c2294433bf6d9e7b4ce4b1dc9f9c6d4a4f68a81414b4e27657402b9b8d3e`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 4.6 MB (4589009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d4e890a7354b6d4c2e1edf68d5979a0679beaf651375c96f606d208f87656f`  
		Last Modified: Thu, 30 Jun 2022 17:55:35 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa3c9d5a27ed6886b4ee359d0344efda21b1e5c80b3a0beb6843b1a01cdbcbd`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be0cdbeeceabf204578c357347b23dedc24b300fab828884daf7c3a5095b51`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 47.3 MB (47255195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24746683571299c7c147954a14ef60aeffedb81f8f4c97b5ddc957632a566e9`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7fdf5b11390c4379d8e8d8133f2e4d3b01142992dc9a890a2289ee9b67b2ff`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 39.8 MB (39788136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca0a906ad0c589647da783239568c1e4d3bd2415efea7f87c60cce702cd2af`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.29-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:083fa211ffb5822bafff1d3d01602870b39e92a4cd1468bd9c3b2b85a3faff49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138689282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441f1a5091104473200f24f007d6b5109b23e02f532af1fd8a1ddb4e2b2b8fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:40:34 GMT
ADD file:deb746f3cc547a36a34f3bfe68510bbd6f8a3b2da72bcca3cce36dfe0e519e77 in / 
# Thu, 30 Jun 2022 17:40:35 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:56:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:56:58 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:57:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:57:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:57:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:57:29 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:57:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:57:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:57:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:57:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:57:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:58:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:58:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:58:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:58:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:58:48 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:58:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c7107c973a1b04b1f048e43f460fd4f030df5f2e53fce3dfb8a13dc7fefdb4b0`  
		Last Modified: Thu, 30 Jun 2022 17:41:32 GMT  
		Size: 38.0 MB (38023864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ff5b23e734a8eeec60c2eb90597cbda9fa27e065d2bec4707d3bfde16a8cf5`  
		Last Modified: Thu, 30 Jun 2022 17:59:25 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878d994e970dcf35ae3f8d4ef9773a6613db5aed1ad17cdf98d0e5c625be7f2`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d2f997a642573befc691f0bdb1a3e66bf8a71a222dd933ad82006f039335e`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 4.4 MB (4417810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193bd54370e31cecfe8f9b83d935d06583f681f633c3e793fb545007b2164329`  
		Last Modified: Thu, 30 Jun 2022 17:59:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094f87b4a3b8b06442f2861ab45eca2bd8b8601b12112e73c8ed1d7e1d22826`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b1f91367333d55f0b315ef7083b0023b753a211321de72fff5fb5b59b7f244`  
		Last Modified: Thu, 30 Jun 2022 17:59:31 GMT  
		Size: 53.3 MB (53317903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3979aa14f69006762d7da4d412945edaf43ac5171fa872adc9caeb7f6c36831`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a181020e9b88f14ae8b99a6bff5417d99f19f2647f7cd08bd39f2fb093fe`  
		Last Modified: Thu, 30 Jun 2022 17:59:28 GMT  
		Size: 42.1 MB (42063118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa33730fe72d9d90227f1756a89841ccb1a6ec991a4233831b2a6cde446ac45`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:a840244706a5fdc3c704b15a3700bfda39fdc069262d7753fa09de2d9faf5f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:b2d83fc6fbd16d59db1adc8d2e81a65663148b243bb36c6dc645f3c6468dc284
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155908369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef9083d9892db139e2b7c81fd133836e7aa32db2b5f1d5702e2593100fa1417`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 28 Jun 2022 00:21:38 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Tue, 28 Jun 2022 00:21:38 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:21:52 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:21:53 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:21:53 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 28 Jun 2022 00:21:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:21:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:21:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:21:54 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:21:54 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f6b647ddb19a4d8418c24e6de80b121ac50563fc8c2d90f0b59dbb619c9507`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09ca0f0cb24ca059efd9c31d1802ff067f77165a930b3ba53b1d3ff9833b18d`  
		Last Modified: Tue, 28 Jun 2022 00:24:35 GMT  
		Size: 109.1 MB (109104549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e223e3cd2fdb62988d08fe4dfdc8a8a3ca0916a0c151f9ce2bb463a8033ce0a`  
		Last Modified: Tue, 28 Jun 2022 00:24:17 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b038d826c6572e26b8ef0a0bc128710feb4dd940bc174c570be426a67a57fff`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33ac6052fc913fd126296376ceeb69c617236fa33d820a02b8744148615f543`  
		Last Modified: Tue, 28 Jun 2022 00:24:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:e9a9bb6104727e8936450b3c03a4b2b5256a302ad23f6ab3e5507b83f5f4b8b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c6996eea0ad2e2001832c8f6bdc6e6fc466abd0ec0729bd0fc7bcb40aa8fc01e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131792367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55abd4f24284f81521e19ffeea65f3def1b08b3f327b18717e6417288d52b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:20:45 GMT
ADD file:03d0377f5864198b250372de990ebf0ef7597cfdcc2e18421e8e0025394a7572 in / 
# Thu, 30 Jun 2022 17:20:46 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:53:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:53:27 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:53:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:53:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:53:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:53:52 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:53:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:54:20 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:54:21 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:54:21 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:54:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:54:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:54:51 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:54:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:54:51 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:54:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:337897a5aaf7b54e691e2ed305fbf00e0e8933d5a8a3c07d6fbb95f10b15c644`  
		Last Modified: Thu, 30 Jun 2022 17:21:37 GMT  
		Size: 39.2 MB (39221672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab90e5959941cb8c7347e011f5afce2db019e988ebb616b297bb4389b910919`  
		Last Modified: Thu, 30 Jun 2022 17:55:39 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca3fb1d80e2666e97623c60a8e9e2612c1200ac9ae2ac744fd22a758ea33f928`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c39c2294433bf6d9e7b4ce4b1dc9f9c6d4a4f68a81414b4e27657402b9b8d3e`  
		Last Modified: Thu, 30 Jun 2022 17:55:36 GMT  
		Size: 4.6 MB (4589009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d4e890a7354b6d4c2e1edf68d5979a0679beaf651375c96f606d208f87656f`  
		Last Modified: Thu, 30 Jun 2022 17:55:35 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa3c9d5a27ed6886b4ee359d0344efda21b1e5c80b3a0beb6843b1a01cdbcbd`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33be0cdbeeceabf204578c357347b23dedc24b300fab828884daf7c3a5095b51`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 47.3 MB (47255195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24746683571299c7c147954a14ef60aeffedb81f8f4c97b5ddc957632a566e9`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7fdf5b11390c4379d8e8d8133f2e4d3b01142992dc9a890a2289ee9b67b2ff`  
		Last Modified: Thu, 30 Jun 2022 17:55:40 GMT  
		Size: 39.8 MB (39788136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ca0a906ad0c589647da783239568c1e4d3bd2415efea7f87c60cce702cd2af`  
		Last Modified: Thu, 30 Jun 2022 17:55:32 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:083fa211ffb5822bafff1d3d01602870b39e92a4cd1468bd9c3b2b85a3faff49
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138689282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441f1a5091104473200f24f007d6b5109b23e02f532af1fd8a1ddb4e2b2b8fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 30 Jun 2022 17:40:34 GMT
ADD file:deb746f3cc547a36a34f3bfe68510bbd6f8a3b2da72bcca3cce36dfe0e519e77 in / 
# Thu, 30 Jun 2022 17:40:35 GMT
CMD ["/bin/bash"]
# Thu, 30 Jun 2022 17:56:58 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Thu, 30 Jun 2022 17:56:58 GMT
ENV GOSU_VERSION=1.14
# Thu, 30 Jun 2022 17:57:04 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 30 Jun 2022 17:57:27 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 30 Jun 2022 17:57:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 30 Jun 2022 17:57:29 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 30 Jun 2022 17:57:30 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:57:31 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 30 Jun 2022 17:57:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 30 Jun 2022 17:57:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 30 Jun 2022 17:57:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Thu, 30 Jun 2022 17:58:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 30 Jun 2022 17:58:46 GMT
VOLUME [/var/lib/mysql]
# Thu, 30 Jun 2022 17:58:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 30 Jun 2022 17:58:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Jun 2022 17:58:48 GMT
EXPOSE 3306 33060
# Thu, 30 Jun 2022 17:58:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c7107c973a1b04b1f048e43f460fd4f030df5f2e53fce3dfb8a13dc7fefdb4b0`  
		Last Modified: Thu, 30 Jun 2022 17:41:32 GMT  
		Size: 38.0 MB (38023864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ff5b23e734a8eeec60c2eb90597cbda9fa27e065d2bec4707d3bfde16a8cf5`  
		Last Modified: Thu, 30 Jun 2022 17:59:25 GMT  
		Size: 1.0 KB (1016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e878d994e970dcf35ae3f8d4ef9773a6613db5aed1ad17cdf98d0e5c625be7f2`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09d2f997a642573befc691f0bdb1a3e66bf8a71a222dd933ad82006f039335e`  
		Last Modified: Thu, 30 Jun 2022 17:59:23 GMT  
		Size: 4.4 MB (4417810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193bd54370e31cecfe8f9b83d935d06583f681f633c3e793fb545007b2164329`  
		Last Modified: Thu, 30 Jun 2022 17:59:22 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094f87b4a3b8b06442f2861ab45eca2bd8b8601b12112e73c8ed1d7e1d22826`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b1f91367333d55f0b315ef7083b0023b753a211321de72fff5fb5b59b7f244`  
		Last Modified: Thu, 30 Jun 2022 17:59:31 GMT  
		Size: 53.3 MB (53317903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3979aa14f69006762d7da4d412945edaf43ac5171fa872adc9caeb7f6c36831`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b794a181020e9b88f14ae8b99a6bff5417d99f19f2647f7cd08bd39f2fb093fe`  
		Last Modified: Thu, 30 Jun 2022 17:59:28 GMT  
		Size: 42.1 MB (42063118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa33730fe72d9d90227f1756a89841ccb1a6ec991a4233831b2a6cde446ac45`  
		Last Modified: Thu, 30 Jun 2022 17:59:20 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
