<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.47`](#mysql5647)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.29`](#mysql5729)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.19`](#mysql8019)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:fbaeced79cfdae5d3c8d4a8c41e883f254f72ed7428c6b93a498824b76d97121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:74cb47745213f69833348f814f378a6e446b53e518e650fab44a71c523f1004b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158202741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413be204e9c34f31476a0680b6521873fb519c749693b181228ff47492a7fe3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:54 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 31 Mar 2020 03:14:55 GMT
ENV MYSQL_VERSION=5.7.29-1debian10
# Tue, 31 Mar 2020 03:14:56 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:15:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 31 Mar 2020 03:15:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:15:34 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:15:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:15:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:15:35 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:15:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466a91a95e2ff5092cced561dee995c1797fddc67ea62a896751c1e2594e0e23`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4554c238f181f1d4992fb95e806ad880272e6f53d0528a27698a2e01238260`  
		Last Modified: Tue, 31 Mar 2020 03:18:06 GMT  
		Size: 112.2 MB (112203092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603b48ead88ca0906e9c1c768a61de2ba1cf9025a8ec1b3459d682d838cd7c21`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 5.1 KB (5074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86a9aa7171b781e088f724e902d34405563d6ffe6b59ed66d9a60fefa4c5e5`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:f0165a6f800d183ca92ab822e2fe6157acebc5752bab3ca2b9e805b2fa894bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:7168ed6c33898ee8e73a372272807f12e5d7c9cdf31710cc6197e9cce57d6752
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102733773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21620125f9e88be1db4560d710ec288e56c142d93b7206ed94a3636bceabe48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:15:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:15:52 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:16:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:16:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:16:23 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:16:24 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 31 Mar 2020 03:16:24 GMT
ENV MYSQL_VERSION=5.6.47-1debian9
# Tue, 31 Mar 2020 03:16:25 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:16:49 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 31 Mar 2020 03:16:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:16:49 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:16:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:16:51 GMT
EXPOSE 3306
# Tue, 31 Mar 2020 03:16:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725652de4539c51ffb42050d30b2dd238e0ffdd552aaf6dd8ec34ff6f4a5141e`  
		Last Modified: Tue, 31 Mar 2020 03:18:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83fcf33afd87307befd566c7c31e26c2a17282f55f31b62b380a2dcf960e4`  
		Last Modified: Tue, 31 Mar 2020 03:18:16 GMT  
		Size: 4.5 MB (4501272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22eed95a35d12589c8a4d79e90ac9fb1d56152d5dd8040c1b4b90debab8b67a`  
		Last Modified: Tue, 31 Mar 2020 03:18:14 GMT  
		Size: 1.3 MB (1270498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6413e9e73acaeaf2dfae8d143144ca092ed8103da248c1e8d1e37658bf520f`  
		Last Modified: Tue, 31 Mar 2020 03:18:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db37ee61b2cc19089c7fcc1c9b42accba9f36339e1b013293d3a63dc64152cc1`  
		Last Modified: Tue, 31 Mar 2020 03:18:19 GMT  
		Size: 10.2 MB (10222763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f352f2d0e1bbb6b9857c884006545b35b9aa581a6a4c039da5098d4e820e5ee`  
		Last Modified: Tue, 31 Mar 2020 03:18:13 GMT  
		Size: 28.3 KB (28327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f664886aa54ba3eca6b90e5b0f7c9be75652a3d8556201def39ff04bd940cfe`  
		Last Modified: Tue, 31 Mar 2020 03:18:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4961f446cc7a713b2ee722f0698145a8dcf25d2d338be043e9804cfcc760a2`  
		Last Modified: Tue, 31 Mar 2020 03:18:29 GMT  
		Size: 64.2 MB (64190248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e610963b475faddb69091466872a34a1ca1a19deb2686678dd69935fe0820c9`  
		Last Modified: Tue, 31 Mar 2020 03:18:12 GMT  
		Size: 5.1 KB (5091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b007da11435a0629fe5f1e2237f6a7e86cc4cc8ec0866b7b2e6f1a1c63457b4`  
		Last Modified: Tue, 31 Mar 2020 03:18:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.47`

```console
$ docker pull mysql@sha256:f0165a6f800d183ca92ab822e2fe6157acebc5752bab3ca2b9e805b2fa894bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.47` - linux; amd64

```console
$ docker pull mysql@sha256:7168ed6c33898ee8e73a372272807f12e5d7c9cdf31710cc6197e9cce57d6752
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102733773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21620125f9e88be1db4560d710ec288e56c142d93b7206ed94a3636bceabe48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:24:08 GMT
ADD file:e077f4d014ea0869fc4b3d5a3e6b3c8b792a97a8b4a328f33a994369225ff222 in / 
# Tue, 31 Mar 2020 01:24:08 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:15:42 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:15:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:15:52 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:16:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:16:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:16:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:16:23 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:16:24 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 31 Mar 2020 03:16:24 GMT
ENV MYSQL_VERSION=5.6.47-1debian9
# Tue, 31 Mar 2020 03:16:25 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:16:49 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 31 Mar 2020 03:16:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:16:49 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:16:51 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:16:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:16:51 GMT
EXPOSE 3306
# Tue, 31 Mar 2020 03:16:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:48839397421a64189661c2b86a34eb515d09a28204587a2b06b59df9f6e2d786`  
		Last Modified: Tue, 31 Mar 2020 01:29:28 GMT  
		Size: 22.5 MB (22513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725652de4539c51ffb42050d30b2dd238e0ffdd552aaf6dd8ec34ff6f4a5141e`  
		Last Modified: Tue, 31 Mar 2020 03:18:15 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e83fcf33afd87307befd566c7c31e26c2a17282f55f31b62b380a2dcf960e4`  
		Last Modified: Tue, 31 Mar 2020 03:18:16 GMT  
		Size: 4.5 MB (4501272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22eed95a35d12589c8a4d79e90ac9fb1d56152d5dd8040c1b4b90debab8b67a`  
		Last Modified: Tue, 31 Mar 2020 03:18:14 GMT  
		Size: 1.3 MB (1270498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6413e9e73acaeaf2dfae8d143144ca092ed8103da248c1e8d1e37658bf520f`  
		Last Modified: Tue, 31 Mar 2020 03:18:13 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db37ee61b2cc19089c7fcc1c9b42accba9f36339e1b013293d3a63dc64152cc1`  
		Last Modified: Tue, 31 Mar 2020 03:18:19 GMT  
		Size: 10.2 MB (10222763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f352f2d0e1bbb6b9857c884006545b35b9aa581a6a4c039da5098d4e820e5ee`  
		Last Modified: Tue, 31 Mar 2020 03:18:13 GMT  
		Size: 28.3 KB (28327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f664886aa54ba3eca6b90e5b0f7c9be75652a3d8556201def39ff04bd940cfe`  
		Last Modified: Tue, 31 Mar 2020 03:18:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4961f446cc7a713b2ee722f0698145a8dcf25d2d338be043e9804cfcc760a2`  
		Last Modified: Tue, 31 Mar 2020 03:18:29 GMT  
		Size: 64.2 MB (64190248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e610963b475faddb69091466872a34a1ca1a19deb2686678dd69935fe0820c9`  
		Last Modified: Tue, 31 Mar 2020 03:18:12 GMT  
		Size: 5.1 KB (5091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b007da11435a0629fe5f1e2237f6a7e86cc4cc8ec0866b7b2e6f1a1c63457b4`  
		Last Modified: Tue, 31 Mar 2020 03:18:12 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:fbaeced79cfdae5d3c8d4a8c41e883f254f72ed7428c6b93a498824b76d97121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:74cb47745213f69833348f814f378a6e446b53e518e650fab44a71c523f1004b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158202741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413be204e9c34f31476a0680b6521873fb519c749693b181228ff47492a7fe3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:54 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 31 Mar 2020 03:14:55 GMT
ENV MYSQL_VERSION=5.7.29-1debian10
# Tue, 31 Mar 2020 03:14:56 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:15:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 31 Mar 2020 03:15:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:15:34 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:15:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:15:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:15:35 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:15:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466a91a95e2ff5092cced561dee995c1797fddc67ea62a896751c1e2594e0e23`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4554c238f181f1d4992fb95e806ad880272e6f53d0528a27698a2e01238260`  
		Last Modified: Tue, 31 Mar 2020 03:18:06 GMT  
		Size: 112.2 MB (112203092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603b48ead88ca0906e9c1c768a61de2ba1cf9025a8ec1b3459d682d838cd7c21`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 5.1 KB (5074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86a9aa7171b781e088f724e902d34405563d6ffe6b59ed66d9a60fefa4c5e5`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.29`

```console
$ docker pull mysql@sha256:fbaeced79cfdae5d3c8d4a8c41e883f254f72ed7428c6b93a498824b76d97121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.29` - linux; amd64

```console
$ docker pull mysql@sha256:74cb47745213f69833348f814f378a6e446b53e518e650fab44a71c523f1004b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158202741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413be204e9c34f31476a0680b6521873fb519c749693b181228ff47492a7fe3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:54 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 31 Mar 2020 03:14:55 GMT
ENV MYSQL_VERSION=5.7.29-1debian10
# Tue, 31 Mar 2020 03:14:56 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:15:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Tue, 31 Mar 2020 03:15:33 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:15:34 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:15:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:15:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:15:35 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:15:36 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466a91a95e2ff5092cced561dee995c1797fddc67ea62a896751c1e2594e0e23`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e4554c238f181f1d4992fb95e806ad880272e6f53d0528a27698a2e01238260`  
		Last Modified: Tue, 31 Mar 2020 03:18:06 GMT  
		Size: 112.2 MB (112203092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603b48ead88ca0906e9c1c768a61de2ba1cf9025a8ec1b3459d682d838cd7c21`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 5.1 KB (5074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e86a9aa7171b781e088f724e902d34405563d6ffe6b59ed66d9a60fefa4c5e5`  
		Last Modified: Tue, 31 Mar 2020 03:17:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:b69d0b62d02ee1eba8c7aeb32eba1bb678b6cfa4ccfb211a5d7931c7755dc4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:fc84f426da06035a0de61789b4241db47db006efdc356286b5e28f4ce4bd38e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9228ee8bac7a8143818a7b028ee3386ea93e30a8f2e8bbf1440ca1ea3c26aa3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 31 Mar 2020 03:14:17 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Tue, 31 Mar 2020 03:14:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:14:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 31 Mar 2020 03:14:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:14:44 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 31 Mar 2020 03:14:44 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:14:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:14:46 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:14:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a808704d40c62b06667399c114521ef6a0a8422a8e54e277180edc80bce7bd9`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826517d075193cb62879b8fce405519b74092c2812a8a57d18e8e6b1661f71c2`  
		Last Modified: Tue, 31 Mar 2020 03:17:35 GMT  
		Size: 113.0 MB (112955573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cd125db92884cb773d9e0d2038450821203c17b598e1585332a8dd3789d484`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c43b8c287976f0e6a323e1ca4ad6d1e85c9962d4a3ed7286668692d7849f9a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 5.1 KB (5075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1811572b5ea5938f38eb7e8ec80b49861f7dc46f36945233ba100168b3cd3c6a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:b69d0b62d02ee1eba8c7aeb32eba1bb678b6cfa4ccfb211a5d7931c7755dc4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:fc84f426da06035a0de61789b4241db47db006efdc356286b5e28f4ce4bd38e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9228ee8bac7a8143818a7b028ee3386ea93e30a8f2e8bbf1440ca1ea3c26aa3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 31 Mar 2020 03:14:17 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Tue, 31 Mar 2020 03:14:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:14:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 31 Mar 2020 03:14:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:14:44 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 31 Mar 2020 03:14:44 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:14:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:14:46 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:14:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a808704d40c62b06667399c114521ef6a0a8422a8e54e277180edc80bce7bd9`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826517d075193cb62879b8fce405519b74092c2812a8a57d18e8e6b1661f71c2`  
		Last Modified: Tue, 31 Mar 2020 03:17:35 GMT  
		Size: 113.0 MB (112955573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cd125db92884cb773d9e0d2038450821203c17b598e1585332a8dd3789d484`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c43b8c287976f0e6a323e1ca4ad6d1e85c9962d4a3ed7286668692d7849f9a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 5.1 KB (5075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1811572b5ea5938f38eb7e8ec80b49861f7dc46f36945233ba100168b3cd3c6a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.19`

```console
$ docker pull mysql@sha256:b69d0b62d02ee1eba8c7aeb32eba1bb678b6cfa4ccfb211a5d7931c7755dc4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.19` - linux; amd64

```console
$ docker pull mysql@sha256:fc84f426da06035a0de61789b4241db47db006efdc356286b5e28f4ce4bd38e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9228ee8bac7a8143818a7b028ee3386ea93e30a8f2e8bbf1440ca1ea3c26aa3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 31 Mar 2020 03:14:17 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Tue, 31 Mar 2020 03:14:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:14:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 31 Mar 2020 03:14:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:14:44 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 31 Mar 2020 03:14:44 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:14:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:14:46 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:14:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a808704d40c62b06667399c114521ef6a0a8422a8e54e277180edc80bce7bd9`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826517d075193cb62879b8fce405519b74092c2812a8a57d18e8e6b1661f71c2`  
		Last Modified: Tue, 31 Mar 2020 03:17:35 GMT  
		Size: 113.0 MB (112955573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cd125db92884cb773d9e0d2038450821203c17b598e1585332a8dd3789d484`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c43b8c287976f0e6a323e1ca4ad6d1e85c9962d4a3ed7286668692d7849f9a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 5.1 KB (5075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1811572b5ea5938f38eb7e8ec80b49861f7dc46f36945233ba100168b3cd3c6a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:b69d0b62d02ee1eba8c7aeb32eba1bb678b6cfa4ccfb211a5d7931c7755dc4a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:fc84f426da06035a0de61789b4241db47db006efdc356286b5e28f4ce4bd38e3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158956124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9228ee8bac7a8143818a7b028ee3386ea93e30a8f2e8bbf1440ca1ea3c26aa3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 03:13:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 31 Mar 2020 03:13:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:13:49 GMT
ENV GOSU_VERSION=1.7
# Tue, 31 Mar 2020 03:14:01 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Tue, 31 Mar 2020 03:14:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 31 Mar 2020 03:14:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 03:14:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 31 Mar 2020 03:14:16 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 31 Mar 2020 03:14:17 GMT
ENV MYSQL_VERSION=8.0.19-1debian10
# Tue, 31 Mar 2020 03:14:18 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Tue, 31 Mar 2020 03:14:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Tue, 31 Mar 2020 03:14:43 GMT
VOLUME [/var/lib/mysql]
# Tue, 31 Mar 2020 03:14:44 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Tue, 31 Mar 2020 03:14:44 GMT
COPY file:4f14a879f00507ec1e489ab2afde4d14871f6edb4a42f72520400388739d7ede in /usr/local/bin/ 
# Tue, 31 Mar 2020 03:14:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 31 Mar 2020 03:14:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 31 Mar 2020 03:14:46 GMT
EXPOSE 3306 33060
# Tue, 31 Mar 2020 03:14:46 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c4cdf4ea75904fad0c7630f749d92ec07bbea623258e92ff327bb3c020229e`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff5091a5a30cfb7be3c4641478d0a28649b7dfb417c752240b5052c9957bd4a`  
		Last Modified: Tue, 31 Mar 2020 03:17:09 GMT  
		Size: 4.2 MB (4178024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fd3d1af940310e7c7f7ca577b44e7fc6c1c636c5e7b4ba60fc137e7484cf426`  
		Last Modified: Tue, 31 Mar 2020 03:17:07 GMT  
		Size: 1.3 MB (1277281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9d26127d1d11a91be76378b08864ed2f80f1612853c57d84d34fefd87970ea`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54a67d4e757984116352e9aaed190144d72652b0aeb51d9b82eb3fdaf80911ed`  
		Last Modified: Tue, 31 Mar 2020 03:17:13 GMT  
		Size: 13.4 MB (13442819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe989230d866ac2dd38d2859062a7dfda5f4f92adc49e5afed66f41402a16cd4`  
		Last Modified: Tue, 31 Mar 2020 03:17:06 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a808704d40c62b06667399c114521ef6a0a8422a8e54e277180edc80bce7bd9`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:826517d075193cb62879b8fce405519b74092c2812a8a57d18e8e6b1661f71c2`  
		Last Modified: Tue, 31 Mar 2020 03:17:35 GMT  
		Size: 113.0 MB (112955573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69cd125db92884cb773d9e0d2038450821203c17b598e1585332a8dd3789d484`  
		Last Modified: Tue, 31 Mar 2020 03:17:05 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c43b8c287976f0e6a323e1ca4ad6d1e85c9962d4a3ed7286668692d7849f9a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 5.1 KB (5075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1811572b5ea5938f38eb7e8ec80b49861f7dc46f36945233ba100168b3cd3c6a`  
		Last Modified: Tue, 31 Mar 2020 03:17:04 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
