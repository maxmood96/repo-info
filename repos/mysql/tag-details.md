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
$ docker pull mysql@sha256:b38555e593300df225daea22aeb104eed79fc80d2f064fde1e16e1804d00d0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:47960a0280616cfab409e46d2891cbd3c98cb6c30ecf4d0821bcb1a18d441d8e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150505380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db39680b63ac47a1d989da7b742f7b382af34d85a68214f8977bad59c05901a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 23:00:07 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 Dec 2019 23:00:08 GMT
ENV MYSQL_VERSION=5.7.28-1debian9
# Sat, 28 Dec 2019 23:00:08 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 28 Dec 2019 23:00:34 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 28 Dec 2019 23:00:34 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 Dec 2019 23:00:34 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 28 Dec 2019 23:00:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 23:00:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 23:00:35 GMT
EXPOSE 3306 33060
# Sat, 28 Dec 2019 23:00:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f1f8385b2776768be664aa98c55dd91afb4721a3c8bcb8874248ef9f5e8491`  
		Last Modified: Sat, 28 Dec 2019 23:01:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a3ad97e819d0edd717909855fa9cfb8772fcf1e116e2c03654ff5bd1da6094`  
		Last Modified: Sat, 28 Dec 2019 23:02:08 GMT  
		Size: 110.1 MB (110066935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bede7828aca4ea144fa23eb0c22b28d04d8a6d6ce2bf4212381c8dd9c904fc`  
		Last Modified: Sat, 28 Dec 2019 23:01:49 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380afa2e69732c4078a9fdc5aa5f8aa7a44cdde9c2158b2af03f62cdfc01646d`  
		Last Modified: Sat, 28 Dec 2019 23:01:49 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:82a505551c0243ca04df445f1287b2c4da3b23463b1a9c0bc2b2476760179950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:cb0ea262eb3261fc5c5b2fa8b08b95c642e1ec112736def5f41eb9b85f914c5f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102683838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ba8643e01a1b582ffcf90cd5eab5ba97af396703ce9b6e2e292f6bbacd1d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 23:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 23:00:49 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 23:00:50 GMT
ENV MYSQL_MAJOR=5.6
# Sat, 28 Dec 2019 23:00:50 GMT
ENV MYSQL_VERSION=5.6.46-1debian9
# Sat, 28 Dec 2019 23:00:50 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 28 Dec 2019 23:01:09 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 28 Dec 2019 23:01:09 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 Dec 2019 23:01:09 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 28 Dec 2019 23:01:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 23:01:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 23:01:11 GMT
EXPOSE 3306
# Sat, 28 Dec 2019 23:01:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc42a3806103d5f78d16740051c07ff7467a77eb0a4771098e608720beb79ca`  
		Last Modified: Sat, 28 Dec 2019 23:02:16 GMT  
		Size: 10.2 MB (10168833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea6d62a85766c2d419fd2b785492507ec1a951d0bb648e8da89ea0d3a91b669`  
		Last Modified: Sat, 28 Dec 2019 23:02:13 GMT  
		Size: 28.3 KB (28326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59b0c57b7622a8f1aacd00f4f50a775bfe8fbae1d4eb9ec45d2cd789ed54323`  
		Last Modified: Sat, 28 Dec 2019 23:02:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa66d796007bfdf9f4b119a53fac3f558728480012a8c97c6e1f239ef10b5267`  
		Last Modified: Sat, 28 Dec 2019 23:02:25 GMT  
		Size: 64.2 MB (64183086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac072c882e77626b92db55c72acf9f43150f3f3dbe281c83555575f800fa1d5`  
		Last Modified: Sat, 28 Dec 2019 23:02:13 GMT  
		Size: 5.0 KB (5030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5014f1a5adeb9549e5f265e71c9547835ad102561ae0e0e3da59a7879f4f5`  
		Last Modified: Sat, 28 Dec 2019 23:02:13 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.47`

**does not exist** (yet?)

## `mysql:5.7`

```console
$ docker pull mysql@sha256:b38555e593300df225daea22aeb104eed79fc80d2f064fde1e16e1804d00d0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:47960a0280616cfab409e46d2891cbd3c98cb6c30ecf4d0821bcb1a18d441d8e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150505380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db39680b63ac47a1d989da7b742f7b382af34d85a68214f8977bad59c05901a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 23:00:07 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 28 Dec 2019 23:00:08 GMT
ENV MYSQL_VERSION=5.7.28-1debian9
# Sat, 28 Dec 2019 23:00:08 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 28 Dec 2019 23:00:34 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Sat, 28 Dec 2019 23:00:34 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 Dec 2019 23:00:34 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 28 Dec 2019 23:00:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 23:00:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 23:00:35 GMT
EXPOSE 3306 33060
# Sat, 28 Dec 2019 23:00:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f1f8385b2776768be664aa98c55dd91afb4721a3c8bcb8874248ef9f5e8491`  
		Last Modified: Sat, 28 Dec 2019 23:01:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a3ad97e819d0edd717909855fa9cfb8772fcf1e116e2c03654ff5bd1da6094`  
		Last Modified: Sat, 28 Dec 2019 23:02:08 GMT  
		Size: 110.1 MB (110066935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bede7828aca4ea144fa23eb0c22b28d04d8a6d6ce2bf4212381c8dd9c904fc`  
		Last Modified: Sat, 28 Dec 2019 23:01:49 GMT  
		Size: 5.0 KB (5027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380afa2e69732c4078a9fdc5aa5f8aa7a44cdde9c2158b2af03f62cdfc01646d`  
		Last Modified: Sat, 28 Dec 2019 23:01:49 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.29`

**does not exist** (yet?)

## `mysql:8`

```console
$ docker pull mysql@sha256:e1b0fd480a11e5c37425a2591b6fbd32af886bfc6d6f404bd362be5e50a2e632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:119ecffb345e201c406e12e203b550aece0dc34671fe19069f00f1825f8d6b98
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134026357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1ffcb5eff39aed723a66ee895854a6417485f85629de7ba87610beb6bf39ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_VERSION=8.0.18-1debian9
# Sat, 28 Dec 2019 22:59:26 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 28 Dec 2019 22:59:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Sat, 28 Dec 2019 22:59:51 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 Dec 2019 22:59:52 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Sat, 28 Dec 2019 22:59:52 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 28 Dec 2019 22:59:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 22:59:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 22:59:53 GMT
EXPOSE 3306 33060
# Sat, 28 Dec 2019 22:59:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e26af62412025df7a69a6ad99b70b75767026efc97385f7ae56b7d39151ebe4`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e70feb9365d70ff6a71900cad555f024541bfaf06bec2f32bfc3156e05c3ff7`  
		Last Modified: Sat, 28 Dec 2019 23:01:43 GMT  
		Size: 93.6 MB (93587012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5595dde544eef9b9975c0052b26fdf1afe303d01dab1a8c0d5e1f98696ae3f4`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87399808d2ba3df84652ccdc6fe39d1ef78f340345cc9c33362b068a1a662bb6`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312ab6d79b5bc02d9a869574a9207160c0ee685b42210acf6036b1450b67407`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:e1b0fd480a11e5c37425a2591b6fbd32af886bfc6d6f404bd362be5e50a2e632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:119ecffb345e201c406e12e203b550aece0dc34671fe19069f00f1825f8d6b98
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134026357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1ffcb5eff39aed723a66ee895854a6417485f85629de7ba87610beb6bf39ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_VERSION=8.0.18-1debian9
# Sat, 28 Dec 2019 22:59:26 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 28 Dec 2019 22:59:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Sat, 28 Dec 2019 22:59:51 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 Dec 2019 22:59:52 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Sat, 28 Dec 2019 22:59:52 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 28 Dec 2019 22:59:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 22:59:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 22:59:53 GMT
EXPOSE 3306 33060
# Sat, 28 Dec 2019 22:59:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e26af62412025df7a69a6ad99b70b75767026efc97385f7ae56b7d39151ebe4`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e70feb9365d70ff6a71900cad555f024541bfaf06bec2f32bfc3156e05c3ff7`  
		Last Modified: Sat, 28 Dec 2019 23:01:43 GMT  
		Size: 93.6 MB (93587012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5595dde544eef9b9975c0052b26fdf1afe303d01dab1a8c0d5e1f98696ae3f4`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87399808d2ba3df84652ccdc6fe39d1ef78f340345cc9c33362b068a1a662bb6`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312ab6d79b5bc02d9a869574a9207160c0ee685b42210acf6036b1450b67407`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.19`

**does not exist** (yet?)

## `mysql:latest`

```console
$ docker pull mysql@sha256:e1b0fd480a11e5c37425a2591b6fbd32af886bfc6d6f404bd362be5e50a2e632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:119ecffb345e201c406e12e203b550aece0dc34671fe19069f00f1825f8d6b98
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134026357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1ffcb5eff39aed723a66ee895854a6417485f85629de7ba87610beb6bf39ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 22:58:40 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 Dec 2019 22:58:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:58:51 GMT
ENV GOSU_VERSION=1.7
# Sat, 28 Dec 2019 22:59:08 GMT
RUN set -x 	&& apt-get update && apt-get install -y --no-install-recommends ca-certificates wget && rm -rf /var/lib/apt/lists/* 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& gpgconf --kill all 	&& rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true 	&& apt-get purge -y --auto-remove ca-certificates wget
# Sat, 28 Dec 2019 22:59:09 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 Dec 2019 22:59:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 22:59:24 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 Dec 2019 22:59:24 GMT
ENV MYSQL_VERSION=8.0.18-1debian9
# Sat, 28 Dec 2019 22:59:26 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Sat, 28 Dec 2019 22:59:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Sat, 28 Dec 2019 22:59:51 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 Dec 2019 22:59:52 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Sat, 28 Dec 2019 22:59:52 GMT
COPY file:b3081195cff78c4726a17cfcbc840d37d0c488bb7d020b6e52445d328ce4024a in /usr/local/bin/ 
# Sat, 28 Dec 2019 22:59:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 Dec 2019 22:59:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 Dec 2019 22:59:53 GMT
EXPOSE 3306 33060
# Sat, 28 Dec 2019 22:59:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53bab4587346e91b0ffe5be44d22584aec078d10072cb07d853f0699a0a658c`  
		Last Modified: Sat, 28 Dec 2019 23:01:25 GMT  
		Size: 1.7 KB (1749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9d72777f90237cc95f691b56ca3bdca20d0366bb2bb082d35e46733df5ae5d`  
		Last Modified: Sat, 28 Dec 2019 23:01:26 GMT  
		Size: 4.5 MB (4501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d7aad6cb96e5facc0f715ade30711c5097c2b95183574e0b23456efe2ff5b76`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 1.3 MB (1270462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6ca35c790828ec92faaad14a1207ad9f745429970ad2a6bf2b0a0ac84626fa`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddae009e7602a2efe8585eaaecdccf3194c5b6e79897d88bdc26bf3a630d9aa`  
		Last Modified: Sat, 28 Dec 2019 23:01:27 GMT  
		Size: 12.1 MB (12106532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327ae67bbe7b37612516d2aea453ae283ea50b8b00e480218c01b5c47e3ecdb4`  
		Last Modified: Sat, 28 Dec 2019 23:01:24 GMT  
		Size: 28.3 KB (28325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e26af62412025df7a69a6ad99b70b75767026efc97385f7ae56b7d39151ebe4`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e70feb9365d70ff6a71900cad555f024541bfaf06bec2f32bfc3156e05c3ff7`  
		Last Modified: Sat, 28 Dec 2019 23:01:43 GMT  
		Size: 93.6 MB (93587012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5595dde544eef9b9975c0052b26fdf1afe303d01dab1a8c0d5e1f98696ae3f4`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87399808d2ba3df84652ccdc6fe39d1ef78f340345cc9c33362b068a1a662bb6`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 5.0 KB (5026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7312ab6d79b5bc02d9a869574a9207160c0ee685b42210acf6036b1450b67407`  
		Last Modified: Sat, 28 Dec 2019 23:01:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
