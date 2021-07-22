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
$ docker pull mysql@sha256:be70d18aedc37927293e7947c8de41ae6490ecd4c79df1db40d1b5b5af7d9596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:4556aec03ad3bec8242ae18d907c798e331d73189b82ddc76ad98758308fb58f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154790015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6250709314f2fcd2669e8643f5d3bdebfe715bddb63990c8c96e5d261d6fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:45:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:45:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:46:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:46:33 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Jul 2021 09:46:33 GMT
ENV MYSQL_VERSION=5.7.35-1debian10
# Thu, 22 Jul 2021 09:46:34 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:46:54 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:46:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:46:56 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:46:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:46:58 GMT
EXPOSE 3306 33060
# Thu, 22 Jul 2021 09:46:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67864e624cb9385283d9c15d7d63cb2df3695df62f54616ceba589fb37ae0`  
		Last Modified: Thu, 22 Jul 2021 09:48:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2b594783f5615223f4e91e8b6cfd89ac66aa5d678fb9296a6390cd64264f1c`  
		Last Modified: Thu, 22 Jul 2021 09:48:51 GMT  
		Size: 4.2 MB (4179259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30e406dd9250eb8283fcf316c29450eae75eddbc22a3b05c1c67cca904bb879`  
		Last Modified: Thu, 22 Jul 2021 09:48:48 GMT  
		Size: 1.4 MB (1419410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48901e306e4c36bbb20c354393adb4e37707cc4313e4618c2dc2a5532b01d17d`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d2b7147fdf54be4906fa8d2046e88d148de73e65b86f54b910f03a0481e78`  
		Last Modified: Thu, 22 Jul 2021 09:48:52 GMT  
		Size: 13.4 MB (13447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa684c1c4a9a004fb5cde0c6f0611f8da574510da43e1aac509a7990922cf`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5a19178915ca4e47eb12e87bde5a9a7463230f451e0c1832aac77df98d3c5b`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ce7411c6e428b3423d68302746da82cb37ffd4c0ff802e7de1fc14b033fe47`  
		Last Modified: Thu, 22 Jul 2021 09:49:46 GMT  
		Size: 108.6 MB (108588381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51f6977d9b262d30b658f3dd3cf87992b0fa00ecf025957960456a7a4bd2638`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb6b16ce012a8ba7c9d24ede0850cb8387afb3307055c486817415a2d8954f8`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:391f655177931dc2905b6fbf6b21d769060f8797ce1b515e8579a157afcce459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:8b4cab0ede1aee1309382ebcf9b37dd811be3e23f0244a27aeb3ef2851e27317
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102970592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e825dc3cfb07643cea8c76442be89ab2145663357a06de541a3e88665aa44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:17 GMT
ADD file:55a25b93e8f2940a796f3cbf1e78bddf5f49c46b1b89b63b9b5673cbed9483ca in / 
# Thu, 22 Jul 2021 00:47:17 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:47:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:47:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:47:15 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:47:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:47:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:47:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:47:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:47:47 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 22 Jul 2021 09:47:48 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Thu, 22 Jul 2021 09:47:49 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:48:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:48:11 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:48:12 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:48:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:48:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:48:13 GMT
EXPOSE 3306
# Thu, 22 Jul 2021 09:48:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:778066204fb734c2fb80cb8127cb35d67d742806a4eaf1aba0b5393c4ae6f2a4`  
		Last Modified: Thu, 22 Jul 2021 00:53:22 GMT  
		Size: 22.5 MB (22527428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4934b98a40c4faccd30f887edd00f6ba96bc5b37801fa497dd5f8d3ef09d0a49`  
		Last Modified: Thu, 22 Jul 2021 09:50:11 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d0034f4cf8a2f6a298988f92dce993f7cc6ac195d645b2f1d84ef69d6b6468`  
		Last Modified: Thu, 22 Jul 2021 09:50:07 GMT  
		Size: 4.5 MB (4503333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5c81076c53779c5ab41a7644522e71f105f025b340802285a56d67eb8e9184`  
		Last Modified: Thu, 22 Jul 2021 09:50:05 GMT  
		Size: 1.4 MB (1412291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e630bfc512080075b8d1123c000315bd533c992b3bbc34267586c74498b4057`  
		Last Modified: Thu, 22 Jul 2021 09:50:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc97236980ffdfe287657b1f2a1fa6010e5c64df38a4320e13e41e200de3d2c4`  
		Last Modified: Thu, 22 Jul 2021 09:50:09 GMT  
		Size: 10.2 MB (10225943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935fd852726a4b2944d94681eedf73079e6e1cf6adf16144ec6ee937a41286f`  
		Last Modified: Thu, 22 Jul 2021 09:50:02 GMT  
		Size: 19.5 KB (19459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25ac4a39a81910258a831815115daf980e9ed8e072c979f6d0513f2675aaec5`  
		Last Modified: Thu, 22 Jul 2021 09:50:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b50ae6b19347a7e19aedcec610b5941b41b5bcf17a5a6bd93728e33be4c4cd`  
		Last Modified: Thu, 22 Jul 2021 09:50:16 GMT  
		Size: 64.3 MB (64274342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0af3588a72c091a7292d99108a2fd2f379845b97cf4f2b4cfe49457d6fd45d`  
		Last Modified: Thu, 22 Jul 2021 09:50:03 GMT  
		Size: 5.6 KB (5558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2c92fcf3d9f3534afef88255426822711d27fa2e346eb184aad825987881a6`  
		Last Modified: Thu, 22 Jul 2021 09:50:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:391f655177931dc2905b6fbf6b21d769060f8797ce1b515e8579a157afcce459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:8b4cab0ede1aee1309382ebcf9b37dd811be3e23f0244a27aeb3ef2851e27317
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102970592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e825dc3cfb07643cea8c76442be89ab2145663357a06de541a3e88665aa44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:17 GMT
ADD file:55a25b93e8f2940a796f3cbf1e78bddf5f49c46b1b89b63b9b5673cbed9483ca in / 
# Thu, 22 Jul 2021 00:47:17 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:47:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:47:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:47:15 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:47:33 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:47:34 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:47:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:47:47 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:47:47 GMT
ENV MYSQL_MAJOR=5.6
# Thu, 22 Jul 2021 09:47:48 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Thu, 22 Jul 2021 09:47:49 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:48:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:48:11 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:48:12 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:48:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:48:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:48:13 GMT
EXPOSE 3306
# Thu, 22 Jul 2021 09:48:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:778066204fb734c2fb80cb8127cb35d67d742806a4eaf1aba0b5393c4ae6f2a4`  
		Last Modified: Thu, 22 Jul 2021 00:53:22 GMT  
		Size: 22.5 MB (22527428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4934b98a40c4faccd30f887edd00f6ba96bc5b37801fa497dd5f8d3ef09d0a49`  
		Last Modified: Thu, 22 Jul 2021 09:50:11 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d0034f4cf8a2f6a298988f92dce993f7cc6ac195d645b2f1d84ef69d6b6468`  
		Last Modified: Thu, 22 Jul 2021 09:50:07 GMT  
		Size: 4.5 MB (4503333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5c81076c53779c5ab41a7644522e71f105f025b340802285a56d67eb8e9184`  
		Last Modified: Thu, 22 Jul 2021 09:50:05 GMT  
		Size: 1.4 MB (1412291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e630bfc512080075b8d1123c000315bd533c992b3bbc34267586c74498b4057`  
		Last Modified: Thu, 22 Jul 2021 09:50:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc97236980ffdfe287657b1f2a1fa6010e5c64df38a4320e13e41e200de3d2c4`  
		Last Modified: Thu, 22 Jul 2021 09:50:09 GMT  
		Size: 10.2 MB (10225943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935fd852726a4b2944d94681eedf73079e6e1cf6adf16144ec6ee937a41286f`  
		Last Modified: Thu, 22 Jul 2021 09:50:02 GMT  
		Size: 19.5 KB (19459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25ac4a39a81910258a831815115daf980e9ed8e072c979f6d0513f2675aaec5`  
		Last Modified: Thu, 22 Jul 2021 09:50:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b50ae6b19347a7e19aedcec610b5941b41b5bcf17a5a6bd93728e33be4c4cd`  
		Last Modified: Thu, 22 Jul 2021 09:50:16 GMT  
		Size: 64.3 MB (64274342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0af3588a72c091a7292d99108a2fd2f379845b97cf4f2b4cfe49457d6fd45d`  
		Last Modified: Thu, 22 Jul 2021 09:50:03 GMT  
		Size: 5.6 KB (5558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2c92fcf3d9f3534afef88255426822711d27fa2e346eb184aad825987881a6`  
		Last Modified: Thu, 22 Jul 2021 09:50:02 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:be70d18aedc37927293e7947c8de41ae6490ecd4c79df1db40d1b5b5af7d9596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:4556aec03ad3bec8242ae18d907c798e331d73189b82ddc76ad98758308fb58f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154790015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6250709314f2fcd2669e8643f5d3bdebfe715bddb63990c8c96e5d261d6fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:45:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:45:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:46:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:46:33 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Jul 2021 09:46:33 GMT
ENV MYSQL_VERSION=5.7.35-1debian10
# Thu, 22 Jul 2021 09:46:34 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:46:54 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:46:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:46:56 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:46:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:46:58 GMT
EXPOSE 3306 33060
# Thu, 22 Jul 2021 09:46:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67864e624cb9385283d9c15d7d63cb2df3695df62f54616ceba589fb37ae0`  
		Last Modified: Thu, 22 Jul 2021 09:48:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2b594783f5615223f4e91e8b6cfd89ac66aa5d678fb9296a6390cd64264f1c`  
		Last Modified: Thu, 22 Jul 2021 09:48:51 GMT  
		Size: 4.2 MB (4179259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30e406dd9250eb8283fcf316c29450eae75eddbc22a3b05c1c67cca904bb879`  
		Last Modified: Thu, 22 Jul 2021 09:48:48 GMT  
		Size: 1.4 MB (1419410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48901e306e4c36bbb20c354393adb4e37707cc4313e4618c2dc2a5532b01d17d`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d2b7147fdf54be4906fa8d2046e88d148de73e65b86f54b910f03a0481e78`  
		Last Modified: Thu, 22 Jul 2021 09:48:52 GMT  
		Size: 13.4 MB (13447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa684c1c4a9a004fb5cde0c6f0611f8da574510da43e1aac509a7990922cf`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5a19178915ca4e47eb12e87bde5a9a7463230f451e0c1832aac77df98d3c5b`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ce7411c6e428b3423d68302746da82cb37ffd4c0ff802e7de1fc14b033fe47`  
		Last Modified: Thu, 22 Jul 2021 09:49:46 GMT  
		Size: 108.6 MB (108588381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51f6977d9b262d30b658f3dd3cf87992b0fa00ecf025957960456a7a4bd2638`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb6b16ce012a8ba7c9d24ede0850cb8387afb3307055c486817415a2d8954f8`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.35`

```console
$ docker pull mysql@sha256:be70d18aedc37927293e7947c8de41ae6490ecd4c79df1db40d1b5b5af7d9596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.35` - linux; amd64

```console
$ docker pull mysql@sha256:4556aec03ad3bec8242ae18d907c798e331d73189b82ddc76ad98758308fb58f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154790015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf6250709314f2fcd2669e8643f5d3bdebfe715bddb63990c8c96e5d261d6fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:45:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:45:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:46:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:46:33 GMT
ENV MYSQL_MAJOR=5.7
# Thu, 22 Jul 2021 09:46:33 GMT
ENV MYSQL_VERSION=5.7.35-1debian10
# Thu, 22 Jul 2021 09:46:34 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:46:54 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:46:55 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:46:56 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:46:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:46:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:46:58 GMT
EXPOSE 3306 33060
# Thu, 22 Jul 2021 09:46:58 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67864e624cb9385283d9c15d7d63cb2df3695df62f54616ceba589fb37ae0`  
		Last Modified: Thu, 22 Jul 2021 09:48:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2b594783f5615223f4e91e8b6cfd89ac66aa5d678fb9296a6390cd64264f1c`  
		Last Modified: Thu, 22 Jul 2021 09:48:51 GMT  
		Size: 4.2 MB (4179259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30e406dd9250eb8283fcf316c29450eae75eddbc22a3b05c1c67cca904bb879`  
		Last Modified: Thu, 22 Jul 2021 09:48:48 GMT  
		Size: 1.4 MB (1419410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48901e306e4c36bbb20c354393adb4e37707cc4313e4618c2dc2a5532b01d17d`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d2b7147fdf54be4906fa8d2046e88d148de73e65b86f54b910f03a0481e78`  
		Last Modified: Thu, 22 Jul 2021 09:48:52 GMT  
		Size: 13.4 MB (13447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa684c1c4a9a004fb5cde0c6f0611f8da574510da43e1aac509a7990922cf`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5a19178915ca4e47eb12e87bde5a9a7463230f451e0c1832aac77df98d3c5b`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ce7411c6e428b3423d68302746da82cb37ffd4c0ff802e7de1fc14b033fe47`  
		Last Modified: Thu, 22 Jul 2021 09:49:46 GMT  
		Size: 108.6 MB (108588381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51f6977d9b262d30b658f3dd3cf87992b0fa00ecf025957960456a7a4bd2638`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb6b16ce012a8ba7c9d24ede0850cb8387afb3307055c486817415a2d8954f8`  
		Last Modified: Thu, 22 Jul 2021 09:49:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:8b928a5117cf5c2238c7a09cd28c2e801ac98f91c3f8203a8938ae51f14700fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:516b92a7ccf2340c1a696a7ad2de1784393d0876d042cc4913bc33fb3f455a75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150592914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d96bd2b771a8e3cae776e02e55ae914a6641139d963defeb3c93388f61707`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:45:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:45:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:46:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Thu, 22 Jul 2021 09:46:10 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:46:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:46:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:46:27 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 22 Jul 2021 09:46:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:46:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:46:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:46:29 GMT
EXPOSE 3306 33060
# Thu, 22 Jul 2021 09:46:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67864e624cb9385283d9c15d7d63cb2df3695df62f54616ceba589fb37ae0`  
		Last Modified: Thu, 22 Jul 2021 09:48:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2b594783f5615223f4e91e8b6cfd89ac66aa5d678fb9296a6390cd64264f1c`  
		Last Modified: Thu, 22 Jul 2021 09:48:51 GMT  
		Size: 4.2 MB (4179259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30e406dd9250eb8283fcf316c29450eae75eddbc22a3b05c1c67cca904bb879`  
		Last Modified: Thu, 22 Jul 2021 09:48:48 GMT  
		Size: 1.4 MB (1419410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48901e306e4c36bbb20c354393adb4e37707cc4313e4618c2dc2a5532b01d17d`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d2b7147fdf54be4906fa8d2046e88d148de73e65b86f54b910f03a0481e78`  
		Last Modified: Thu, 22 Jul 2021 09:48:52 GMT  
		Size: 13.4 MB (13447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa684c1c4a9a004fb5cde0c6f0611f8da574510da43e1aac509a7990922cf`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d3c143a062c12a411d2917d5119eda4aeccf9bdcd316567a25528de9ba6a5`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6978e1b7a5113b48511c0757d860e7c35a15ae349191e6e9620cff6cfb446e3a`  
		Last Modified: Thu, 22 Jul 2021 09:49:07 GMT  
		Size: 104.4 MB (104390438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d78b0ac1be7141ac803e34695bebc7a7e8a291caf36e92907e3a87de2bac10`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a94d251ed180a36bd9b75feb9b5bc15a215cce80c6c10502897bda639c0274`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f75719b1a9b020a38ba3ffc0ad8b26ab97e8d2d51a4c62e34d7db787f9e689`  
		Last Modified: Thu, 22 Jul 2021 09:48:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:8b928a5117cf5c2238c7a09cd28c2e801ac98f91c3f8203a8938ae51f14700fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:516b92a7ccf2340c1a696a7ad2de1784393d0876d042cc4913bc33fb3f455a75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150592914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d96bd2b771a8e3cae776e02e55ae914a6641139d963defeb3c93388f61707`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:45:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:45:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:46:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Thu, 22 Jul 2021 09:46:10 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:46:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:46:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:46:27 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 22 Jul 2021 09:46:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:46:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:46:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:46:29 GMT
EXPOSE 3306 33060
# Thu, 22 Jul 2021 09:46:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67864e624cb9385283d9c15d7d63cb2df3695df62f54616ceba589fb37ae0`  
		Last Modified: Thu, 22 Jul 2021 09:48:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2b594783f5615223f4e91e8b6cfd89ac66aa5d678fb9296a6390cd64264f1c`  
		Last Modified: Thu, 22 Jul 2021 09:48:51 GMT  
		Size: 4.2 MB (4179259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30e406dd9250eb8283fcf316c29450eae75eddbc22a3b05c1c67cca904bb879`  
		Last Modified: Thu, 22 Jul 2021 09:48:48 GMT  
		Size: 1.4 MB (1419410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48901e306e4c36bbb20c354393adb4e37707cc4313e4618c2dc2a5532b01d17d`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d2b7147fdf54be4906fa8d2046e88d148de73e65b86f54b910f03a0481e78`  
		Last Modified: Thu, 22 Jul 2021 09:48:52 GMT  
		Size: 13.4 MB (13447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa684c1c4a9a004fb5cde0c6f0611f8da574510da43e1aac509a7990922cf`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d3c143a062c12a411d2917d5119eda4aeccf9bdcd316567a25528de9ba6a5`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6978e1b7a5113b48511c0757d860e7c35a15ae349191e6e9620cff6cfb446e3a`  
		Last Modified: Thu, 22 Jul 2021 09:49:07 GMT  
		Size: 104.4 MB (104390438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d78b0ac1be7141ac803e34695bebc7a7e8a291caf36e92907e3a87de2bac10`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a94d251ed180a36bd9b75feb9b5bc15a215cce80c6c10502897bda639c0274`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f75719b1a9b020a38ba3ffc0ad8b26ab97e8d2d51a4c62e34d7db787f9e689`  
		Last Modified: Thu, 22 Jul 2021 09:48:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.26`

```console
$ docker pull mysql@sha256:8b928a5117cf5c2238c7a09cd28c2e801ac98f91c3f8203a8938ae51f14700fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.26` - linux; amd64

```console
$ docker pull mysql@sha256:516b92a7ccf2340c1a696a7ad2de1784393d0876d042cc4913bc33fb3f455a75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150592914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d96bd2b771a8e3cae776e02e55ae914a6641139d963defeb3c93388f61707`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:45:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:45:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:46:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Thu, 22 Jul 2021 09:46:10 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:46:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:46:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:46:27 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 22 Jul 2021 09:46:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:46:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:46:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:46:29 GMT
EXPOSE 3306 33060
# Thu, 22 Jul 2021 09:46:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67864e624cb9385283d9c15d7d63cb2df3695df62f54616ceba589fb37ae0`  
		Last Modified: Thu, 22 Jul 2021 09:48:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2b594783f5615223f4e91e8b6cfd89ac66aa5d678fb9296a6390cd64264f1c`  
		Last Modified: Thu, 22 Jul 2021 09:48:51 GMT  
		Size: 4.2 MB (4179259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30e406dd9250eb8283fcf316c29450eae75eddbc22a3b05c1c67cca904bb879`  
		Last Modified: Thu, 22 Jul 2021 09:48:48 GMT  
		Size: 1.4 MB (1419410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48901e306e4c36bbb20c354393adb4e37707cc4313e4618c2dc2a5532b01d17d`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d2b7147fdf54be4906fa8d2046e88d148de73e65b86f54b910f03a0481e78`  
		Last Modified: Thu, 22 Jul 2021 09:48:52 GMT  
		Size: 13.4 MB (13447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa684c1c4a9a004fb5cde0c6f0611f8da574510da43e1aac509a7990922cf`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d3c143a062c12a411d2917d5119eda4aeccf9bdcd316567a25528de9ba6a5`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6978e1b7a5113b48511c0757d860e7c35a15ae349191e6e9620cff6cfb446e3a`  
		Last Modified: Thu, 22 Jul 2021 09:49:07 GMT  
		Size: 104.4 MB (104390438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d78b0ac1be7141ac803e34695bebc7a7e8a291caf36e92907e3a87de2bac10`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a94d251ed180a36bd9b75feb9b5bc15a215cce80c6c10502897bda639c0274`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f75719b1a9b020a38ba3ffc0ad8b26ab97e8d2d51a4c62e34d7db787f9e689`  
		Last Modified: Thu, 22 Jul 2021 09:48:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:8b928a5117cf5c2238c7a09cd28c2e801ac98f91c3f8203a8938ae51f14700fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:516b92a7ccf2340c1a696a7ad2de1784393d0876d042cc4913bc33fb3f455a75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150592914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c60d96bd2b771a8e3cae776e02e55ae914a6641139d963defeb3c93388f61707`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:43 GMT
ADD file:45f5dfa135c848a348382413cb8b66a3b1dac3276814fbbe4684b39101d1b148 in / 
# Thu, 22 Jul 2021 00:45:44 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:45:43 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 22 Jul 2021 09:45:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:45:49 GMT
ENV GOSU_VERSION=1.12
# Thu, 22 Jul 2021 09:45:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 22 Jul 2021 09:45:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Jul 2021 09:46:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 09:46:09 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 22 Jul 2021 09:46:09 GMT
ENV MYSQL_VERSION=8.0.26-1debian10
# Thu, 22 Jul 2021 09:46:10 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Thu, 22 Jul 2021 09:46:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Thu, 22 Jul 2021 09:46:27 GMT
VOLUME [/var/lib/mysql]
# Thu, 22 Jul 2021 09:46:27 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Thu, 22 Jul 2021 09:46:28 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Thu, 22 Jul 2021 09:46:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 22 Jul 2021 09:46:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Jul 2021 09:46:29 GMT
EXPOSE 3306 33060
# Thu, 22 Jul 2021 09:46:29 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:33847f680f63fb1b343a9fc782e267b5abdbdb50d65d4b9bd2a136291d67cf75`  
		Last Modified: Thu, 22 Jul 2021 00:50:35 GMT  
		Size: 27.1 MB (27145795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb67864e624cb9385283d9c15d7d63cb2df3695df62f54616ceba589fb37ae0`  
		Last Modified: Thu, 22 Jul 2021 09:48:50 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2b594783f5615223f4e91e8b6cfd89ac66aa5d678fb9296a6390cd64264f1c`  
		Last Modified: Thu, 22 Jul 2021 09:48:51 GMT  
		Size: 4.2 MB (4179259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30e406dd9250eb8283fcf316c29450eae75eddbc22a3b05c1c67cca904bb879`  
		Last Modified: Thu, 22 Jul 2021 09:48:48 GMT  
		Size: 1.4 MB (1419410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48901e306e4c36bbb20c354393adb4e37707cc4313e4618c2dc2a5532b01d17d`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603d2b7147fdf54be4906fa8d2046e88d148de73e65b86f54b910f03a0481e78`  
		Last Modified: Thu, 22 Jul 2021 09:48:52 GMT  
		Size: 13.4 MB (13447526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802aa684c1c4a9a004fb5cde0c6f0611f8da574510da43e1aac509a7990922cf`  
		Last Modified: Thu, 22 Jul 2021 09:48:47 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d3c143a062c12a411d2917d5119eda4aeccf9bdcd316567a25528de9ba6a5`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6978e1b7a5113b48511c0757d860e7c35a15ae349191e6e9620cff6cfb446e3a`  
		Last Modified: Thu, 22 Jul 2021 09:49:07 GMT  
		Size: 104.4 MB (104390438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d78b0ac1be7141ac803e34695bebc7a7e8a291caf36e92907e3a87de2bac10`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a94d251ed180a36bd9b75feb9b5bc15a215cce80c6c10502897bda639c0274`  
		Last Modified: Thu, 22 Jul 2021 09:48:44 GMT  
		Size: 5.5 KB (5540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f75719b1a9b020a38ba3ffc0ad8b26ab97e8d2d51a4c62e34d7db787f9e689`  
		Last Modified: Thu, 22 Jul 2021 09:48:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
