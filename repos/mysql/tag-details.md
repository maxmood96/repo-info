<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.51`](#mysql5651)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.33`](#mysql5733)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.23`](#mysql8023)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:6b33c0c4224e341938a7e97f1d19737ff8d436dc574086dd129a8c7556cb8eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:2f51df7c1ab69dde4697130a5d5242bf2f80db2cb3282056394731019c8a5327
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154597208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3473143edd4d8c7c87d87d202de3529b1ac9b9825aa49c2d0700e004b2a95e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:40:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:22 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:40:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:40:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:41:15 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 27 Mar 2021 06:41:15 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Sat, 27 Mar 2021 06:41:17 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:41:39 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:41:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:41:40 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:41:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:41:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:41:42 GMT
EXPOSE 3306 33060
# Sat, 27 Mar 2021 06:41:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4d5966d009db5e1fdb79dc66571186bc239cd9ac8a04728fe1a261f8845a9`  
		Last Modified: Sat, 27 Mar 2021 06:43:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8e9739c9eee764cf4a141db8282b611ef449cf417833268082b707222cf87`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 4.2 MB (4179177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd773bacd125e8480c1d42ae5b50fbd62432c0b164594261b2f7f247bd3c667`  
		Last Modified: Sat, 27 Mar 2021 06:43:20 GMT  
		Size: 1.4 MB (1419334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbceeecb7f3cedb1851810d37bb4121c6ce4490b9f76aed57c33581d816e9d5`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53011e5d0402c2f5acf7636e9a37c2d6610ee1eb4e7f36dbf21b7e11edfaa1`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 13.4 MB (13447645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae8cea62cbb34627c348f33d0b0af9fc2b56b96d098fed207530c5faa7f897`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5c6fd32f0563c03543ead9f4d51b621a7f9f4d9438f64b31337442399622ad`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34240da42b5c1d8f7a9f170ca3c23efb55235ab9151b2bec9b1c8b7d6aabb39`  
		Last Modified: Sat, 27 Mar 2021 06:44:20 GMT  
		Size: 108.4 MB (108439914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e62ee1f8e19bb5b7225fefa0d53a520e56bd3b44ac1b546c45da302e5f3d7c`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b1117e790ccd950f2f10912b08926999ef671f4dbfad85825fa507837b2da`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:dc5d576f0e1eddd606f033abfa52a4092e254fd0075d90a9509d0a1f2318e282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:2f3887574424f301fc51b59025b73e3c67f19872f5184d761a679e915cb8302d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102981027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4f8ea7ee60ff05ad0a81a0f18cdd94eab5b30ba86e3603db538e91b7da53b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:41:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:41:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:41:54 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:42:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:42:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:42:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:42:22 GMT
ENV MYSQL_MAJOR=5.6
# Sat, 27 Mar 2021 06:42:23 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Sat, 27 Mar 2021 06:42:24 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:42:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:42:45 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:42:45 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:42:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:42:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:42:48 GMT
EXPOSE 3306
# Sat, 27 Mar 2021 06:42:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f043a334d312c9990426dd2e0b151538bad668db8d81e912c0fb58c7475268`  
		Last Modified: Sat, 27 Mar 2021 06:44:40 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc55a8e93ff2837998feb3816140f02108f49dc80cddb56bb44b87eb0cedf05c`  
		Last Modified: Sat, 27 Mar 2021 06:44:39 GMT  
		Size: 4.5 MB (4503298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3042318a3bd655c9de4b3ef171f673cb00ef302883fa7f19cfcd1570e7f67b`  
		Last Modified: Sat, 27 Mar 2021 06:44:38 GMT  
		Size: 1.4 MB (1412282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63d16ff885125d653338d22ff90962435a66b17f994a5c90d0b3ff7a63bfc1`  
		Last Modified: Sat, 27 Mar 2021 06:44:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0405a1c9e5b1b14fa41aec97744e8cff571031ee5e76f9ee92af64f2b416610f`  
		Last Modified: Sat, 27 Mar 2021 06:44:43 GMT  
		Size: 10.2 MB (10225951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b584aa6803f3e9d4204209a19383332cde3b6710ed0af0a7d4c7288b87f360e2`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856a26a656f61b8f8ac590dea90563fc45b313a209061af49a45a2a517e9589`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4236a5b5e0082439257134e5321e8ff46d774f15da906a79853bc3b29eb047a6`  
		Last Modified: Sat, 27 Mar 2021 06:44:51 GMT  
		Size: 64.3 MB (64274365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d096a6038d1816d16367e1d0de120b85d22516a50e37cdc3b599c7bbf4070f7`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 5.5 KB (5537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a14ee30c53c225cc14f612cdd403a4e5e44e82b9973d685db2418f46446c1`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:dc5d576f0e1eddd606f033abfa52a4092e254fd0075d90a9509d0a1f2318e282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:2f3887574424f301fc51b59025b73e3c67f19872f5184d761a679e915cb8302d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102981027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4f8ea7ee60ff05ad0a81a0f18cdd94eab5b30ba86e3603db538e91b7da53b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:23:32 GMT
ADD file:72268d05e43fe7fe347fba8d003dbe9926a595c116e761cf3997af09cfa0ee19 in / 
# Fri, 26 Mar 2021 15:23:32 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:41:46 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:41:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:41:54 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:42:09 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:42:11 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:42:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:42:22 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:42:22 GMT
ENV MYSQL_MAJOR=5.6
# Sat, 27 Mar 2021 06:42:23 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Sat, 27 Mar 2021 06:42:24 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:42:45 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:42:45 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:42:45 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:42:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:42:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:42:48 GMT
EXPOSE 3306
# Sat, 27 Mar 2021 06:42:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b5887238bf65fc2f40fdd004509b96300faa112cc64eb2865a09895474269ee7`  
		Last Modified: Fri, 26 Mar 2021 15:32:49 GMT  
		Size: 22.5 MB (22528402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f043a334d312c9990426dd2e0b151538bad668db8d81e912c0fb58c7475268`  
		Last Modified: Sat, 27 Mar 2021 06:44:40 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc55a8e93ff2837998feb3816140f02108f49dc80cddb56bb44b87eb0cedf05c`  
		Last Modified: Sat, 27 Mar 2021 06:44:39 GMT  
		Size: 4.5 MB (4503298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3042318a3bd655c9de4b3ef171f673cb00ef302883fa7f19cfcd1570e7f67b`  
		Last Modified: Sat, 27 Mar 2021 06:44:38 GMT  
		Size: 1.4 MB (1412282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b63d16ff885125d653338d22ff90962435a66b17f994a5c90d0b3ff7a63bfc1`  
		Last Modified: Sat, 27 Mar 2021 06:44:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0405a1c9e5b1b14fa41aec97744e8cff571031ee5e76f9ee92af64f2b416610f`  
		Last Modified: Sat, 27 Mar 2021 06:44:43 GMT  
		Size: 10.2 MB (10225951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b584aa6803f3e9d4204209a19383332cde3b6710ed0af0a7d4c7288b87f360e2`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a856a26a656f61b8f8ac590dea90563fc45b313a209061af49a45a2a517e9589`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4236a5b5e0082439257134e5321e8ff46d774f15da906a79853bc3b29eb047a6`  
		Last Modified: Sat, 27 Mar 2021 06:44:51 GMT  
		Size: 64.3 MB (64274365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d096a6038d1816d16367e1d0de120b85d22516a50e37cdc3b599c7bbf4070f7`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 5.5 KB (5537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238a14ee30c53c225cc14f612cdd403a4e5e44e82b9973d685db2418f46446c1`  
		Last Modified: Sat, 27 Mar 2021 06:44:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:6b33c0c4224e341938a7e97f1d19737ff8d436dc574086dd129a8c7556cb8eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:2f51df7c1ab69dde4697130a5d5242bf2f80db2cb3282056394731019c8a5327
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154597208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3473143edd4d8c7c87d87d202de3529b1ac9b9825aa49c2d0700e004b2a95e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:40:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:22 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:40:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:40:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:41:15 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 27 Mar 2021 06:41:15 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Sat, 27 Mar 2021 06:41:17 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:41:39 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:41:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:41:40 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:41:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:41:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:41:42 GMT
EXPOSE 3306 33060
# Sat, 27 Mar 2021 06:41:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4d5966d009db5e1fdb79dc66571186bc239cd9ac8a04728fe1a261f8845a9`  
		Last Modified: Sat, 27 Mar 2021 06:43:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8e9739c9eee764cf4a141db8282b611ef449cf417833268082b707222cf87`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 4.2 MB (4179177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd773bacd125e8480c1d42ae5b50fbd62432c0b164594261b2f7f247bd3c667`  
		Last Modified: Sat, 27 Mar 2021 06:43:20 GMT  
		Size: 1.4 MB (1419334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbceeecb7f3cedb1851810d37bb4121c6ce4490b9f76aed57c33581d816e9d5`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53011e5d0402c2f5acf7636e9a37c2d6610ee1eb4e7f36dbf21b7e11edfaa1`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 13.4 MB (13447645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae8cea62cbb34627c348f33d0b0af9fc2b56b96d098fed207530c5faa7f897`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5c6fd32f0563c03543ead9f4d51b621a7f9f4d9438f64b31337442399622ad`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34240da42b5c1d8f7a9f170ca3c23efb55235ab9151b2bec9b1c8b7d6aabb39`  
		Last Modified: Sat, 27 Mar 2021 06:44:20 GMT  
		Size: 108.4 MB (108439914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e62ee1f8e19bb5b7225fefa0d53a520e56bd3b44ac1b546c45da302e5f3d7c`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b1117e790ccd950f2f10912b08926999ef671f4dbfad85825fa507837b2da`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.33`

```console
$ docker pull mysql@sha256:6b33c0c4224e341938a7e97f1d19737ff8d436dc574086dd129a8c7556cb8eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.33` - linux; amd64

```console
$ docker pull mysql@sha256:2f51df7c1ab69dde4697130a5d5242bf2f80db2cb3282056394731019c8a5327
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.6 MB (154597208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3473143edd4d8c7c87d87d202de3529b1ac9b9825aa49c2d0700e004b2a95e5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:40:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:22 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:40:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:40:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:41:15 GMT
ENV MYSQL_MAJOR=5.7
# Sat, 27 Mar 2021 06:41:15 GMT
ENV MYSQL_VERSION=5.7.33-1debian10
# Sat, 27 Mar 2021 06:41:17 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:41:39 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:41:40 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:41:40 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:41:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:41:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:41:42 GMT
EXPOSE 3306 33060
# Sat, 27 Mar 2021 06:41:42 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4d5966d009db5e1fdb79dc66571186bc239cd9ac8a04728fe1a261f8845a9`  
		Last Modified: Sat, 27 Mar 2021 06:43:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8e9739c9eee764cf4a141db8282b611ef449cf417833268082b707222cf87`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 4.2 MB (4179177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd773bacd125e8480c1d42ae5b50fbd62432c0b164594261b2f7f247bd3c667`  
		Last Modified: Sat, 27 Mar 2021 06:43:20 GMT  
		Size: 1.4 MB (1419334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbceeecb7f3cedb1851810d37bb4121c6ce4490b9f76aed57c33581d816e9d5`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53011e5d0402c2f5acf7636e9a37c2d6610ee1eb4e7f36dbf21b7e11edfaa1`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 13.4 MB (13447645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae8cea62cbb34627c348f33d0b0af9fc2b56b96d098fed207530c5faa7f897`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5c6fd32f0563c03543ead9f4d51b621a7f9f4d9438f64b31337442399622ad`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34240da42b5c1d8f7a9f170ca3c23efb55235ab9151b2bec9b1c8b7d6aabb39`  
		Last Modified: Sat, 27 Mar 2021 06:44:20 GMT  
		Size: 108.4 MB (108439914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e62ee1f8e19bb5b7225fefa0d53a520e56bd3b44ac1b546c45da302e5f3d7c`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 5.5 KB (5521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458b1117e790ccd950f2f10912b08926999ef671f4dbfad85825fa507837b2da`  
		Last Modified: Sat, 27 Mar 2021 06:44:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:00b627abbd6e91d5d0e4be786869930497b9759bf40db3f15408bb894daf5263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:48a2ccb946d971bc89a58fdff61df839253511407012fd5ea9103a4ad2d28050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159285133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d757c3ddbb3b30fa246a0fe6575700ceded1409dacd53423b8d0ffe045f6114e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:40:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:22 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:40:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:40:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:40:46 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 27 Mar 2021 06:40:47 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Sat, 27 Mar 2021 06:40:48 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:41:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:41:09 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:41:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 27 Mar 2021 06:41:09 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:41:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:41:11 GMT
EXPOSE 3306 33060
# Sat, 27 Mar 2021 06:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4d5966d009db5e1fdb79dc66571186bc239cd9ac8a04728fe1a261f8845a9`  
		Last Modified: Sat, 27 Mar 2021 06:43:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8e9739c9eee764cf4a141db8282b611ef449cf417833268082b707222cf87`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 4.2 MB (4179177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd773bacd125e8480c1d42ae5b50fbd62432c0b164594261b2f7f247bd3c667`  
		Last Modified: Sat, 27 Mar 2021 06:43:20 GMT  
		Size: 1.4 MB (1419334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbceeecb7f3cedb1851810d37bb4121c6ce4490b9f76aed57c33581d816e9d5`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53011e5d0402c2f5acf7636e9a37c2d6610ee1eb4e7f36dbf21b7e11edfaa1`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 13.4 MB (13447645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae8cea62cbb34627c348f33d0b0af9fc2b56b96d098fed207530c5faa7f897`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09f068015c7de284e2089a91c86dc377e84e9c0ce37c09a04125570111ca8b`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d80f48621dae0adcc281d50c93c53e92b1e56867cafa46bd6b8f03469702c7`  
		Last Modified: Sat, 27 Mar 2021 06:43:41 GMT  
		Size: 113.1 MB (113126995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d48194f313163dc274d8b0a1908fa0ac7291aa1413e0c1ec601bdd4b564d8`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea01c86a52bcf568d44e61542f0363a8277da0b8e5b317d7c80ab033fc322f1`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 5.5 KB (5522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e9db22376c045a62155830e59c56c9c6d1c1de0828ef780b7bab4af64b6921`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:00b627abbd6e91d5d0e4be786869930497b9759bf40db3f15408bb894daf5263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:48a2ccb946d971bc89a58fdff61df839253511407012fd5ea9103a4ad2d28050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159285133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d757c3ddbb3b30fa246a0fe6575700ceded1409dacd53423b8d0ffe045f6114e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:40:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:22 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:40:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:40:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:40:46 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 27 Mar 2021 06:40:47 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Sat, 27 Mar 2021 06:40:48 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:41:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:41:09 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:41:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 27 Mar 2021 06:41:09 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:41:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:41:11 GMT
EXPOSE 3306 33060
# Sat, 27 Mar 2021 06:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4d5966d009db5e1fdb79dc66571186bc239cd9ac8a04728fe1a261f8845a9`  
		Last Modified: Sat, 27 Mar 2021 06:43:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8e9739c9eee764cf4a141db8282b611ef449cf417833268082b707222cf87`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 4.2 MB (4179177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd773bacd125e8480c1d42ae5b50fbd62432c0b164594261b2f7f247bd3c667`  
		Last Modified: Sat, 27 Mar 2021 06:43:20 GMT  
		Size: 1.4 MB (1419334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbceeecb7f3cedb1851810d37bb4121c6ce4490b9f76aed57c33581d816e9d5`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53011e5d0402c2f5acf7636e9a37c2d6610ee1eb4e7f36dbf21b7e11edfaa1`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 13.4 MB (13447645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae8cea62cbb34627c348f33d0b0af9fc2b56b96d098fed207530c5faa7f897`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09f068015c7de284e2089a91c86dc377e84e9c0ce37c09a04125570111ca8b`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d80f48621dae0adcc281d50c93c53e92b1e56867cafa46bd6b8f03469702c7`  
		Last Modified: Sat, 27 Mar 2021 06:43:41 GMT  
		Size: 113.1 MB (113126995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d48194f313163dc274d8b0a1908fa0ac7291aa1413e0c1ec601bdd4b564d8`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea01c86a52bcf568d44e61542f0363a8277da0b8e5b317d7c80ab033fc322f1`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 5.5 KB (5522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e9db22376c045a62155830e59c56c9c6d1c1de0828ef780b7bab4af64b6921`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.23`

```console
$ docker pull mysql@sha256:00b627abbd6e91d5d0e4be786869930497b9759bf40db3f15408bb894daf5263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.23` - linux; amd64

```console
$ docker pull mysql@sha256:48a2ccb946d971bc89a58fdff61df839253511407012fd5ea9103a4ad2d28050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159285133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d757c3ddbb3b30fa246a0fe6575700ceded1409dacd53423b8d0ffe045f6114e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:40:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:22 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:40:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:40:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:40:46 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 27 Mar 2021 06:40:47 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Sat, 27 Mar 2021 06:40:48 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:41:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:41:09 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:41:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 27 Mar 2021 06:41:09 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:41:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:41:11 GMT
EXPOSE 3306 33060
# Sat, 27 Mar 2021 06:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4d5966d009db5e1fdb79dc66571186bc239cd9ac8a04728fe1a261f8845a9`  
		Last Modified: Sat, 27 Mar 2021 06:43:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8e9739c9eee764cf4a141db8282b611ef449cf417833268082b707222cf87`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 4.2 MB (4179177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd773bacd125e8480c1d42ae5b50fbd62432c0b164594261b2f7f247bd3c667`  
		Last Modified: Sat, 27 Mar 2021 06:43:20 GMT  
		Size: 1.4 MB (1419334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbceeecb7f3cedb1851810d37bb4121c6ce4490b9f76aed57c33581d816e9d5`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53011e5d0402c2f5acf7636e9a37c2d6610ee1eb4e7f36dbf21b7e11edfaa1`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 13.4 MB (13447645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae8cea62cbb34627c348f33d0b0af9fc2b56b96d098fed207530c5faa7f897`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09f068015c7de284e2089a91c86dc377e84e9c0ce37c09a04125570111ca8b`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d80f48621dae0adcc281d50c93c53e92b1e56867cafa46bd6b8f03469702c7`  
		Last Modified: Sat, 27 Mar 2021 06:43:41 GMT  
		Size: 113.1 MB (113126995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d48194f313163dc274d8b0a1908fa0ac7291aa1413e0c1ec601bdd4b564d8`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea01c86a52bcf568d44e61542f0363a8277da0b8e5b317d7c80ab033fc322f1`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 5.5 KB (5522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e9db22376c045a62155830e59c56c9c6d1c1de0828ef780b7bab4af64b6921`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:00b627abbd6e91d5d0e4be786869930497b9759bf40db3f15408bb894daf5263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:48a2ccb946d971bc89a58fdff61df839253511407012fd5ea9103a4ad2d28050
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159285133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d757c3ddbb3b30fa246a0fe6575700ceded1409dacd53423b8d0ffe045f6114e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:59 GMT
ADD file:b2085f4b0a7cb0e5754874c712254e5cd941062b27b8d7ed2080520196b91597 in / 
# Fri, 26 Mar 2021 15:20:59 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 06:40:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 27 Mar 2021 06:40:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:22 GMT
ENV GOSU_VERSION=1.12
# Sat, 27 Mar 2021 06:40:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 27 Mar 2021 06:40:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 27 Mar 2021 06:40:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 06:40:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Sat, 27 Mar 2021 06:40:46 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 27 Mar 2021 06:40:47 GMT
ENV MYSQL_VERSION=8.0.23-1debian10
# Sat, 27 Mar 2021 06:40:48 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 27 Mar 2021 06:41:08 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 27 Mar 2021 06:41:09 GMT
VOLUME [/var/lib/mysql]
# Sat, 27 Mar 2021 06:41:09 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 27 Mar 2021 06:41:09 GMT
COPY file:2c6221a2517649db2e9dd27098cc9ae1bdaff205f8d6f0299b20a41b86084d77 in /usr/local/bin/ 
# Sat, 27 Mar 2021 06:41:10 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 27 Mar 2021 06:41:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Mar 2021 06:41:11 GMT
EXPOSE 3306 33060
# Sat, 27 Mar 2021 06:41:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ac2522cc72690febc428fb46fb39a4efc5e0a721c3ad15d9992b01515f2fad1a`  
		Last Modified: Fri, 26 Mar 2021 15:27:47 GMT  
		Size: 27.1 MB (27100996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff4d5966d009db5e1fdb79dc66571186bc239cd9ac8a04728fe1a261f8845a9`  
		Last Modified: Sat, 27 Mar 2021 06:43:22 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8e9739c9eee764cf4a141db8282b611ef449cf417833268082b707222cf87`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 4.2 MB (4179177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd773bacd125e8480c1d42ae5b50fbd62432c0b164594261b2f7f247bd3c667`  
		Last Modified: Sat, 27 Mar 2021 06:43:20 GMT  
		Size: 1.4 MB (1419334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbceeecb7f3cedb1851810d37bb4121c6ce4490b9f76aed57c33581d816e9d5`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b53011e5d0402c2f5acf7636e9a37c2d6610ee1eb4e7f36dbf21b7e11edfaa1`  
		Last Modified: Sat, 27 Mar 2021 06:43:23 GMT  
		Size: 13.4 MB (13447645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ae8cea62cbb34627c348f33d0b0af9fc2b56b96d098fed207530c5faa7f897`  
		Last Modified: Sat, 27 Mar 2021 06:43:19 GMT  
		Size: 2.4 KB (2392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09f068015c7de284e2089a91c86dc377e84e9c0ce37c09a04125570111ca8b`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d80f48621dae0adcc281d50c93c53e92b1e56867cafa46bd6b8f03469702c7`  
		Last Modified: Sat, 27 Mar 2021 06:43:41 GMT  
		Size: 113.1 MB (113126995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9d48194f313163dc274d8b0a1908fa0ac7291aa1413e0c1ec601bdd4b564d8`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 843.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea01c86a52bcf568d44e61542f0363a8277da0b8e5b317d7c80ab033fc322f1`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 5.5 KB (5522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e9db22376c045a62155830e59c56c9c6d1c1de0828ef780b7bab4af64b6921`  
		Last Modified: Sat, 27 Mar 2021 06:43:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
