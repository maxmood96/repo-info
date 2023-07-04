## `mysql:debian`

```console
$ docker pull mysql@sha256:7cade3f2720efda2be0e6184d8e050d1c3b9e84297e18d9a4566173afe41a031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:1db9b0e99314bae1b8285f369fff1291b8f911bfcbc0e93e3cf8e9aa2c884599
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179716041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5557a1823e3010b0b659f0f388f7fddd2df56326896370cf7a16767089753ae9`
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
# Tue, 04 Jul 2023 16:40:21 GMT
ENV MYSQL_VERSION=8.0.33-1debian11
# Tue, 04 Jul 2023 16:40:22 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 04 Jul 2023 16:40:37 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 04 Jul 2023 16:40:38 GMT
VOLUME [/var/lib/mysql]
# Tue, 04 Jul 2023 16:40:38 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 04 Jul 2023 16:40:38 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 04 Jul 2023 16:40:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 04 Jul 2023 16:40:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Jul 2023 16:40:38 GMT
EXPOSE 3306 33060
# Tue, 04 Jul 2023 16:40:39 GMT
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
	-	`sha256:91c8338bebc08fd94875a670c7a3fde461c905aee593ffa00fbe699f98e2fefb`  
		Last Modified: Tue, 04 Jul 2023 16:42:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001a9c226c59f3cfbef49ab0e01347aa3201d202440bfaa469ec84ca4393cf3b`  
		Last Modified: Tue, 04 Jul 2023 16:42:35 GMT  
		Size: 129.7 MB (129739240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74bd03e6832e22792ec6507355ca65899a59fb442587ab1b9a2b8ad310298017`  
		Last Modified: Tue, 04 Jul 2023 16:42:17 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20867e10013d172dbf130c2d282973c83dd13b3bba86a8fab429dff990e9b096`  
		Last Modified: Tue, 04 Jul 2023 16:42:17 GMT  
		Size: 5.4 KB (5386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d2995730ac54cb82ea8294ee1a56fedee0b3d817fa969ed1c998f40f9dd386`  
		Last Modified: Tue, 04 Jul 2023 16:42:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
