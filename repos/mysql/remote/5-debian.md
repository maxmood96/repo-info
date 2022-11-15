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
