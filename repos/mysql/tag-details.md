<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.48`](#mysql5648)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.30`](#mysql5730)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.20`](#mysql8020)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:5c9fd7949bc0f076429fa2c40d0e7406e095bdb5216a923257b31972a6f3ae4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:5a33c79153a8b1896465ce8b32b304a6ca0c9a7524ada2e3d78ff3725a1af7db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154406110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84d68d0a7db79194091fae58b71afb6a56ae25cb297e91f68db2a8e404a4ecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Fri, 15 May 2020 20:10:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:11:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:11:01 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:11:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:11:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:11:03 GMT
EXPOSE 3306 33060
# Fri, 15 May 2020 20:11:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec965ae405548af46a704346d97fcf663f9de2df1d71cbd6113ee803ef0556`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a531a782d709df74f09b2ba98298d124b08e89842a4eae8a918d3c5440b4b584`  
		Last Modified: Fri, 15 May 2020 20:13:21 GMT  
		Size: 108.3 MB (108257035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e94c02b50883056f91ee32a32a1ec0c85b193ee1ae8d0fe1b79203a97543db`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799a94b968efa71c047991e9a858ff8203dd69030a7ff73676a496f9769504bb`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:ed580a3179ee3f67dc854d46d3ba7c0f3af4f0cb3fecad48725b2fac707e9b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:c10336e6eca7890effd3c42e5e18250ef015457f9f8f1cb2406ee4ba0ec40015
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102887199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac12c9a0ad71b8e93c2cd06e9b66a4a630f379e75335c12ce59feecc65c6d722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:11:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:21 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:11:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:11:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_MAJOR=5.6
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Fri, 15 May 2020 20:11:47 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:12:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:12:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:12:08 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:12:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:12:10 GMT
EXPOSE 3306
# Fri, 15 May 2020 20:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4539e638b12dd4ea320a33239ccd7797ba40cdf743c134b2e59aedbc8e347fb`  
		Last Modified: Fri, 15 May 2020 20:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb8f0db2a3779eeb29488ed6fd4922daff7d67424665225276a92c03f8b790`  
		Last Modified: Fri, 15 May 2020 20:13:30 GMT  
		Size: 4.5 MB (4501267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27254901ad3716966d3dc2a05025da58414131cbefac01fb983a02c10f6f69c`  
		Last Modified: Fri, 15 May 2020 20:13:28 GMT  
		Size: 1.4 MB (1412320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e4d538a032b3c580856e0e341e2ec6b8e699eb225f7397226a90045bc95080`  
		Last Modified: Fri, 15 May 2020 20:13:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8608c48c2d6986e8653a844ab5b2cb81d95e3847c4436491da35d147fcbbdfa6`  
		Last Modified: Fri, 15 May 2020 20:13:33 GMT  
		Size: 10.2 MB (10222816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bbeb5e044578c3e7f070948cf75c66eeac765eaf0dccfe61060bc028706c8`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 28.3 KB (28328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c472cfc00c1ed45631189fd52dae6d7358373f57b7889a5a0c053190f6e5b`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3081c249e0eea462831eb7c0d51c38cd3cb97ed63253eb7dfd3a7db366ffaa4a`  
		Last Modified: Fri, 15 May 2020 20:13:43 GMT  
		Size: 64.2 MB (64195226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498227b783434687472bd8a679d24a3ae3eb8c6185b4392e9dfdfdf4e7f2dd76`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea5b6224af08e1f388a1e68a7d45b067d328979ef361db7e652f676c6d4cb15`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.48`

```console
$ docker pull mysql@sha256:ed580a3179ee3f67dc854d46d3ba7c0f3af4f0cb3fecad48725b2fac707e9b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.6.48` - linux; amd64

```console
$ docker pull mysql@sha256:c10336e6eca7890effd3c42e5e18250ef015457f9f8f1cb2406ee4ba0ec40015
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102887199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac12c9a0ad71b8e93c2cd06e9b66a4a630f379e75335c12ce59feecc65c6d722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:33:44 GMT
ADD file:ff87497c2a2fce1d776e432139030782373ac1549522a8366694786b45387306 in / 
# Fri, 15 May 2020 06:33:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:11:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:11:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:21 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:11:35 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:11:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:11:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_MAJOR=5.6
# Fri, 15 May 2020 20:11:46 GMT
ENV MYSQL_VERSION=5.6.48-1debian9
# Fri, 15 May 2020 20:11:47 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ stretch mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:12:07 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:12:07 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:12:08 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:12:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:12:10 GMT
EXPOSE 3306
# Fri, 15 May 2020 20:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e62d08fa1eb18131b4109c7cbece97f4f7e37d6ea09845a21beb3a899d0c963d`  
		Last Modified: Fri, 15 May 2020 06:40:45 GMT  
		Size: 22.5 MB (22519887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4539e638b12dd4ea320a33239ccd7797ba40cdf743c134b2e59aedbc8e347fb`  
		Last Modified: Fri, 15 May 2020 20:13:29 GMT  
		Size: 1.7 KB (1747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb8f0db2a3779eeb29488ed6fd4922daff7d67424665225276a92c03f8b790`  
		Last Modified: Fri, 15 May 2020 20:13:30 GMT  
		Size: 4.5 MB (4501267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27254901ad3716966d3dc2a05025da58414131cbefac01fb983a02c10f6f69c`  
		Last Modified: Fri, 15 May 2020 20:13:28 GMT  
		Size: 1.4 MB (1412320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e4d538a032b3c580856e0e341e2ec6b8e699eb225f7397226a90045bc95080`  
		Last Modified: Fri, 15 May 2020 20:13:27 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8608c48c2d6986e8653a844ab5b2cb81d95e3847c4436491da35d147fcbbdfa6`  
		Last Modified: Fri, 15 May 2020 20:13:33 GMT  
		Size: 10.2 MB (10222816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bbeb5e044578c3e7f070948cf75c66eeac765eaf0dccfe61060bc028706c8`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 28.3 KB (28328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86c472cfc00c1ed45631189fd52dae6d7358373f57b7889a5a0c053190f6e5b`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3081c249e0eea462831eb7c0d51c38cd3cb97ed63253eb7dfd3a7db366ffaa4a`  
		Last Modified: Fri, 15 May 2020 20:13:43 GMT  
		Size: 64.2 MB (64195226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498227b783434687472bd8a679d24a3ae3eb8c6185b4392e9dfdfdf4e7f2dd76`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 5.1 KB (5149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea5b6224af08e1f388a1e68a7d45b067d328979ef361db7e652f676c6d4cb15`  
		Last Modified: Fri, 15 May 2020 20:13:26 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:5c9fd7949bc0f076429fa2c40d0e7406e095bdb5216a923257b31972a6f3ae4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:5a33c79153a8b1896465ce8b32b304a6ca0c9a7524ada2e3d78ff3725a1af7db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154406110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84d68d0a7db79194091fae58b71afb6a56ae25cb297e91f68db2a8e404a4ecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Fri, 15 May 2020 20:10:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:11:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:11:01 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:11:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:11:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:11:03 GMT
EXPOSE 3306 33060
# Fri, 15 May 2020 20:11:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec965ae405548af46a704346d97fcf663f9de2df1d71cbd6113ee803ef0556`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a531a782d709df74f09b2ba98298d124b08e89842a4eae8a918d3c5440b4b584`  
		Last Modified: Fri, 15 May 2020 20:13:21 GMT  
		Size: 108.3 MB (108257035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e94c02b50883056f91ee32a32a1ec0c85b193ee1ae8d0fe1b79203a97543db`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799a94b968efa71c047991e9a858ff8203dd69030a7ff73676a496f9769504bb`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.30`

```console
$ docker pull mysql@sha256:5c9fd7949bc0f076429fa2c40d0e7406e095bdb5216a923257b31972a6f3ae4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:5.7.30` - linux; amd64

```console
$ docker pull mysql@sha256:5a33c79153a8b1896465ce8b32b304a6ca0c9a7524ada2e3d78ff3725a1af7db
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154406110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84d68d0a7db79194091fae58b71afb6a56ae25cb297e91f68db2a8e404a4ecb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_MAJOR=5.7
# Fri, 15 May 2020 20:10:36 GMT
ENV MYSQL_VERSION=5.7.30-1debian10
# Fri, 15 May 2020 20:10:37 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:11:00 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-server="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf
# Fri, 15 May 2020 20:11:01 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:11:01 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:11:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:11:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:11:03 GMT
EXPOSE 3306 33060
# Fri, 15 May 2020 20:11:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eec965ae405548af46a704346d97fcf663f9de2df1d71cbd6113ee803ef0556`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a531a782d709df74f09b2ba98298d124b08e89842a4eae8a918d3c5440b4b584`  
		Last Modified: Fri, 15 May 2020 20:13:21 GMT  
		Size: 108.3 MB (108257035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e94c02b50883056f91ee32a32a1ec0c85b193ee1ae8d0fe1b79203a97543db`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 5.1 KB (5136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799a94b968efa71c047991e9a858ff8203dd69030a7ff73676a496f9769504bb`  
		Last Modified: Fri, 15 May 2020 20:12:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:beba993cc5720da07129078d13441745c02560a2a0181071143e599ad9c497fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:a610e100737408fc69f45885371a6396810b88651326f2b21ff5217d38387533
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dff5fab37f18946165632a45d8ff738ee97dc7a9dfde945b0862d52ecc5b08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Fri, 15 May 2020 20:10:17 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:10:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:10:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:10:19 GMT
EXPOSE 3306 33060
# Fri, 15 May 2020 20:10:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f78cccacbe466367aebd7c0e56e64d6003540faef3330d81be303719a16ce`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623a5dae2b423caebfc0c11a0ca38f221a20fd50733c56ebbb97953f1e43116e`  
		Last Modified: Fri, 15 May 2020 20:12:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:beba993cc5720da07129078d13441745c02560a2a0181071143e599ad9c497fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:a610e100737408fc69f45885371a6396810b88651326f2b21ff5217d38387533
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dff5fab37f18946165632a45d8ff738ee97dc7a9dfde945b0862d52ecc5b08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Fri, 15 May 2020 20:10:17 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:10:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:10:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:10:19 GMT
EXPOSE 3306 33060
# Fri, 15 May 2020 20:10:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f78cccacbe466367aebd7c0e56e64d6003540faef3330d81be303719a16ce`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623a5dae2b423caebfc0c11a0ca38f221a20fd50733c56ebbb97953f1e43116e`  
		Last Modified: Fri, 15 May 2020 20:12:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.20`

```console
$ docker pull mysql@sha256:beba993cc5720da07129078d13441745c02560a2a0181071143e599ad9c497fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:8.0.20` - linux; amd64

```console
$ docker pull mysql@sha256:a610e100737408fc69f45885371a6396810b88651326f2b21ff5217d38387533
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dff5fab37f18946165632a45d8ff738ee97dc7a9dfde945b0862d52ecc5b08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Fri, 15 May 2020 20:10:17 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:10:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:10:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:10:19 GMT
EXPOSE 3306 33060
# Fri, 15 May 2020 20:10:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f78cccacbe466367aebd7c0e56e64d6003540faef3330d81be303719a16ce`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623a5dae2b423caebfc0c11a0ca38f221a20fd50733c56ebbb97953f1e43116e`  
		Last Modified: Fri, 15 May 2020 20:12:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:beba993cc5720da07129078d13441745c02560a2a0181071143e599ad9c497fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a610e100737408fc69f45885371a6396810b88651326f2b21ff5217d38387533
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dff5fab37f18946165632a45d8ff738ee97dc7a9dfde945b0862d52ecc5b08`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 20:09:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Fri, 15 May 2020 20:09:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:17 GMT
ENV GOSU_VERSION=1.12
# Fri, 15 May 2020 20:09:31 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 15 May 2020 20:09:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 15 May 2020 20:09:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 20:09:46 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 15 May 2020 20:09:47 GMT
ENV MYSQL_VERSION=8.0.20-1debian10
# Fri, 15 May 2020 20:09:48 GMT
RUN echo "deb http://repo.mysql.com/apt/debian/ buster mysql-${MYSQL_MAJOR}" > /etc/apt/sources.list.d/mysql.list
# Fri, 15 May 2020 20:10:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update && apt-get install -y mysql-community-client="${MYSQL_VERSION}" mysql-community-server-core="${MYSQL_VERSION}" && rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 777 /var/run/mysqld
# Fri, 15 May 2020 20:10:16 GMT
VOLUME [/var/lib/mysql]
# Fri, 15 May 2020 20:10:16 GMT
COPY dir:478f098f3681084f7493af1f04cbcd3eeda6f10e0dd2f5c740acd25328a73455 in /etc/mysql/ 
# Fri, 15 May 2020 20:10:17 GMT
COPY file:b09451ebd8fb98d90335352b9649da1b3336a789513bb4ae725c9eadafd519b6 in /usr/local/bin/ 
# Fri, 15 May 2020 20:10:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 15 May 2020 20:10:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 May 2020 20:10:19 GMT
EXPOSE 3306 33060
# Fri, 15 May 2020 20:10:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bdc5971ba4035759e184ecce9f8031af4e0690f7c8c80a0c2e0c39f3da4c465`  
		Last Modified: Fri, 15 May 2020 20:12:23 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ae94a2c72907664de4150bee73ee5a22100db9c3136927d49472da652d95cb`  
		Last Modified: Fri, 15 May 2020 20:12:24 GMT  
		Size: 4.2 MB (4178132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f777521d340edb8fcb9714ec8bfc01228ee5d195cdf524373c8d19536dc6eda2`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 1.4 MB (1419265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1393ff7fc87173f46263d6db1614b86ead200c281e88c9a8d333b97a91a9312e`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a499b89994d925373aa1c07042356f177f73e79529c729abc85a2d9026387978`  
		Last Modified: Fri, 15 May 2020 20:12:26 GMT  
		Size: 13.4 MB (13443197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebe8eefbafebdf9de25921d3569e5274c4f4c4ec253ce756dca0abe09e7d958`  
		Last Modified: Fri, 15 May 2020 20:12:22 GMT  
		Size: 2.4 KB (2395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597069368ef1ce225516b1597000747b3490cadcfc3becb2bc850de0bd68912a`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce39a5501878554bce3bd6fcbf89eeaa87e004ffe6b67bf73f3e9c00c3317733`  
		Last Modified: Fri, 15 May 2020 20:12:49 GMT  
		Size: 111.5 MB (111486682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d545bca14bf36c108e916a30ff7cf643598eaede713f8f9501cc33a2504e4a2`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f78cccacbe466367aebd7c0e56e64d6003540faef3330d81be303719a16ce`  
		Last Modified: Fri, 15 May 2020 20:12:20 GMT  
		Size: 5.1 KB (5135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:623a5dae2b423caebfc0c11a0ca38f221a20fd50733c56ebbb97953f1e43116e`  
		Last Modified: Fri, 15 May 2020 20:12:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
