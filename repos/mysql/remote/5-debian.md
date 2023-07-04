## `mysql:5-debian`

```console
$ docker pull mysql@sha256:c0a0e68b9bc8d6cebdbdef8a6e769df5502a361f9190be694bd84e4035fecfb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9f266e88e9418d3e290303eeff93b2b0b1091e48979dda1407168716e8e00aae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162760797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d7c63fe3391e41709423d7663a381baea7ee5ca33a923a0a4768009cc45a44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:47 GMT
ADD file:ca4076bfffab8d09636384070ca253570590554cff76a132afaae5cd89b363b5 in / 
# Tue, 04 Jul 2023 01:20:48 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:40:44 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Jul 2023 16:40:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:40:49 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 16:40:58 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 16:40:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 16:41:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:41:05 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 16:41:05 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 04 Jul 2023 16:41:05 GMT
ENV MYSQL_VERSION=5.7.42-1debian10
# Tue, 04 Jul 2023 16:41:06 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 04 Jul 2023 16:41:24 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 04 Jul 2023 16:41:24 GMT
VOLUME [/var/lib/mysql]
# Tue, 04 Jul 2023 16:41:24 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 04 Jul 2023 16:41:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 16:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 16:41:25 GMT
EXPOSE 3306 33060
# Tue, 04 Jul 2023 16:41:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:90ac1ecaf92c8ae0cb37d29d8cc01b5802612c12edb933c369ad4c586ea94c6c`  
		Last Modified: Tue, 04 Jul 2023 01:26:21 GMT  
		Size: 27.1 MB (27138502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5332fa444fcbc9427056611d173b59e9fb27193696d2caff0ce93902012bf2c`  
		Last Modified: Tue, 04 Jul 2023 16:42:55 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df99bbd075464fe4c45ccfb06b4f3261dcb494b081d2bf090ed8bdb72c6f273`  
		Last Modified: Tue, 04 Jul 2023 16:42:54 GMT  
		Size: 4.2 MB (4182356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1074e6f5cec3a9ad3219a0bf1b7c4d342e68b9311b347a3c0bbdb9b519f104f6`  
		Last Modified: Tue, 04 Jul 2023 16:42:53 GMT  
		Size: 1.4 MB (1441848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bbcb49a75325f17e87e7366fd5499c77bd750fd0a563ecf4fa330598b567ad`  
		Last Modified: Tue, 04 Jul 2023 16:42:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b88e8cde452e8be99b1b7b0e95df9f144877dd3f6a5a751d8d84b5bf98172d`  
		Last Modified: Tue, 04 Jul 2023 16:42:56 GMT  
		Size: 14.1 MB (14089552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd01f08045baa85450d1a60acdb8043f3822f8f08fbc23a6427b43e0d31907b1`  
		Last Modified: Tue, 04 Jul 2023 16:42:51 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6ca6adc2aaa205cfce0083344463b5b459968a0894526ecac3305a1eac1830`  
		Last Modified: Tue, 04 Jul 2023 16:42:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57f7cb4781685a978155f98f294792b9c1eaa227c7a22edf025b79e3a5ba5c2`  
		Last Modified: Tue, 04 Jul 2023 16:43:05 GMT  
		Size: 115.9 MB (115898351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d80f44b4d6a403257ac7dfb82cf09de4952b0ce1723f75732a045ba5c92556`  
		Last Modified: Tue, 04 Jul 2023 16:42:51 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2a073f32ef118e7b46e8ff821eb2b0b0a56eb101918cda05b274f0ad3caf49`  
		Last Modified: Tue, 04 Jul 2023 16:42:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
