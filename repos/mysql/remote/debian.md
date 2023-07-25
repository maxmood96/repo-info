## `mysql:debian`

```console
$ docker pull mysql@sha256:e0d273da8349eaa4eb56c9581239aa3a7a652ad16dab3057a875bfd3f884b4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:bfda5f8532c03cbf9c7d9e1c9ab5099b4b03f7cc345fb5a3db9771c48c7c45a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179508913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b746d14d1a955938b5a739381210993616e020e85557679b5878e99fec8fc7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 16:40:01 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 04 Jul 2023 16:40:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:40:06 GMT
ENV GOSU_VERSION=1.16
# Tue, 04 Jul 2023 16:40:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 04 Jul 2023 16:40:14 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 04 Jul 2023 16:40:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 16:40:21 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 04 Jul 2023 16:40:21 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 25 Jul 2023 01:38:57 GMT
ENV MYSQL_VERSION=8.0.34-1debian11
# Tue, 25 Jul 2023 01:38:58 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 25 Jul 2023 01:39:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 25 Jul 2023 01:39:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 25 Jul 2023 01:39:14 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 25 Jul 2023 01:39:15 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 25 Jul 2023 01:39:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 25 Jul 2023 01:39:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Jul 2023 01:39:15 GMT
EXPOSE 3306 33060
# Tue, 25 Jul 2023 01:39:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b694d81657a2feaabf9dd99971bd263fcf6e6365a9088a19fa255cbbbd3bb5`  
		Last Modified: Tue, 04 Jul 2023 16:42:21 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c16d5c24c0e588a5ced581dcb0b12a2608480f00d8c9ac214a45b463632263a6`  
		Last Modified: Tue, 04 Jul 2023 16:42:22 GMT  
		Size: 4.4 MB (4415050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c78718e67739ad983a38d623f4bc0f8c5c712b57384f4a852b04c48f87d30c1`  
		Last Modified: Tue, 04 Jul 2023 16:42:20 GMT  
		Size: 1.5 MB (1471510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf8c2abf7d7e75cca7b9d6dd26a939bc3568604779a0e31bf9d077f244d1282`  
		Last Modified: Tue, 04 Jul 2023 16:42:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96b9824aacf27d6bf0a547ca61f950cf76367b65e8857a3a35db10d11ac064d`  
		Last Modified: Tue, 04 Jul 2023 16:42:22 GMT  
		Size: 12.7 MB (12661822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab06d32a3885f91fb15d03b06b1810f1dca279106872eda0260a50f3d204e27b`  
		Last Modified: Tue, 04 Jul 2023 16:42:19 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae2d5d8ae814fa58b139f40a7504dbc46e20d71a6dc71a21d8acef81d538db0`  
		Last Modified: Tue, 25 Jul 2023 01:41:00 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce73b08b33f23db94c267e98f63f3ef1df28f3ffb17e3785ccb191d64046eda`  
		Last Modified: Tue, 25 Jul 2023 01:41:18 GMT  
		Size: 129.5 MB (129532101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2e4e9baaf2b2fad7f792dc2cd34e94492bb600e119a4eb24553df070f0a35a`  
		Last Modified: Tue, 25 Jul 2023 01:41:00 GMT  
		Size: 846.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c856433c0e516be6d11e8ff33e2890b081b2fe4065f410c4b4b7f32f86214da`  
		Last Modified: Tue, 25 Jul 2023 01:41:00 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969c57b7601c7031884ac6204e6ceb6d9626bb34fb2dc114b8615806dfb3ff82`  
		Last Modified: Tue, 25 Jul 2023 01:41:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
