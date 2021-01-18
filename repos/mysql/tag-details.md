<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.50`](#mysql5650)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.33`](#mysql5733)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.23`](#mysql8023)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:e08834258fcc0efd01df358222333919df53d4a0d9b2a54da05b204b822e3b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:860f4bcc18607de9f40a7453c7dc160313ecc3a5a46be3b060569b6216d348f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154509028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8775c0fe94cd6cbfc494688d09b078cda9bced9d9324d5c28bddf032344fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:10:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Jan 2021 10:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:10:45 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Jan 2021 10:11:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Jan 2021 10:11:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Jan 2021 10:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:11:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Jan 2021 10:12:05 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 12 Jan 2021 10:12:06 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Tue, 12 Jan 2021 10:12:07 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Jan 2021 10:12:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Jan 2021 10:12:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Jan 2021 10:12:41 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Tue, 12 Jan 2021 10:12:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 10:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 10:12:43 GMT
EXPOSE 3306 33060
# Tue, 12 Jan 2021 10:12:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c208f3f991dcbc417fed8efde391f887c0551d77ed0c1a125fd28f4841e1cc`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9455a9165654c855c2614bc1dc1f574e7d9265ecb39a3211e0bfc55926729`  
		Last Modified: Tue, 12 Jan 2021 10:14:48 GMT  
		Size: 4.2 MB (4178395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c9b8427c60dac1a77115209e657b93011196642d047d08e63fe8efc3a16c7`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.4 MB (1419257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c88599c0b25840a8671b24aba0e3b11707ea831f942271cfb1f6965e2a48cf9`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5c6debdaf0cdad9d7b385d0feed9ee0dc10c8eb328d07787ef87326ee57db`  
		Last Modified: Tue, 12 Jan 2021 10:14:52 GMT  
		Size: 13.4 MB (13447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a5816f16170063a978d1eb0310df536bb5637175d736fedd5b240b1a9e05d3`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7065aaa2655f38309f376982c6f52a426ce2f5647e4761595453317c8155d739`  
		Last Modified: Tue, 12 Jan 2021 10:15:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bc531db40fb993db42d46123bc500d95e92f3f6e06967fef9470485b6c7297`  
		Last Modified: Tue, 12 Jan 2021 10:15:47 GMT  
		Size: 108.3 MB (108346191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e9d7c9815f1f6a9ca6761825fd276476783ea3fee09cc85a5e445b6594b87`  
		Last Modified: Tue, 12 Jan 2021 10:15:28 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadfb9734ed22677bbf5452a152e4c69e4afe17d3a0cfb4a753a721db493c588`  
		Last Modified: Tue, 12 Jan 2021 10:15:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:427635d7f0e3be6f5e085728da4e9d8e657130d941e3b0f261a1916cf5741810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:cdd92b8764d609e0fd4af54633a6cb155b2deae9363b362c1115120bd2fece50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102939410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e68afc1976f2aa759a7f2520ee173440e1fe78a3d783f7c721e9d9d1cd5b6bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:12:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Jan 2021 10:13:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:13:06 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Jan 2021 10:13:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Jan 2021 10:13:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Jan 2021 10:13:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:13:40 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Jan 2021 10:13:40 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 12 Jan 2021 10:13:41 GMT
ENV MYSQL_VERSION=5.6.50-1debian9
# Tue, 12 Jan 2021 10:13:43 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Jan 2021 10:14:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Jan 2021 10:14:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Jan 2021 10:14:08 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Tue, 12 Jan 2021 10:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 10:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 10:14:10 GMT
EXPOSE 3306
# Tue, 12 Jan 2021 10:14:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fc34c9927b80992a64c2d0cad423d7806727c89e1e99fbc75c9ba06eac53c`  
		Last Modified: Tue, 12 Jan 2021 10:16:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dfb473d52ef420284e53a70284b74a68b0645c1e598b3b4a86c214a0cf732f`  
		Last Modified: Tue, 12 Jan 2021 10:16:03 GMT  
		Size: 4.5 MB (4502223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702c333a167eb2923635dd5335130dbe73abcf31092f0feec58d29133965a800`  
		Last Modified: Tue, 12 Jan 2021 10:16:00 GMT  
		Size: 1.4 MB (1412140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699bc078b4523267053f673c0b55f130f20016938f99cab926631edf94d30c21`  
		Last Modified: Tue, 12 Jan 2021 10:16:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dd862365bd0231e76a6a966deb4f34deec87713fd2992306e21fc4a1375229`  
		Last Modified: Tue, 12 Jan 2021 10:16:03 GMT  
		Size: 10.2 MB (10225346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbfc4425b5a61260db302afa3ad299d5fd8da47b9a5f88cb6807a00efce7174`  
		Last Modified: Tue, 12 Jan 2021 10:15:58 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48cbe0a83dc943e35d35cdb0aa8031a6babf4a6cd247335851b1b0ed6875afd`  
		Last Modified: Tue, 12 Jan 2021 10:15:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191adddbb24b74275a0a97acc384500779c5ae5294c8c2a184a3cc2bf48a7b88`  
		Last Modified: Tue, 12 Jan 2021 10:16:17 GMT  
		Size: 64.2 MB (64234779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b887ee6e990f3d0da11de8693ba523104ea989d77730c5c046aef7704212bc`  
		Last Modified: Tue, 12 Jan 2021 10:15:59 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f676c0b559fd43d6ccf6ff5cc09cccfa6a66f4e1b601f9d7644f87d1b293f8e`  
		Last Modified: Tue, 12 Jan 2021 10:15:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.50`

```console
$ docker pull mysql@sha256:427635d7f0e3be6f5e085728da4e9d8e657130d941e3b0f261a1916cf5741810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.50` - linux; amd64

```console
$ docker pull mysql@sha256:cdd92b8764d609e0fd4af54633a6cb155b2deae9363b362c1115120bd2fece50
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102939410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e68afc1976f2aa759a7f2520ee173440e1fe78a3d783f7c721e9d9d1cd5b6bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Jan 2021 00:35:21 GMT
ADD file:f47757e25d3861a5c0180542919c21264323d4dace1f5a6761fc2f38b53a9003 in / 
# Tue, 12 Jan 2021 00:35:21 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:12:55 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Jan 2021 10:13:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:13:06 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Jan 2021 10:13:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Jan 2021 10:13:25 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Jan 2021 10:13:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:13:40 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Jan 2021 10:13:40 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 12 Jan 2021 10:13:41 GMT
ENV MYSQL_VERSION=5.6.50-1debian9
# Tue, 12 Jan 2021 10:13:43 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Jan 2021 10:14:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Jan 2021 10:14:07 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Jan 2021 10:14:08 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Tue, 12 Jan 2021 10:14:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 10:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 10:14:10 GMT
EXPOSE 3306
# Tue, 12 Jan 2021 10:14:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8aff230071c97ddc86b6d29fbbb7a4caae7a0183a83f08aa5a06e69e26ce2c81`  
		Last Modified: Tue, 12 Jan 2021 00:43:25 GMT  
		Size: 22.5 MB (22528609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134fc34c9927b80992a64c2d0cad423d7806727c89e1e99fbc75c9ba06eac53c`  
		Last Modified: Tue, 12 Jan 2021 10:16:03 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27dfb473d52ef420284e53a70284b74a68b0645c1e598b3b4a86c214a0cf732f`  
		Last Modified: Tue, 12 Jan 2021 10:16:03 GMT  
		Size: 4.5 MB (4502223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702c333a167eb2923635dd5335130dbe73abcf31092f0feec58d29133965a800`  
		Last Modified: Tue, 12 Jan 2021 10:16:00 GMT  
		Size: 1.4 MB (1412140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699bc078b4523267053f673c0b55f130f20016938f99cab926631edf94d30c21`  
		Last Modified: Tue, 12 Jan 2021 10:16:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dd862365bd0231e76a6a966deb4f34deec87713fd2992306e21fc4a1375229`  
		Last Modified: Tue, 12 Jan 2021 10:16:03 GMT  
		Size: 10.2 MB (10225346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dbfc4425b5a61260db302afa3ad299d5fd8da47b9a5f88cb6807a00efce7174`  
		Last Modified: Tue, 12 Jan 2021 10:15:58 GMT  
		Size: 29.0 KB (28956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48cbe0a83dc943e35d35cdb0aa8031a6babf4a6cd247335851b1b0ed6875afd`  
		Last Modified: Tue, 12 Jan 2021 10:15:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191adddbb24b74275a0a97acc384500779c5ae5294c8c2a184a3cc2bf48a7b88`  
		Last Modified: Tue, 12 Jan 2021 10:16:17 GMT  
		Size: 64.2 MB (64234779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b887ee6e990f3d0da11de8693ba523104ea989d77730c5c046aef7704212bc`  
		Last Modified: Tue, 12 Jan 2021 10:15:59 GMT  
		Size: 5.2 KB (5155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f676c0b559fd43d6ccf6ff5cc09cccfa6a66f4e1b601f9d7644f87d1b293f8e`  
		Last Modified: Tue, 12 Jan 2021 10:15:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:e08834258fcc0efd01df358222333919df53d4a0d9b2a54da05b204b822e3b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:860f4bcc18607de9f40a7453c7dc160313ecc3a5a46be3b060569b6216d348f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154509028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8775c0fe94cd6cbfc494688d09b078cda9bced9d9324d5c28bddf032344fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:10:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Jan 2021 10:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:10:45 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Jan 2021 10:11:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Jan 2021 10:11:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Jan 2021 10:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:11:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Jan 2021 10:12:05 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 12 Jan 2021 10:12:06 GMT
ENV MYSQL_VERSION=5.7.32-1debian10
# Tue, 12 Jan 2021 10:12:07 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Jan 2021 10:12:40 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Jan 2021 10:12:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Jan 2021 10:12:41 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Tue, 12 Jan 2021 10:12:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 10:12:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 10:12:43 GMT
EXPOSE 3306 33060
# Tue, 12 Jan 2021 10:12:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c208f3f991dcbc417fed8efde391f887c0551d77ed0c1a125fd28f4841e1cc`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9455a9165654c855c2614bc1dc1f574e7d9265ecb39a3211e0bfc55926729`  
		Last Modified: Tue, 12 Jan 2021 10:14:48 GMT  
		Size: 4.2 MB (4178395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c9b8427c60dac1a77115209e657b93011196642d047d08e63fe8efc3a16c7`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.4 MB (1419257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c88599c0b25840a8671b24aba0e3b11707ea831f942271cfb1f6965e2a48cf9`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5c6debdaf0cdad9d7b385d0feed9ee0dc10c8eb328d07787ef87326ee57db`  
		Last Modified: Tue, 12 Jan 2021 10:14:52 GMT  
		Size: 13.4 MB (13447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a5816f16170063a978d1eb0310df536bb5637175d736fedd5b240b1a9e05d3`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7065aaa2655f38309f376982c6f52a426ce2f5647e4761595453317c8155d739`  
		Last Modified: Tue, 12 Jan 2021 10:15:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bc531db40fb993db42d46123bc500d95e92f3f6e06967fef9470485b6c7297`  
		Last Modified: Tue, 12 Jan 2021 10:15:47 GMT  
		Size: 108.3 MB (108346191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e9d7c9815f1f6a9ca6761825fd276476783ea3fee09cc85a5e445b6594b87`  
		Last Modified: Tue, 12 Jan 2021 10:15:28 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadfb9734ed22677bbf5452a152e4c69e4afe17d3a0cfb4a753a721db493c588`  
		Last Modified: Tue, 12 Jan 2021 10:15:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.33`

**does not exist** (yet?)

## `mysql:8`

```console
$ docker pull mysql@sha256:0fd2898dc1c946b34dceaccc3b80d38b1049285c1dab70df7480de62265d6213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:7d83f4d89c92d7e72b366cc9d0f5c19b12cba934c5e135d21d81b2b84651df69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158963400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c3cafb11d573699728f9e7de10d1b976089b01298c0360e03f0afd9a1a8b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:10:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Jan 2021 10:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:10:45 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Jan 2021 10:11:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Jan 2021 10:11:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Jan 2021 10:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:11:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Jan 2021 10:11:17 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Jan 2021 10:11:17 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Tue, 12 Jan 2021 10:11:18 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Jan 2021 10:11:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Jan 2021 10:11:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Jan 2021 10:11:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 12 Jan 2021 10:11:47 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Tue, 12 Jan 2021 10:11:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 10:11:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 10:11:50 GMT
EXPOSE 3306 33060
# Tue, 12 Jan 2021 10:11:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c208f3f991dcbc417fed8efde391f887c0551d77ed0c1a125fd28f4841e1cc`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9455a9165654c855c2614bc1dc1f574e7d9265ecb39a3211e0bfc55926729`  
		Last Modified: Tue, 12 Jan 2021 10:14:48 GMT  
		Size: 4.2 MB (4178395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c9b8427c60dac1a77115209e657b93011196642d047d08e63fe8efc3a16c7`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.4 MB (1419257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c88599c0b25840a8671b24aba0e3b11707ea831f942271cfb1f6965e2a48cf9`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5c6debdaf0cdad9d7b385d0feed9ee0dc10c8eb328d07787ef87326ee57db`  
		Last Modified: Tue, 12 Jan 2021 10:14:52 GMT  
		Size: 13.4 MB (13447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a5816f16170063a978d1eb0310df536bb5637175d736fedd5b240b1a9e05d3`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dd1fbf9190298195bd417b36a85e61157fae9618c97974b07113b2be80da4d`  
		Last Modified: Tue, 12 Jan 2021 10:14:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5346a60dcee8c23d2de0fc739187f46ef314bd43ca8fe1ccdd9dc41f50cbbaf3`  
		Last Modified: Tue, 12 Jan 2021 10:15:16 GMT  
		Size: 112.8 MB (112799719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef28da371fc949e6870650dfb2222264d2bac3cf5f190c402f018f92ef5ab37a`  
		Last Modified: Tue, 12 Jan 2021 10:14:43 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd04d935b85221ffcd1adb72f6a20802983c9df185a27188ccf9bd2903773d81`  
		Last Modified: Tue, 12 Jan 2021 10:14:44 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c49742ea268afc80316ef48d98bb122e844fbc1ec6a54c8aed19fa9ad268d`  
		Last Modified: Tue, 12 Jan 2021 10:14:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0fd2898dc1c946b34dceaccc3b80d38b1049285c1dab70df7480de62265d6213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:7d83f4d89c92d7e72b366cc9d0f5c19b12cba934c5e135d21d81b2b84651df69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158963400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c3cafb11d573699728f9e7de10d1b976089b01298c0360e03f0afd9a1a8b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:10:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Jan 2021 10:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:10:45 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Jan 2021 10:11:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Jan 2021 10:11:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Jan 2021 10:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:11:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Jan 2021 10:11:17 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Jan 2021 10:11:17 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Tue, 12 Jan 2021 10:11:18 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Jan 2021 10:11:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Jan 2021 10:11:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Jan 2021 10:11:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 12 Jan 2021 10:11:47 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Tue, 12 Jan 2021 10:11:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 10:11:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 10:11:50 GMT
EXPOSE 3306 33060
# Tue, 12 Jan 2021 10:11:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c208f3f991dcbc417fed8efde391f887c0551d77ed0c1a125fd28f4841e1cc`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9455a9165654c855c2614bc1dc1f574e7d9265ecb39a3211e0bfc55926729`  
		Last Modified: Tue, 12 Jan 2021 10:14:48 GMT  
		Size: 4.2 MB (4178395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c9b8427c60dac1a77115209e657b93011196642d047d08e63fe8efc3a16c7`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.4 MB (1419257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c88599c0b25840a8671b24aba0e3b11707ea831f942271cfb1f6965e2a48cf9`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5c6debdaf0cdad9d7b385d0feed9ee0dc10c8eb328d07787ef87326ee57db`  
		Last Modified: Tue, 12 Jan 2021 10:14:52 GMT  
		Size: 13.4 MB (13447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a5816f16170063a978d1eb0310df536bb5637175d736fedd5b240b1a9e05d3`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dd1fbf9190298195bd417b36a85e61157fae9618c97974b07113b2be80da4d`  
		Last Modified: Tue, 12 Jan 2021 10:14:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5346a60dcee8c23d2de0fc739187f46ef314bd43ca8fe1ccdd9dc41f50cbbaf3`  
		Last Modified: Tue, 12 Jan 2021 10:15:16 GMT  
		Size: 112.8 MB (112799719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef28da371fc949e6870650dfb2222264d2bac3cf5f190c402f018f92ef5ab37a`  
		Last Modified: Tue, 12 Jan 2021 10:14:43 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd04d935b85221ffcd1adb72f6a20802983c9df185a27188ccf9bd2903773d81`  
		Last Modified: Tue, 12 Jan 2021 10:14:44 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c49742ea268afc80316ef48d98bb122e844fbc1ec6a54c8aed19fa9ad268d`  
		Last Modified: Tue, 12 Jan 2021 10:14:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.23`

**does not exist** (yet?)

## `mysql:latest`

```console
$ docker pull mysql@sha256:0fd2898dc1c946b34dceaccc3b80d38b1049285c1dab70df7480de62265d6213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:7d83f4d89c92d7e72b366cc9d0f5c19b12cba934c5e135d21d81b2b84651df69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158963400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c3cafb11d573699728f9e7de10d1b976089b01298c0360e03f0afd9a1a8b36`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Jan 2021 00:32:51 GMT
ADD file:422aca8901ae3d869a815051cea7f1e4c0204fad16884e7cd01da57d142f2e3a in / 
# Tue, 12 Jan 2021 00:32:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 10:10:35 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Jan 2021 10:10:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:10:45 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Jan 2021 10:11:00 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Jan 2021 10:11:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Jan 2021 10:11:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 10:11:16 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Jan 2021 10:11:17 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 12 Jan 2021 10:11:17 GMT
ENV MYSQL_VERSION=8.0.22-1debian10
# Tue, 12 Jan 2021 10:11:18 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Jan 2021 10:11:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Jan 2021 10:11:47 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Jan 2021 10:11:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 12 Jan 2021 10:11:47 GMT
COPY file:a209112a748b68e09c2f024b0d9630bcca79e1f73e9152a984e09a9b94b1df93 in /usr/local/bin/ 
# Tue, 12 Jan 2021 10:11:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Jan 2021 10:11:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Jan 2021 10:11:50 GMT
EXPOSE 3306 33060
# Tue, 12 Jan 2021 10:11:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:a076a628af6f7dcabc536bee373c0d9b48d9f0516788e64080c4e841746e6ce6`  
		Last Modified: Tue, 12 Jan 2021 00:39:13 GMT  
		Size: 27.1 MB (27108069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c208f3f991dcbc417fed8efde391f887c0551d77ed0c1a125fd28f4841e1cc`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a9455a9165654c855c2614bc1dc1f574e7d9265ecb39a3211e0bfc55926729`  
		Last Modified: Tue, 12 Jan 2021 10:14:48 GMT  
		Size: 4.2 MB (4178395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c9b8427c60dac1a77115209e657b93011196642d047d08e63fe8efc3a16c7`  
		Last Modified: Tue, 12 Jan 2021 10:14:46 GMT  
		Size: 1.4 MB (1419257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c88599c0b25840a8671b24aba0e3b11707ea831f942271cfb1f6965e2a48cf9`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b5c6debdaf0cdad9d7b385d0feed9ee0dc10c8eb328d07787ef87326ee57db`  
		Last Modified: Tue, 12 Jan 2021 10:14:52 GMT  
		Size: 13.4 MB (13447377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a5816f16170063a978d1eb0310df536bb5637175d736fedd5b240b1a9e05d3`  
		Last Modified: Tue, 12 Jan 2021 10:14:45 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dd1fbf9190298195bd417b36a85e61157fae9618c97974b07113b2be80da4d`  
		Last Modified: Tue, 12 Jan 2021 10:14:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5346a60dcee8c23d2de0fc739187f46ef314bd43ca8fe1ccdd9dc41f50cbbaf3`  
		Last Modified: Tue, 12 Jan 2021 10:15:16 GMT  
		Size: 112.8 MB (112799719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef28da371fc949e6870650dfb2222264d2bac3cf5f190c402f018f92ef5ab37a`  
		Last Modified: Tue, 12 Jan 2021 10:14:43 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd04d935b85221ffcd1adb72f6a20802983c9df185a27188ccf9bd2903773d81`  
		Last Modified: Tue, 12 Jan 2021 10:14:44 GMT  
		Size: 5.1 KB (5141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050c49742ea268afc80316ef48d98bb122e844fbc1ec6a54c8aed19fa9ad268d`  
		Last Modified: Tue, 12 Jan 2021 10:14:43 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
