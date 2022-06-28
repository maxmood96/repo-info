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
$ docker pull mysql@sha256:60adb6e158c126a6cd93aa7d4aaee15bcf1beae224c04363cbf088193a696802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:3bfe80b544c3eab56180ce31f7d2ffaefd102aef456e67e4a92bc1baaacb0551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162455990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6a7ec181f30ef057aceb9ee70680497cde2128e2f0e8b7895dcefe5684927`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Thu, 23 Jun 2022 04:06:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:38 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:39 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:39 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55f87b960ba60fdf9904d8162ee1c85660f3d22ed460c364165aca6e8603fa9`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459044ae96d113c919f15cdf316e7d153663d23955a08e1b9f894bfdf4a7bd74`  
		Last Modified: Thu, 23 Jun 2022 04:08:08 GMT  
		Size: 115.7 MB (115675698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc62f07e93a5407036b7a3800d3d58044725a81a8168c4724075c4297b82572`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9a5e106092c3f06ca35c9a385836db1cd5225b6b5fa1aad35a26373e1e79f`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:60adb6e158c126a6cd93aa7d4aaee15bcf1beae224c04363cbf088193a696802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3bfe80b544c3eab56180ce31f7d2ffaefd102aef456e67e4a92bc1baaacb0551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162455990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6a7ec181f30ef057aceb9ee70680497cde2128e2f0e8b7895dcefe5684927`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Thu, 23 Jun 2022 04:06:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:38 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:39 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:39 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55f87b960ba60fdf9904d8162ee1c85660f3d22ed460c364165aca6e8603fa9`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459044ae96d113c919f15cdf316e7d153663d23955a08e1b9f894bfdf4a7bd74`  
		Last Modified: Thu, 23 Jun 2022 04:08:08 GMT  
		Size: 115.7 MB (115675698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc62f07e93a5407036b7a3800d3d58044725a81a8168c4724075c4297b82572`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9a5e106092c3f06ca35c9a385836db1cd5225b6b5fa1aad35a26373e1e79f`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:c67e9e97879305e0c7a4934372f35bdb7d79d4a0914d7304d0ee6836be0127a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3030fdb1154e62ed44c2e2dbbc7dee2643ee27fb6dd201b06b19a87682498e8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19b3d18c4a01f69bdb995e46233fcdcc66c1ef84bc8d28396e981c020e395ee`
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
# Thu, 16 Jun 2022 01:38:55 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 16 Jun 2022 01:38:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 16 Jun 2022 01:38:56 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 16 Jun 2022 01:38:56 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Thu, 16 Jun 2022 01:38:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 16 Jun 2022 01:39:11 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 16 Jun 2022 01:39:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 16 Jun 2022 01:39:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Thu, 16 Jun 2022 01:39:29 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 16 Jun 2022 01:39:30 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Jun 2022 01:39:30 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 16 Jun 2022 01:39:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jun 2022 01:39:31 GMT
EXPOSE 3306 33060
# Thu, 16 Jun 2022 01:39:31 GMT
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
	-	`sha256:8e1ea46ae00991c24638c08d268652beb0ce5b878c83d34964f12345618c8941`  
		Last Modified: Thu, 16 Jun 2022 01:40:11 GMT  
		Size: 3.8 MB (3750823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15dccdcd437d9fe54d225731d32bb52246dc75794a5d49e7f12010322dd06c1`  
		Last Modified: Thu, 16 Jun 2022 01:40:08 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1050fbf8b84448d369e5743034ffd13580e9313a7e5092eace10220aa687f9b`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848d1501cd8fc9f77a4e51a2e6dc077dcc0e468191ffaf2f433a4ffb4f7f63c1`  
		Last Modified: Thu, 16 Jun 2022 01:40:10 GMT  
		Size: 25.5 MB (25466694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f50b8fa8c9ba100ca41212bdb8cb892fa707fb9395959c967bcc9355b3ddea`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b3d4a8dbcebd64c0cd3dcde292b97e52335441dac4d3c0e8e010d1197578b`  
		Last Modified: Thu, 16 Jun 2022 01:40:15 GMT  
		Size: 48.0 MB (47957859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4284667ffa5966a13950eda5dee3eb23bc10e60d2dee427c9e7c18c789099568`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:60adb6e158c126a6cd93aa7d4aaee15bcf1beae224c04363cbf088193a696802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:3bfe80b544c3eab56180ce31f7d2ffaefd102aef456e67e4a92bc1baaacb0551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162455990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6a7ec181f30ef057aceb9ee70680497cde2128e2f0e8b7895dcefe5684927`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Thu, 23 Jun 2022 04:06:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:38 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:39 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:39 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55f87b960ba60fdf9904d8162ee1c85660f3d22ed460c364165aca6e8603fa9`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459044ae96d113c919f15cdf316e7d153663d23955a08e1b9f894bfdf4a7bd74`  
		Last Modified: Thu, 23 Jun 2022 04:08:08 GMT  
		Size: 115.7 MB (115675698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc62f07e93a5407036b7a3800d3d58044725a81a8168c4724075c4297b82572`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9a5e106092c3f06ca35c9a385836db1cd5225b6b5fa1aad35a26373e1e79f`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:60adb6e158c126a6cd93aa7d4aaee15bcf1beae224c04363cbf088193a696802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3bfe80b544c3eab56180ce31f7d2ffaefd102aef456e67e4a92bc1baaacb0551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162455990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6a7ec181f30ef057aceb9ee70680497cde2128e2f0e8b7895dcefe5684927`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Thu, 23 Jun 2022 04:06:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:38 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:39 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:39 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55f87b960ba60fdf9904d8162ee1c85660f3d22ed460c364165aca6e8603fa9`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459044ae96d113c919f15cdf316e7d153663d23955a08e1b9f894bfdf4a7bd74`  
		Last Modified: Thu, 23 Jun 2022 04:08:08 GMT  
		Size: 115.7 MB (115675698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc62f07e93a5407036b7a3800d3d58044725a81a8168c4724075c4297b82572`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9a5e106092c3f06ca35c9a385836db1cd5225b6b5fa1aad35a26373e1e79f`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:c67e9e97879305e0c7a4934372f35bdb7d79d4a0914d7304d0ee6836be0127a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3030fdb1154e62ed44c2e2dbbc7dee2643ee27fb6dd201b06b19a87682498e8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19b3d18c4a01f69bdb995e46233fcdcc66c1ef84bc8d28396e981c020e395ee`
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
# Thu, 16 Jun 2022 01:38:55 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 16 Jun 2022 01:38:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 16 Jun 2022 01:38:56 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 16 Jun 2022 01:38:56 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Thu, 16 Jun 2022 01:38:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 16 Jun 2022 01:39:11 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 16 Jun 2022 01:39:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 16 Jun 2022 01:39:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Thu, 16 Jun 2022 01:39:29 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 16 Jun 2022 01:39:30 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Jun 2022 01:39:30 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 16 Jun 2022 01:39:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jun 2022 01:39:31 GMT
EXPOSE 3306 33060
# Thu, 16 Jun 2022 01:39:31 GMT
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
	-	`sha256:8e1ea46ae00991c24638c08d268652beb0ce5b878c83d34964f12345618c8941`  
		Last Modified: Thu, 16 Jun 2022 01:40:11 GMT  
		Size: 3.8 MB (3750823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15dccdcd437d9fe54d225731d32bb52246dc75794a5d49e7f12010322dd06c1`  
		Last Modified: Thu, 16 Jun 2022 01:40:08 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1050fbf8b84448d369e5743034ffd13580e9313a7e5092eace10220aa687f9b`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848d1501cd8fc9f77a4e51a2e6dc077dcc0e468191ffaf2f433a4ffb4f7f63c1`  
		Last Modified: Thu, 16 Jun 2022 01:40:10 GMT  
		Size: 25.5 MB (25466694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f50b8fa8c9ba100ca41212bdb8cb892fa707fb9395959c967bcc9355b3ddea`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b3d4a8dbcebd64c0cd3dcde292b97e52335441dac4d3c0e8e010d1197578b`  
		Last Modified: Thu, 16 Jun 2022 01:40:15 GMT  
		Size: 48.0 MB (47957859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4284667ffa5966a13950eda5dee3eb23bc10e60d2dee427c9e7c18c789099568`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38`

```console
$ docker pull mysql@sha256:60adb6e158c126a6cd93aa7d4aaee15bcf1beae224c04363cbf088193a696802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38` - linux; amd64

```console
$ docker pull mysql@sha256:3bfe80b544c3eab56180ce31f7d2ffaefd102aef456e67e4a92bc1baaacb0551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162455990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6a7ec181f30ef057aceb9ee70680497cde2128e2f0e8b7895dcefe5684927`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Thu, 23 Jun 2022 04:06:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:38 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:39 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:39 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55f87b960ba60fdf9904d8162ee1c85660f3d22ed460c364165aca6e8603fa9`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459044ae96d113c919f15cdf316e7d153663d23955a08e1b9f894bfdf4a7bd74`  
		Last Modified: Thu, 23 Jun 2022 04:08:08 GMT  
		Size: 115.7 MB (115675698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc62f07e93a5407036b7a3800d3d58044725a81a8168c4724075c4297b82572`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9a5e106092c3f06ca35c9a385836db1cd5225b6b5fa1aad35a26373e1e79f`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-debian`

```console
$ docker pull mysql@sha256:60adb6e158c126a6cd93aa7d4aaee15bcf1beae224c04363cbf088193a696802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3bfe80b544c3eab56180ce31f7d2ffaefd102aef456e67e4a92bc1baaacb0551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162455990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6a7ec181f30ef057aceb9ee70680497cde2128e2f0e8b7895dcefe5684927`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 23 Jun 2022 04:06:19 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Thu, 23 Jun 2022 04:06:20 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:38 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:38 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:39 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:39 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55f87b960ba60fdf9904d8162ee1c85660f3d22ed460c364165aca6e8603fa9`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:459044ae96d113c919f15cdf316e7d153663d23955a08e1b9f894bfdf4a7bd74`  
		Last Modified: Thu, 23 Jun 2022 04:08:08 GMT  
		Size: 115.7 MB (115675698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc62f07e93a5407036b7a3800d3d58044725a81a8168c4724075c4297b82572`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b9a5e106092c3f06ca35c9a385836db1cd5225b6b5fa1aad35a26373e1e79f`  
		Last Modified: Thu, 23 Jun 2022 04:07:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-oracle`

```console
$ docker pull mysql@sha256:c67e9e97879305e0c7a4934372f35bdb7d79d4a0914d7304d0ee6836be0127a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3030fdb1154e62ed44c2e2dbbc7dee2643ee27fb6dd201b06b19a87682498e8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126873058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19b3d18c4a01f69bdb995e46233fcdcc66c1ef84bc8d28396e981c020e395ee`
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
# Thu, 16 Jun 2022 01:38:55 GMT
RUN set -eux; 	yum install -y 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Thu, 16 Jun 2022 01:38:56 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 16 Jun 2022 01:38:56 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 16 Jun 2022 01:38:56 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Thu, 16 Jun 2022 01:38:57 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 16 Jun 2022 01:39:11 GMT
RUN set -eux; 	yum install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Thu, 16 Jun 2022 01:39:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 16 Jun 2022 01:39:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Thu, 16 Jun 2022 01:39:29 GMT
RUN set -eux; 	yum install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Thu, 16 Jun 2022 01:39:30 GMT
VOLUME [/var/lib/mysql]
# Thu, 16 Jun 2022 01:39:30 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 16 Jun 2022 01:39:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Jun 2022 01:39:31 GMT
EXPOSE 3306 33060
# Thu, 16 Jun 2022 01:39:31 GMT
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
	-	`sha256:8e1ea46ae00991c24638c08d268652beb0ce5b878c83d34964f12345618c8941`  
		Last Modified: Thu, 16 Jun 2022 01:40:11 GMT  
		Size: 3.8 MB (3750823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15dccdcd437d9fe54d225731d32bb52246dc75794a5d49e7f12010322dd06c1`  
		Last Modified: Thu, 16 Jun 2022 01:40:08 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1050fbf8b84448d369e5743034ffd13580e9313a7e5092eace10220aa687f9b`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848d1501cd8fc9f77a4e51a2e6dc077dcc0e468191ffaf2f433a4ffb4f7f63c1`  
		Last Modified: Thu, 16 Jun 2022 01:40:10 GMT  
		Size: 25.5 MB (25466694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f50b8fa8c9ba100ca41212bdb8cb892fa707fb9395959c967bcc9355b3ddea`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8b3d4a8dbcebd64c0cd3dcde292b97e52335441dac4d3c0e8e010d1197578b`  
		Last Modified: Thu, 16 Jun 2022 01:40:15 GMT  
		Size: 48.0 MB (47957859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4284667ffa5966a13950eda5dee3eb23bc10e60d2dee427c9e7c18c789099568`  
		Last Modified: Thu, 16 Jun 2022 01:40:06 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:56bf447e156cf9abcd862d140527647d25331cd18f3546849e684de1172c6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:940fdfa3dc408fb792a8cceb21cafda4b7cd56ce4fbc32833766bdd2a57d6a4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfb2bcbf716a71cdb2dd51277575869547854e0c57519c03cd5d5cec58a9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:39:39 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 18:39:39 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 18:39:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 14 Jun 2022 18:40:04 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:40:05 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:40:06 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 14 Jun 2022 18:40:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 14 Jun 2022 18:40:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 14 Jun 2022 18:40:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:41:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 14 Jun 2022 18:41:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jun 2022 18:41:10 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 14 Jun 2022 18:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jun 2022 18:41:11 GMT
EXPOSE 3306 33060
# Tue, 14 Jun 2022 18:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c3d841d1984f858257755bdf734554725af4f926f3b1d1b22f119cce8bda9`  
		Last Modified: Tue, 14 Jun 2022 18:41:49 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f026b3ec1ed102cfe531d812e2063669bad08ac3a0ac68a31e44083d9b9a5f5d`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b2ddd662a38dbb423dbaa2be04afd41904253b436138b52f2a73aa46a5547`  
		Last Modified: Tue, 14 Jun 2022 18:41:48 GMT  
		Size: 4.5 MB (4535169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7724a6d28d1e789da86c89f0010caa7de0e4747dfcd360fa981a194850951f`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122570b85fec5c1d3bc0c08a48be2657da195b764c9a13b1a791a086c007368`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea018df6cdc3d2aa821feb43a3035926c0c296b3c363e64ab0fa95f144f2e7b`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 47.2 MB (47244178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8066c16abd2efdd49dd1fe3fab6fec9d250b699d9c0227f69c779c8da2c2acd6`  
		Last Modified: Tue, 14 Jun 2022 18:41:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd480e7da7ced7cfb1fb54d07fc5eb08057151be162150bd053f4eb89d9ba85f`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 39.7 MB (39698832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b680e02f092e5330cf0200abf3ba02bddc3d440d02ebb11ec6ed8bf2ba3155`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0418232b74414d7e223da6fc26f47d9498abd72b4ca3bb1cd826f8f05ea55374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138660393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0eef221ccdafeb4649e0af86a16d1bf826ed66807fd64248a212871c04c2a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 19:17:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 19:17:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 27 Jun 2022 23:40:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Mon, 27 Jun 2022 23:40:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Mon, 27 Jun 2022 23:40:28 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 27 Jun 2022 23:40:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:40:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Mon, 27 Jun 2022 23:40:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:41:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Mon, 27 Jun 2022 23:41:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 27 Jun 2022 23:41:29 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 27 Jun 2022 23:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 23:41:30 GMT
EXPOSE 3306 33060
# Mon, 27 Jun 2022 23:41:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428f9d18fc319262a774f75a5849d4819b5b44cbf07fbb5e3c262e5cf30c22d`  
		Last Modified: Tue, 14 Jun 2022 19:19:14 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cba94044003680a99c76f187ea817c71b843de38bb7f28faf8ca6508efd45e`  
		Last Modified: Tue, 14 Jun 2022 19:19:12 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac1107eaf64ada9002dc0dbf73e0a8b8c2a3e2dfe557a59ee79ae5296dd6d35`  
		Last Modified: Mon, 27 Jun 2022 23:41:57 GMT  
		Size: 4.4 MB (4400369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287b497aedf9bf453ca624e6f7b036489fa7091918b209ff279b763cecaff56e`  
		Last Modified: Mon, 27 Jun 2022 23:41:56 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95691dcdde5f2ee25bddc7d7b86e909e83b4afb1e4df5fad18d9522c3f510579`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782ffaaa3341fdec1b0c7406c0492d5cff1a9970a6bd418392b7174e60bea6f`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 53.3 MB (53324071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01dd932f22732278b472cba5572dc1447697a6c2ef0d4ad0fb6f0d9ae009d07`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d729e5c05f924689961a0ec3f59e39b68696747fe8e84592e0c7d3466f264bef`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 42.1 MB (42056996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abe7fac72065516d8f16acb9fddfb5df729c103afd883ab5c353157a60ae4be`  
		Last Modified: Mon, 27 Jun 2022 23:41:53 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:56bf447e156cf9abcd862d140527647d25331cd18f3546849e684de1172c6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:940fdfa3dc408fb792a8cceb21cafda4b7cd56ce4fbc32833766bdd2a57d6a4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfb2bcbf716a71cdb2dd51277575869547854e0c57519c03cd5d5cec58a9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:39:39 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 18:39:39 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 18:39:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 14 Jun 2022 18:40:04 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:40:05 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:40:06 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 14 Jun 2022 18:40:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 14 Jun 2022 18:40:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 14 Jun 2022 18:40:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:41:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 14 Jun 2022 18:41:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jun 2022 18:41:10 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 14 Jun 2022 18:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jun 2022 18:41:11 GMT
EXPOSE 3306 33060
# Tue, 14 Jun 2022 18:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c3d841d1984f858257755bdf734554725af4f926f3b1d1b22f119cce8bda9`  
		Last Modified: Tue, 14 Jun 2022 18:41:49 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f026b3ec1ed102cfe531d812e2063669bad08ac3a0ac68a31e44083d9b9a5f5d`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b2ddd662a38dbb423dbaa2be04afd41904253b436138b52f2a73aa46a5547`  
		Last Modified: Tue, 14 Jun 2022 18:41:48 GMT  
		Size: 4.5 MB (4535169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7724a6d28d1e789da86c89f0010caa7de0e4747dfcd360fa981a194850951f`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122570b85fec5c1d3bc0c08a48be2657da195b764c9a13b1a791a086c007368`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea018df6cdc3d2aa821feb43a3035926c0c296b3c363e64ab0fa95f144f2e7b`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 47.2 MB (47244178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8066c16abd2efdd49dd1fe3fab6fec9d250b699d9c0227f69c779c8da2c2acd6`  
		Last Modified: Tue, 14 Jun 2022 18:41:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd480e7da7ced7cfb1fb54d07fc5eb08057151be162150bd053f4eb89d9ba85f`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 39.7 MB (39698832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b680e02f092e5330cf0200abf3ba02bddc3d440d02ebb11ec6ed8bf2ba3155`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0418232b74414d7e223da6fc26f47d9498abd72b4ca3bb1cd826f8f05ea55374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138660393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0eef221ccdafeb4649e0af86a16d1bf826ed66807fd64248a212871c04c2a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 19:17:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 19:17:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 27 Jun 2022 23:40:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Mon, 27 Jun 2022 23:40:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Mon, 27 Jun 2022 23:40:28 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 27 Jun 2022 23:40:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:40:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Mon, 27 Jun 2022 23:40:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:41:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Mon, 27 Jun 2022 23:41:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 27 Jun 2022 23:41:29 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 27 Jun 2022 23:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 23:41:30 GMT
EXPOSE 3306 33060
# Mon, 27 Jun 2022 23:41:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428f9d18fc319262a774f75a5849d4819b5b44cbf07fbb5e3c262e5cf30c22d`  
		Last Modified: Tue, 14 Jun 2022 19:19:14 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cba94044003680a99c76f187ea817c71b843de38bb7f28faf8ca6508efd45e`  
		Last Modified: Tue, 14 Jun 2022 19:19:12 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac1107eaf64ada9002dc0dbf73e0a8b8c2a3e2dfe557a59ee79ae5296dd6d35`  
		Last Modified: Mon, 27 Jun 2022 23:41:57 GMT  
		Size: 4.4 MB (4400369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287b497aedf9bf453ca624e6f7b036489fa7091918b209ff279b763cecaff56e`  
		Last Modified: Mon, 27 Jun 2022 23:41:56 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95691dcdde5f2ee25bddc7d7b86e909e83b4afb1e4df5fad18d9522c3f510579`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782ffaaa3341fdec1b0c7406c0492d5cff1a9970a6bd418392b7174e60bea6f`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 53.3 MB (53324071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01dd932f22732278b472cba5572dc1447697a6c2ef0d4ad0fb6f0d9ae009d07`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d729e5c05f924689961a0ec3f59e39b68696747fe8e84592e0c7d3466f264bef`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 42.1 MB (42056996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abe7fac72065516d8f16acb9fddfb5df729c103afd883ab5c353157a60ae4be`  
		Last Modified: Mon, 27 Jun 2022 23:41:53 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-debian`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29-debian` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-oracle`

```console
$ docker pull mysql@sha256:56bf447e156cf9abcd862d140527647d25331cd18f3546849e684de1172c6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.29-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:940fdfa3dc408fb792a8cceb21cafda4b7cd56ce4fbc32833766bdd2a57d6a4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfb2bcbf716a71cdb2dd51277575869547854e0c57519c03cd5d5cec58a9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:39:39 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 18:39:39 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 18:39:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 14 Jun 2022 18:40:04 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:40:05 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:40:06 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 14 Jun 2022 18:40:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 14 Jun 2022 18:40:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 14 Jun 2022 18:40:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:41:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 14 Jun 2022 18:41:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jun 2022 18:41:10 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 14 Jun 2022 18:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jun 2022 18:41:11 GMT
EXPOSE 3306 33060
# Tue, 14 Jun 2022 18:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c3d841d1984f858257755bdf734554725af4f926f3b1d1b22f119cce8bda9`  
		Last Modified: Tue, 14 Jun 2022 18:41:49 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f026b3ec1ed102cfe531d812e2063669bad08ac3a0ac68a31e44083d9b9a5f5d`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b2ddd662a38dbb423dbaa2be04afd41904253b436138b52f2a73aa46a5547`  
		Last Modified: Tue, 14 Jun 2022 18:41:48 GMT  
		Size: 4.5 MB (4535169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7724a6d28d1e789da86c89f0010caa7de0e4747dfcd360fa981a194850951f`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122570b85fec5c1d3bc0c08a48be2657da195b764c9a13b1a791a086c007368`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea018df6cdc3d2aa821feb43a3035926c0c296b3c363e64ab0fa95f144f2e7b`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 47.2 MB (47244178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8066c16abd2efdd49dd1fe3fab6fec9d250b699d9c0227f69c779c8da2c2acd6`  
		Last Modified: Tue, 14 Jun 2022 18:41:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd480e7da7ced7cfb1fb54d07fc5eb08057151be162150bd053f4eb89d9ba85f`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 39.7 MB (39698832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b680e02f092e5330cf0200abf3ba02bddc3d440d02ebb11ec6ed8bf2ba3155`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.29-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0418232b74414d7e223da6fc26f47d9498abd72b4ca3bb1cd826f8f05ea55374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138660393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0eef221ccdafeb4649e0af86a16d1bf826ed66807fd64248a212871c04c2a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 19:17:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 19:17:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 27 Jun 2022 23:40:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Mon, 27 Jun 2022 23:40:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Mon, 27 Jun 2022 23:40:28 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 27 Jun 2022 23:40:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:40:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Mon, 27 Jun 2022 23:40:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:41:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Mon, 27 Jun 2022 23:41:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 27 Jun 2022 23:41:29 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 27 Jun 2022 23:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 23:41:30 GMT
EXPOSE 3306 33060
# Mon, 27 Jun 2022 23:41:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428f9d18fc319262a774f75a5849d4819b5b44cbf07fbb5e3c262e5cf30c22d`  
		Last Modified: Tue, 14 Jun 2022 19:19:14 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cba94044003680a99c76f187ea817c71b843de38bb7f28faf8ca6508efd45e`  
		Last Modified: Tue, 14 Jun 2022 19:19:12 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac1107eaf64ada9002dc0dbf73e0a8b8c2a3e2dfe557a59ee79ae5296dd6d35`  
		Last Modified: Mon, 27 Jun 2022 23:41:57 GMT  
		Size: 4.4 MB (4400369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287b497aedf9bf453ca624e6f7b036489fa7091918b209ff279b763cecaff56e`  
		Last Modified: Mon, 27 Jun 2022 23:41:56 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95691dcdde5f2ee25bddc7d7b86e909e83b4afb1e4df5fad18d9522c3f510579`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782ffaaa3341fdec1b0c7406c0492d5cff1a9970a6bd418392b7174e60bea6f`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 53.3 MB (53324071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01dd932f22732278b472cba5572dc1447697a6c2ef0d4ad0fb6f0d9ae009d07`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d729e5c05f924689961a0ec3f59e39b68696747fe8e84592e0c7d3466f264bef`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 42.1 MB (42056996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abe7fac72065516d8f16acb9fddfb5df729c103afd883ab5c353157a60ae4be`  
		Last Modified: Mon, 27 Jun 2022 23:41:53 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:bed914af3f2dea400c4bc83136d6b3a8cf7edcf96f5c08bbbdec8a10cc021a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a05245c2b031387e07f86aeb6f9d7e35a771e1dfc85458c8aa3b02f67085fa65
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968083d5be3605e3b447838e3688ba43cfc297f9a6dec9c708389cfcfc36a080`
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
# Thu, 23 Jun 2022 04:05:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 23 Jun 2022 04:05:52 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Thu, 23 Jun 2022 04:05:53 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 23 Jun 2022 04:06:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 23 Jun 2022 04:06:08 GMT
VOLUME [/var/lib/mysql]
# Thu, 23 Jun 2022 04:06:08 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 23 Jun 2022 04:06:08 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 23 Jun 2022 04:06:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 23 Jun 2022 04:06:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 04:06:09 GMT
EXPOSE 3306 33060
# Thu, 23 Jun 2022 04:06:09 GMT
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
	-	`sha256:32cfafb64feec49978becdecb502d0ad9f31c876265514aa4f2ebfcbd29609f7`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 14.1 MB (14064315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9caad7ee0fc84322eefd314c6b0038f6118f2767b8bc3e0cfde713a4fa35c4d`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ed38840e96e53752528926957e0067dd594eb1021be26a59e7f519bc0790a3`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a172dc2c4c7d38fada39395a5db52f0ca112b6ee2b5ab72c31c6b82e706606e`  
		Last Modified: Thu, 23 Jun 2022 04:07:23 GMT  
		Size: 109.1 MB (109103673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800b83bd0240f41f2cb8352909a3dd8ea177d095b5fdad170483865dc625b42`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20e07df03fa936c6c54593ecf95be53bd632d767fad30e398c7b79b0ef2d1c1`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 5.2 KB (5156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ad187ab64aadaf3bc6ceeb8c41dbedb2bf541f4e257c5214bdc7d1fbe098`  
		Last Modified: Thu, 23 Jun 2022 04:07:07 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:56bf447e156cf9abcd862d140527647d25331cd18f3546849e684de1172c6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:940fdfa3dc408fb792a8cceb21cafda4b7cd56ce4fbc32833766bdd2a57d6a4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.6 MB (131636256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcfb2bcbf716a71cdb2dd51277575869547854e0c57519c03cd5d5cec58a9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:23:26 GMT
ADD file:837f6c6e7e20067b92edb72e78a8399e6cbbd72dab23db7b5b5a301c58d2a0de in / 
# Tue, 14 Jun 2022 18:23:26 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 18:39:39 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 18:39:39 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 18:39:43 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 14 Jun 2022 18:40:04 GMT
RUN set -eux; 	microdnf install -y 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 14 Jun 2022 18:40:05 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 14 Jun 2022 18:40:06 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:40:06 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 14 Jun 2022 18:40:34 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 14 Jun 2022 18:40:35 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 14 Jun 2022 18:40:35 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 14 Jun 2022 18:41:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 14 Jun 2022 18:41:10 GMT
VOLUME [/var/lib/mysql]
# Tue, 14 Jun 2022 18:41:10 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 14 Jun 2022 18:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Jun 2022 18:41:11 GMT
EXPOSE 3306 33060
# Tue, 14 Jun 2022 18:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:5f160c0f6cac587a73883b48a8857f5cce0930112792cef25c62510e256e93dc`  
		Last Modified: Tue, 14 Jun 2022 18:24:18 GMT  
		Size: 39.2 MB (39219730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c3d841d1984f858257755bdf734554725af4f926f3b1d1b22f119cce8bda9`  
		Last Modified: Tue, 14 Jun 2022 18:41:49 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f026b3ec1ed102cfe531d812e2063669bad08ac3a0ac68a31e44083d9b9a5f5d`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 928.8 KB (928831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d80b2ddd662a38dbb423dbaa2be04afd41904253b436138b52f2a73aa46a5547`  
		Last Modified: Tue, 14 Jun 2022 18:41:48 GMT  
		Size: 4.5 MB (4535169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7724a6d28d1e789da86c89f0010caa7de0e4747dfcd360fa981a194850951f`  
		Last Modified: Tue, 14 Jun 2022 18:41:47 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122570b85fec5c1d3bc0c08a48be2657da195b764c9a13b1a791a086c007368`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea018df6cdc3d2aa821feb43a3035926c0c296b3c363e64ab0fa95f144f2e7b`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 47.2 MB (47244178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8066c16abd2efdd49dd1fe3fab6fec9d250b699d9c0227f69c779c8da2c2acd6`  
		Last Modified: Tue, 14 Jun 2022 18:41:44 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd480e7da7ced7cfb1fb54d07fc5eb08057151be162150bd053f4eb89d9ba85f`  
		Last Modified: Tue, 14 Jun 2022 18:41:52 GMT  
		Size: 39.7 MB (39698832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b680e02f092e5330cf0200abf3ba02bddc3d440d02ebb11ec6ed8bf2ba3155`  
		Last Modified: Tue, 14 Jun 2022 18:41:45 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:0418232b74414d7e223da6fc26f47d9498abd72b4ca3bb1cd826f8f05ea55374
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138660393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a0eef221ccdafeb4649e0af86a16d1bf826ed66807fd64248a212871c04c2a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 14 Jun 2022 18:41:36 GMT
ADD file:4a6ee90ad73353bfb87b2f121e06bddaed6104536e485baa83fadbe7facc774c in / 
# Tue, 14 Jun 2022 18:41:37 GMT
CMD ["/bin/bash"]
# Tue, 14 Jun 2022 19:17:17 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 14 Jun 2022 19:17:17 GMT
ENV GOSU_VERSION=1.14
# Tue, 14 Jun 2022 19:17:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 27 Jun 2022 23:40:26 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Mon, 27 Jun 2022 23:40:27 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Mon, 27 Jun 2022 23:40:28 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 27 Jun 2022 23:40:29 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:40:30 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Mon, 27 Jun 2022 23:40:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Mon, 27 Jun 2022 23:40:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Mon, 27 Jun 2022 23:41:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Mon, 27 Jun 2022 23:41:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 27 Jun 2022 23:41:29 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Mon, 27 Jun 2022 23:41:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 27 Jun 2022 23:41:30 GMT
EXPOSE 3306 33060
# Mon, 27 Jun 2022 23:41:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2bbc1bf883bd601c0da5735b538963308bcc17f90d36525ecc93456ffad79064`  
		Last Modified: Tue, 14 Jun 2022 18:42:39 GMT  
		Size: 38.0 MB (38012371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8428f9d18fc319262a774f75a5849d4819b5b44cbf07fbb5e3c262e5cf30c22d`  
		Last Modified: Tue, 14 Jun 2022 19:19:14 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cba94044003680a99c76f187ea817c71b843de38bb7f28faf8ca6508efd45e`  
		Last Modified: Tue, 14 Jun 2022 19:19:12 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac1107eaf64ada9002dc0dbf73e0a8b8c2a3e2dfe557a59ee79ae5296dd6d35`  
		Last Modified: Mon, 27 Jun 2022 23:41:57 GMT  
		Size: 4.4 MB (4400369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287b497aedf9bf453ca624e6f7b036489fa7091918b209ff279b763cecaff56e`  
		Last Modified: Mon, 27 Jun 2022 23:41:56 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95691dcdde5f2ee25bddc7d7b86e909e83b4afb1e4df5fad18d9522c3f510579`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5782ffaaa3341fdec1b0c7406c0492d5cff1a9970a6bd418392b7174e60bea6f`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 53.3 MB (53324071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01dd932f22732278b472cba5572dc1447697a6c2ef0d4ad0fb6f0d9ae009d07`  
		Last Modified: Mon, 27 Jun 2022 23:41:54 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d729e5c05f924689961a0ec3f59e39b68696747fe8e84592e0c7d3466f264bef`  
		Last Modified: Mon, 27 Jun 2022 23:42:01 GMT  
		Size: 42.1 MB (42056996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4abe7fac72065516d8f16acb9fddfb5df729c103afd883ab5c353157a60ae4be`  
		Last Modified: Mon, 27 Jun 2022 23:41:53 GMT  
		Size: 5.2 KB (5161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
