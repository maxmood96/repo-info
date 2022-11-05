<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.40`](#mysql5740)
-	[`mysql:5.7.40-debian`](#mysql5740-debian)
-	[`mysql:5.7.40-oracle`](#mysql5740-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.31`](#mysql8031)
-	[`mysql:8.0.31-debian`](#mysql8031-debian)
-	[`mysql:8.0.31-oracle`](#mysql8031-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:0e3435e72c493aec752d8274379b1eac4d634f47a7781a7a92b8636fa1dc94c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:55d2f4aa17fd27821a7fc575d2921485681a8aa5ac8411b75d7a163d895dfba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144285975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef0fab001e8dea739d538688b09e162bf54dd6c2bc04066bff99b5335cd6223`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:35 GMT
ADD file:aaaadfdf901c2df5f641e6c43b10817fcbd0caca73acb7672608f43ba71cefeb in / 
# Fri, 04 Nov 2022 23:33:36 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:36:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:36:26 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:36:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:36:47 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:37:06 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:37:07 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:37:07 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Sat, 05 Nov 2022 02:37:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:37:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:37:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:37:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:37:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:37:33 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:37:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a0b9cd2dfe62ff7a933afe41891425abf01b0aaed70cedb028f03392d60037f`  
		Last Modified: Fri, 04 Nov 2022 23:35:26 GMT  
		Size: 49.8 MB (49827924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c637408ee7df7cd6e62a9fede4cb967dfff2c78d5fc9696bdda5753e03cffb0c`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c517093c276008b69d7c9ae4e322cd0e97369293f972c009ab6e3ac05f50798`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cc7d68c2a6517d07d136b6dd69d0ba624db02c2b425b85cd5095463498328`  
		Last Modified: Sat, 05 Nov 2022 02:38:54 GMT  
		Size: 4.5 MB (4538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca9bf9231a468ca8e638952c4e25435965f5446e72162f87740f3852574421`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 2.7 KB (2655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae101e5c786802330f0f482df1b4c751a8dc07bc7977bd05a7dcd22e3421ed7`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04baa409344ebae1d939845540196f7a24ba0db7da5aea2fb2bdf7b93913ef8a`  
		Last Modified: Sat, 05 Nov 2022 02:38:55 GMT  
		Size: 25.5 MB (25530141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b6015bf8537db46f7559e2a143a18db66ba37fafb8ddb3ede1a008631026a2`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6005bb052ef827d58b0bb7daa74921592043a9057f71c7f55f616dd53df1beb7`  
		Last Modified: Sat, 05 Nov 2022 02:39:03 GMT  
		Size: 63.4 MB (63449434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f303d570503342f3a4d383aad6093f58fdc135006c2e1a6155ec8549daa63d`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a9a80c1df068cf45f516b05f99daa1b06825919403e44324c66ef15d2cdbb`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:5e635c84607a845d3e047e7408857451084f279909fdd327130b9f4ef0cc2fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:404888dcc38122f46785bc7e60cd06876cb5f6197acb113c50c4980ef013a131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43d9c52e05e2a26e663b1b48bbf1729cc5ba64f1bb8fa5533108762db8f434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:08:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:09:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:09:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:09:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 25 Oct 2022 04:09:11 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 25 Oct 2022 04:09:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:09:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:09:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:09:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:09:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:09:32 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:09:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059edac3aef17c3091953acf82cd6ad2e31910b4fbc27ec2425c02e53b1493`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07515d4341a353a0625e0a892a555254e1d79a2404e9e0eb3805ba5386b8f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:41 GMT  
		Size: 4.2 MB (4182256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633aa3637fd05c7e011322a68ce50d9b2a6fb38661555106c3d365c03e8c8495`  
		Last Modified: Tue, 25 Oct 2022 04:10:40 GMT  
		Size: 1.4 MB (1388862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76bbd35d5959d0771fa34770dd4b62b95182bb8eab9ad298355998252c31c48`  
		Last Modified: Tue, 25 Oct 2022 04:10:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d35b4452aa509eb9742ba3f45d42469fd0041a9be3ddb6ba7f18d3ebb6bf7`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 14.1 MB (14089435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344c9b35352e2a1940bbc242656fe4bf4da1c33bfdef6c5492082dd22a84424`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff5eb436cc3aaa4a5b92c86d0bf978a1a92538f11edeb159cf2f96048f0c94`  
		Last Modified: Tue, 25 Oct 2022 04:10:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da69d8bcdc1d21659d1d4957e0b442128ee0f8b5a26ad2873212abe592e557`  
		Last Modified: Tue, 25 Oct 2022 04:10:53 GMT  
		Size: 115.8 MB (115785755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78147effd009e90fee4d441176b823bdddd38fb6e64c0920eb8938d106d299f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb5c0492fcf8cb70b8b6000f76206d520baf253aab77d11538911b5cf73aad`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:0e3435e72c493aec752d8274379b1eac4d634f47a7781a7a92b8636fa1dc94c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:55d2f4aa17fd27821a7fc575d2921485681a8aa5ac8411b75d7a163d895dfba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144285975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef0fab001e8dea739d538688b09e162bf54dd6c2bc04066bff99b5335cd6223`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:35 GMT
ADD file:aaaadfdf901c2df5f641e6c43b10817fcbd0caca73acb7672608f43ba71cefeb in / 
# Fri, 04 Nov 2022 23:33:36 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:36:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:36:26 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:36:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:36:47 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:37:06 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:37:07 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:37:07 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Sat, 05 Nov 2022 02:37:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:37:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:37:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:37:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:37:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:37:33 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:37:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a0b9cd2dfe62ff7a933afe41891425abf01b0aaed70cedb028f03392d60037f`  
		Last Modified: Fri, 04 Nov 2022 23:35:26 GMT  
		Size: 49.8 MB (49827924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c637408ee7df7cd6e62a9fede4cb967dfff2c78d5fc9696bdda5753e03cffb0c`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c517093c276008b69d7c9ae4e322cd0e97369293f972c009ab6e3ac05f50798`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cc7d68c2a6517d07d136b6dd69d0ba624db02c2b425b85cd5095463498328`  
		Last Modified: Sat, 05 Nov 2022 02:38:54 GMT  
		Size: 4.5 MB (4538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca9bf9231a468ca8e638952c4e25435965f5446e72162f87740f3852574421`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 2.7 KB (2655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae101e5c786802330f0f482df1b4c751a8dc07bc7977bd05a7dcd22e3421ed7`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04baa409344ebae1d939845540196f7a24ba0db7da5aea2fb2bdf7b93913ef8a`  
		Last Modified: Sat, 05 Nov 2022 02:38:55 GMT  
		Size: 25.5 MB (25530141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b6015bf8537db46f7559e2a143a18db66ba37fafb8ddb3ede1a008631026a2`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6005bb052ef827d58b0bb7daa74921592043a9057f71c7f55f616dd53df1beb7`  
		Last Modified: Sat, 05 Nov 2022 02:39:03 GMT  
		Size: 63.4 MB (63449434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f303d570503342f3a4d383aad6093f58fdc135006c2e1a6155ec8549daa63d`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a9a80c1df068cf45f516b05f99daa1b06825919403e44324c66ef15d2cdbb`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:0e3435e72c493aec752d8274379b1eac4d634f47a7781a7a92b8636fa1dc94c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:55d2f4aa17fd27821a7fc575d2921485681a8aa5ac8411b75d7a163d895dfba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144285975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef0fab001e8dea739d538688b09e162bf54dd6c2bc04066bff99b5335cd6223`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:35 GMT
ADD file:aaaadfdf901c2df5f641e6c43b10817fcbd0caca73acb7672608f43ba71cefeb in / 
# Fri, 04 Nov 2022 23:33:36 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:36:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:36:26 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:36:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:36:47 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:37:06 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:37:07 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:37:07 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Sat, 05 Nov 2022 02:37:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:37:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:37:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:37:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:37:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:37:33 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:37:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a0b9cd2dfe62ff7a933afe41891425abf01b0aaed70cedb028f03392d60037f`  
		Last Modified: Fri, 04 Nov 2022 23:35:26 GMT  
		Size: 49.8 MB (49827924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c637408ee7df7cd6e62a9fede4cb967dfff2c78d5fc9696bdda5753e03cffb0c`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c517093c276008b69d7c9ae4e322cd0e97369293f972c009ab6e3ac05f50798`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cc7d68c2a6517d07d136b6dd69d0ba624db02c2b425b85cd5095463498328`  
		Last Modified: Sat, 05 Nov 2022 02:38:54 GMT  
		Size: 4.5 MB (4538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca9bf9231a468ca8e638952c4e25435965f5446e72162f87740f3852574421`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 2.7 KB (2655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae101e5c786802330f0f482df1b4c751a8dc07bc7977bd05a7dcd22e3421ed7`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04baa409344ebae1d939845540196f7a24ba0db7da5aea2fb2bdf7b93913ef8a`  
		Last Modified: Sat, 05 Nov 2022 02:38:55 GMT  
		Size: 25.5 MB (25530141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b6015bf8537db46f7559e2a143a18db66ba37fafb8ddb3ede1a008631026a2`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6005bb052ef827d58b0bb7daa74921592043a9057f71c7f55f616dd53df1beb7`  
		Last Modified: Sat, 05 Nov 2022 02:39:03 GMT  
		Size: 63.4 MB (63449434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f303d570503342f3a4d383aad6093f58fdc135006c2e1a6155ec8549daa63d`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a9a80c1df068cf45f516b05f99daa1b06825919403e44324c66ef15d2cdbb`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:5e635c84607a845d3e047e7408857451084f279909fdd327130b9f4ef0cc2fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:404888dcc38122f46785bc7e60cd06876cb5f6197acb113c50c4980ef013a131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43d9c52e05e2a26e663b1b48bbf1729cc5ba64f1bb8fa5533108762db8f434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:08:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:09:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:09:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:09:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 25 Oct 2022 04:09:11 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 25 Oct 2022 04:09:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:09:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:09:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:09:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:09:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:09:32 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:09:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059edac3aef17c3091953acf82cd6ad2e31910b4fbc27ec2425c02e53b1493`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07515d4341a353a0625e0a892a555254e1d79a2404e9e0eb3805ba5386b8f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:41 GMT  
		Size: 4.2 MB (4182256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633aa3637fd05c7e011322a68ce50d9b2a6fb38661555106c3d365c03e8c8495`  
		Last Modified: Tue, 25 Oct 2022 04:10:40 GMT  
		Size: 1.4 MB (1388862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76bbd35d5959d0771fa34770dd4b62b95182bb8eab9ad298355998252c31c48`  
		Last Modified: Tue, 25 Oct 2022 04:10:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d35b4452aa509eb9742ba3f45d42469fd0041a9be3ddb6ba7f18d3ebb6bf7`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 14.1 MB (14089435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344c9b35352e2a1940bbc242656fe4bf4da1c33bfdef6c5492082dd22a84424`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff5eb436cc3aaa4a5b92c86d0bf978a1a92538f11edeb159cf2f96048f0c94`  
		Last Modified: Tue, 25 Oct 2022 04:10:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da69d8bcdc1d21659d1d4957e0b442128ee0f8b5a26ad2873212abe592e557`  
		Last Modified: Tue, 25 Oct 2022 04:10:53 GMT  
		Size: 115.8 MB (115785755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78147effd009e90fee4d441176b823bdddd38fb6e64c0920eb8938d106d299f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb5c0492fcf8cb70b8b6000f76206d520baf253aab77d11538911b5cf73aad`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:0e3435e72c493aec752d8274379b1eac4d634f47a7781a7a92b8636fa1dc94c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:55d2f4aa17fd27821a7fc575d2921485681a8aa5ac8411b75d7a163d895dfba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144285975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef0fab001e8dea739d538688b09e162bf54dd6c2bc04066bff99b5335cd6223`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:35 GMT
ADD file:aaaadfdf901c2df5f641e6c43b10817fcbd0caca73acb7672608f43ba71cefeb in / 
# Fri, 04 Nov 2022 23:33:36 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:36:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:36:26 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:36:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:36:47 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:37:06 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:37:07 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:37:07 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Sat, 05 Nov 2022 02:37:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:37:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:37:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:37:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:37:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:37:33 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:37:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a0b9cd2dfe62ff7a933afe41891425abf01b0aaed70cedb028f03392d60037f`  
		Last Modified: Fri, 04 Nov 2022 23:35:26 GMT  
		Size: 49.8 MB (49827924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c637408ee7df7cd6e62a9fede4cb967dfff2c78d5fc9696bdda5753e03cffb0c`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c517093c276008b69d7c9ae4e322cd0e97369293f972c009ab6e3ac05f50798`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cc7d68c2a6517d07d136b6dd69d0ba624db02c2b425b85cd5095463498328`  
		Last Modified: Sat, 05 Nov 2022 02:38:54 GMT  
		Size: 4.5 MB (4538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca9bf9231a468ca8e638952c4e25435965f5446e72162f87740f3852574421`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 2.7 KB (2655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae101e5c786802330f0f482df1b4c751a8dc07bc7977bd05a7dcd22e3421ed7`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04baa409344ebae1d939845540196f7a24ba0db7da5aea2fb2bdf7b93913ef8a`  
		Last Modified: Sat, 05 Nov 2022 02:38:55 GMT  
		Size: 25.5 MB (25530141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b6015bf8537db46f7559e2a143a18db66ba37fafb8ddb3ede1a008631026a2`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6005bb052ef827d58b0bb7daa74921592043a9057f71c7f55f616dd53df1beb7`  
		Last Modified: Sat, 05 Nov 2022 02:39:03 GMT  
		Size: 63.4 MB (63449434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f303d570503342f3a4d383aad6093f58fdc135006c2e1a6155ec8549daa63d`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a9a80c1df068cf45f516b05f99daa1b06825919403e44324c66ef15d2cdbb`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40`

```console
$ docker pull mysql@sha256:0e3435e72c493aec752d8274379b1eac4d634f47a7781a7a92b8636fa1dc94c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40` - linux; amd64

```console
$ docker pull mysql@sha256:55d2f4aa17fd27821a7fc575d2921485681a8aa5ac8411b75d7a163d895dfba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144285975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef0fab001e8dea739d538688b09e162bf54dd6c2bc04066bff99b5335cd6223`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:35 GMT
ADD file:aaaadfdf901c2df5f641e6c43b10817fcbd0caca73acb7672608f43ba71cefeb in / 
# Fri, 04 Nov 2022 23:33:36 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:36:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:36:26 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:36:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:36:47 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:37:06 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:37:07 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:37:07 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Sat, 05 Nov 2022 02:37:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:37:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:37:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:37:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:37:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:37:33 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:37:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a0b9cd2dfe62ff7a933afe41891425abf01b0aaed70cedb028f03392d60037f`  
		Last Modified: Fri, 04 Nov 2022 23:35:26 GMT  
		Size: 49.8 MB (49827924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c637408ee7df7cd6e62a9fede4cb967dfff2c78d5fc9696bdda5753e03cffb0c`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c517093c276008b69d7c9ae4e322cd0e97369293f972c009ab6e3ac05f50798`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cc7d68c2a6517d07d136b6dd69d0ba624db02c2b425b85cd5095463498328`  
		Last Modified: Sat, 05 Nov 2022 02:38:54 GMT  
		Size: 4.5 MB (4538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca9bf9231a468ca8e638952c4e25435965f5446e72162f87740f3852574421`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 2.7 KB (2655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae101e5c786802330f0f482df1b4c751a8dc07bc7977bd05a7dcd22e3421ed7`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04baa409344ebae1d939845540196f7a24ba0db7da5aea2fb2bdf7b93913ef8a`  
		Last Modified: Sat, 05 Nov 2022 02:38:55 GMT  
		Size: 25.5 MB (25530141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b6015bf8537db46f7559e2a143a18db66ba37fafb8ddb3ede1a008631026a2`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6005bb052ef827d58b0bb7daa74921592043a9057f71c7f55f616dd53df1beb7`  
		Last Modified: Sat, 05 Nov 2022 02:39:03 GMT  
		Size: 63.4 MB (63449434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f303d570503342f3a4d383aad6093f58fdc135006c2e1a6155ec8549daa63d`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a9a80c1df068cf45f516b05f99daa1b06825919403e44324c66ef15d2cdbb`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40-debian`

```console
$ docker pull mysql@sha256:5e635c84607a845d3e047e7408857451084f279909fdd327130b9f4ef0cc2fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40-debian` - linux; amd64

```console
$ docker pull mysql@sha256:404888dcc38122f46785bc7e60cd06876cb5f6197acb113c50c4980ef013a131
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee43d9c52e05e2a26e663b1b48bbf1729cc5ba64f1bb8fa5533108762db8f434`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:12 GMT
ADD file:14c4aa7a136ce9eb1fae0ba0f394509990d44126be801a2713cf8722fbb2e6b9 in / 
# Tue, 25 Oct 2022 01:44:12 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:08:47 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:09:02 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:09:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:09:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:09:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 25 Oct 2022 04:09:11 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 25 Oct 2022 04:09:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:09:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:09:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:09:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:09:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:09:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:09:32 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:09:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4500a762c54620411ae491a547c66b61d577c1369ecbf5a7e91b4e153181854b`  
		Last Modified: Tue, 25 Oct 2022 01:48:40 GMT  
		Size: 27.1 MB (27140832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059edac3aef17c3091953acf82cd6ad2e31910b4fbc27ec2425c02e53b1493`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c07515d4341a353a0625e0a892a555254e1d79a2404e9e0eb3805ba5386b8f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:41 GMT  
		Size: 4.2 MB (4182256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633aa3637fd05c7e011322a68ce50d9b2a6fb38661555106c3d365c03e8c8495`  
		Last Modified: Tue, 25 Oct 2022 04:10:40 GMT  
		Size: 1.4 MB (1388862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76bbd35d5959d0771fa34770dd4b62b95182bb8eab9ad298355998252c31c48`  
		Last Modified: Tue, 25 Oct 2022 04:10:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4d35b4452aa509eb9742ba3f45d42469fd0041a9be3ddb6ba7f18d3ebb6bf7`  
		Last Modified: Tue, 25 Oct 2022 04:10:42 GMT  
		Size: 14.1 MB (14089435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6344c9b35352e2a1940bbc242656fe4bf4da1c33bfdef6c5492082dd22a84424`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff5eb436cc3aaa4a5b92c86d0bf978a1a92538f11edeb159cf2f96048f0c94`  
		Last Modified: Tue, 25 Oct 2022 04:10:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da69d8bcdc1d21659d1d4957e0b442128ee0f8b5a26ad2873212abe592e557`  
		Last Modified: Tue, 25 Oct 2022 04:10:53 GMT  
		Size: 115.8 MB (115785755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78147effd009e90fee4d441176b823bdddd38fb6e64c0920eb8938d106d299f6`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92bb5c0492fcf8cb70b8b6000f76206d520baf253aab77d11538911b5cf73aad`  
		Last Modified: Tue, 25 Oct 2022 04:10:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40-oracle`

```console
$ docker pull mysql@sha256:0e3435e72c493aec752d8274379b1eac4d634f47a7781a7a92b8636fa1dc94c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:55d2f4aa17fd27821a7fc575d2921485681a8aa5ac8411b75d7a163d895dfba1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144285975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef0fab001e8dea739d538688b09e162bf54dd6c2bc04066bff99b5335cd6223`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:35 GMT
ADD file:aaaadfdf901c2df5f641e6c43b10817fcbd0caca73acb7672608f43ba71cefeb in / 
# Fri, 04 Nov 2022 23:33:36 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:36:26 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:36:26 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:36:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:36:47 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 05 Nov 2022 02:36:48 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Sat, 05 Nov 2022 02:36:48 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:37:06 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:37:07 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:37:07 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Sat, 05 Nov 2022 02:37:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:37:32 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:37:32 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:37:33 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:37:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:37:33 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:37:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a0b9cd2dfe62ff7a933afe41891425abf01b0aaed70cedb028f03392d60037f`  
		Last Modified: Fri, 04 Nov 2022 23:35:26 GMT  
		Size: 49.8 MB (49827924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c637408ee7df7cd6e62a9fede4cb967dfff2c78d5fc9696bdda5753e03cffb0c`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c517093c276008b69d7c9ae4e322cd0e97369293f972c009ab6e3ac05f50798`  
		Last Modified: Sat, 05 Nov 2022 02:38:56 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cc7d68c2a6517d07d136b6dd69d0ba624db02c2b425b85cd5095463498328`  
		Last Modified: Sat, 05 Nov 2022 02:38:54 GMT  
		Size: 4.5 MB (4538562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ca9bf9231a468ca8e638952c4e25435965f5446e72162f87740f3852574421`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 2.7 KB (2655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae101e5c786802330f0f482df1b4c751a8dc07bc7977bd05a7dcd22e3421ed7`  
		Last Modified: Sat, 05 Nov 2022 02:38:53 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04baa409344ebae1d939845540196f7a24ba0db7da5aea2fb2bdf7b93913ef8a`  
		Last Modified: Sat, 05 Nov 2022 02:38:55 GMT  
		Size: 25.5 MB (25530141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b6015bf8537db46f7559e2a143a18db66ba37fafb8ddb3ede1a008631026a2`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6005bb052ef827d58b0bb7daa74921592043a9057f71c7f55f616dd53df1beb7`  
		Last Modified: Sat, 05 Nov 2022 02:39:03 GMT  
		Size: 63.4 MB (63449434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f303d570503342f3a4d383aad6093f58fdc135006c2e1a6155ec8549daa63d`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a9a80c1df068cf45f516b05f99daa1b06825919403e44324c66ef15d2cdbb`  
		Last Modified: Sat, 05 Nov 2022 02:38:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.31` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.31` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31-debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.31-debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31-oracle`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.31-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.31-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:ffafc1726ac6bf6b10d07a2e5a150c827a777ab99cb6db94a0efe58dd67d1a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:646002f07f3db3a3b72cc18003502d19fff01087edaf8109f001e663bf150f45
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177574213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1633d83240cb4bd4aad272d24e698576dc386c64e96b66df2de50e073ab994`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 04:07:56 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 25 Oct 2022 04:08:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 25 Oct 2022 04:08:10 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 25 Oct 2022 04:08:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 25 Oct 2022 04:08:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 04:08:18 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Oct 2022 04:08:18 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 25 Oct 2022 04:08:19 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Oct 2022 04:08:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Oct 2022 04:08:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Oct 2022 04:08:34 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Oct 2022 04:08:35 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Oct 2022 04:08:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Oct 2022 04:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Oct 2022 04:08:35 GMT
EXPOSE 3306 33060
# Tue, 25 Oct 2022 04:08:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cb2f1dc0c299aa27b9798599b29b9fcb17ddd8a88851efe3933787d953776e`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03008f2cf7e68cf1f24a12ec42187ae403f60826c4b5b1d176587f5d2f2424c`  
		Last Modified: Tue, 25 Oct 2022 04:10:04 GMT  
		Size: 4.4 MB (4415505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d344900ccc214009349407ef0b22b89f5fd04fd4336987d11ec3766c739c2c`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 1.4 MB (1419552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63d306dfeafb7a7d8ae0dadb9cc4d20a08c3013eaa78f20c3dadc1ec2e03389`  
		Last Modified: Tue, 25 Oct 2022 04:10:02 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37a6e488ddfe94964d5fab5ec6f0c19e9337bae9dd9db3f9c288c3c8be1d78e`  
		Last Modified: Tue, 25 Oct 2022 04:10:05 GMT  
		Size: 12.7 MB (12662660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:654714d6b537232e1e9b38635a37d603f9ed1e146856fb06a35fb3d6a560c46f`  
		Last Modified: Tue, 25 Oct 2022 04:10:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a15b533b284b5f92f5980d1e8211c57226c3bf5ad85d7c295e2c53a2860ab5`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e328312ef69e0c89c920b6390cee8f9f4e352a5b2b7c8dddd1bd15d666753c9`  
		Last Modified: Tue, 25 Oct 2022 04:10:19 GMT  
		Size: 127.6 MB (127645425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7db89f2542a0797193200f7c2e7c80d8affa8fdba7113ba0fb51292645e4d851`  
		Last Modified: Tue, 25 Oct 2022 04:10:00 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbcd220112ba48dda4876c2bf9b129988cbeb66c1c01c8a85a16f0b9dc2a17`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2904d017323530a2501fdcb6b806db30310e0e4957cacb5d853037707dbbad03`  
		Last Modified: Tue, 25 Oct 2022 04:09:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:717e6f25ed8997b7ecb0408e063c4dcba202a68b341ebac4c4d97f51439b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:bd6a2996d80605c41b1ebd8f822894471695b1fd2427505ac518e650a14ef8c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.2 MB (157232215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04bf34fdf036292486d39f731cffaf0bb56522c340fe4841b2c71cf89c9d62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 23:33:07 GMT
ADD file:00e6899b8d3eccf7f795d17f9316af6ae0f3955ef2204b61bd064f5173c18357 in / 
# Fri, 04 Nov 2022 23:33:07 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 02:34:46 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 02:34:46 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 02:34:50 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 02:35:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 02:35:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 02:35:14 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:35:15 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 02:35:44 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 02:35:45 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 02:35:45 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 02:36:18 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 02:36:19 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 02:36:19 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 02:36:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 02:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 02:36:20 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 02:36:20 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:feec22b5b79860f47a87861bed3a29d5431a279cc239b44a2522a9ab5459d844`  
		Last Modified: Fri, 04 Nov 2022 23:34:48 GMT  
		Size: 40.6 MB (40580917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b33952322b1265ccfb1a2fa879b86ccb58a3c5f02567a902cac8d7d1e1fbcac`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8632ee03bb1ca20bb263a7bab04dda4995925a4ed5e2a16fa83e174a53a840c3`  
		Last Modified: Sat, 05 Nov 2022 02:38:17 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:636ccd115361ca8e84b27ef37d14d6119748b71900dade590ecd963afab4450c`  
		Last Modified: Sat, 05 Nov 2022 02:38:16 GMT  
		Size: 4.6 MB (4596992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07c8fac8eead4f4a9e8284577eaf9ae5ca2c78a3cbecf1b9f0c7a4b78337665`  
		Last Modified: Sat, 05 Nov 2022 02:38:15 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44c54db9c140998b59508c389ead06ffbe863051125b2dd2b150db5d8f87010`  
		Last Modified: Sat, 05 Nov 2022 02:38:14 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9c45749101c2502030b52b11f5cf1031d08ceabeab91283742467bdbe2dc62`  
		Last Modified: Sat, 05 Nov 2022 02:38:21 GMT  
		Size: 56.0 MB (56047607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fa3febc47da546527aae2d8de736b7562b0e8f5a37a63778aa86307af8d2d`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5e1d3c311ae16390016bcf09a400cc9e67473f8ea5787abe0855f510e917b`  
		Last Modified: Sat, 05 Nov 2022 02:38:23 GMT  
		Size: 55.1 MB (55068188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3db2c5d8ec681907739aa09873795aa7ffacfacfbd43d79f140331029f8517`  
		Last Modified: Sat, 05 Nov 2022 02:38:13 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ead729abd92d539d786eed0146f98fbfb8a970de2f0b082e9a0aa4ecc6d1fc`  
		Last Modified: Sat, 05 Nov 2022 02:38:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d96e939151420ccf4df0ba678f6ed3e61dcaa4f4790c3ae900caf0da69d91f7b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155535108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5148355a8b6c9dac3f9554a010d015d009f30614b5d8db21281a25bcee98a5ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 04 Nov 2022 22:50:08 GMT
ADD file:efa6454225ba5be177493364c69d425968d42231b708b5d492a41f9ab14d64f4 in / 
# Fri, 04 Nov 2022 22:50:08 GMT
CMD ["/bin/bash"]
# Sat, 05 Nov 2022 00:57:35 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Sat, 05 Nov 2022 00:57:35 GMT
ENV GOSU_VERSION=1.14
# Sat, 05 Nov 2022 00:57:39 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 05 Nov 2022 00:57:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Sat, 05 Nov 2022 00:58:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 05 Nov 2022 00:58:00 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:01 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Sat, 05 Nov 2022 00:58:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Sat, 05 Nov 2022 00:58:27 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Sat, 05 Nov 2022 00:58:27 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Sat, 05 Nov 2022 00:58:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Sat, 05 Nov 2022 00:58:54 GMT
VOLUME [/var/lib/mysql]
# Sat, 05 Nov 2022 00:58:54 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Sat, 05 Nov 2022 00:58:55 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 05 Nov 2022 00:58:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 05 Nov 2022 00:58:55 GMT
EXPOSE 3306 33060
# Sat, 05 Nov 2022 00:58:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a13cd8cb50ab4c8c5cb15a9929fa5faf1b7833f87c827551a9a54e84789b1e0b`  
		Last Modified: Fri, 04 Nov 2022 22:51:35 GMT  
		Size: 39.4 MB (39401738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8eb5d9079c50473fff35ffde4fb2546949491adaeee2bbd845224f136771296`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eba161e5c47e6570474914fb9155e32e0d13e77c321da1b084309566474344b`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326e34d03d61e22d55d8802e4fd7938025291b7adb846f4b59d332da7ea1d74`  
		Last Modified: Sat, 05 Nov 2022 00:59:15 GMT  
		Size: 4.4 MB (4432072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6040b78fa4cb3ddd503441e1fe1cd37af3a5e8a60b73580cbc427d8a6fc5d356`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a6482f791f82ad3876fb348fcdb842ddbcc0a355e3a27fb9e3a4ce30437b0`  
		Last Modified: Sat, 05 Nov 2022 00:59:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af12750742edfafae2ae6688ec04814d81b3d24b1c8b387e00d51fa8175efd7c`  
		Last Modified: Sat, 05 Nov 2022 00:59:16 GMT  
		Size: 55.4 MB (55412667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe604010a887b88e3aa9f524d9cce8a7494da0a2f22f640ad8877755b2a906`  
		Last Modified: Sat, 05 Nov 2022 00:59:10 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4246ba10d864e7f2ce81418da4cee6a0da7ca849140f246f9a4cbd4e917f8fde`  
		Last Modified: Sat, 05 Nov 2022 00:59:18 GMT  
		Size: 55.4 MB (55421785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b193100b91775f76d9638e79a261ee23740ddec46365b7013da360e37f2f7bc`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f75c456f31a86bdf36b9098d5a9c46e57b0e0e65668a339866db8bf10ba77c13`  
		Last Modified: Sat, 05 Nov 2022 00:59:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
