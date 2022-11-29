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
$ docker pull mysql@sha256:4149a92977a54d27cbd6f81cca3817e6278a844d566b45f9ff1908bb2714b1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:d984f298e32e8f81e2a821a6e771214c924b9f31db6d0c9dcf4b16f87f4cbebf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144288550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d44289af6858f5d6b118c8d1547679d70b752ec179740785d7452081de8cb31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:40:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:40:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:40:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:40:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:41:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:41:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:41:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Tue, 29 Nov 2022 19:41:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:41:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:41:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:41:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:41:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:41:39 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:41:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feae47af51d5f4035f28ed6483d53446e27ca9a23d69287f9a4fa64daf185041`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d38b9fa31e439ed2eebb9c14f5880600bb44f5dda47872008e02a89af7275`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da689aaabebf7976a587488d0de04efdef955e838850c8777ac85acd70b97837`  
		Last Modified: Tue, 29 Nov 2022 19:42:52 GMT  
		Size: 4.5 MB (4538915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a532732deb806e40acfcdb0d32d19a3bfabd6b3ace779002a098e6f94ffde`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9063a4855045ea193d5757ab3b873e8329edc94ded524c8c5747b896176cadf6`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a84b6adf6c71ed27390306faffb1d36960a0708f0dadc706fd590c7c4dbce`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 25.5 MB (25531824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7084e7269f301d2e1ffdf0baf60a5d36447aee8205c39f432417135c2c0976b5`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161795475ff3e916bbd9969c72a9e325f1643b09ce403bfee1468ea51fffd9b8`  
		Last Modified: Tue, 29 Nov 2022 19:43:01 GMT  
		Size: 63.4 MB (63449731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f7a84c8fc14f3e17e08a228839803e09ab9ca40170cba3292bc2d8f7a3df7`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf120096e55e03864f868a4131aecb131259c201755b888816f4654791fed01f`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:b877923d9a3a233605b6fff7b1b66096ef95347953bdf8b53c644e4e4c2d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b70c887f9caf0bbdd214a7c6c768355de13ecc7ccb9b03cafc4e0e72873e129d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162596876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85827503cde163497fe4dbc3c1c81d705b4db09166376e8b53a4d82763afd3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:02:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 15 Nov 2022 13:02:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 15 Nov 2022 13:03:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 13:03:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 15 Nov 2022 13:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:03:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 15 Nov 2022 13:03:09 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 15 Nov 2022 13:03:10 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 15 Nov 2022 13:03:10 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 15 Nov 2022 13:03:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 15 Nov 2022 13:03:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Nov 2022 13:03:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 15 Nov 2022 13:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:03:32 GMT
EXPOSE 3306 33060
# Tue, 15 Nov 2022 13:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a510d044b7fa285ab11ff2b921630bf7ef7f783b0d3b542b234756ff720a31`  
		Last Modified: Tue, 15 Nov 2022 13:04:46 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500105bda35026801de8c6b90a30c9c85dec9b17f329cc3cc8a290f7ec05d6c6`  
		Last Modified: Tue, 15 Nov 2022 13:04:44 GMT  
		Size: 4.2 MB (4182273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec0e829cb9c63abf33de3fba81f75214179f0e5fee33b4214497d2a1f6ceea1`  
		Last Modified: Tue, 15 Nov 2022 13:04:44 GMT  
		Size: 1.4 MB (1388891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05c9bcf57a0a6c938a4b447879a9b8b036037261f3284ceee456e7b02b3550b`  
		Last Modified: Tue, 15 Nov 2022 13:04:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fdb9acf81ea37d01f79d899999afd5cd9ad86595417f864e19cdb3d5a1fffb`  
		Last Modified: Tue, 15 Nov 2022 13:04:46 GMT  
		Size: 14.1 MB (14089378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f2f570a6edd65c0b3b554251d968470097014d810adfb27b96a98cd2e4a433`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e884a2e58d9fcc54acea7d3e39908d7ecd42e1edfef73bb68191b54f991c6e67`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9a1ff5f61c69e0b99c23045ec864acc99c0977ee4ff08e72fec757c2553f2b`  
		Last Modified: Tue, 15 Nov 2022 13:04:57 GMT  
		Size: 115.8 MB (115785814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db447849bdf4798b71bf9356ea7bb877bccdb13cbfcc41950625bd7f999a6ebb`  
		Last Modified: Tue, 15 Nov 2022 13:04:41 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4186431df56dd92a17a34b42da70b499494a80076ce02b2f62ab6d4b842d04c`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:4149a92977a54d27cbd6f81cca3817e6278a844d566b45f9ff1908bb2714b1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d984f298e32e8f81e2a821a6e771214c924b9f31db6d0c9dcf4b16f87f4cbebf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144288550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d44289af6858f5d6b118c8d1547679d70b752ec179740785d7452081de8cb31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:40:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:40:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:40:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:40:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:41:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:41:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:41:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Tue, 29 Nov 2022 19:41:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:41:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:41:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:41:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:41:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:41:39 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:41:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feae47af51d5f4035f28ed6483d53446e27ca9a23d69287f9a4fa64daf185041`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d38b9fa31e439ed2eebb9c14f5880600bb44f5dda47872008e02a89af7275`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da689aaabebf7976a587488d0de04efdef955e838850c8777ac85acd70b97837`  
		Last Modified: Tue, 29 Nov 2022 19:42:52 GMT  
		Size: 4.5 MB (4538915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a532732deb806e40acfcdb0d32d19a3bfabd6b3ace779002a098e6f94ffde`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9063a4855045ea193d5757ab3b873e8329edc94ded524c8c5747b896176cadf6`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a84b6adf6c71ed27390306faffb1d36960a0708f0dadc706fd590c7c4dbce`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 25.5 MB (25531824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7084e7269f301d2e1ffdf0baf60a5d36447aee8205c39f432417135c2c0976b5`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161795475ff3e916bbd9969c72a9e325f1643b09ce403bfee1468ea51fffd9b8`  
		Last Modified: Tue, 29 Nov 2022 19:43:01 GMT  
		Size: 63.4 MB (63449731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f7a84c8fc14f3e17e08a228839803e09ab9ca40170cba3292bc2d8f7a3df7`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf120096e55e03864f868a4131aecb131259c201755b888816f4654791fed01f`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:4149a92977a54d27cbd6f81cca3817e6278a844d566b45f9ff1908bb2714b1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:d984f298e32e8f81e2a821a6e771214c924b9f31db6d0c9dcf4b16f87f4cbebf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144288550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d44289af6858f5d6b118c8d1547679d70b752ec179740785d7452081de8cb31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:40:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:40:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:40:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:40:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:41:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:41:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:41:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Tue, 29 Nov 2022 19:41:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:41:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:41:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:41:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:41:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:41:39 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:41:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feae47af51d5f4035f28ed6483d53446e27ca9a23d69287f9a4fa64daf185041`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d38b9fa31e439ed2eebb9c14f5880600bb44f5dda47872008e02a89af7275`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da689aaabebf7976a587488d0de04efdef955e838850c8777ac85acd70b97837`  
		Last Modified: Tue, 29 Nov 2022 19:42:52 GMT  
		Size: 4.5 MB (4538915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a532732deb806e40acfcdb0d32d19a3bfabd6b3ace779002a098e6f94ffde`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9063a4855045ea193d5757ab3b873e8329edc94ded524c8c5747b896176cadf6`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a84b6adf6c71ed27390306faffb1d36960a0708f0dadc706fd590c7c4dbce`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 25.5 MB (25531824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7084e7269f301d2e1ffdf0baf60a5d36447aee8205c39f432417135c2c0976b5`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161795475ff3e916bbd9969c72a9e325f1643b09ce403bfee1468ea51fffd9b8`  
		Last Modified: Tue, 29 Nov 2022 19:43:01 GMT  
		Size: 63.4 MB (63449731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f7a84c8fc14f3e17e08a228839803e09ab9ca40170cba3292bc2d8f7a3df7`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf120096e55e03864f868a4131aecb131259c201755b888816f4654791fed01f`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:b877923d9a3a233605b6fff7b1b66096ef95347953bdf8b53c644e4e4c2d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b70c887f9caf0bbdd214a7c6c768355de13ecc7ccb9b03cafc4e0e72873e129d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162596876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85827503cde163497fe4dbc3c1c81d705b4db09166376e8b53a4d82763afd3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:02:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 15 Nov 2022 13:02:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 15 Nov 2022 13:03:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 13:03:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 15 Nov 2022 13:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:03:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 15 Nov 2022 13:03:09 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 15 Nov 2022 13:03:10 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 15 Nov 2022 13:03:10 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 15 Nov 2022 13:03:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 15 Nov 2022 13:03:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Nov 2022 13:03:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 15 Nov 2022 13:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:03:32 GMT
EXPOSE 3306 33060
# Tue, 15 Nov 2022 13:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a510d044b7fa285ab11ff2b921630bf7ef7f783b0d3b542b234756ff720a31`  
		Last Modified: Tue, 15 Nov 2022 13:04:46 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500105bda35026801de8c6b90a30c9c85dec9b17f329cc3cc8a290f7ec05d6c6`  
		Last Modified: Tue, 15 Nov 2022 13:04:44 GMT  
		Size: 4.2 MB (4182273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec0e829cb9c63abf33de3fba81f75214179f0e5fee33b4214497d2a1f6ceea1`  
		Last Modified: Tue, 15 Nov 2022 13:04:44 GMT  
		Size: 1.4 MB (1388891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05c9bcf57a0a6c938a4b447879a9b8b036037261f3284ceee456e7b02b3550b`  
		Last Modified: Tue, 15 Nov 2022 13:04:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fdb9acf81ea37d01f79d899999afd5cd9ad86595417f864e19cdb3d5a1fffb`  
		Last Modified: Tue, 15 Nov 2022 13:04:46 GMT  
		Size: 14.1 MB (14089378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f2f570a6edd65c0b3b554251d968470097014d810adfb27b96a98cd2e4a433`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e884a2e58d9fcc54acea7d3e39908d7ecd42e1edfef73bb68191b54f991c6e67`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9a1ff5f61c69e0b99c23045ec864acc99c0977ee4ff08e72fec757c2553f2b`  
		Last Modified: Tue, 15 Nov 2022 13:04:57 GMT  
		Size: 115.8 MB (115785814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db447849bdf4798b71bf9356ea7bb877bccdb13cbfcc41950625bd7f999a6ebb`  
		Last Modified: Tue, 15 Nov 2022 13:04:41 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4186431df56dd92a17a34b42da70b499494a80076ce02b2f62ab6d4b842d04c`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:4149a92977a54d27cbd6f81cca3817e6278a844d566b45f9ff1908bb2714b1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d984f298e32e8f81e2a821a6e771214c924b9f31db6d0c9dcf4b16f87f4cbebf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144288550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d44289af6858f5d6b118c8d1547679d70b752ec179740785d7452081de8cb31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:40:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:40:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:40:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:40:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:41:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:41:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:41:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Tue, 29 Nov 2022 19:41:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:41:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:41:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:41:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:41:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:41:39 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:41:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feae47af51d5f4035f28ed6483d53446e27ca9a23d69287f9a4fa64daf185041`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d38b9fa31e439ed2eebb9c14f5880600bb44f5dda47872008e02a89af7275`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da689aaabebf7976a587488d0de04efdef955e838850c8777ac85acd70b97837`  
		Last Modified: Tue, 29 Nov 2022 19:42:52 GMT  
		Size: 4.5 MB (4538915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a532732deb806e40acfcdb0d32d19a3bfabd6b3ace779002a098e6f94ffde`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9063a4855045ea193d5757ab3b873e8329edc94ded524c8c5747b896176cadf6`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a84b6adf6c71ed27390306faffb1d36960a0708f0dadc706fd590c7c4dbce`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 25.5 MB (25531824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7084e7269f301d2e1ffdf0baf60a5d36447aee8205c39f432417135c2c0976b5`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161795475ff3e916bbd9969c72a9e325f1643b09ce403bfee1468ea51fffd9b8`  
		Last Modified: Tue, 29 Nov 2022 19:43:01 GMT  
		Size: 63.4 MB (63449731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f7a84c8fc14f3e17e08a228839803e09ab9ca40170cba3292bc2d8f7a3df7`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf120096e55e03864f868a4131aecb131259c201755b888816f4654791fed01f`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40`

```console
$ docker pull mysql@sha256:4149a92977a54d27cbd6f81cca3817e6278a844d566b45f9ff1908bb2714b1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40` - linux; amd64

```console
$ docker pull mysql@sha256:d984f298e32e8f81e2a821a6e771214c924b9f31db6d0c9dcf4b16f87f4cbebf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144288550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d44289af6858f5d6b118c8d1547679d70b752ec179740785d7452081de8cb31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:40:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:40:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:40:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:40:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:41:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:41:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:41:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Tue, 29 Nov 2022 19:41:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:41:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:41:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:41:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:41:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:41:39 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:41:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feae47af51d5f4035f28ed6483d53446e27ca9a23d69287f9a4fa64daf185041`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d38b9fa31e439ed2eebb9c14f5880600bb44f5dda47872008e02a89af7275`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da689aaabebf7976a587488d0de04efdef955e838850c8777ac85acd70b97837`  
		Last Modified: Tue, 29 Nov 2022 19:42:52 GMT  
		Size: 4.5 MB (4538915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a532732deb806e40acfcdb0d32d19a3bfabd6b3ace779002a098e6f94ffde`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9063a4855045ea193d5757ab3b873e8329edc94ded524c8c5747b896176cadf6`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a84b6adf6c71ed27390306faffb1d36960a0708f0dadc706fd590c7c4dbce`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 25.5 MB (25531824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7084e7269f301d2e1ffdf0baf60a5d36447aee8205c39f432417135c2c0976b5`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161795475ff3e916bbd9969c72a9e325f1643b09ce403bfee1468ea51fffd9b8`  
		Last Modified: Tue, 29 Nov 2022 19:43:01 GMT  
		Size: 63.4 MB (63449731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f7a84c8fc14f3e17e08a228839803e09ab9ca40170cba3292bc2d8f7a3df7`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf120096e55e03864f868a4131aecb131259c201755b888816f4654791fed01f`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40-debian`

```console
$ docker pull mysql@sha256:b877923d9a3a233605b6fff7b1b66096ef95347953bdf8b53c644e4e4c2d6bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b70c887f9caf0bbdd214a7c6c768355de13ecc7ccb9b03cafc4e0e72873e129d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162596876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85827503cde163497fe4dbc3c1c81d705b4db09166376e8b53a4d82763afd3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Nov 2022 04:05:14 GMT
ADD file:9461639b945ced6fb6164491a7e0131261a1b7d69264cce516e75c71e4df22d2 in / 
# Tue, 15 Nov 2022 04:05:14 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:02:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 15 Nov 2022 13:02:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:52 GMT
ENV GOSU_VERSION=1.14
# Tue, 15 Nov 2022 13:03:01 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 13:03:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 15 Nov 2022 13:03:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:03:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 15 Nov 2022 13:03:09 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 15 Nov 2022 13:03:10 GMT
ENV MYSQL_VERSION=5.7.40-1debian10
# Tue, 15 Nov 2022 13:03:10 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 15 Nov 2022 13:03:30 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 15 Nov 2022 13:03:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Nov 2022 13:03:31 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:03:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 15 Nov 2022 13:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:03:32 GMT
EXPOSE 3306 33060
# Tue, 15 Nov 2022 13:03:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:32820e52a00eb22dc76d70d992be7082cd24b636cfb597ff3951d29a821b46b9`  
		Last Modified: Tue, 15 Nov 2022 04:09:26 GMT  
		Size: 27.1 MB (27140332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a510d044b7fa285ab11ff2b921630bf7ef7f783b0d3b542b234756ff720a31`  
		Last Modified: Tue, 15 Nov 2022 13:04:46 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:500105bda35026801de8c6b90a30c9c85dec9b17f329cc3cc8a290f7ec05d6c6`  
		Last Modified: Tue, 15 Nov 2022 13:04:44 GMT  
		Size: 4.2 MB (4182273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec0e829cb9c63abf33de3fba81f75214179f0e5fee33b4214497d2a1f6ceea1`  
		Last Modified: Tue, 15 Nov 2022 13:04:44 GMT  
		Size: 1.4 MB (1388891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05c9bcf57a0a6c938a4b447879a9b8b036037261f3284ceee456e7b02b3550b`  
		Last Modified: Tue, 15 Nov 2022 13:04:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fdb9acf81ea37d01f79d899999afd5cd9ad86595417f864e19cdb3d5a1fffb`  
		Last Modified: Tue, 15 Nov 2022 13:04:46 GMT  
		Size: 14.1 MB (14089378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f2f570a6edd65c0b3b554251d968470097014d810adfb27b96a98cd2e4a433`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e884a2e58d9fcc54acea7d3e39908d7ecd42e1edfef73bb68191b54f991c6e67`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9a1ff5f61c69e0b99c23045ec864acc99c0977ee4ff08e72fec757c2553f2b`  
		Last Modified: Tue, 15 Nov 2022 13:04:57 GMT  
		Size: 115.8 MB (115785814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db447849bdf4798b71bf9356ea7bb877bccdb13cbfcc41950625bd7f999a6ebb`  
		Last Modified: Tue, 15 Nov 2022 13:04:41 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4186431df56dd92a17a34b42da70b499494a80076ce02b2f62ab6d4b842d04c`  
		Last Modified: Tue, 15 Nov 2022 13:04:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.40-oracle`

```console
$ docker pull mysql@sha256:4149a92977a54d27cbd6f81cca3817e6278a844d566b45f9ff1908bb2714b1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.40-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d984f298e32e8f81e2a821a6e771214c924b9f31db6d0c9dcf4b16f87f4cbebf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144288550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d44289af6858f5d6b118c8d1547679d70b752ec179740785d7452081de8cb31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:21:24 GMT
ADD file:ec2c8d4fc7614a3584827f15c6278d01c6d7f42892747f20aeccfa2feb526412 in / 
# Tue, 29 Nov 2022 19:21:25 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:40:29 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:40:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:40:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:40:52 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 29 Nov 2022 19:40:53 GMT
ENV MYSQL_VERSION=5.7.40-1.el7
# Tue, 29 Nov 2022 19:40:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:41:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:41:12 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:41:12 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el7
# Tue, 29 Nov 2022 19:41:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:41:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:41:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:41:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:41:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:41:39 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:41:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d96bccd7291ff1dc9e55f40b596e14900d110382763aa46814bc43ac1b40f57c`  
		Last Modified: Tue, 29 Nov 2022 19:23:17 GMT  
		Size: 49.8 MB (49828163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feae47af51d5f4035f28ed6483d53446e27ca9a23d69287f9a4fa64daf185041`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64d38b9fa31e439ed2eebb9c14f5880600bb44f5dda47872008e02a89af7275`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da689aaabebf7976a587488d0de04efdef955e838850c8777ac85acd70b97837`  
		Last Modified: Tue, 29 Nov 2022 19:42:52 GMT  
		Size: 4.5 MB (4538915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a532732deb806e40acfcdb0d32d19a3bfabd6b3ace779002a098e6f94ffde`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 2.7 KB (2654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9063a4855045ea193d5757ab3b873e8329edc94ded524c8c5747b896176cadf6`  
		Last Modified: Tue, 29 Nov 2022 19:42:51 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a84b6adf6c71ed27390306faffb1d36960a0708f0dadc706fd590c7c4dbce`  
		Last Modified: Tue, 29 Nov 2022 19:42:53 GMT  
		Size: 25.5 MB (25531824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7084e7269f301d2e1ffdf0baf60a5d36447aee8205c39f432417135c2c0976b5`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161795475ff3e916bbd9969c72a9e325f1643b09ce403bfee1468ea51fffd9b8`  
		Last Modified: Tue, 29 Nov 2022 19:43:01 GMT  
		Size: 63.4 MB (63449731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2f7a84c8fc14f3e17e08a228839803e09ab9ca40170cba3292bc2d8f7a3df7`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 5.4 KB (5391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf120096e55e03864f868a4131aecb131259c201755b888816f4654791fed01f`  
		Last Modified: Tue, 29 Nov 2022 19:42:49 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:a5f0cdc27aaaf52e125ef95feb8f16c8e01b6dfdc19bd4eee22d208877f7fec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b7723f5c0013576dded81e7da91a0292780c41c87ac0d141c7c11ac0c7b40bf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177566940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7b8f072515bf2a39727cd3cbdd5e43895134aab2dab401fcbaefe720a4a447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:01:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 15 Nov 2022 13:02:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 15 Nov 2022 13:02:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 13:02:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 15 Nov 2022 13:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 15 Nov 2022 13:02:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 15 Nov 2022 13:02:21 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 15 Nov 2022 13:02:21 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 15 Nov 2022 13:02:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 15 Nov 2022 13:02:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Nov 2022 13:02:38 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 15 Nov 2022 13:02:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:02:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 15 Nov 2022 13:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:02:39 GMT
EXPOSE 3306 33060
# Tue, 15 Nov 2022 13:02:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c5f46b86bcde1607df33835202723f7b164fd874d81a292fdc328c68e714a3`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c41730774e57a40d58b667771334846a553c84ce0cb8a5cd1525ab637ab56f`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 4.4 MB (4415531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b738276122ae857e7479755a5e0d5b75e21a1b92541afd6bd3c723ca17cb2`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.4 MB (1419597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e2a4ee2f48e0bdb4367b24613350cb231b44cf2337d62cef351cdcecf9dea4`  
		Last Modified: Tue, 15 Nov 2022 13:04:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98e97140efbd3e579539602d0908ec7f8f90d71d73a0850aa13480e28e64a1a`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 12.7 MB (12662693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25338f20c7cbc43f390e1dd932c88cc77fca7dcd28c224b225f1292b495129`  
		Last Modified: Tue, 15 Nov 2022 13:04:07 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab7c6b6e5a076a7d08e4a4b9d812324a3aa2732efd34a61ad88340b4120f3d`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca68c51cd74b5a9928a31416fee5f7c053909f4dd69a871c032ba3b1c6e0c0`  
		Last Modified: Tue, 15 Nov 2022 13:04:26 GMT  
		Size: 127.6 MB (127645462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97b3e2ff53ba242734da8a86e131f21c5ed0088a2f320944b0a9208093553`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f36551fe8601acb1b3a61be725080a34ebbdce748037cdfce1457bce5190fae`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbb3d0b9f8d905f0092d8dfc76996f24463ad13647feefd50946202fe7c4a31`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:a5f0cdc27aaaf52e125ef95feb8f16c8e01b6dfdc19bd4eee22d208877f7fec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b7723f5c0013576dded81e7da91a0292780c41c87ac0d141c7c11ac0c7b40bf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177566940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7b8f072515bf2a39727cd3cbdd5e43895134aab2dab401fcbaefe720a4a447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:01:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 15 Nov 2022 13:02:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 15 Nov 2022 13:02:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 13:02:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 15 Nov 2022 13:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 15 Nov 2022 13:02:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 15 Nov 2022 13:02:21 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 15 Nov 2022 13:02:21 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 15 Nov 2022 13:02:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 15 Nov 2022 13:02:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Nov 2022 13:02:38 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 15 Nov 2022 13:02:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:02:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 15 Nov 2022 13:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:02:39 GMT
EXPOSE 3306 33060
# Tue, 15 Nov 2022 13:02:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c5f46b86bcde1607df33835202723f7b164fd874d81a292fdc328c68e714a3`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c41730774e57a40d58b667771334846a553c84ce0cb8a5cd1525ab637ab56f`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 4.4 MB (4415531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b738276122ae857e7479755a5e0d5b75e21a1b92541afd6bd3c723ca17cb2`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.4 MB (1419597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e2a4ee2f48e0bdb4367b24613350cb231b44cf2337d62cef351cdcecf9dea4`  
		Last Modified: Tue, 15 Nov 2022 13:04:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98e97140efbd3e579539602d0908ec7f8f90d71d73a0850aa13480e28e64a1a`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 12.7 MB (12662693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25338f20c7cbc43f390e1dd932c88cc77fca7dcd28c224b225f1292b495129`  
		Last Modified: Tue, 15 Nov 2022 13:04:07 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab7c6b6e5a076a7d08e4a4b9d812324a3aa2732efd34a61ad88340b4120f3d`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca68c51cd74b5a9928a31416fee5f7c053909f4dd69a871c032ba3b1c6e0c0`  
		Last Modified: Tue, 15 Nov 2022 13:04:26 GMT  
		Size: 127.6 MB (127645462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97b3e2ff53ba242734da8a86e131f21c5ed0088a2f320944b0a9208093553`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f36551fe8601acb1b3a61be725080a34ebbdce748037cdfce1457bce5190fae`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbb3d0b9f8d905f0092d8dfc76996f24463ad13647feefd50946202fe7c4a31`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.31` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.31` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31-debian`

```console
$ docker pull mysql@sha256:a5f0cdc27aaaf52e125ef95feb8f16c8e01b6dfdc19bd4eee22d208877f7fec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.31-debian` - linux; amd64

```console
$ docker pull mysql@sha256:b7723f5c0013576dded81e7da91a0292780c41c87ac0d141c7c11ac0c7b40bf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177566940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7b8f072515bf2a39727cd3cbdd5e43895134aab2dab401fcbaefe720a4a447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:01:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 15 Nov 2022 13:02:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 15 Nov 2022 13:02:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 13:02:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 15 Nov 2022 13:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 15 Nov 2022 13:02:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 15 Nov 2022 13:02:21 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 15 Nov 2022 13:02:21 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 15 Nov 2022 13:02:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 15 Nov 2022 13:02:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Nov 2022 13:02:38 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 15 Nov 2022 13:02:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:02:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 15 Nov 2022 13:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:02:39 GMT
EXPOSE 3306 33060
# Tue, 15 Nov 2022 13:02:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c5f46b86bcde1607df33835202723f7b164fd874d81a292fdc328c68e714a3`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c41730774e57a40d58b667771334846a553c84ce0cb8a5cd1525ab637ab56f`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 4.4 MB (4415531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b738276122ae857e7479755a5e0d5b75e21a1b92541afd6bd3c723ca17cb2`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.4 MB (1419597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e2a4ee2f48e0bdb4367b24613350cb231b44cf2337d62cef351cdcecf9dea4`  
		Last Modified: Tue, 15 Nov 2022 13:04:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98e97140efbd3e579539602d0908ec7f8f90d71d73a0850aa13480e28e64a1a`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 12.7 MB (12662693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25338f20c7cbc43f390e1dd932c88cc77fca7dcd28c224b225f1292b495129`  
		Last Modified: Tue, 15 Nov 2022 13:04:07 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab7c6b6e5a076a7d08e4a4b9d812324a3aa2732efd34a61ad88340b4120f3d`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca68c51cd74b5a9928a31416fee5f7c053909f4dd69a871c032ba3b1c6e0c0`  
		Last Modified: Tue, 15 Nov 2022 13:04:26 GMT  
		Size: 127.6 MB (127645462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97b3e2ff53ba242734da8a86e131f21c5ed0088a2f320944b0a9208093553`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f36551fe8601acb1b3a61be725080a34ebbdce748037cdfce1457bce5190fae`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbb3d0b9f8d905f0092d8dfc76996f24463ad13647feefd50946202fe7c4a31`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.31-oracle`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.31-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.31-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:a5f0cdc27aaaf52e125ef95feb8f16c8e01b6dfdc19bd4eee22d208877f7fec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:b7723f5c0013576dded81e7da91a0292780c41c87ac0d141c7c11ac0c7b40bf6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177566940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7b8f072515bf2a39727cd3cbdd5e43895134aab2dab401fcbaefe720a4a447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:01:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 15 Nov 2022 13:02:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:02 GMT
ENV GOSU_VERSION=1.14
# Tue, 15 Nov 2022 13:02:12 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 15 Nov 2022 13:02:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 15 Nov 2022 13:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 13:02:20 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 15 Nov 2022 13:02:20 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 15 Nov 2022 13:02:21 GMT
ENV MYSQL_VERSION=8.0.31-1debian11
# Tue, 15 Nov 2022 13:02:21 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 15 Nov 2022 13:02:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 15 Nov 2022 13:02:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 15 Nov 2022 13:02:38 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 15 Nov 2022 13:02:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 15 Nov 2022 13:02:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 15 Nov 2022 13:02:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 15 Nov 2022 13:02:39 GMT
EXPOSE 3306 33060
# Tue, 15 Nov 2022 13:02:39 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c5f46b86bcde1607df33835202723f7b164fd874d81a292fdc328c68e714a3`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c41730774e57a40d58b667771334846a553c84ce0cb8a5cd1525ab637ab56f`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 4.4 MB (4415531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b738276122ae857e7479755a5e0d5b75e21a1b92541afd6bd3c723ca17cb2`  
		Last Modified: Tue, 15 Nov 2022 13:04:09 GMT  
		Size: 1.4 MB (1419597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e2a4ee2f48e0bdb4367b24613350cb231b44cf2337d62cef351cdcecf9dea4`  
		Last Modified: Tue, 15 Nov 2022 13:04:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98e97140efbd3e579539602d0908ec7f8f90d71d73a0850aa13480e28e64a1a`  
		Last Modified: Tue, 15 Nov 2022 13:04:10 GMT  
		Size: 12.7 MB (12662693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a25338f20c7cbc43f390e1dd932c88cc77fca7dcd28c224b225f1292b495129`  
		Last Modified: Tue, 15 Nov 2022 13:04:07 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab7c6b6e5a076a7d08e4a4b9d812324a3aa2732efd34a61ad88340b4120f3d`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cca68c51cd74b5a9928a31416fee5f7c053909f4dd69a871c032ba3b1c6e0c0`  
		Last Modified: Tue, 15 Nov 2022 13:04:26 GMT  
		Size: 127.6 MB (127645462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb97b3e2ff53ba242734da8a86e131f21c5ed0088a2f320944b0a9208093553`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f36551fe8601acb1b3a61be725080a34ebbdce748037cdfce1457bce5190fae`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbb3d0b9f8d905f0092d8dfc76996f24463ad13647feefd50946202fe7c4a31`  
		Last Modified: Tue, 15 Nov 2022 13:04:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:66efaaa129f12b1c5871508bc8481a9b28c5b388d74ac5d2a6fc314359bbef91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d8d877b2f0709bc815e7aa11c102e67c992f9e326666313da3aa5f9fd19365a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.6 MB (160579229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a2968869cf080dbbd2adaac9e4075cc358b50a1451ff5e2b9ae90551a4735f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:20:57 GMT
ADD file:6767deed84cff167f77f7d9f835925cd8a5d3093d0b99f0180245cfd6312ae06 in / 
# Tue, 29 Nov 2022 19:20:58 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 19:38:33 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 19:38:33 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 19:38:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 19:39:00 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 19:39:01 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 19:39:02 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:39:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 19:39:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 19:39:33 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 19:39:33 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 19:40:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 19:40:09 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 19:40:09 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 19:40:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 19:40:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 19:40:10 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 19:40:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:996f1bba14d621751efdd3a7ff3a65db06e0edb9b3e211ef1c3e68223e053af7`  
		Last Modified: Tue, 29 Nov 2022 19:22:40 GMT  
		Size: 43.9 MB (43871608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4355e2c82df587ed934b06f05ef0d4f0dc52ddcb3d6d3f2741baaece07b0dc5`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 885.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d7aedb7ad7b9bdd786de98dc2885754fe7de085d6a9dadc7585704a695f7a3`  
		Last Modified: Tue, 29 Nov 2022 19:42:18 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ee75d8667dff4986f7a490d9d8cd9e49790550f25f67f710ee6f486b5eeddd`  
		Last Modified: Tue, 29 Nov 2022 19:42:17 GMT  
		Size: 4.6 MB (4612132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8c1ec8ff26b9fc798479e15e16b6f19748d21ebfae2b0625e5806462ee187d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8748759282d39a34bf7d532293ef8df5b5042ddaaab0e3d60ff8d976b6d07d`  
		Last Modified: Tue, 29 Nov 2022 19:42:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0859d5816eecdfb950f46dc174471c18ae4884aaa74e848d6ca978a4859cc11`  
		Last Modified: Tue, 29 Nov 2022 19:42:23 GMT  
		Size: 56.1 MB (56063041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e144df551bc3962efdaea4ed3290eeef740e1708c46a5c327d8efd5b59ab6b`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878df6a0cc3eb11e7bdb3fdc4a13ee404dfc6cf9d6b4d8acf385a22b3be195b`  
		Last Modified: Tue, 29 Nov 2022 19:42:24 GMT  
		Size: 55.1 MB (55093935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43b187428e35ea1a2e674f017c92179d64e0c4e3178024b59267c19b21d50b8`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:202e454031c60bd40c645b6ed9879e7839bac3d35cadf4dbf47e9ac0352ea632`  
		Last Modified: Tue, 29 Nov 2022 19:42:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:505a7fd4a2f74f491e463fe9db6fe02db8df7d5b5a94cdff71ff972891ccb8c7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.1 MB (159071407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ff7e619492a26961e1ee98089d97184ba490fa629554c04a87be261acea374`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 29 Nov 2022 19:48:22 GMT
ADD file:8919add412c121e3fffd8882c8379cfef3889b0d6b18afc150e1bd4a4bae08d4 in / 
# Tue, 29 Nov 2022 19:48:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Nov 2022 20:13:53 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Tue, 29 Nov 2022 20:13:53 GMT
ENV GOSU_VERSION=1.14
# Tue, 29 Nov 2022 20:13:57 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 29 Nov 2022 20:14:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 29 Nov 2022 20:14:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 29 Nov 2022 20:14:22 GMT
ENV MYSQL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:14:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 29 Nov 2022 20:14:49 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 29 Nov 2022 20:14:50 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 29 Nov 2022 20:14:50 GMT
ENV MYSQL_SHELL_VERSION=8.0.31-1.el8
# Tue, 29 Nov 2022 20:15:20 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 29 Nov 2022 20:15:22 GMT
VOLUME [/var/lib/mysql]
# Tue, 29 Nov 2022 20:15:22 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 29 Nov 2022 20:15:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 29 Nov 2022 20:15:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 29 Nov 2022 20:15:22 GMT
EXPOSE 3306 33060
# Tue, 29 Nov 2022 20:15:23 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e16f89d504be05b35448ef4e921fc7ea5f090b53960d0bc6764f6d31a0ea2f4a`  
		Last Modified: Tue, 29 Nov 2022 19:49:52 GMT  
		Size: 42.8 MB (42775103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a892d9359c82f2adc3d508f9b46ec72d8d0ff56907bb2d748969b2a03dafafcd`  
		Last Modified: Tue, 29 Nov 2022 20:15:45 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f921010330ec907e75c83dedfec21a3ca3c6e54d9bb37ca466d72f13988e7bb2`  
		Last Modified: Tue, 29 Nov 2022 20:15:46 GMT  
		Size: 857.2 KB (857169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb132090e12e6c0f9b63763d3b4ada5c6bf0602182cb3f9bed6d59d1a841663`  
		Last Modified: Tue, 29 Nov 2022 20:15:44 GMT  
		Size: 4.5 MB (4465988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8359ebe56abaaba82d896b8b032629ef75f47c50bd97feeec609950485071d05`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ab25fb4cac58efc397132f327183872f6192dd3e36681ffcd290f2f453443b`  
		Last Modified: Tue, 29 Nov 2022 20:15:43 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ee456884baa041385eb63407475b209303693972de50c332470c7f61d2bd7`  
		Last Modified: Tue, 29 Nov 2022 20:15:48 GMT  
		Size: 55.5 MB (55454017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2cd79745f00410adf211a82464dd238ba210cc6c412060239b31f062bdb74f`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447264fb841229c8b0c5a7d6ec0e231768f70bc3ebdc6a5dbe5812a98166caa2`  
		Last Modified: Tue, 29 Nov 2022 20:15:49 GMT  
		Size: 55.5 MB (55509454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3250d681934834605510a03ad5d11f9c331bc3c4f2b45717337d25afc74cd960`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 5.4 KB (5387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2d1537ae4039263b126e14e375c3ed333ff9acf8a7d8b4a043d8b2b19dc563`  
		Last Modified: Tue, 29 Nov 2022 20:15:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
