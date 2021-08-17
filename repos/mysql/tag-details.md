<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.51`](#mysql5651)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.35`](#mysql5735)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.26`](#mysql8026)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:7cf2e7d7ff876f93c8601406a5aa17484e6623875e64e7acc71432ad8e0a3d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:eb9ea64bb30594a785563139df3d58f658bd31df3cc3a86a65da8637db4b8a7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154790665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20ffa54f8674203e91e3225e489aa505fa04b8d482954a8b6d7414842c6de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:29:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:29:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:30:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:30:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:30:36 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:31:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Aug 2021 11:31:14 GMT
ENV MYSQL_VERSION=5.7.35-1debian10
# Tue, 17 Aug 2021 11:31:15 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:31:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:31:45 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:31:46 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:31:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:31:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:31:48 GMT
EXPOSE 3306 33060
# Tue, 17 Aug 2021 11:31:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed879327370a64c0bce7b3105f32557f95bbab187b23f88eef1f7eabedd73aa`  
		Last Modified: Tue, 17 Aug 2021 11:33:45 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285f80bafd8314f1454a95519f147a8a23a1513d87f1b58a10b9eaec220005`  
		Last Modified: Tue, 17 Aug 2021 11:33:47 GMT  
		Size: 4.2 MB (4179305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc17412a00a6b2ffb9d46adc91d61efac70ff52fb6833b144df9783d4e8279d`  
		Last Modified: Tue, 17 Aug 2021 11:33:44 GMT  
		Size: 1.4 MB (1419411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f556ecc09d1be245be2316ca09f4de24383e180185ff83e2acd3d96186d7dbf`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5528e468d8f57ba7b35a246fb6c5170467046ddb4ac3f47d6cab6334c7b48`  
		Last Modified: Tue, 17 Aug 2021 11:33:48 GMT  
		Size: 13.4 MB (13447612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afc286d5d531578457cd0090779d173dcde261905a4298e64826ad09563e255`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2d9261e3ad42ceec6995fd174b5ef0b6841e6e9d07502e0eb16a0cb1cb588b`  
		Last Modified: Tue, 17 Aug 2021 11:34:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac609d7b31f8697f08de806f61ac61546f03e3caef828b4dde5d525d9e003964`  
		Last Modified: Tue, 17 Aug 2021 11:34:44 GMT  
		Size: 108.6 MB (108588714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ee1339bc3a582e01dc785ac148e07cf8c7ef9c56fa6781de7fde9f3f53ed88`  
		Last Modified: Tue, 17 Aug 2021 11:34:23 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c0a831a707324809be9fef7f9492cfd1b03112e9b7235633043f4b5ced6891`  
		Last Modified: Tue, 17 Aug 2021 11:34:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:82ed63d45a770a8a980cbbd40735761d6594617a776f17e1a2dede45f815ae50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:c4b789385aba46b5bc5ace07412a8d7152fa304a5325541bde00955f5cc3e7c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102970712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8929383df06aefc4af008a734e72065bfb1699956ff4a1f764c67013fbe171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:31:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:32:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:32:08 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:32:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:32:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:32:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:32:50 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:32:51 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 17 Aug 2021 11:32:51 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Tue, 17 Aug 2021 11:32:52 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:33:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:33:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:33:16 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:33:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:33:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:33:19 GMT
EXPOSE 3306
# Tue, 17 Aug 2021 11:33:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a385fdbf971f430719af65e17821be17f76ca3b54c26b908a87a249ffa4d5e5b`  
		Last Modified: Tue, 17 Aug 2021 11:35:03 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5e63309de4755675df9d578ffcbd88ee6f286c3cc6a291603cc2619419facb`  
		Last Modified: Tue, 17 Aug 2021 11:35:02 GMT  
		Size: 4.5 MB (4503281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11909d531764571bde789a0896e0da85d2abbd886294e6266be2c2370b99b0d`  
		Last Modified: Tue, 17 Aug 2021 11:35:01 GMT  
		Size: 1.4 MB (1412311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09abb6a6cea095063b0f90209e9aeb09e7b61836220c882b9c993b01938a6bbb`  
		Last Modified: Tue, 17 Aug 2021 11:35:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf965e5da7aba765797b91a5e96a44a3eb940f24a7bb6d79d2b33c62d26d93`  
		Last Modified: Tue, 17 Aug 2021 11:35:05 GMT  
		Size: 10.2 MB (10225714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e17e8aa5de4d4dc3dbf5f310396166eaf496842c1dc15b513a09a533a8ce06`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 19.5 KB (19457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18b831d04a6fee31bbbac44789ec47be8a825171ce53d57e65b3af20c31b821`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524aab626ae1866e566b5b1fc82983c16b1f42ec726217bc787c28c857831e21`  
		Last Modified: Tue, 17 Aug 2021 11:35:13 GMT  
		Size: 64.3 MB (64274408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc922d41f67990e7b4b10629b2eec1dc8864f628e41624046e1ca237f39b81a7`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce28bdd434bff9b2336b008ca4cf329870239d064f01c925a0fecc5fd0ee2a2`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:82ed63d45a770a8a980cbbd40735761d6594617a776f17e1a2dede45f815ae50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:c4b789385aba46b5bc5ace07412a8d7152fa304a5325541bde00955f5cc3e7c5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102970712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8929383df06aefc4af008a734e72065bfb1699956ff4a1f764c67013fbe171`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:26:09 GMT
ADD file:f6c4487fa1f7a4e17f5d88fd0c91031a6efc7fa210d363a1d43d8b0f3a8d1d03 in / 
# Tue, 17 Aug 2021 01:26:09 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:31:58 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:32:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:32:08 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:32:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:32:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:32:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:32:50 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:32:51 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 17 Aug 2021 11:32:51 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Tue, 17 Aug 2021 11:32:52 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:33:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:33:16 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:33:16 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:33:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:33:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:33:19 GMT
EXPOSE 3306
# Tue, 17 Aug 2021 11:33:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33f99cea3b7da8c6e0143c9fd7590c6d56f7d310ddd59b11be4ad485ae4cab2a`  
		Last Modified: Tue, 17 Aug 2021 01:33:27 GMT  
		Size: 22.5 MB (22527748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a385fdbf971f430719af65e17821be17f76ca3b54c26b908a87a249ffa4d5e5b`  
		Last Modified: Tue, 17 Aug 2021 11:35:03 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5e63309de4755675df9d578ffcbd88ee6f286c3cc6a291603cc2619419facb`  
		Last Modified: Tue, 17 Aug 2021 11:35:02 GMT  
		Size: 4.5 MB (4503281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11909d531764571bde789a0896e0da85d2abbd886294e6266be2c2370b99b0d`  
		Last Modified: Tue, 17 Aug 2021 11:35:01 GMT  
		Size: 1.4 MB (1412311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09abb6a6cea095063b0f90209e9aeb09e7b61836220c882b9c993b01938a6bbb`  
		Last Modified: Tue, 17 Aug 2021 11:35:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bf965e5da7aba765797b91a5e96a44a3eb940f24a7bb6d79d2b33c62d26d93`  
		Last Modified: Tue, 17 Aug 2021 11:35:05 GMT  
		Size: 10.2 MB (10225714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e17e8aa5de4d4dc3dbf5f310396166eaf496842c1dc15b513a09a533a8ce06`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 19.5 KB (19457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18b831d04a6fee31bbbac44789ec47be8a825171ce53d57e65b3af20c31b821`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:524aab626ae1866e566b5b1fc82983c16b1f42ec726217bc787c28c857831e21`  
		Last Modified: Tue, 17 Aug 2021 11:35:13 GMT  
		Size: 64.3 MB (64274408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc922d41f67990e7b4b10629b2eec1dc8864f628e41624046e1ca237f39b81a7`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 5.6 KB (5554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce28bdd434bff9b2336b008ca4cf329870239d064f01c925a0fecc5fd0ee2a2`  
		Last Modified: Tue, 17 Aug 2021 11:34:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:7cf2e7d7ff876f93c8601406a5aa17484e6623875e64e7acc71432ad8e0a3d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:eb9ea64bb30594a785563139df3d58f658bd31df3cc3a86a65da8637db4b8a7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154790665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20ffa54f8674203e91e3225e489aa505fa04b8d482954a8b6d7414842c6de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:29:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:29:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:30:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:30:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:30:36 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:31:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Aug 2021 11:31:14 GMT
ENV MYSQL_VERSION=5.7.35-1debian10
# Tue, 17 Aug 2021 11:31:15 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:31:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:31:45 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:31:46 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:31:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:31:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:31:48 GMT
EXPOSE 3306 33060
# Tue, 17 Aug 2021 11:31:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed879327370a64c0bce7b3105f32557f95bbab187b23f88eef1f7eabedd73aa`  
		Last Modified: Tue, 17 Aug 2021 11:33:45 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285f80bafd8314f1454a95519f147a8a23a1513d87f1b58a10b9eaec220005`  
		Last Modified: Tue, 17 Aug 2021 11:33:47 GMT  
		Size: 4.2 MB (4179305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc17412a00a6b2ffb9d46adc91d61efac70ff52fb6833b144df9783d4e8279d`  
		Last Modified: Tue, 17 Aug 2021 11:33:44 GMT  
		Size: 1.4 MB (1419411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f556ecc09d1be245be2316ca09f4de24383e180185ff83e2acd3d96186d7dbf`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5528e468d8f57ba7b35a246fb6c5170467046ddb4ac3f47d6cab6334c7b48`  
		Last Modified: Tue, 17 Aug 2021 11:33:48 GMT  
		Size: 13.4 MB (13447612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afc286d5d531578457cd0090779d173dcde261905a4298e64826ad09563e255`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2d9261e3ad42ceec6995fd174b5ef0b6841e6e9d07502e0eb16a0cb1cb588b`  
		Last Modified: Tue, 17 Aug 2021 11:34:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac609d7b31f8697f08de806f61ac61546f03e3caef828b4dde5d525d9e003964`  
		Last Modified: Tue, 17 Aug 2021 11:34:44 GMT  
		Size: 108.6 MB (108588714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ee1339bc3a582e01dc785ac148e07cf8c7ef9c56fa6781de7fde9f3f53ed88`  
		Last Modified: Tue, 17 Aug 2021 11:34:23 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c0a831a707324809be9fef7f9492cfd1b03112e9b7235633043f4b5ced6891`  
		Last Modified: Tue, 17 Aug 2021 11:34:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.35`

```console
$ docker pull mysql@sha256:7cf2e7d7ff876f93c8601406a5aa17484e6623875e64e7acc71432ad8e0a3d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.35` - linux; amd64

```console
$ docker pull mysql@sha256:eb9ea64bb30594a785563139df3d58f658bd31df3cc3a86a65da8637db4b8a7a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154790665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c20ffa54f8674203e91e3225e489aa505fa04b8d482954a8b6d7414842c6de4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:29:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:29:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:30:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:30:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:30:36 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:31:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Aug 2021 11:31:14 GMT
ENV MYSQL_VERSION=5.7.35-1debian10
# Tue, 17 Aug 2021 11:31:15 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:31:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:31:45 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:31:46 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:31:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:31:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:31:48 GMT
EXPOSE 3306 33060
# Tue, 17 Aug 2021 11:31:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed879327370a64c0bce7b3105f32557f95bbab187b23f88eef1f7eabedd73aa`  
		Last Modified: Tue, 17 Aug 2021 11:33:45 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285f80bafd8314f1454a95519f147a8a23a1513d87f1b58a10b9eaec220005`  
		Last Modified: Tue, 17 Aug 2021 11:33:47 GMT  
		Size: 4.2 MB (4179305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc17412a00a6b2ffb9d46adc91d61efac70ff52fb6833b144df9783d4e8279d`  
		Last Modified: Tue, 17 Aug 2021 11:33:44 GMT  
		Size: 1.4 MB (1419411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f556ecc09d1be245be2316ca09f4de24383e180185ff83e2acd3d96186d7dbf`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5528e468d8f57ba7b35a246fb6c5170467046ddb4ac3f47d6cab6334c7b48`  
		Last Modified: Tue, 17 Aug 2021 11:33:48 GMT  
		Size: 13.4 MB (13447612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afc286d5d531578457cd0090779d173dcde261905a4298e64826ad09563e255`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2d9261e3ad42ceec6995fd174b5ef0b6841e6e9d07502e0eb16a0cb1cb588b`  
		Last Modified: Tue, 17 Aug 2021 11:34:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac609d7b31f8697f08de806f61ac61546f03e3caef828b4dde5d525d9e003964`  
		Last Modified: Tue, 17 Aug 2021 11:34:44 GMT  
		Size: 108.6 MB (108588714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ee1339bc3a582e01dc785ac148e07cf8c7ef9c56fa6781de7fde9f3f53ed88`  
		Last Modified: Tue, 17 Aug 2021 11:34:23 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c0a831a707324809be9fef7f9492cfd1b03112e9b7235633043f4b5ced6891`  
		Last Modified: Tue, 17 Aug 2021 11:34:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:d45561a65aba6edac77be36e0a53f0c1fba67b951cb728348522b671ad63f926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:c744f48715807b821411cc52862676fdd18a2458b4a179cae56854d320c85538
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150593288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4e492065c722ec8cc7413552bafc6fd5434c5ad90797e898ccc4e347e21aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:29:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:29:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:30:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:30:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:30:36 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:30:36 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Aug 2021 11:30:37 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Tue, 17 Aug 2021 11:30:38 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:31:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Aug 2021 11:31:04 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:31:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:31:06 GMT
EXPOSE 3306 33060
# Tue, 17 Aug 2021 11:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed879327370a64c0bce7b3105f32557f95bbab187b23f88eef1f7eabedd73aa`  
		Last Modified: Tue, 17 Aug 2021 11:33:45 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285f80bafd8314f1454a95519f147a8a23a1513d87f1b58a10b9eaec220005`  
		Last Modified: Tue, 17 Aug 2021 11:33:47 GMT  
		Size: 4.2 MB (4179305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc17412a00a6b2ffb9d46adc91d61efac70ff52fb6833b144df9783d4e8279d`  
		Last Modified: Tue, 17 Aug 2021 11:33:44 GMT  
		Size: 1.4 MB (1419411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f556ecc09d1be245be2316ca09f4de24383e180185ff83e2acd3d96186d7dbf`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5528e468d8f57ba7b35a246fb6c5170467046ddb4ac3f47d6cab6334c7b48`  
		Last Modified: Tue, 17 Aug 2021 11:33:48 GMT  
		Size: 13.4 MB (13447612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afc286d5d531578457cd0090779d173dcde261905a4298e64826ad09563e255`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c724a59adff64de723ca4ee2528de62c2b399f0a8894dcecc9e9332e5c33ff1`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2345f8b0a3fc69b36f1f2b2870629cf840553bfab5b23ba27703a59d4bac7a`  
		Last Modified: Tue, 17 Aug 2021 11:34:05 GMT  
		Size: 104.4 MB (104390497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8461a25b23b9c6c8aeae4d7f48d6ff97020bb81bbfbe8bb081ae23ab510a0e0`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adb49279bed24155b18b49b9f8fdaac948e5f3020a5e70209607b8b2e723599`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f22cd6c363b28c51bf66c5d11695951a05cf7a88eb9d6a9ca6b243ceb24218`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:d45561a65aba6edac77be36e0a53f0c1fba67b951cb728348522b671ad63f926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:c744f48715807b821411cc52862676fdd18a2458b4a179cae56854d320c85538
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150593288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4e492065c722ec8cc7413552bafc6fd5434c5ad90797e898ccc4e347e21aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:29:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:29:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:30:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:30:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:30:36 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:30:36 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Aug 2021 11:30:37 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Tue, 17 Aug 2021 11:30:38 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:31:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Aug 2021 11:31:04 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:31:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:31:06 GMT
EXPOSE 3306 33060
# Tue, 17 Aug 2021 11:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed879327370a64c0bce7b3105f32557f95bbab187b23f88eef1f7eabedd73aa`  
		Last Modified: Tue, 17 Aug 2021 11:33:45 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285f80bafd8314f1454a95519f147a8a23a1513d87f1b58a10b9eaec220005`  
		Last Modified: Tue, 17 Aug 2021 11:33:47 GMT  
		Size: 4.2 MB (4179305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc17412a00a6b2ffb9d46adc91d61efac70ff52fb6833b144df9783d4e8279d`  
		Last Modified: Tue, 17 Aug 2021 11:33:44 GMT  
		Size: 1.4 MB (1419411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f556ecc09d1be245be2316ca09f4de24383e180185ff83e2acd3d96186d7dbf`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5528e468d8f57ba7b35a246fb6c5170467046ddb4ac3f47d6cab6334c7b48`  
		Last Modified: Tue, 17 Aug 2021 11:33:48 GMT  
		Size: 13.4 MB (13447612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afc286d5d531578457cd0090779d173dcde261905a4298e64826ad09563e255`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c724a59adff64de723ca4ee2528de62c2b399f0a8894dcecc9e9332e5c33ff1`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2345f8b0a3fc69b36f1f2b2870629cf840553bfab5b23ba27703a59d4bac7a`  
		Last Modified: Tue, 17 Aug 2021 11:34:05 GMT  
		Size: 104.4 MB (104390497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8461a25b23b9c6c8aeae4d7f48d6ff97020bb81bbfbe8bb081ae23ab510a0e0`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adb49279bed24155b18b49b9f8fdaac948e5f3020a5e70209607b8b2e723599`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f22cd6c363b28c51bf66c5d11695951a05cf7a88eb9d6a9ca6b243ceb24218`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.26`

```console
$ docker pull mysql@sha256:d45561a65aba6edac77be36e0a53f0c1fba67b951cb728348522b671ad63f926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.26` - linux; amd64

```console
$ docker pull mysql@sha256:c744f48715807b821411cc52862676fdd18a2458b4a179cae56854d320c85538
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150593288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4e492065c722ec8cc7413552bafc6fd5434c5ad90797e898ccc4e347e21aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:29:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:29:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:30:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:30:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:30:36 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:30:36 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Aug 2021 11:30:37 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Tue, 17 Aug 2021 11:30:38 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:31:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Aug 2021 11:31:04 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:31:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:31:06 GMT
EXPOSE 3306 33060
# Tue, 17 Aug 2021 11:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed879327370a64c0bce7b3105f32557f95bbab187b23f88eef1f7eabedd73aa`  
		Last Modified: Tue, 17 Aug 2021 11:33:45 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285f80bafd8314f1454a95519f147a8a23a1513d87f1b58a10b9eaec220005`  
		Last Modified: Tue, 17 Aug 2021 11:33:47 GMT  
		Size: 4.2 MB (4179305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc17412a00a6b2ffb9d46adc91d61efac70ff52fb6833b144df9783d4e8279d`  
		Last Modified: Tue, 17 Aug 2021 11:33:44 GMT  
		Size: 1.4 MB (1419411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f556ecc09d1be245be2316ca09f4de24383e180185ff83e2acd3d96186d7dbf`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5528e468d8f57ba7b35a246fb6c5170467046ddb4ac3f47d6cab6334c7b48`  
		Last Modified: Tue, 17 Aug 2021 11:33:48 GMT  
		Size: 13.4 MB (13447612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afc286d5d531578457cd0090779d173dcde261905a4298e64826ad09563e255`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c724a59adff64de723ca4ee2528de62c2b399f0a8894dcecc9e9332e5c33ff1`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2345f8b0a3fc69b36f1f2b2870629cf840553bfab5b23ba27703a59d4bac7a`  
		Last Modified: Tue, 17 Aug 2021 11:34:05 GMT  
		Size: 104.4 MB (104390497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8461a25b23b9c6c8aeae4d7f48d6ff97020bb81bbfbe8bb081ae23ab510a0e0`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adb49279bed24155b18b49b9f8fdaac948e5f3020a5e70209607b8b2e723599`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f22cd6c363b28c51bf66c5d11695951a05cf7a88eb9d6a9ca6b243ceb24218`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:d45561a65aba6edac77be36e0a53f0c1fba67b951cb728348522b671ad63f926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:c744f48715807b821411cc52862676fdd18a2458b4a179cae56854d320c85538
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150593288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4e492065c722ec8cc7413552bafc6fd5434c5ad90797e898ccc4e347e21aa5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 11:29:49 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 17 Aug 2021 11:29:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:29:59 GMT
ENV GOSU_VERSION=1.12
# Tue, 17 Aug 2021 11:30:19 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 17 Aug 2021 11:30:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 17 Aug 2021 11:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 11:30:36 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 17 Aug 2021 11:30:36 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Aug 2021 11:30:37 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Tue, 17 Aug 2021 11:30:38 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Aug 2021 11:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Aug 2021 11:31:03 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Aug 2021 11:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Aug 2021 11:31:04 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 17 Aug 2021 11:31:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Aug 2021 11:31:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Aug 2021 11:31:06 GMT
EXPOSE 3306 33060
# Tue, 17 Aug 2021 11:31:06 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bed879327370a64c0bce7b3105f32557f95bbab187b23f88eef1f7eabedd73aa`  
		Last Modified: Tue, 17 Aug 2021 11:33:45 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03285f80bafd8314f1454a95519f147a8a23a1513d87f1b58a10b9eaec220005`  
		Last Modified: Tue, 17 Aug 2021 11:33:47 GMT  
		Size: 4.2 MB (4179305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc17412a00a6b2ffb9d46adc91d61efac70ff52fb6833b144df9783d4e8279d`  
		Last Modified: Tue, 17 Aug 2021 11:33:44 GMT  
		Size: 1.4 MB (1419411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f556ecc09d1be245be2316ca09f4de24383e180185ff83e2acd3d96186d7dbf`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc5528e468d8f57ba7b35a246fb6c5170467046ddb4ac3f47d6cab6334c7b48`  
		Last Modified: Tue, 17 Aug 2021 11:33:48 GMT  
		Size: 13.4 MB (13447612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afc286d5d531578457cd0090779d173dcde261905a4298e64826ad09563e255`  
		Last Modified: Tue, 17 Aug 2021 11:33:43 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c724a59adff64de723ca4ee2528de62c2b399f0a8894dcecc9e9332e5c33ff1`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2345f8b0a3fc69b36f1f2b2870629cf840553bfab5b23ba27703a59d4bac7a`  
		Last Modified: Tue, 17 Aug 2021 11:34:05 GMT  
		Size: 104.4 MB (104390497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8461a25b23b9c6c8aeae4d7f48d6ff97020bb81bbfbe8bb081ae23ab510a0e0`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3adb49279bed24155b18b49b9f8fdaac948e5f3020a5e70209607b8b2e723599`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f22cd6c363b28c51bf66c5d11695951a05cf7a88eb9d6a9ca6b243ceb24218`  
		Last Modified: Tue, 17 Aug 2021 11:33:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
