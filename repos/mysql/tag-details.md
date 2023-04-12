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
$ docker pull mysql@sha256:bf18020f32cc5d8f5e2add516d52fbf3afc3de431457076340e938596c528171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:47b0250a983e600ab247e6f25a4c99069d4cb637fd8dc6a11a43e83a83e9308c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130056950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3447deacaa5bacab184fabbf821a785e13303b2e340465bdf7815b0284497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 22:29:01 GMT
ADD file:a14b5a8b8b6993aeee5ac6052fdf283560d65365e5bcf133ab21c4756439384a in / 
# Fri, 31 Mar 2023 22:29:01 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:23:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 23:23:04 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 23:23:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 23:23:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 23:23:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 23:23:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 23:23:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Fri, 31 Mar 2023 23:24:07 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 23:24:08 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 23:24:08 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 23:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 23:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 23:24:09 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 23:24:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83e8f2e82cc31391cd0cb4f5ba574ba5eb9708fc0f5dcc34fef53b03ef28f31`  
		Last Modified: Fri, 31 Mar 2023 22:30:40 GMT  
		Size: 50.5 MB (50496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23deb01b847d9dd0fc43ede2d2dacda423b95fdbf64e0ce21a6f542f6a167e`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bda3b184ea984d363fc64e635076bcb405620effc23b2eac44f23e662bfd57`  
		Last Modified: Fri, 31 Mar 2023 23:25:05 GMT  
		Size: 983.7 KB (983706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed17edbc6604e6a5d584a08fa036d3d0711dde7676b4a6fe0adeb03b148ba5e7`  
		Last Modified: Fri, 31 Mar 2023 23:25:03 GMT  
		Size: 4.6 MB (4585198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a94a6acfa729dcf5f76be5966ecdc31692840ba7619f81d82d5e6dfc717c03`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 2.7 KB (2653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3686cf92b89d34f1d5ef195eae6471104f3a875645541473e013e18d4b595e5e`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81535a6a8bfbe8280ee0edbb4f5e8472a38785d2c36fd5c59b85996314f8ad4`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 25.5 MB (25532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bffb03ea5e2bb6d0867f6130190cdd297dc62dcd87b40f33ef7242ae6c76106`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49348ef8dcaad9bf9de316da06cf84291bcbeb9dd40b063fc9dfe852e4e3f0fc`  
		Last Modified: Fri, 31 Mar 2023 23:25:09 GMT  
		Size: 48.4 MB (48449817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509d665d0cf5e0b271d7d16a0f0fd46a59006b6c62a8e860701622fa702a2826`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc919b937fd60ace9e14a4d9963cdadb2f1939b0c5501cb83caf17f50eb4cfd`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:c4e3a2c745f7f07baf8c31e1f77f5ca1bb9a0a9deae13eb723f552cb196abb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:4f93278b6e87ce3c88366f6bd4d21822ac8f70d94b3bbe2f4c2a1c612e899522
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162692772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcfde5007783863b4085f7d7ce7f3298e676683df916f92a7e2b1a923274d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:31:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:31:14 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:31:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:31:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:31:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:31:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:31:31 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 12 Apr 2023 08:31:31 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Wed, 12 Apr 2023 08:31:31 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:49 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:50 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8509999956d8524e05b2eefe3a24f5e98d8874f64ec733f4c0e6575ea7dd9f`  
		Last Modified: Wed, 12 Apr 2023 08:32:50 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906b1388e5e7848b53d373a3d273ebf2410bb203a7649fa1963b02c1dcdcd89`  
		Last Modified: Wed, 12 Apr 2023 08:32:49 GMT  
		Size: 4.2 MB (4182293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e739cd0d39690dcce8976e89b341ebc218700bc704253075dc0656d49a0bf7`  
		Last Modified: Wed, 12 Apr 2023 08:32:49 GMT  
		Size: 1.4 MB (1441734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca1d6c3dbcc2cc64396e3645ef49c2e5df89ff26dd9fb87370ebde5d8bf24b`  
		Last Modified: Wed, 12 Apr 2023 08:32:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e6dcb9ed14decaba96a565bad9985c5da6f64da5d971444bfabdabb7deefb1`  
		Last Modified: Wed, 12 Apr 2023 08:32:51 GMT  
		Size: 14.1 MB (14086858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef841f838f6562f42727112bd0b64954fd7c4060b3f5dd6acd65b900bfd3b98`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc9cf51afcd1daec60ca50d245bf0dd2922ee6653811727ed0ccbfcfed1d91d`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712f6915d80a2844310456b06c064f294ef6236fda6db2e3ea3e403df6ec7417`  
		Last Modified: Wed, 12 Apr 2023 08:33:01 GMT  
		Size: 115.8 MB (115832777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66d31b25a4472d58ffe706dbf1e7acdfc090f9826bfc809f751f58b99189b34`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03eca2b719f66e40c8260b872df27a079a4c2ea81a35961259b07f8db0178314`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:bf18020f32cc5d8f5e2add516d52fbf3afc3de431457076340e938596c528171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:47b0250a983e600ab247e6f25a4c99069d4cb637fd8dc6a11a43e83a83e9308c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130056950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3447deacaa5bacab184fabbf821a785e13303b2e340465bdf7815b0284497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 22:29:01 GMT
ADD file:a14b5a8b8b6993aeee5ac6052fdf283560d65365e5bcf133ab21c4756439384a in / 
# Fri, 31 Mar 2023 22:29:01 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:23:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 23:23:04 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 23:23:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 23:23:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 23:23:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 23:23:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 23:23:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Fri, 31 Mar 2023 23:24:07 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 23:24:08 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 23:24:08 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 23:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 23:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 23:24:09 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 23:24:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83e8f2e82cc31391cd0cb4f5ba574ba5eb9708fc0f5dcc34fef53b03ef28f31`  
		Last Modified: Fri, 31 Mar 2023 22:30:40 GMT  
		Size: 50.5 MB (50496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23deb01b847d9dd0fc43ede2d2dacda423b95fdbf64e0ce21a6f542f6a167e`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bda3b184ea984d363fc64e635076bcb405620effc23b2eac44f23e662bfd57`  
		Last Modified: Fri, 31 Mar 2023 23:25:05 GMT  
		Size: 983.7 KB (983706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed17edbc6604e6a5d584a08fa036d3d0711dde7676b4a6fe0adeb03b148ba5e7`  
		Last Modified: Fri, 31 Mar 2023 23:25:03 GMT  
		Size: 4.6 MB (4585198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a94a6acfa729dcf5f76be5966ecdc31692840ba7619f81d82d5e6dfc717c03`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 2.7 KB (2653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3686cf92b89d34f1d5ef195eae6471104f3a875645541473e013e18d4b595e5e`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81535a6a8bfbe8280ee0edbb4f5e8472a38785d2c36fd5c59b85996314f8ad4`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 25.5 MB (25532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bffb03ea5e2bb6d0867f6130190cdd297dc62dcd87b40f33ef7242ae6c76106`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49348ef8dcaad9bf9de316da06cf84291bcbeb9dd40b063fc9dfe852e4e3f0fc`  
		Last Modified: Fri, 31 Mar 2023 23:25:09 GMT  
		Size: 48.4 MB (48449817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509d665d0cf5e0b271d7d16a0f0fd46a59006b6c62a8e860701622fa702a2826`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc919b937fd60ace9e14a4d9963cdadb2f1939b0c5501cb83caf17f50eb4cfd`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:bf18020f32cc5d8f5e2add516d52fbf3afc3de431457076340e938596c528171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:47b0250a983e600ab247e6f25a4c99069d4cb637fd8dc6a11a43e83a83e9308c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130056950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3447deacaa5bacab184fabbf821a785e13303b2e340465bdf7815b0284497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 22:29:01 GMT
ADD file:a14b5a8b8b6993aeee5ac6052fdf283560d65365e5bcf133ab21c4756439384a in / 
# Fri, 31 Mar 2023 22:29:01 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:23:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 23:23:04 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 23:23:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 23:23:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 23:23:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 23:23:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 23:23:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Fri, 31 Mar 2023 23:24:07 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 23:24:08 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 23:24:08 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 23:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 23:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 23:24:09 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 23:24:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83e8f2e82cc31391cd0cb4f5ba574ba5eb9708fc0f5dcc34fef53b03ef28f31`  
		Last Modified: Fri, 31 Mar 2023 22:30:40 GMT  
		Size: 50.5 MB (50496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23deb01b847d9dd0fc43ede2d2dacda423b95fdbf64e0ce21a6f542f6a167e`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bda3b184ea984d363fc64e635076bcb405620effc23b2eac44f23e662bfd57`  
		Last Modified: Fri, 31 Mar 2023 23:25:05 GMT  
		Size: 983.7 KB (983706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed17edbc6604e6a5d584a08fa036d3d0711dde7676b4a6fe0adeb03b148ba5e7`  
		Last Modified: Fri, 31 Mar 2023 23:25:03 GMT  
		Size: 4.6 MB (4585198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a94a6acfa729dcf5f76be5966ecdc31692840ba7619f81d82d5e6dfc717c03`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 2.7 KB (2653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3686cf92b89d34f1d5ef195eae6471104f3a875645541473e013e18d4b595e5e`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81535a6a8bfbe8280ee0edbb4f5e8472a38785d2c36fd5c59b85996314f8ad4`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 25.5 MB (25532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bffb03ea5e2bb6d0867f6130190cdd297dc62dcd87b40f33ef7242ae6c76106`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49348ef8dcaad9bf9de316da06cf84291bcbeb9dd40b063fc9dfe852e4e3f0fc`  
		Last Modified: Fri, 31 Mar 2023 23:25:09 GMT  
		Size: 48.4 MB (48449817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509d665d0cf5e0b271d7d16a0f0fd46a59006b6c62a8e860701622fa702a2826`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc919b937fd60ace9e14a4d9963cdadb2f1939b0c5501cb83caf17f50eb4cfd`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:c4e3a2c745f7f07baf8c31e1f77f5ca1bb9a0a9deae13eb723f552cb196abb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:4f93278b6e87ce3c88366f6bd4d21822ac8f70d94b3bbe2f4c2a1c612e899522
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162692772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcfde5007783863b4085f7d7ce7f3298e676683df916f92a7e2b1a923274d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:31:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:31:14 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:31:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:31:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:31:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:31:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:31:31 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 12 Apr 2023 08:31:31 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Wed, 12 Apr 2023 08:31:31 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:49 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:50 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8509999956d8524e05b2eefe3a24f5e98d8874f64ec733f4c0e6575ea7dd9f`  
		Last Modified: Wed, 12 Apr 2023 08:32:50 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906b1388e5e7848b53d373a3d273ebf2410bb203a7649fa1963b02c1dcdcd89`  
		Last Modified: Wed, 12 Apr 2023 08:32:49 GMT  
		Size: 4.2 MB (4182293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e739cd0d39690dcce8976e89b341ebc218700bc704253075dc0656d49a0bf7`  
		Last Modified: Wed, 12 Apr 2023 08:32:49 GMT  
		Size: 1.4 MB (1441734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca1d6c3dbcc2cc64396e3645ef49c2e5df89ff26dd9fb87370ebde5d8bf24b`  
		Last Modified: Wed, 12 Apr 2023 08:32:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e6dcb9ed14decaba96a565bad9985c5da6f64da5d971444bfabdabb7deefb1`  
		Last Modified: Wed, 12 Apr 2023 08:32:51 GMT  
		Size: 14.1 MB (14086858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef841f838f6562f42727112bd0b64954fd7c4060b3f5dd6acd65b900bfd3b98`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc9cf51afcd1daec60ca50d245bf0dd2922ee6653811727ed0ccbfcfed1d91d`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712f6915d80a2844310456b06c064f294ef6236fda6db2e3ea3e403df6ec7417`  
		Last Modified: Wed, 12 Apr 2023 08:33:01 GMT  
		Size: 115.8 MB (115832777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66d31b25a4472d58ffe706dbf1e7acdfc090f9826bfc809f751f58b99189b34`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03eca2b719f66e40c8260b872df27a079a4c2ea81a35961259b07f8db0178314`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:bf18020f32cc5d8f5e2add516d52fbf3afc3de431457076340e938596c528171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:47b0250a983e600ab247e6f25a4c99069d4cb637fd8dc6a11a43e83a83e9308c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130056950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3447deacaa5bacab184fabbf821a785e13303b2e340465bdf7815b0284497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 22:29:01 GMT
ADD file:a14b5a8b8b6993aeee5ac6052fdf283560d65365e5bcf133ab21c4756439384a in / 
# Fri, 31 Mar 2023 22:29:01 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:23:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 23:23:04 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 23:23:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 23:23:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 23:23:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 23:23:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 23:23:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Fri, 31 Mar 2023 23:24:07 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 23:24:08 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 23:24:08 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 23:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 23:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 23:24:09 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 23:24:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83e8f2e82cc31391cd0cb4f5ba574ba5eb9708fc0f5dcc34fef53b03ef28f31`  
		Last Modified: Fri, 31 Mar 2023 22:30:40 GMT  
		Size: 50.5 MB (50496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23deb01b847d9dd0fc43ede2d2dacda423b95fdbf64e0ce21a6f542f6a167e`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bda3b184ea984d363fc64e635076bcb405620effc23b2eac44f23e662bfd57`  
		Last Modified: Fri, 31 Mar 2023 23:25:05 GMT  
		Size: 983.7 KB (983706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed17edbc6604e6a5d584a08fa036d3d0711dde7676b4a6fe0adeb03b148ba5e7`  
		Last Modified: Fri, 31 Mar 2023 23:25:03 GMT  
		Size: 4.6 MB (4585198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a94a6acfa729dcf5f76be5966ecdc31692840ba7619f81d82d5e6dfc717c03`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 2.7 KB (2653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3686cf92b89d34f1d5ef195eae6471104f3a875645541473e013e18d4b595e5e`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81535a6a8bfbe8280ee0edbb4f5e8472a38785d2c36fd5c59b85996314f8ad4`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 25.5 MB (25532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bffb03ea5e2bb6d0867f6130190cdd297dc62dcd87b40f33ef7242ae6c76106`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49348ef8dcaad9bf9de316da06cf84291bcbeb9dd40b063fc9dfe852e4e3f0fc`  
		Last Modified: Fri, 31 Mar 2023 23:25:09 GMT  
		Size: 48.4 MB (48449817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509d665d0cf5e0b271d7d16a0f0fd46a59006b6c62a8e860701622fa702a2826`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc919b937fd60ace9e14a4d9963cdadb2f1939b0c5501cb83caf17f50eb4cfd`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41`

```console
$ docker pull mysql@sha256:bf18020f32cc5d8f5e2add516d52fbf3afc3de431457076340e938596c528171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41` - linux; amd64

```console
$ docker pull mysql@sha256:47b0250a983e600ab247e6f25a4c99069d4cb637fd8dc6a11a43e83a83e9308c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130056950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3447deacaa5bacab184fabbf821a785e13303b2e340465bdf7815b0284497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 22:29:01 GMT
ADD file:a14b5a8b8b6993aeee5ac6052fdf283560d65365e5bcf133ab21c4756439384a in / 
# Fri, 31 Mar 2023 22:29:01 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:23:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 23:23:04 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 23:23:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 23:23:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 23:23:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 23:23:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 23:23:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Fri, 31 Mar 2023 23:24:07 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 23:24:08 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 23:24:08 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 23:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 23:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 23:24:09 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 23:24:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83e8f2e82cc31391cd0cb4f5ba574ba5eb9708fc0f5dcc34fef53b03ef28f31`  
		Last Modified: Fri, 31 Mar 2023 22:30:40 GMT  
		Size: 50.5 MB (50496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23deb01b847d9dd0fc43ede2d2dacda423b95fdbf64e0ce21a6f542f6a167e`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bda3b184ea984d363fc64e635076bcb405620effc23b2eac44f23e662bfd57`  
		Last Modified: Fri, 31 Mar 2023 23:25:05 GMT  
		Size: 983.7 KB (983706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed17edbc6604e6a5d584a08fa036d3d0711dde7676b4a6fe0adeb03b148ba5e7`  
		Last Modified: Fri, 31 Mar 2023 23:25:03 GMT  
		Size: 4.6 MB (4585198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a94a6acfa729dcf5f76be5966ecdc31692840ba7619f81d82d5e6dfc717c03`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 2.7 KB (2653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3686cf92b89d34f1d5ef195eae6471104f3a875645541473e013e18d4b595e5e`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81535a6a8bfbe8280ee0edbb4f5e8472a38785d2c36fd5c59b85996314f8ad4`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 25.5 MB (25532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bffb03ea5e2bb6d0867f6130190cdd297dc62dcd87b40f33ef7242ae6c76106`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49348ef8dcaad9bf9de316da06cf84291bcbeb9dd40b063fc9dfe852e4e3f0fc`  
		Last Modified: Fri, 31 Mar 2023 23:25:09 GMT  
		Size: 48.4 MB (48449817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509d665d0cf5e0b271d7d16a0f0fd46a59006b6c62a8e860701622fa702a2826`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc919b937fd60ace9e14a4d9963cdadb2f1939b0c5501cb83caf17f50eb4cfd`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-debian`

```console
$ docker pull mysql@sha256:c4e3a2c745f7f07baf8c31e1f77f5ca1bb9a0a9deae13eb723f552cb196abb9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:4f93278b6e87ce3c88366f6bd4d21822ac8f70d94b3bbe2f4c2a1c612e899522
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162692772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbcfde5007783863b4085f7d7ce7f3298e676683df916f92a7e2b1a923274d0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:25 GMT
ADD file:e614539607055bdbde0cc1a94ef9783fe3627c8553ef1b21071ecb5c27ea27e4 in / 
# Wed, 12 Apr 2023 00:20:26 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:31:09 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:31:14 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:31:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:31:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:31:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:31:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:31:31 GMT
ENV MYSQL_MAJOR=5.7
# Wed, 12 Apr 2023 08:31:31 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Wed, 12 Apr 2023 08:31:31 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:49 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:49 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:50 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9fbefa3370776b7ec7633cf07efc14cc24e0c0cd53893ad0e7e3f44ffdc1bedb`  
		Last Modified: Wed, 12 Apr 2023 00:24:22 GMT  
		Size: 27.1 MB (27138920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8509999956d8524e05b2eefe3a24f5e98d8874f64ec733f4c0e6575ea7dd9f`  
		Last Modified: Wed, 12 Apr 2023 08:32:50 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f906b1388e5e7848b53d373a3d273ebf2410bb203a7649fa1963b02c1dcdcd89`  
		Last Modified: Wed, 12 Apr 2023 08:32:49 GMT  
		Size: 4.2 MB (4182293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e739cd0d39690dcce8976e89b341ebc218700bc704253075dc0656d49a0bf7`  
		Last Modified: Wed, 12 Apr 2023 08:32:49 GMT  
		Size: 1.4 MB (1441734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ca1d6c3dbcc2cc64396e3645ef49c2e5df89ff26dd9fb87370ebde5d8bf24b`  
		Last Modified: Wed, 12 Apr 2023 08:32:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e6dcb9ed14decaba96a565bad9985c5da6f64da5d971444bfabdabb7deefb1`  
		Last Modified: Wed, 12 Apr 2023 08:32:51 GMT  
		Size: 14.1 MB (14086858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef841f838f6562f42727112bd0b64954fd7c4060b3f5dd6acd65b900bfd3b98`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc9cf51afcd1daec60ca50d245bf0dd2922ee6653811727ed0ccbfcfed1d91d`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712f6915d80a2844310456b06c064f294ef6236fda6db2e3ea3e403df6ec7417`  
		Last Modified: Wed, 12 Apr 2023 08:33:01 GMT  
		Size: 115.8 MB (115832777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66d31b25a4472d58ffe706dbf1e7acdfc090f9826bfc809f751f58b99189b34`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03eca2b719f66e40c8260b872df27a079a4c2ea81a35961259b07f8db0178314`  
		Last Modified: Wed, 12 Apr 2023 08:32:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-oracle`

```console
$ docker pull mysql@sha256:bf18020f32cc5d8f5e2add516d52fbf3afc3de431457076340e938596c528171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:47b0250a983e600ab247e6f25a4c99069d4cb637fd8dc6a11a43e83a83e9308c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130056950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3447deacaa5bacab184fabbf821a785e13303b2e340465bdf7815b0284497b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 22:29:01 GMT
ADD file:a14b5a8b8b6993aeee5ac6052fdf283560d65365e5bcf133ab21c4756439384a in / 
# Fri, 31 Mar 2023 22:29:01 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 23:23:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 23:23:04 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 23:23:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 23:23:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 31 Mar 2023 23:23:25 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Fri, 31 Mar 2023 23:23:25 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 23:23:43 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 23:23:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 23:23:44 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Fri, 31 Mar 2023 23:24:07 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 23:24:08 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 23:24:08 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 23:24:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 23:24:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 23:24:09 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 23:24:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83e8f2e82cc31391cd0cb4f5ba574ba5eb9708fc0f5dcc34fef53b03ef28f31`  
		Last Modified: Fri, 31 Mar 2023 22:30:40 GMT  
		Size: 50.5 MB (50496029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23deb01b847d9dd0fc43ede2d2dacda423b95fdbf64e0ce21a6f542f6a167e`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bda3b184ea984d363fc64e635076bcb405620effc23b2eac44f23e662bfd57`  
		Last Modified: Fri, 31 Mar 2023 23:25:05 GMT  
		Size: 983.7 KB (983706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed17edbc6604e6a5d584a08fa036d3d0711dde7676b4a6fe0adeb03b148ba5e7`  
		Last Modified: Fri, 31 Mar 2023 23:25:03 GMT  
		Size: 4.6 MB (4585198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a94a6acfa729dcf5f76be5966ecdc31692840ba7619f81d82d5e6dfc717c03`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 2.7 KB (2653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3686cf92b89d34f1d5ef195eae6471104f3a875645541473e013e18d4b595e5e`  
		Last Modified: Fri, 31 Mar 2023 23:25:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81535a6a8bfbe8280ee0edbb4f5e8472a38785d2c36fd5c59b85996314f8ad4`  
		Last Modified: Fri, 31 Mar 2023 23:25:04 GMT  
		Size: 25.5 MB (25532514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bffb03ea5e2bb6d0867f6130190cdd297dc62dcd87b40f33ef7242ae6c76106`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49348ef8dcaad9bf9de316da06cf84291bcbeb9dd40b063fc9dfe852e4e3f0fc`  
		Last Modified: Fri, 31 Mar 2023 23:25:09 GMT  
		Size: 48.4 MB (48449817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509d665d0cf5e0b271d7d16a0f0fd46a59006b6c62a8e860701622fa702a2826`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc919b937fd60ace9e14a4d9963cdadb2f1939b0c5501cb83caf17f50eb4cfd`  
		Last Modified: Fri, 31 Mar 2023 23:25:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:e83ca0235010bfdb321e6838db61bdcfcd75376e2ad7344b48f9e6274e439805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e54e01ca605ee64672bf588cd1782a669cb387954593ccd1c9dcd551598d1df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177773688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28218708df49341b2be096626a48460fdd27f50b16526c9198eca087bdfbee09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:32 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:30:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:30:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Wed, 12 Apr 2023 08:30:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 Apr 2023 08:31:03 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:04 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a04d5366306e8a589995f9f73ab93e6891f61c650a23925fb5b7390b6064595`  
		Last Modified: Wed, 12 Apr 2023 08:32:17 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba5474d63b96ac334caf465b6aa1a5de64b2013b2d04a1bfebfafff8f91fc38`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 4.4 MB (4415052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c021e7c8f4a7a4ce5520958fdb931906c4e230b830ed9b727f6cfdca9fb5869`  
		Last Modified: Wed, 12 Apr 2023 08:32:16 GMT  
		Size: 1.5 MB (1471552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3a9a62a81ba7372c6da71311f49a2bbdf341b2df76733730983af435b5103e`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02df4487ae5565f727156b1002cf5d23384f0b11f48e41459c11560fd112a5c`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9945ed239183eb77212dda7cc43cbcd8e45243e6170f8f35c607da06f841f7`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6089a839b76ce60e6835308ff44b5c5d5919e2afec303b4514e59f23a89321`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f5a3e0cd76dff603c1470b1fddebbc741ffb0b44bf38ffb90a6f5e9583d10`  
		Last Modified: Wed, 12 Apr 2023 08:32:32 GMT  
		Size: 127.8 MB (127795797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe4fd79b488e38d5c4ea7a9f20adbd65a591adb7d90a44e49f7c8d749ce9aa`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d9ed5bdeecafea3da68feb5f223f2ffec451cedc0fe1c99dc41618d32e398`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a37d470a30b7376b79582f9254c94a5d90aed021707d4ad2ea38dc485ed277`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:e83ca0235010bfdb321e6838db61bdcfcd75376e2ad7344b48f9e6274e439805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e54e01ca605ee64672bf588cd1782a669cb387954593ccd1c9dcd551598d1df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177773688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28218708df49341b2be096626a48460fdd27f50b16526c9198eca087bdfbee09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:32 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:30:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:30:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Wed, 12 Apr 2023 08:30:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 Apr 2023 08:31:03 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:04 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a04d5366306e8a589995f9f73ab93e6891f61c650a23925fb5b7390b6064595`  
		Last Modified: Wed, 12 Apr 2023 08:32:17 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba5474d63b96ac334caf465b6aa1a5de64b2013b2d04a1bfebfafff8f91fc38`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 4.4 MB (4415052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c021e7c8f4a7a4ce5520958fdb931906c4e230b830ed9b727f6cfdca9fb5869`  
		Last Modified: Wed, 12 Apr 2023 08:32:16 GMT  
		Size: 1.5 MB (1471552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3a9a62a81ba7372c6da71311f49a2bbdf341b2df76733730983af435b5103e`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02df4487ae5565f727156b1002cf5d23384f0b11f48e41459c11560fd112a5c`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9945ed239183eb77212dda7cc43cbcd8e45243e6170f8f35c607da06f841f7`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6089a839b76ce60e6835308ff44b5c5d5919e2afec303b4514e59f23a89321`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f5a3e0cd76dff603c1470b1fddebbc741ffb0b44bf38ffb90a6f5e9583d10`  
		Last Modified: Wed, 12 Apr 2023 08:32:32 GMT  
		Size: 127.8 MB (127795797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe4fd79b488e38d5c4ea7a9f20adbd65a591adb7d90a44e49f7c8d749ce9aa`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d9ed5bdeecafea3da68feb5f223f2ffec451cedc0fe1c99dc41618d32e398`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a37d470a30b7376b79582f9254c94a5d90aed021707d4ad2ea38dc485ed277`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-debian`

```console
$ docker pull mysql@sha256:e83ca0235010bfdb321e6838db61bdcfcd75376e2ad7344b48f9e6274e439805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.32-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e54e01ca605ee64672bf588cd1782a669cb387954593ccd1c9dcd551598d1df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177773688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28218708df49341b2be096626a48460fdd27f50b16526c9198eca087bdfbee09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:32 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:30:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:30:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Wed, 12 Apr 2023 08:30:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 Apr 2023 08:31:03 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:04 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a04d5366306e8a589995f9f73ab93e6891f61c650a23925fb5b7390b6064595`  
		Last Modified: Wed, 12 Apr 2023 08:32:17 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba5474d63b96ac334caf465b6aa1a5de64b2013b2d04a1bfebfafff8f91fc38`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 4.4 MB (4415052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c021e7c8f4a7a4ce5520958fdb931906c4e230b830ed9b727f6cfdca9fb5869`  
		Last Modified: Wed, 12 Apr 2023 08:32:16 GMT  
		Size: 1.5 MB (1471552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3a9a62a81ba7372c6da71311f49a2bbdf341b2df76733730983af435b5103e`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02df4487ae5565f727156b1002cf5d23384f0b11f48e41459c11560fd112a5c`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9945ed239183eb77212dda7cc43cbcd8e45243e6170f8f35c607da06f841f7`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6089a839b76ce60e6835308ff44b5c5d5919e2afec303b4514e59f23a89321`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f5a3e0cd76dff603c1470b1fddebbc741ffb0b44bf38ffb90a6f5e9583d10`  
		Last Modified: Wed, 12 Apr 2023 08:32:32 GMT  
		Size: 127.8 MB (127795797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe4fd79b488e38d5c4ea7a9f20adbd65a591adb7d90a44e49f7c8d749ce9aa`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d9ed5bdeecafea3da68feb5f223f2ffec451cedc0fe1c99dc41618d32e398`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a37d470a30b7376b79582f9254c94a5d90aed021707d4ad2ea38dc485ed277`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-oracle`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:e83ca0235010bfdb321e6838db61bdcfcd75376e2ad7344b48f9e6274e439805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e54e01ca605ee64672bf588cd1782a669cb387954593ccd1c9dcd551598d1df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177773688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28218708df49341b2be096626a48460fdd27f50b16526c9198eca087bdfbee09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:32 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:30:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:30:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Wed, 12 Apr 2023 08:30:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 Apr 2023 08:31:03 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:04 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a04d5366306e8a589995f9f73ab93e6891f61c650a23925fb5b7390b6064595`  
		Last Modified: Wed, 12 Apr 2023 08:32:17 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba5474d63b96ac334caf465b6aa1a5de64b2013b2d04a1bfebfafff8f91fc38`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 4.4 MB (4415052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c021e7c8f4a7a4ce5520958fdb931906c4e230b830ed9b727f6cfdca9fb5869`  
		Last Modified: Wed, 12 Apr 2023 08:32:16 GMT  
		Size: 1.5 MB (1471552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3a9a62a81ba7372c6da71311f49a2bbdf341b2df76733730983af435b5103e`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02df4487ae5565f727156b1002cf5d23384f0b11f48e41459c11560fd112a5c`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9945ed239183eb77212dda7cc43cbcd8e45243e6170f8f35c607da06f841f7`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6089a839b76ce60e6835308ff44b5c5d5919e2afec303b4514e59f23a89321`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f5a3e0cd76dff603c1470b1fddebbc741ffb0b44bf38ffb90a6f5e9583d10`  
		Last Modified: Wed, 12 Apr 2023 08:32:32 GMT  
		Size: 127.8 MB (127795797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe4fd79b488e38d5c4ea7a9f20adbd65a591adb7d90a44e49f7c8d749ce9aa`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d9ed5bdeecafea3da68feb5f223f2ffec451cedc0fe1c99dc41618d32e398`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a37d470a30b7376b79582f9254c94a5d90aed021707d4ad2ea38dc485ed277`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:f496c25da703053a6e0717f1d52092205775304ea57535cc9fcaa6f35867800b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:c86dfd69b3d1437e5d192447f0bdc57407d48bd379b97a453e11d72b97962e3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156537781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b8cc72e4a28e086097c3fcb1ca391beaefe86bc421a57bc53f7596461ce3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:20:31 GMT
ADD file:61a2085af5116916e7b117c2e7ad7116bdc0282d8fa9ce76191c4101f5e866ff in / 
# Thu, 06 Apr 2023 18:20:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:43:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:43:29 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:43:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:43:56 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:43:58 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:43:58 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:44:29 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:44:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:44:30 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:45:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:45:05 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:45:05 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:45:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:45:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:45:06 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:45:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:328ba678bf27575937f8b9dfbf5b5f39b21941af068f8e5960de8131e289da85`  
		Last Modified: Thu, 06 Apr 2023 18:21:19 GMT  
		Size: 44.6 MB (44563902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f5ff008d73bef1d4c8e1a4c73a7efc7697e8087a950065fb369c83a03df08d`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7054d6d0c7c57672cd9e48e8a92eda15a4f0ae24dc78413fdce3fce3064a77`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 982.8 KB (982819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b5d4e8750e78990227fa3f3df12b6ccdf3b2486b4248677b7959dd95c0e77b`  
		Last Modified: Thu, 06 Apr 2023 18:45:41 GMT  
		Size: 4.6 MB (4608287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc4a7b43bdd822158ae54cac5da309097088de0253879cbb07e31829d8f4561`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9c0b61a8f3ab0cb6ee9094ebcf1ce53269d267ca59797630f181d2df6b8b85`  
		Last Modified: Thu, 06 Apr 2023 18:45:39 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806a08b6c085f3679c3209e729afe0384bba01916fd388fecb139aec18e394c5`  
		Last Modified: Thu, 06 Apr 2023 18:45:46 GMT  
		Size: 56.2 MB (56202024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b2cebd832f6d6ea73a28b2880ed13c26f43c56ea6e762c0a9d1048e5ce834`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad31ba45b26b6b9dfa92a089a49c5c15e123bead7b7a6163e78911c45c12857b`  
		Last Modified: Thu, 06 Apr 2023 18:45:47 GMT  
		Size: 50.2 MB (50171069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4c2bd59d1c615ab233b0f79c0c2108c26b9923bbc433651505e4970bd08ca3`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148dcef42e3b313097040f66cbf47cc1f31f870e53d57d32837d4f5963b3fb2c`  
		Last Modified: Thu, 06 Apr 2023 18:45:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6b6a9ff1092a3aad91ceb61eae1a78b2d43b5a80be2de05b269ec2403ae03b40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155461000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21978c3803cadf60e8a2bd2723372465082383f95b0b9dc8732db719de6d259f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 06 Apr 2023 18:40:07 GMT
ADD file:c798bcae4b9271a204dc37f132bce1f0042c02cb1ad5a2237f56dec227d44438 in / 
# Thu, 06 Apr 2023 18:40:07 GMT
CMD ["/bin/bash"]
# Thu, 06 Apr 2023 18:55:56 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 06 Apr 2023 18:55:56 GMT
ENV GOSU_VERSION=1.16
# Thu, 06 Apr 2023 18:55:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 06 Apr 2023 18:56:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 06 Apr 2023 18:56:27 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:56:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 06 Apr 2023 18:56:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 06 Apr 2023 18:56:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 06 Apr 2023 18:56:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Thu, 06 Apr 2023 18:57:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 06 Apr 2023 18:57:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 06 Apr 2023 18:57:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Thu, 06 Apr 2023 18:57:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 06 Apr 2023 18:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 06 Apr 2023 18:57:33 GMT
EXPOSE 3306 33060
# Thu, 06 Apr 2023 18:57:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6425367b44c9c3f59fd1e81f8fa2e9170ca2ef552d63f35a08ef3969ee4ff557`  
		Last Modified: Thu, 06 Apr 2023 18:40:43 GMT  
		Size: 43.5 MB (43477048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cef374d113a386d9e9eb540635c8e0d47e85deb38985982b5aeddc4798f67c7`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1751ddbc0d77eedc43d2aad156c590e2fec2c2f75fde0aef0757c69a0ba49f6d`  
		Last Modified: Thu, 06 Apr 2023 18:57:59 GMT  
		Size: 913.0 KB (912995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41e9e3c6d9abdfec73965f0105ee343f69e0c909c07b665ea81a2642e19365f`  
		Last Modified: Thu, 06 Apr 2023 18:57:58 GMT  
		Size: 4.5 MB (4465472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26e9c11cd2da41af092e3a224bcb367ba5201e02509f5e39bf009085eafe838`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 2.6 KB (2627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86abc2724c488e3a2873ea2be6352e0ee8dd16f2549ca85a445be408b5e871bd`  
		Last Modified: Thu, 06 Apr 2023 18:57:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fff401a325b71d640265f21c0f0245e05bf98a78e3e3a573f1819f0a07dd221`  
		Last Modified: Thu, 06 Apr 2023 18:58:01 GMT  
		Size: 55.6 MB (55605546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08f29b17c274e86657777b30c3eefdee4bacc6c03b0cfba4b1b7936f2191a9`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46bc4d9c3488fb3d8f55c494cd0b33e3bfe166e4a11fcdb90ec56cccd58c1f4b`  
		Last Modified: Thu, 06 Apr 2023 18:58:03 GMT  
		Size: 51.0 MB (50990261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa0499c02dddce545e072791626b1769c83e17d78855d2b75550eb5ef0ec9a7`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887e90506ede77b60f6bdcec3fdd19a3ffd2af0a295feaa0641d007c94680f52`  
		Last Modified: Thu, 06 Apr 2023 18:57:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
