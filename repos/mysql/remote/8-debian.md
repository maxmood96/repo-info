## `mysql:8-debian`

```console
$ docker pull mysql@sha256:e83ca0235010bfdb321e6838db61bdcfcd75376e2ad7344b48f9e6274e439805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e54e01ca605ee64672bf588cd1782a669cb387954593ccd1c9dcd551598d1df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177773688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28218708df49341b2be096626a48460fdd27f50b16526c9198eca087bdfbee09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:30:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 12 Apr 2023 08:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:32 GMT
ENV GOSU_VERSION=1.16
# Wed, 12 Apr 2023 08:30:40 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 12 Apr 2023 08:30:41 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 12 Apr 2023 08:30:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 08:30:47 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 12 Apr 2023 08:30:47 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Wed, 12 Apr 2023 08:30:48 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Wed, 12 Apr 2023 08:31:02 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Wed, 12 Apr 2023 08:31:03 GMT
VOLUME [/var/lib/mysql]
# Wed, 12 Apr 2023 08:31:03 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Wed, 12 Apr 2023 08:31:03 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Wed, 12 Apr 2023 08:31:04 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 08:31:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 12 Apr 2023 08:31:04 GMT
EXPOSE 3306 33060
# Wed, 12 Apr 2023 08:31:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a04d5366306e8a589995f9f73ab93e6891f61c650a23925fb5b7390b6064595`  
		Last Modified: Wed, 12 Apr 2023 08:32:17 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba5474d63b96ac334caf465b6aa1a5de64b2013b2d04a1bfebfafff8f91fc38`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 4.4 MB (4415052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c021e7c8f4a7a4ce5520958fdb931906c4e230b830ed9b727f6cfdca9fb5869`  
		Last Modified: Wed, 12 Apr 2023 08:32:16 GMT  
		Size: 1.5 MB (1471552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3a9a62a81ba7372c6da71311f49a2bbdf341b2df76733730983af435b5103e`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02df4487ae5565f727156b1002cf5d23384f0b11f48e41459c11560fd112a5c`  
		Last Modified: Wed, 12 Apr 2023 08:32:18 GMT  
		Size: 12.7 MB (12662023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f9945ed239183eb77212dda7cc43cbcd8e45243e6170f8f35c607da06f841f7`  
		Last Modified: Wed, 12 Apr 2023 08:32:15 GMT  
		Size: 2.5 KB (2549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6089a839b76ce60e6835308ff44b5c5d5919e2afec303b4514e59f23a89321`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63f5a3e0cd76dff603c1470b1fddebbc741ffb0b44bf38ffb90a6f5e9583d10`  
		Last Modified: Wed, 12 Apr 2023 08:32:32 GMT  
		Size: 127.8 MB (127795797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe4fd79b488e38d5c4ea7a9f20adbd65a591adb7d90a44e49f7c8d749ce9aa`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3d9ed5bdeecafea3da68feb5f223f2ffec451cedc0fe1c99dc41618d32e398`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 5.4 KB (5389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a37d470a30b7376b79582f9254c94a5d90aed021707d4ad2ea38dc485ed277`  
		Last Modified: Wed, 12 Apr 2023 08:32:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
