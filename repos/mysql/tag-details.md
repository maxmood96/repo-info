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
$ docker pull mysql@sha256:6c75a3ede385188dca74670e94c92ce11a0307a0ad4448265afe0d3c815dfe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:d97492764f2b61c8ea0dbdff1e956fd2f31ad401fb9126f9e5a472db0a5e8945
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154815555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181d485f6500849992cc568b26cfe13d98a7a2f995bc49a3e47b2fedf6468fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:24:44 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:24:45 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Feb 2022 01:24:45 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:25:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:25:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:25:07 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:25:08 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4aec225fa3798474cb7869aaefbd8d1ef6b7f77f477690543bc7c6a6af433`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8d7e9eac10666d92da1cfe84102726d948c1b40fced8df716feb2893cb180`  
		Last Modified: Fri, 18 Feb 2022 01:27:24 GMT  
		Size: 108.6 MB (108637249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7660d55cfd076fccd3ffb7adaf7bea38517f64db7fd19fdb07273f09190b3`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4976e34a8d299465c434eae493ccb3831ab270ce61be87b94de5a566a465836`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:6c75a3ede385188dca74670e94c92ce11a0307a0ad4448265afe0d3c815dfe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:d97492764f2b61c8ea0dbdff1e956fd2f31ad401fb9126f9e5a472db0a5e8945
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154815555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181d485f6500849992cc568b26cfe13d98a7a2f995bc49a3e47b2fedf6468fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:24:44 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:24:45 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Feb 2022 01:24:45 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:25:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:25:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:25:07 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:25:08 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4aec225fa3798474cb7869aaefbd8d1ef6b7f77f477690543bc7c6a6af433`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8d7e9eac10666d92da1cfe84102726d948c1b40fced8df716feb2893cb180`  
		Last Modified: Fri, 18 Feb 2022 01:27:24 GMT  
		Size: 108.6 MB (108637249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7660d55cfd076fccd3ffb7adaf7bea38517f64db7fd19fdb07273f09190b3`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4976e34a8d299465c434eae493ccb3831ab270ce61be87b94de5a566a465836`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:389a29c739eb68f3e25be1aa442b19eeac992066cf83ffed4a45b401c55dbc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7651ab2be2a687f6a33956efebfd66f17643507d33cd188f950cf38364038336
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120942338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89be9f36a1613c0d31713707109039564c3f49c1de0aa05301b53f022b9c350d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Jan 2022 22:34:30 GMT
ADD file:18acb1f3ef1ffe1aeaff1aa22861026180d22104f6f14dd8bc4656777800fd9f in / 
# Wed, 12 Jan 2022 22:34:30 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:23:36 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:23:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:23:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:53 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:23:53 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Fri, 18 Feb 2022 01:23:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:24:17 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:24:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:24:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Fri, 18 Feb 2022 01:24:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:24:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:24:38 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:24:39 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:24:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1e1d49338f200e5dab7ef55f9d3a37259af48812603e07ae59e43615f9038b27`  
		Last Modified: Wed, 12 Jan 2022 22:35:18 GMT  
		Size: 48.3 MB (48330956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66218a3b537b220bfcc60a7592e8334f387d5189667b2364be8266fdf038a03f`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e2fa6d94c92997a80329028540d0f0e421e44aa0d58069d03944a79c152089`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b11e41160ce2b0e3e1d23091fbfa2dec6e3d2154958daaefed975d7717948`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80805c820cc05291535eebb177b429cfeac226e9c1ccbc3bac8db137afd7b349`  
		Last Modified: Fri, 18 Feb 2022 01:26:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574267d6067e69db2a75f6b98062629536047f844b9e5bd7d6c27dc4f00fd2b`  
		Last Modified: Fri, 18 Feb 2022 01:26:50 GMT  
		Size: 25.4 MB (25378008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41de9d18e044f6fd1101cce671f1fc94254ba0fe43455a4bd6f6f9392240b710`  
		Last Modified: Fri, 18 Feb 2022 01:26:46 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518b7b15895f42580bde98a5b75ef4c0a74e6c424f569419ae44595055733e`  
		Last Modified: Fri, 18 Feb 2022 01:26:55 GMT  
		Size: 46.3 MB (46293817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6e6a93d63ae0775a7ae09afd7ec572a4a2e60d9c9a61c031ed14691f8bdba`  
		Last Modified: Fri, 18 Feb 2022 01:26:45 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:6c75a3ede385188dca74670e94c92ce11a0307a0ad4448265afe0d3c815dfe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:d97492764f2b61c8ea0dbdff1e956fd2f31ad401fb9126f9e5a472db0a5e8945
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154815555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181d485f6500849992cc568b26cfe13d98a7a2f995bc49a3e47b2fedf6468fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:24:44 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:24:45 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Feb 2022 01:24:45 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:25:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:25:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:25:07 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:25:08 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4aec225fa3798474cb7869aaefbd8d1ef6b7f77f477690543bc7c6a6af433`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8d7e9eac10666d92da1cfe84102726d948c1b40fced8df716feb2893cb180`  
		Last Modified: Fri, 18 Feb 2022 01:27:24 GMT  
		Size: 108.6 MB (108637249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7660d55cfd076fccd3ffb7adaf7bea38517f64db7fd19fdb07273f09190b3`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4976e34a8d299465c434eae493ccb3831ab270ce61be87b94de5a566a465836`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:6c75a3ede385188dca74670e94c92ce11a0307a0ad4448265afe0d3c815dfe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:d97492764f2b61c8ea0dbdff1e956fd2f31ad401fb9126f9e5a472db0a5e8945
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154815555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181d485f6500849992cc568b26cfe13d98a7a2f995bc49a3e47b2fedf6468fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:24:44 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:24:45 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Feb 2022 01:24:45 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:25:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:25:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:25:07 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:25:08 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4aec225fa3798474cb7869aaefbd8d1ef6b7f77f477690543bc7c6a6af433`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8d7e9eac10666d92da1cfe84102726d948c1b40fced8df716feb2893cb180`  
		Last Modified: Fri, 18 Feb 2022 01:27:24 GMT  
		Size: 108.6 MB (108637249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7660d55cfd076fccd3ffb7adaf7bea38517f64db7fd19fdb07273f09190b3`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4976e34a8d299465c434eae493ccb3831ab270ce61be87b94de5a566a465836`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:389a29c739eb68f3e25be1aa442b19eeac992066cf83ffed4a45b401c55dbc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7651ab2be2a687f6a33956efebfd66f17643507d33cd188f950cf38364038336
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120942338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89be9f36a1613c0d31713707109039564c3f49c1de0aa05301b53f022b9c350d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Jan 2022 22:34:30 GMT
ADD file:18acb1f3ef1ffe1aeaff1aa22861026180d22104f6f14dd8bc4656777800fd9f in / 
# Wed, 12 Jan 2022 22:34:30 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:23:36 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:23:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:23:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:53 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:23:53 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Fri, 18 Feb 2022 01:23:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:24:17 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:24:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:24:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Fri, 18 Feb 2022 01:24:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:24:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:24:38 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:24:39 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:24:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1e1d49338f200e5dab7ef55f9d3a37259af48812603e07ae59e43615f9038b27`  
		Last Modified: Wed, 12 Jan 2022 22:35:18 GMT  
		Size: 48.3 MB (48330956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66218a3b537b220bfcc60a7592e8334f387d5189667b2364be8266fdf038a03f`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e2fa6d94c92997a80329028540d0f0e421e44aa0d58069d03944a79c152089`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b11e41160ce2b0e3e1d23091fbfa2dec6e3d2154958daaefed975d7717948`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80805c820cc05291535eebb177b429cfeac226e9c1ccbc3bac8db137afd7b349`  
		Last Modified: Fri, 18 Feb 2022 01:26:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574267d6067e69db2a75f6b98062629536047f844b9e5bd7d6c27dc4f00fd2b`  
		Last Modified: Fri, 18 Feb 2022 01:26:50 GMT  
		Size: 25.4 MB (25378008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41de9d18e044f6fd1101cce671f1fc94254ba0fe43455a4bd6f6f9392240b710`  
		Last Modified: Fri, 18 Feb 2022 01:26:46 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518b7b15895f42580bde98a5b75ef4c0a74e6c424f569419ae44595055733e`  
		Last Modified: Fri, 18 Feb 2022 01:26:55 GMT  
		Size: 46.3 MB (46293817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6e6a93d63ae0775a7ae09afd7ec572a4a2e60d9c9a61c031ed14691f8bdba`  
		Last Modified: Fri, 18 Feb 2022 01:26:45 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37`

```console
$ docker pull mysql@sha256:6c75a3ede385188dca74670e94c92ce11a0307a0ad4448265afe0d3c815dfe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37` - linux; amd64

```console
$ docker pull mysql@sha256:d97492764f2b61c8ea0dbdff1e956fd2f31ad401fb9126f9e5a472db0a5e8945
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154815555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181d485f6500849992cc568b26cfe13d98a7a2f995bc49a3e47b2fedf6468fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:24:44 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:24:45 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Feb 2022 01:24:45 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:25:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:25:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:25:07 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:25:08 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4aec225fa3798474cb7869aaefbd8d1ef6b7f77f477690543bc7c6a6af433`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8d7e9eac10666d92da1cfe84102726d948c1b40fced8df716feb2893cb180`  
		Last Modified: Fri, 18 Feb 2022 01:27:24 GMT  
		Size: 108.6 MB (108637249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7660d55cfd076fccd3ffb7adaf7bea38517f64db7fd19fdb07273f09190b3`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4976e34a8d299465c434eae493ccb3831ab270ce61be87b94de5a566a465836`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-debian`

```console
$ docker pull mysql@sha256:6c75a3ede385188dca74670e94c92ce11a0307a0ad4448265afe0d3c815dfe48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:d97492764f2b61c8ea0dbdff1e956fd2f31ad401fb9126f9e5a472db0a5e8945
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154815555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181d485f6500849992cc568b26cfe13d98a7a2f995bc49a3e47b2fedf6468fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:24:44 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:24:45 GMT
ENV MYSQL_VERSION=5.7.37-1debian10
# Fri, 18 Feb 2022 01:24:45 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:25:06 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:25:06 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:25:07 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:25:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:25:08 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f4aec225fa3798474cb7869aaefbd8d1ef6b7f77f477690543bc7c6a6af433`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a8d7e9eac10666d92da1cfe84102726d948c1b40fced8df716feb2893cb180`  
		Last Modified: Fri, 18 Feb 2022 01:27:24 GMT  
		Size: 108.6 MB (108637249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d7660d55cfd076fccd3ffb7adaf7bea38517f64db7fd19fdb07273f09190b3`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4976e34a8d299465c434eae493ccb3831ab270ce61be87b94de5a566a465836`  
		Last Modified: Fri, 18 Feb 2022 01:27:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.37-oracle`

```console
$ docker pull mysql@sha256:389a29c739eb68f3e25be1aa442b19eeac992066cf83ffed4a45b401c55dbc77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7651ab2be2a687f6a33956efebfd66f17643507d33cd188f950cf38364038336
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.9 MB (120942338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89be9f36a1613c0d31713707109039564c3f49c1de0aa05301b53f022b9c350d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Jan 2022 22:34:30 GMT
ADD file:18acb1f3ef1ffe1aeaff1aa22861026180d22104f6f14dd8bc4656777800fd9f in / 
# Wed, 12 Jan 2022 22:34:30 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:23:36 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:23:36 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:23:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:23:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:53 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 18 Feb 2022 01:23:53 GMT
ENV MYSQL_VERSION=5.7.37-1.el7
# Fri, 18 Feb 2022 01:23:54 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:24:17 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:24:18 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:24:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el7
# Fri, 18 Feb 2022 01:24:37 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:24:38 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:24:38 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:24:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:24:39 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:24:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1e1d49338f200e5dab7ef55f9d3a37259af48812603e07ae59e43615f9038b27`  
		Last Modified: Wed, 12 Jan 2022 22:35:18 GMT  
		Size: 48.3 MB (48330956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66218a3b537b220bfcc60a7592e8334f387d5189667b2364be8266fdf038a03f`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e2fa6d94c92997a80329028540d0f0e421e44aa0d58069d03944a79c152089`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee7b11e41160ce2b0e3e1d23091fbfa2dec6e3d2154958daaefed975d7717948`  
		Last Modified: Fri, 18 Feb 2022 01:26:48 GMT  
		Size: 2.7 KB (2665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80805c820cc05291535eebb177b429cfeac226e9c1ccbc3bac8db137afd7b349`  
		Last Modified: Fri, 18 Feb 2022 01:26:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e574267d6067e69db2a75f6b98062629536047f844b9e5bd7d6c27dc4f00fd2b`  
		Last Modified: Fri, 18 Feb 2022 01:26:50 GMT  
		Size: 25.4 MB (25378008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41de9d18e044f6fd1101cce671f1fc94254ba0fe43455a4bd6f6f9392240b710`  
		Last Modified: Fri, 18 Feb 2022 01:26:46 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc518b7b15895f42580bde98a5b75ef4c0a74e6c424f569419ae44595055733e`  
		Last Modified: Fri, 18 Feb 2022 01:26:55 GMT  
		Size: 46.3 MB (46293817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6e6a93d63ae0775a7ae09afd7ec572a4a2e60d9c9a61c031ed14691f8bdba`  
		Last Modified: Fri, 18 Feb 2022 01:26:45 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:808d02026b5b3edf185e9201db89abdf701fcce11f980ce810adf49c7c7342b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a1fc8cc7d62da0e5e35e098c8f99e12d6dfe253249c1a8e7392644e5ec9fbf2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131247835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666b7bdb9b1e4dd70402bf89b44145af4ee43e8a1f8b6823a7348df3d4b5347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:20:31 GMT
ADD file:636d5d8575ec6ddd380a3bbf41530219d37249378b4abd151d94842377cc55d9 in / 
# Fri, 11 Feb 2022 18:20:32 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:20:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:20:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:20:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:20:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:21:18 GMT
RUN set -eux; microdnf install -y findutils; microdnf clean all
# Fri, 18 Feb 2022 01:21:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:21:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:21:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:21:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:21:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:22:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:22:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:22:54 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:22:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:22:55 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:22:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:010357f4c091049bd23724817a1881f575ff94d35f4c621b4f87b2876049650b`  
		Last Modified: Fri, 11 Feb 2022 18:21:24 GMT  
		Size: 42.1 MB (42105112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa408bcdb6fa7a3da670da56c2117a4fc7969a39ab0e37db4bb4e52b1d38ba`  
		Last Modified: Fri, 18 Feb 2022 01:25:39 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290fe0478d05d79d3ad6a2676a72d0ba98072c8e9fad91f0ff027c0db9e7d5e8`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e475a5588ead2e9a8ae74a3294b26b4b5e795e112c6d54779b307f634296a245`  
		Last Modified: Fri, 18 Feb 2022 01:25:37 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367255e5d85a8f2afeeba49f8c0d98c53ce2e201fb284a84ff4984b30c8eeef9`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 2.8 MB (2771655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0145e7f2d239af74be7d51a6fff3109e8b1616bf8c5b0513becf1aca4b95c7`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2c7c0af6e385712bfc837437da2f4005768173e65e7309f05177e737bc58a2`  
		Last Modified: Fri, 18 Feb 2022 01:25:44 GMT  
		Size: 47.2 MB (47214228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8104a253cabe5deab9f62b2230e88688a12a40259b99e381146ff74be5590`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12a051e07b4ace9aad8389609189650858c935b6ad3a35337ca9d33e5e1066c`  
		Last Modified: Fri, 18 Feb 2022 01:25:43 GMT  
		Size: 38.2 MB (38218699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008ae851b8156d7791e78f5dc696d017706f11c2618cb0f7de591fbb6b9a39ea`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b156b996b09d1509a78a84dd5a71cf673b5ff60c3ae22c27194e62ac2a7d1266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139997480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b3b1d5bc990340c2df8472a7a78af238dfb761ace123d9b13ccd4d3dfc4332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:58:36 GMT
ADD file:8d5a0dcc45ab23c7b507e80b63e5752d94837f490600ce95fb8ba8ed2f7baa2d in / 
# Fri, 11 Feb 2022 18:58:37 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:40:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:40:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:40:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Feb 2022 21:40:19 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Wed, 23 Feb 2022 21:41:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 21:41:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 21:41:02 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 23 Feb 2022 21:41:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 23 Feb 2022 21:41:26 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 23 Feb 2022 21:41:26 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 23 Feb 2022 21:41:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 21:41:56 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 21:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 21:41:57 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 21:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffdd659a9f05cadeed9c2d5cead839f585163662ca7f847a41fd64bb4e503f0c`  
		Last Modified: Fri, 11 Feb 2022 18:59:38 GMT  
		Size: 42.0 MB (42018804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0160f0527322be235d3dfdb8e677d5ef11bf2da725fc7a4c77f93c96d3d43c`  
		Last Modified: Fri, 18 Feb 2022 01:42:53 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f9628b4dd4430ea84a7c1a9fc0c2c79a4528061ce123f84f5c31588ebe3aa`  
		Last Modified: Fri, 18 Feb 2022 01:42:51 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af70585b7a192f4e200798deae1a8cba89afbc03b7097032112e5bc4571f2660`  
		Last Modified: Wed, 23 Feb 2022 21:42:28 GMT  
		Size: 3.3 MB (3258221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a63cf661d5c4d9057b557f1268efa4cf1770596543728a33c76e31c3c38bf7`  
		Last Modified: Wed, 23 Feb 2022 21:42:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20f69348b09e5a78b36c179334aed779d534c322ee73c63149283f619fdf480`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d6f7910557f5385a0a152ca459c4a3a513a0be5091c54bea6c889e1093911`  
		Last Modified: Wed, 23 Feb 2022 21:42:33 GMT  
		Size: 53.4 MB (53382212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a314c288f953196b7101c88f8b67bf0ae5a07cbc362202f3ec30fddc9ac2f`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef4c71a5c7ada2f9db19897deb642356f81aa03dbf6811019ae506d089cad2e`  
		Last Modified: Wed, 23 Feb 2022 21:42:32 GMT  
		Size: 40.5 MB (40471863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb56c1084a5c94c7e6a9ee9e65bb8cbbe3fccf7193667900469ff5fa3756bc77`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:808d02026b5b3edf185e9201db89abdf701fcce11f980ce810adf49c7c7342b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a1fc8cc7d62da0e5e35e098c8f99e12d6dfe253249c1a8e7392644e5ec9fbf2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131247835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666b7bdb9b1e4dd70402bf89b44145af4ee43e8a1f8b6823a7348df3d4b5347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:20:31 GMT
ADD file:636d5d8575ec6ddd380a3bbf41530219d37249378b4abd151d94842377cc55d9 in / 
# Fri, 11 Feb 2022 18:20:32 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:20:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:20:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:20:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:20:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:21:18 GMT
RUN set -eux; microdnf install -y findutils; microdnf clean all
# Fri, 18 Feb 2022 01:21:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:21:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:21:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:21:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:21:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:22:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:22:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:22:54 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:22:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:22:55 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:22:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:010357f4c091049bd23724817a1881f575ff94d35f4c621b4f87b2876049650b`  
		Last Modified: Fri, 11 Feb 2022 18:21:24 GMT  
		Size: 42.1 MB (42105112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa408bcdb6fa7a3da670da56c2117a4fc7969a39ab0e37db4bb4e52b1d38ba`  
		Last Modified: Fri, 18 Feb 2022 01:25:39 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290fe0478d05d79d3ad6a2676a72d0ba98072c8e9fad91f0ff027c0db9e7d5e8`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e475a5588ead2e9a8ae74a3294b26b4b5e795e112c6d54779b307f634296a245`  
		Last Modified: Fri, 18 Feb 2022 01:25:37 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367255e5d85a8f2afeeba49f8c0d98c53ce2e201fb284a84ff4984b30c8eeef9`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 2.8 MB (2771655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0145e7f2d239af74be7d51a6fff3109e8b1616bf8c5b0513becf1aca4b95c7`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2c7c0af6e385712bfc837437da2f4005768173e65e7309f05177e737bc58a2`  
		Last Modified: Fri, 18 Feb 2022 01:25:44 GMT  
		Size: 47.2 MB (47214228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8104a253cabe5deab9f62b2230e88688a12a40259b99e381146ff74be5590`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12a051e07b4ace9aad8389609189650858c935b6ad3a35337ca9d33e5e1066c`  
		Last Modified: Fri, 18 Feb 2022 01:25:43 GMT  
		Size: 38.2 MB (38218699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008ae851b8156d7791e78f5dc696d017706f11c2618cb0f7de591fbb6b9a39ea`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b156b996b09d1509a78a84dd5a71cf673b5ff60c3ae22c27194e62ac2a7d1266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139997480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b3b1d5bc990340c2df8472a7a78af238dfb761ace123d9b13ccd4d3dfc4332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:58:36 GMT
ADD file:8d5a0dcc45ab23c7b507e80b63e5752d94837f490600ce95fb8ba8ed2f7baa2d in / 
# Fri, 11 Feb 2022 18:58:37 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:40:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:40:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:40:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Feb 2022 21:40:19 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Wed, 23 Feb 2022 21:41:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 21:41:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 21:41:02 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 23 Feb 2022 21:41:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 23 Feb 2022 21:41:26 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 23 Feb 2022 21:41:26 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 23 Feb 2022 21:41:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 21:41:56 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 21:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 21:41:57 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 21:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffdd659a9f05cadeed9c2d5cead839f585163662ca7f847a41fd64bb4e503f0c`  
		Last Modified: Fri, 11 Feb 2022 18:59:38 GMT  
		Size: 42.0 MB (42018804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0160f0527322be235d3dfdb8e677d5ef11bf2da725fc7a4c77f93c96d3d43c`  
		Last Modified: Fri, 18 Feb 2022 01:42:53 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f9628b4dd4430ea84a7c1a9fc0c2c79a4528061ce123f84f5c31588ebe3aa`  
		Last Modified: Fri, 18 Feb 2022 01:42:51 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af70585b7a192f4e200798deae1a8cba89afbc03b7097032112e5bc4571f2660`  
		Last Modified: Wed, 23 Feb 2022 21:42:28 GMT  
		Size: 3.3 MB (3258221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a63cf661d5c4d9057b557f1268efa4cf1770596543728a33c76e31c3c38bf7`  
		Last Modified: Wed, 23 Feb 2022 21:42:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20f69348b09e5a78b36c179334aed779d534c322ee73c63149283f619fdf480`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d6f7910557f5385a0a152ca459c4a3a513a0be5091c54bea6c889e1093911`  
		Last Modified: Wed, 23 Feb 2022 21:42:33 GMT  
		Size: 53.4 MB (53382212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a314c288f953196b7101c88f8b67bf0ae5a07cbc362202f3ec30fddc9ac2f`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef4c71a5c7ada2f9db19897deb642356f81aa03dbf6811019ae506d089cad2e`  
		Last Modified: Wed, 23 Feb 2022 21:42:32 GMT  
		Size: 40.5 MB (40471863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb56c1084a5c94c7e6a9ee9e65bb8cbbe3fccf7193667900469ff5fa3756bc77`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-debian`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.28-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.28-oracle`

```console
$ docker pull mysql@sha256:808d02026b5b3edf185e9201db89abdf701fcce11f980ce810adf49c7c7342b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.28-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a1fc8cc7d62da0e5e35e098c8f99e12d6dfe253249c1a8e7392644e5ec9fbf2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131247835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666b7bdb9b1e4dd70402bf89b44145af4ee43e8a1f8b6823a7348df3d4b5347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:20:31 GMT
ADD file:636d5d8575ec6ddd380a3bbf41530219d37249378b4abd151d94842377cc55d9 in / 
# Fri, 11 Feb 2022 18:20:32 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:20:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:20:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:20:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:20:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:21:18 GMT
RUN set -eux; microdnf install -y findutils; microdnf clean all
# Fri, 18 Feb 2022 01:21:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:21:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:21:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:21:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:21:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:22:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:22:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:22:54 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:22:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:22:55 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:22:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:010357f4c091049bd23724817a1881f575ff94d35f4c621b4f87b2876049650b`  
		Last Modified: Fri, 11 Feb 2022 18:21:24 GMT  
		Size: 42.1 MB (42105112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa408bcdb6fa7a3da670da56c2117a4fc7969a39ab0e37db4bb4e52b1d38ba`  
		Last Modified: Fri, 18 Feb 2022 01:25:39 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290fe0478d05d79d3ad6a2676a72d0ba98072c8e9fad91f0ff027c0db9e7d5e8`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e475a5588ead2e9a8ae74a3294b26b4b5e795e112c6d54779b307f634296a245`  
		Last Modified: Fri, 18 Feb 2022 01:25:37 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367255e5d85a8f2afeeba49f8c0d98c53ce2e201fb284a84ff4984b30c8eeef9`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 2.8 MB (2771655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0145e7f2d239af74be7d51a6fff3109e8b1616bf8c5b0513becf1aca4b95c7`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2c7c0af6e385712bfc837437da2f4005768173e65e7309f05177e737bc58a2`  
		Last Modified: Fri, 18 Feb 2022 01:25:44 GMT  
		Size: 47.2 MB (47214228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8104a253cabe5deab9f62b2230e88688a12a40259b99e381146ff74be5590`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12a051e07b4ace9aad8389609189650858c935b6ad3a35337ca9d33e5e1066c`  
		Last Modified: Fri, 18 Feb 2022 01:25:43 GMT  
		Size: 38.2 MB (38218699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008ae851b8156d7791e78f5dc696d017706f11c2618cb0f7de591fbb6b9a39ea`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.28-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b156b996b09d1509a78a84dd5a71cf673b5ff60c3ae22c27194e62ac2a7d1266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139997480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b3b1d5bc990340c2df8472a7a78af238dfb761ace123d9b13ccd4d3dfc4332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:58:36 GMT
ADD file:8d5a0dcc45ab23c7b507e80b63e5752d94837f490600ce95fb8ba8ed2f7baa2d in / 
# Fri, 11 Feb 2022 18:58:37 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:40:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:40:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:40:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Feb 2022 21:40:19 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Wed, 23 Feb 2022 21:41:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 21:41:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 21:41:02 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 23 Feb 2022 21:41:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 23 Feb 2022 21:41:26 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 23 Feb 2022 21:41:26 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 23 Feb 2022 21:41:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 21:41:56 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 21:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 21:41:57 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 21:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffdd659a9f05cadeed9c2d5cead839f585163662ca7f847a41fd64bb4e503f0c`  
		Last Modified: Fri, 11 Feb 2022 18:59:38 GMT  
		Size: 42.0 MB (42018804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0160f0527322be235d3dfdb8e677d5ef11bf2da725fc7a4c77f93c96d3d43c`  
		Last Modified: Fri, 18 Feb 2022 01:42:53 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f9628b4dd4430ea84a7c1a9fc0c2c79a4528061ce123f84f5c31588ebe3aa`  
		Last Modified: Fri, 18 Feb 2022 01:42:51 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af70585b7a192f4e200798deae1a8cba89afbc03b7097032112e5bc4571f2660`  
		Last Modified: Wed, 23 Feb 2022 21:42:28 GMT  
		Size: 3.3 MB (3258221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a63cf661d5c4d9057b557f1268efa4cf1770596543728a33c76e31c3c38bf7`  
		Last Modified: Wed, 23 Feb 2022 21:42:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20f69348b09e5a78b36c179334aed779d534c322ee73c63149283f619fdf480`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d6f7910557f5385a0a152ca459c4a3a513a0be5091c54bea6c889e1093911`  
		Last Modified: Wed, 23 Feb 2022 21:42:33 GMT  
		Size: 53.4 MB (53382212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a314c288f953196b7101c88f8b67bf0ae5a07cbc362202f3ec30fddc9ac2f`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef4c71a5c7ada2f9db19897deb642356f81aa03dbf6811019ae506d089cad2e`  
		Last Modified: Wed, 23 Feb 2022 21:42:32 GMT  
		Size: 40.5 MB (40471863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb56c1084a5c94c7e6a9ee9e65bb8cbbe3fccf7193667900469ff5fa3756bc77`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:e3358f55ea2b0cd432685d7e3c79a33a85c7a359b35fa87fc4993514b9573446
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:e9c9e3680bbadd5230a62c5548793bd8e59cbcc868032781e48bd53e888bd82f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.0 MB (153984327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b062d639f4a10bf2439de7204856ea552a68fa5d7cd2f28c16066e340358c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 26 Jan 2022 01:40:59 GMT
ADD file:c51141702f568a28a7e3e7a2748f5ead5754e32d7b1cf7ebc8f4326273d05206 in / 
# Wed, 26 Jan 2022 01:40:59 GMT
CMD ["bash"]
# Thu, 27 Jan 2022 00:56:31 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 27 Jan 2022 00:56:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 27 Jan 2022 00:56:43 GMT
ENV GOSU_VERSION=1.14
# Thu, 27 Jan 2022 00:57:05 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 27 Jan 2022 00:57:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 27 Jan 2022 00:57:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Feb 2022 01:23:10 GMT
RUN set -ex; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:23:11 GMT
ENV MYSQL_VERSION=8.0.28-1debian10
# Fri, 18 Feb 2022 01:23:12 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Fri, 18 Feb 2022 01:23:27 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Fri, 18 Feb 2022 01:23:28 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:23:28 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Fri, 18 Feb 2022 01:23:29 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:23:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 18 Feb 2022 01:23:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:23:30 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:23:30 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6552179c3509e3c4314b4065e0d2790563d01cd474e2fdd58be4d46acd48af6a`  
		Last Modified: Wed, 26 Jan 2022 01:47:31 GMT  
		Size: 27.2 MB (27153731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69aa66e4482016fae7907ce17f46b3f7588c5ee17cc5c7dff11324e05c92bd5`  
		Last Modified: Thu, 27 Jan 2022 00:59:07 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b19465b002b6638a15647e41bd6bff7d4cabc190c35b5a50025e0c4370a2794`  
		Last Modified: Thu, 27 Jan 2022 00:59:08 GMT  
		Size: 4.2 MB (4179346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0cfe99a1632d64b2986e131d8dd95ddb8b8bef124c690ab1958c961b8d20`  
		Last Modified: Thu, 27 Jan 2022 00:59:05 GMT  
		Size: 1.4 MB (1386744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ccd5a5c898747a41e6e4498e0c4a9c034ee1fb06c94f48e580de8521f668670`  
		Last Modified: Thu, 27 Jan 2022 00:59:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab00d7d23292a0f5b287db2bad228cb779b536fb31303442115d7b2b6f8ec3`  
		Last Modified: Thu, 27 Jan 2022 00:59:10 GMT  
		Size: 13.4 MB (13448734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d726bac08eac44e8c39b1afbe20d14e2288e6846dd17299ae5725de86124bc7`  
		Last Modified: Fri, 18 Feb 2022 01:26:01 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11bb049c7b945cb3b8912753d7beeee39d47a8f030aef219eaa34410736a0883`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcdd679c4586030a483b3484ad65880017ac4a790b4a9a8ddc734e9b7976e74`  
		Last Modified: Fri, 18 Feb 2022 01:26:17 GMT  
		Size: 107.8 MB (107805176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11585aaf4aad70fff078dd27ceac48c6c25f9e5a918c1f2d84ceeea011500170`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dc265cb1d984f698f6de7bc1bc7a375b63a1199661bbc76e0678e4c02d9b7`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 4.9 KB (4948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd400d64ffecaafda263cbf1e21c1394d91cbb89d320563e70e8f3cb62af91a0`  
		Last Modified: Fri, 18 Feb 2022 01:25:59 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:808d02026b5b3edf185e9201db89abdf701fcce11f980ce810adf49c7c7342b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a1fc8cc7d62da0e5e35e098c8f99e12d6dfe253249c1a8e7392644e5ec9fbf2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131247835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666b7bdb9b1e4dd70402bf89b44145af4ee43e8a1f8b6823a7348df3d4b5347f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:20:31 GMT
ADD file:636d5d8575ec6ddd380a3bbf41530219d37249378b4abd151d94842377cc55d9 in / 
# Fri, 11 Feb 2022 18:20:32 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:20:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:20:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:20:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 18 Feb 2022 01:20:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 18 Feb 2022 01:21:18 GMT
RUN set -eux; microdnf install -y findutils; microdnf clean all
# Fri, 18 Feb 2022 01:21:18 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 18 Feb 2022 01:21:19 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:21:19 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 18 Feb 2022 01:21:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Fri, 18 Feb 2022 01:21:59 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 18 Feb 2022 01:21:59 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Fri, 18 Feb 2022 01:22:53 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 18 Feb 2022 01:22:54 GMT
VOLUME [/var/lib/mysql]
# Fri, 18 Feb 2022 01:22:54 GMT
COPY file:d57b295d94f2cdf7e03ab477cd2ec310252c354b198beb96deb500bea04e2010 in /usr/local/bin/ 
# Fri, 18 Feb 2022 01:22:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 18 Feb 2022 01:22:55 GMT
EXPOSE 3306 33060
# Fri, 18 Feb 2022 01:22:55 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:010357f4c091049bd23724817a1881f575ff94d35f4c621b4f87b2876049650b`  
		Last Modified: Fri, 11 Feb 2022 18:21:24 GMT  
		Size: 42.1 MB (42105112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa408bcdb6fa7a3da670da56c2117a4fc7969a39ab0e37db4bb4e52b1d38ba`  
		Last Modified: Fri, 18 Feb 2022 01:25:39 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:290fe0478d05d79d3ad6a2676a72d0ba98072c8e9fad91f0ff027c0db9e7d5e8`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 928.8 KB (928833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e475a5588ead2e9a8ae74a3294b26b4b5e795e112c6d54779b307f634296a245`  
		Last Modified: Fri, 18 Feb 2022 01:25:37 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367255e5d85a8f2afeeba49f8c0d98c53ce2e201fb284a84ff4984b30c8eeef9`  
		Last Modified: Fri, 18 Feb 2022 01:25:38 GMT  
		Size: 2.8 MB (2771655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac0145e7f2d239af74be7d51a6fff3109e8b1616bf8c5b0513becf1aca4b95c7`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2c7c0af6e385712bfc837437da2f4005768173e65e7309f05177e737bc58a2`  
		Last Modified: Fri, 18 Feb 2022 01:25:44 GMT  
		Size: 47.2 MB (47214228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2e8104a253cabe5deab9f62b2230e88688a12a40259b99e381146ff74be5590`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d12a051e07b4ace9aad8389609189650858c935b6ad3a35337ca9d33e5e1066c`  
		Last Modified: Fri, 18 Feb 2022 01:25:43 GMT  
		Size: 38.2 MB (38218699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008ae851b8156d7791e78f5dc696d017706f11c2618cb0f7de591fbb6b9a39ea`  
		Last Modified: Fri, 18 Feb 2022 01:25:35 GMT  
		Size: 4.9 KB (4947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b156b996b09d1509a78a84dd5a71cf673b5ff60c3ae22c27194e62ac2a7d1266
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139997480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b3b1d5bc990340c2df8472a7a78af238dfb761ace123d9b13ccd4d3dfc4332`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 11 Feb 2022 18:58:36 GMT
ADD file:8d5a0dcc45ab23c7b507e80b63e5752d94837f490600ce95fb8ba8ed2f7baa2d in / 
# Fri, 11 Feb 2022 18:58:37 GMT
CMD ["/bin/bash"]
# Fri, 18 Feb 2022 01:40:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Fri, 18 Feb 2022 01:40:09 GMT
ENV GOSU_VERSION=1.14
# Fri, 18 Feb 2022 01:40:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 23 Feb 2022 21:40:19 GMT
RUN set -eux; 	microdnf install -y 		gzip 		xz 		findutils 	; 	microdnf clean all
# Wed, 23 Feb 2022 21:41:00 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 23 Feb 2022 21:41:01 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 23 Feb 2022 21:41:02 GMT
ENV MYSQL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Wed, 23 Feb 2022 21:41:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Wed, 23 Feb 2022 21:41:26 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Wed, 23 Feb 2022 21:41:26 GMT
ENV MYSQL_SHELL_VERSION=8.0.28-1.el8
# Wed, 23 Feb 2022 21:41:54 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Wed, 23 Feb 2022 21:41:54 GMT
VOLUME [/var/lib/mysql]
# Wed, 23 Feb 2022 21:41:56 GMT
COPY file:baf57873956bd59e060e26b6c80f401272ee89005e3d62d008bf3de68c4c7545 in /usr/local/bin/ 
# Wed, 23 Feb 2022 21:41:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Feb 2022 21:41:57 GMT
EXPOSE 3306 33060
# Wed, 23 Feb 2022 21:41:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ffdd659a9f05cadeed9c2d5cead839f585163662ca7f847a41fd64bb4e503f0c`  
		Last Modified: Fri, 11 Feb 2022 18:59:38 GMT  
		Size: 42.0 MB (42018804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0160f0527322be235d3dfdb8e677d5ef11bf2da725fc7a4c77f93c96d3d43c`  
		Last Modified: Fri, 18 Feb 2022 01:42:53 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4f9628b4dd4430ea84a7c1a9fc0c2c79a4528061ce123f84f5c31588ebe3aa`  
		Last Modified: Fri, 18 Feb 2022 01:42:51 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af70585b7a192f4e200798deae1a8cba89afbc03b7097032112e5bc4571f2660`  
		Last Modified: Wed, 23 Feb 2022 21:42:28 GMT  
		Size: 3.3 MB (3258221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a63cf661d5c4d9057b557f1268efa4cf1770596543728a33c76e31c3c38bf7`  
		Last Modified: Wed, 23 Feb 2022 21:42:27 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20f69348b09e5a78b36c179334aed779d534c322ee73c63149283f619fdf480`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165d6f7910557f5385a0a152ca459c4a3a513a0be5091c54bea6c889e1093911`  
		Last Modified: Wed, 23 Feb 2022 21:42:33 GMT  
		Size: 53.4 MB (53382212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a314c288f953196b7101c88f8b67bf0ae5a07cbc362202f3ec30fddc9ac2f`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef4c71a5c7ada2f9db19897deb642356f81aa03dbf6811019ae506d089cad2e`  
		Last Modified: Wed, 23 Feb 2022 21:42:32 GMT  
		Size: 40.5 MB (40471863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb56c1084a5c94c7e6a9ee9e65bb8cbbe3fccf7193667900469ff5fa3756bc77`  
		Last Modified: Wed, 23 Feb 2022 21:42:25 GMT  
		Size: 5.0 KB (4956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
