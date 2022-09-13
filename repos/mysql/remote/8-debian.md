## `mysql:8-debian`

```console
$ docker pull mysql@sha256:9e0bdb3b54035e8deb547fd0291b21762c86669bd48f5b4819c079c94c425816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:2506c5888811a468d1bb01f18ef37a7a13847122c7e48e9ad1ba013b9b8c52fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157873370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119434801ff2d09c0f7cc72bff23e5876109309b189302c59b40d38ec736f245`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 13:28:37 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 13 Sep 2022 13:28:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:42 GMT
ENV GOSU_VERSION=1.14
# Tue, 13 Sep 2022 13:28:50 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 13 Sep 2022 13:28:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 13 Sep 2022 13:28:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 13:28:58 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 13 Sep 2022 13:28:58 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 13 Sep 2022 13:28:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 13 Sep 2022 13:29:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 13 Sep 2022 13:29:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 13 Sep 2022 13:29:13 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 13 Sep 2022 13:29:14 GMT
COPY file:5e84598933ec95c9918378d8dde5be8d5f80b0e1fc321a029f840f313201ebce in /usr/local/bin/ 
# Tue, 13 Sep 2022 13:29:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 13 Sep 2022 13:29:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Sep 2022 13:29:14 GMT
EXPOSE 3306 33060
# Tue, 13 Sep 2022 13:29:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c5efc42d0a2eac340f0b7f83239cdd89743a262660794b6b4125048bf6d67`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6acb3aa78cebf34a1c1dcac56576d08c293736a9e5d2af49d4abcf74717eb936`  
		Last Modified: Tue, 13 Sep 2022 13:30:39 GMT  
		Size: 4.4 MB (4414806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3edf2bce1ded759b2621e3f9b6d08c0aaa774b41d0a75644723e75c18333f5`  
		Last Modified: Tue, 13 Sep 2022 13:30:37 GMT  
		Size: 1.4 MB (1418436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e9b048283778fc1730490adba5e9108c9d2be7ec217bca6d2aae6147a5409c`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef175ef2e26b0a73ffc1e4139460ac9857413163333b0b48cd4ebae090a6c23`  
		Last Modified: Tue, 13 Sep 2022 13:30:38 GMT  
		Size: 12.7 MB (12661855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2805f7502c031da7089f62f19829407ae4d4e28609461b6c797d8e8c6469b651`  
		Last Modified: Tue, 13 Sep 2022 13:30:35 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf7ff40073185d68c0e971013dadecaec0807d064de3ea39c696ff1522aa336`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60dfbd1dbaeca6ed4bb7011a37155a4b41169b2ac8b51190a2eeb3117edf624`  
		Last Modified: Tue, 13 Sep 2022 13:30:50 GMT  
		Size: 108.0 MB (107963119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:893b8ebac2e8391238177c2f59bb38c87d62578f4105192dfdd480c575fba1e3`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c758363844a5d6c01628e945d14648ae844cb9d4a75f6d162557b372d626730`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 5.4 KB (5385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9663382eaa47c2752415ea0b14d4ad4fe670882ad23493f48d5434a83ed9276c`  
		Last Modified: Tue, 13 Sep 2022 13:30:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
