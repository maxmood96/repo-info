## `mysql:8-debian`

```console
$ docker pull mysql@sha256:548da4c67fd8a71908f17c308b8ddb098acf5191d3d7694e56801c6a8b2072cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0c0beeac7ca1937d60f54e1fb0c4a5c0b0ffee2aae37488fbc9f5ea301425551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155884977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b636d5542b73254ce90cc4b895597dc1adc2c661ca553c38eda159979dded1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Sat, 28 May 2022 01:20:43 GMT
ADD file:0513eda9512e010cb9459591b62e0c9d9319750923df091b64250ad6e98c2878 in / 
# Sat, 28 May 2022 01:20:43 GMT
CMD ["bash"]
# Sat, 28 May 2022 05:33:08 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Sat, 28 May 2022 05:33:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:14 GMT
ENV GOSU_VERSION=1.14
# Sat, 28 May 2022 05:33:23 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Sat, 28 May 2022 05:33:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 28 May 2022 05:33:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 05:33:31 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Sat, 28 May 2022 05:33:31 GMT
ENV MYSQL_MAJOR=8.0
# Sat, 28 May 2022 05:33:32 GMT
ENV MYSQL_VERSION=8.0.29-1debian10
# Sat, 28 May 2022 05:33:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Sat, 28 May 2022 05:33:46 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Sat, 28 May 2022 05:33:47 GMT
VOLUME [/var/lib/mysql]
# Sat, 28 May 2022 05:33:47 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Sat, 28 May 2022 05:33:47 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Sat, 28 May 2022 05:33:48 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 28 May 2022 05:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 28 May 2022 05:33:48 GMT
EXPOSE 3306 33060
# Sat, 28 May 2022 05:33:48 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c1ad9731b2c7bf7fddea67f2f3f553515179a375c489e591e2372700fcaca766`  
		Last Modified: Sat, 28 May 2022 01:26:05 GMT  
		Size: 27.1 MB (27140144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f6eb0ee84d0c793cbd8456f03775cc5d88f72c576ec455596dca4ad465df07`  
		Last Modified: Sat, 28 May 2022 05:34:47 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cffcf8691bc5ddfc0c45d837fef9c77c7e264f7a69faf37073d0c4b31fb87156`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 4.2 MB (4179298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a783b5ac8a82c6355c62896648cb37efdc387f41b31b5c1d09418ce1808e81`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 1.4 MB (1386680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8393c7be5fa5ff5d50fba15ce47f16cb29d3363d3885632e7892c0854a4d9c`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af768d0b181edf1d8a35699d64f8e71d05d7648a28c37a5ab6fe2e36ffddc5e0`  
		Last Modified: Sat, 28 May 2022 05:34:48 GMT  
		Size: 14.1 MB (14064399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d6aaaf54a9c0c9d817fd1615f43aaf0194bcc1fca1574a90e90d8f6d66c6a`  
		Last Modified: Sat, 28 May 2022 05:34:45 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e014a8ae4c97230ff31778e48cc8801fe3d3b141b8e0a878270d1e2ddc4b4f3`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a821425a33418d8b2e6373a86d9bdca37a6a4d7315ca23302665c2556269fd64`  
		Last Modified: Sat, 28 May 2022 05:35:00 GMT  
		Size: 109.1 MB (109103661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a10c2652132a5609dcf19779c0bebde64ef5f5d9e7d8a50f3127c274d56c894`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4419638feac46fa0870175acf37fdb6aea243ba43de9dea79a31fc9afbff395b`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 5.2 KB (5152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681aeed97dfe0d4bc23a8411287a322f495b790026a8b476b956f90355c9aae0`  
		Last Modified: Sat, 28 May 2022 05:34:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
