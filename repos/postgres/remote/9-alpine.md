## `postgres:9-alpine`

```console
$ docker pull postgres@sha256:e87ff453511e9fb0256d130e570789c3d96d795198916d0021f293f820f39d1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `postgres:9-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:ecde67d70493d93748a687baf3268f6b85ce233fbab4cf76732903668f54e6b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 MB (14546921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f919dc044efe305034fc7115570f5925c31b922896c41bb83f39a4dc9d868b0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:44:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 03:44:32 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 03:44:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 04:12:22 GMT
ENV PG_MAJOR=9.6
# Thu, 15 Apr 2021 04:12:22 GMT
ENV PG_VERSION=9.6.21
# Thu, 15 Apr 2021 04:12:23 GMT
ENV PG_SHA256=930feaef28885c97ec40c26ab6221903751eeb625de92b22602706d7d47d1634
# Thu, 15 Apr 2021 04:15:23 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 04:15:24 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 04:15:25 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 04:15:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 04:15:27 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 04:15:27 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 04:15:27 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:15:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 04:15:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:15:29 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 04:15:29 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 04:15:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cb73039552ea36b22e7ea1fabf738b87f83b2c9347901ce77b79c790389bb7`  
		Last Modified: Thu, 15 Apr 2021 04:21:20 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39855706e49a3eeebf4c28a2ff3d706c5cdbe7bb1726d272188f08e91a46bfb8`  
		Last Modified: Thu, 15 Apr 2021 04:21:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22058ee3b26e2590c358ccfe3ebbe498165524f61d7258e4d03a99dd56b1795`  
		Last Modified: Thu, 15 Apr 2021 04:22:58 GMT  
		Size: 11.7 MB (11721484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed63bd9a265a0d38fecb9d1ae10c573e5bb537626bab14ef8cfc1392dd15a1d`  
		Last Modified: Thu, 15 Apr 2021 04:22:53 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c133afa1d76f43efc63f81223f41e2d0f2f087c0bdd137bcdff788af9c6941`  
		Last Modified: Thu, 15 Apr 2021 04:22:53 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be9cb2246cc70938d4712cb6a644fa774a668620a7d35cf306d606e4889895e5`  
		Last Modified: Thu, 15 Apr 2021 04:22:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97dbb7181aa99aa941fc84db0e06fc6d13133369f18b41047e50a909e36bd8b1`  
		Last Modified: Thu, 15 Apr 2021 04:22:53 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4ac968e21898472062eea6b1d595f3239554e1fc09c8836a63fcbb1c0f3724`  
		Last Modified: Thu, 15 Apr 2021 04:22:53 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:230577b96eb66fd27e7173774e901908571d5a9d3f4948a9bce3e667ab048d71
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13930625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf20e563c9f0b812b0cf8ef34779df9b13df5c55a60f58bbcb5ff9add8a90a07`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:39:44 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 02:39:45 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 02:39:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 03:03:54 GMT
ENV PG_MAJOR=9.6
# Thu, 15 Apr 2021 03:03:56 GMT
ENV PG_VERSION=9.6.21
# Thu, 15 Apr 2021 03:03:57 GMT
ENV PG_SHA256=930feaef28885c97ec40c26ab6221903751eeb625de92b22602706d7d47d1634
# Thu, 15 Apr 2021 03:06:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 03:06:34 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 03:06:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 03:06:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 03:06:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 03:06:41 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 03:06:42 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:06:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 03:06:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:06:48 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 03:06:49 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 03:06:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb015ae0de556d839b1cce178f0d7aac974efbf85f07dae41e1cb18f4704b7f2`  
		Last Modified: Thu, 15 Apr 2021 03:12:23 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce063f2d27607cdd3336512bf1e2cdeb8caa1488efded3002dcaf4c6c267a296`  
		Last Modified: Thu, 15 Apr 2021 03:12:23 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:458a326e4774321e126b88c343a9f9ac81cce245548a6288cfb6713973218e1f`  
		Last Modified: Thu, 15 Apr 2021 03:14:10 GMT  
		Size: 11.3 MB (11295023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b6af1265f5aa2c1d21d3b426aed99a2d8e5b58b15a5a5f911c388c49fecd22e`  
		Last Modified: Thu, 15 Apr 2021 03:14:03 GMT  
		Size: 7.2 KB (7161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980432ebe8387ffc2f5644f92775327f4b250aab9a93bd2594bfa4e0fb0a4b8e`  
		Last Modified: Thu, 15 Apr 2021 03:14:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063f015d92e8f18076110e913986a9b76ee891916d45255a505c0f4a7e44e2db`  
		Last Modified: Thu, 15 Apr 2021 03:14:03 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13a75d6b36686aafd0a991cb860626c676394fcc921b0dc07862ec2e27ed030`  
		Last Modified: Thu, 15 Apr 2021 03:14:03 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b0d4ed9f74011041bc9f645a8bffcb3f35259f93e9972e589c488cbd69768c`  
		Last Modified: Thu, 15 Apr 2021 03:14:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e8a50eb2ae409f761b1755e0843152e0d5621417551374a6a5b02f7b2b9ec765
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13079009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79fd0588200a2f0515b0a9072e8486a65edfe2ba2d8b5c7d4eca7c38ea06bf0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:39 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Wed, 14 Apr 2021 18:57:39 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:45:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 03:45:30 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 03:45:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 04:03:12 GMT
ENV PG_MAJOR=9.6
# Thu, 15 Apr 2021 04:03:13 GMT
ENV PG_VERSION=9.6.21
# Thu, 15 Apr 2021 04:03:15 GMT
ENV PG_SHA256=930feaef28885c97ec40c26ab6221903751eeb625de92b22602706d7d47d1634
# Thu, 15 Apr 2021 04:05:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 04:05:40 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 04:05:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 04:05:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 04:05:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 04:05:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 04:05:50 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:05:54 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 04:05:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:05:57 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 04:05:58 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 04:05:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d289031c7f8e86cc05ec575d7c122bc6d615e827ae76e96bca00fd9b0bba9dfb`  
		Last Modified: Thu, 15 Apr 2021 04:10:49 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b79752b7fbad651a271862e12e829d3ce7258cfa9386e5945f7c4232008d57`  
		Last Modified: Thu, 15 Apr 2021 04:10:49 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f95030768117145741b1fb97d693af217044cff3acfcf8388b81537d5bc9459`  
		Last Modified: Thu, 15 Apr 2021 04:12:32 GMT  
		Size: 10.6 MB (10641397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c292532581cfd8380682f374d7a70680e1ed868bf3bb475b853e71afbe79371`  
		Last Modified: Thu, 15 Apr 2021 04:12:31 GMT  
		Size: 7.2 KB (7161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1187ef3a466f26a8a460f37a8586b86929d0040c741cee28f84894f58b5c8cba`  
		Last Modified: Thu, 15 Apr 2021 04:12:29 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdf8eb92d43cfe5c0bd42bbb9482d99d642290531600deabb576ae532ea6f3e2`  
		Last Modified: Thu, 15 Apr 2021 04:12:28 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e72014c3aaef9f094404b7745d3f716bbd3daf37e22637a0fb6413cfab72598`  
		Last Modified: Thu, 15 Apr 2021 04:12:28 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d1f6bf762dc343470d939f795853efc271d3540dcc29cae4c033dddeb6c84b`  
		Last Modified: Thu, 15 Apr 2021 04:12:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:380b94009c8b544b424ed2c0c7470504f04192a6acc80f92a1918157b40601aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14259832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402f431e2831b1287a76a971e188cbf4f36fbfa39f0dd28017ed0516fe7a4e38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Mar 2021 17:21:21 GMT
ADD file:3b16ffee2b26d8af5db152fcc582aaccd9e1ec9e3343874e9969a205550fe07d in / 
# Wed, 31 Mar 2021 17:21:23 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 15:34:32 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 01 Apr 2021 15:34:33 GMT
ENV LANG=en_US.utf8
# Thu, 01 Apr 2021 15:34:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 01 Apr 2021 15:50:45 GMT
ENV PG_MAJOR=9.6
# Thu, 01 Apr 2021 15:50:45 GMT
ENV PG_VERSION=9.6.21
# Thu, 01 Apr 2021 15:50:46 GMT
ENV PG_SHA256=930feaef28885c97ec40c26ab6221903751eeb625de92b22602706d7d47d1634
# Thu, 01 Apr 2021 15:53:26 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 15:53:30 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 15:53:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 15:53:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 15:53:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 15:53:38 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 15:53:39 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 01 Apr 2021 15:53:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 01 Apr 2021 15:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 15:53:46 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 15:53:47 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 15:53:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:912815139b61c8926da31f7701f0a924e7964e3713052bf1a53193a4562157f6`  
		Last Modified: Wed, 31 Mar 2021 17:22:41 GMT  
		Size: 2.7 MB (2711920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4dca3142c84013c57ea8b52a2f4eaa1e53cdce28775ef34cbd2ddaa4a1cc05`  
		Last Modified: Thu, 01 Apr 2021 15:57:51 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f81a7d11e07a928a969377701dbc21b8602aac636b711973d628e633ecbe1a`  
		Last Modified: Thu, 01 Apr 2021 15:57:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5d613d89d288c48f8ed5ea6e1b0f3253660efd274629b3d6d2b7981c6419be`  
		Last Modified: Thu, 01 Apr 2021 15:59:34 GMT  
		Size: 11.5 MB (11534439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6661de22ea2f5880ca8cb54b7f173348dcf50bbbf7d9b8ed108f0604ec022ab`  
		Last Modified: Thu, 01 Apr 2021 15:59:29 GMT  
		Size: 7.2 KB (7162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47164bc15462c23b9c52e0c02bd2224048d4ea60abb69412e78cc4aa14c869f7`  
		Last Modified: Thu, 01 Apr 2021 15:59:29 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772d46525380693ed25e44535cc7496a7c2f53a90fffd33e4c0ce8e8782ae9bf`  
		Last Modified: Thu, 01 Apr 2021 15:59:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0abecd80ab844673945cb2ed2201238e8ec386a888b8a1c2c7da5a596a439e`  
		Last Modified: Thu, 01 Apr 2021 15:59:30 GMT  
		Size: 4.4 KB (4410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109083aeea24a78ccd8d1eb2c851135994cd2b2e4df48b0d0ec6fd8f2bac6494`  
		Last Modified: Thu, 01 Apr 2021 15:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; 386

```console
$ docker pull postgres@sha256:0ccd6b07e4d969f8a4cdba96a364868d5f15f3c5e379e684e757c5864ac0b1f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200076ccf5106deac57e546aeb2f5071ca01a8be7330357a11eeff9e6db46eb8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Mar 2021 17:43:00 GMT
ADD file:245767f958e2b5e6fad41d45d3361849e7c6b2255303e3c785f0f2c86019553a in / 
# Wed, 31 Mar 2021 17:43:00 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 05:30:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 01 Apr 2021 05:30:17 GMT
ENV LANG=en_US.utf8
# Thu, 01 Apr 2021 05:30:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 01 Apr 2021 05:56:02 GMT
ENV PG_MAJOR=9.6
# Thu, 01 Apr 2021 05:56:02 GMT
ENV PG_VERSION=9.6.21
# Thu, 01 Apr 2021 05:56:02 GMT
ENV PG_SHA256=930feaef28885c97ec40c26ab6221903751eeb625de92b22602706d7d47d1634
# Thu, 01 Apr 2021 05:59:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 05:59:40 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 05:59:41 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 05:59:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 05:59:42 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 05:59:42 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 05:59:42 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 01 Apr 2021 05:59:43 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 01 Apr 2021 05:59:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 05:59:43 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 05:59:44 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 05:59:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b22e590ebf70a9a5901c380b07232ef3c07cb13440402934dfdffb8f8721a949`  
		Last Modified: Wed, 31 Mar 2021 17:44:05 GMT  
		Size: 2.8 MB (2818802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a2b068c1bb76272b0315637db84ae4363b9ba40df2261e23d86c98af1424e7`  
		Last Modified: Thu, 01 Apr 2021 06:04:58 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd976245f3039bbee485288603aab3601719ac5fe74d0adad8c6a81dc749c662`  
		Last Modified: Thu, 01 Apr 2021 06:04:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1a14ae372bc51cc1189f748a4e8e7dcae2ac361fd010cdff9fab1993dd8095`  
		Last Modified: Thu, 01 Apr 2021 06:07:10 GMT  
		Size: 12.4 MB (12356373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b169f69774406503742b97a0ff029cda2e4d50cffda6b7117c2a11d6f80a84`  
		Last Modified: Thu, 01 Apr 2021 06:07:04 GMT  
		Size: 7.2 KB (7157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37727442944d2cafc62313d67736ab8b6226421b403d21b3bb4cc337cf5968ce`  
		Last Modified: Thu, 01 Apr 2021 06:07:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22a9eff9da1a9b0527d80976655deb74d7167f7208d6018a8b350dbed3141c5`  
		Last Modified: Thu, 01 Apr 2021 06:07:06 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda0f1ab17103dc6554e52ea291fedf506733bc2dba2ac2e5fee11cb262135d5`  
		Last Modified: Thu, 01 Apr 2021 06:07:06 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071239e89bfcc2ccfc3a4c2a43dc189226ddb19eddedc84a21d43c75066c9464`  
		Last Modified: Thu, 01 Apr 2021 06:07:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:f97b3c2d13d7e63339ec0ffe8e863b06317ff7bd1a71e3a14a296c7c98072796
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15558520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9da5690aa6f90ae16ddf6f1304a3103006fc9074fdef3d2cc5b31be07a38ca5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 31 Mar 2021 18:55:41 GMT
ADD file:1dd3315eb685a1b6729efb6f5b634e414f3da0f065078952bc6c0339dc09512d in / 
# Wed, 31 Mar 2021 18:55:49 GMT
CMD ["/bin/sh"]
# Thu, 01 Apr 2021 23:54:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 01 Apr 2021 23:54:51 GMT
ENV LANG=en_US.utf8
# Thu, 01 Apr 2021 23:55:10 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 02 Apr 2021 00:23:06 GMT
ENV PG_MAJOR=9.6
# Fri, 02 Apr 2021 00:23:11 GMT
ENV PG_VERSION=9.6.21
# Fri, 02 Apr 2021 00:23:19 GMT
ENV PG_SHA256=930feaef28885c97ec40c26ab6221903751eeb625de92b22602706d7d47d1634
# Fri, 02 Apr 2021 00:26:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 02 Apr 2021 00:26:57 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 02 Apr 2021 00:27:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 02 Apr 2021 00:27:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 02 Apr 2021 00:27:41 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 02 Apr 2021 00:27:54 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 02 Apr 2021 00:27:58 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Fri, 02 Apr 2021 00:28:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 02 Apr 2021 00:28:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Apr 2021 00:28:34 GMT
STOPSIGNAL SIGINT
# Fri, 02 Apr 2021 00:28:43 GMT
EXPOSE 5432
# Fri, 02 Apr 2021 00:28:49 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:dc4792b25345295bf964e1db1bceedb2338bfad8f0fb64f0cc07b152df9aef84`  
		Last Modified: Wed, 31 Mar 2021 18:57:19 GMT  
		Size: 2.8 MB (2813219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e2ee829b243db77878a7d15d4126a4e817b6216820082d82dfb11cc8756e45`  
		Last Modified: Fri, 02 Apr 2021 00:35:00 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d13418e7dceb873ab132346668dbf070e938bac34b9ec7f0ad08583ed7387b`  
		Last Modified: Fri, 02 Apr 2021 00:35:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b759c6a0d3873f3f591b3c90e90cdb2b15813f7cafe1254fbc271b2dcf2ef24c`  
		Last Modified: Fri, 02 Apr 2021 00:36:50 GMT  
		Size: 12.7 MB (12731831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624a5527d783f8c9d0a504a254dcde0caf67d80083601187fb2d8274649a5ee3`  
		Last Modified: Fri, 02 Apr 2021 00:36:44 GMT  
		Size: 7.2 KB (7155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e879745b1e8d1d835ad6de976b2eb3bbdf60a4043f8299ed061d3a94d69818`  
		Last Modified: Fri, 02 Apr 2021 00:36:44 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198535fe0ec8e875f5532bc44acbfdff94661adef837f932e196f8fbbaf02141`  
		Last Modified: Fri, 02 Apr 2021 00:36:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9af56132a5cbc43b0bee499858c4b16c059ccbad6edaea6f789944f6c33793`  
		Last Modified: Fri, 02 Apr 2021 00:36:46 GMT  
		Size: 4.4 KB (4409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9254b35a0c827f5f0b690336f0f8dcf10cfbf91fd0366bb69e6afe9b2c3b73`  
		Last Modified: Fri, 02 Apr 2021 00:36:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:854b0b788c6ab5d0c60922de8be63cf8f895b63dc6c6534cd9210547217c337e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14224496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96999c94f1ae32a4b55c91ec529a8dc13fd51b563a92c4e7ea079d7ee2248f71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 02:35:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 15 Apr 2021 02:35:26 GMT
ENV LANG=en_US.utf8
# Thu, 15 Apr 2021 02:35:27 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 15 Apr 2021 02:50:28 GMT
ENV PG_MAJOR=9.6
# Thu, 15 Apr 2021 02:50:29 GMT
ENV PG_VERSION=9.6.21
# Thu, 15 Apr 2021 02:50:29 GMT
ENV PG_SHA256=930feaef28885c97ec40c26ab6221903751eeb625de92b22602706d7d47d1634
# Thu, 15 Apr 2021 02:52:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:52:35 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:52:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:52:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:52:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:52:37 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:52:37 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:52:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 02:52:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:52:38 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:52:39 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:52:39 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f539beccb9c12dbbd5eb5238188d7421b0e766e3e536f47e5a25dce4187b138f`  
		Last Modified: Thu, 15 Apr 2021 02:55:28 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78639c932051e59362713e29f35ff376c4cd5627ea231422efbf7cf7b253ec7a`  
		Last Modified: Thu, 15 Apr 2021 02:55:28 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74278cf029449b55037da3fef8987f1e53a653afbff88ea4dca29943304076bf`  
		Last Modified: Thu, 15 Apr 2021 02:56:29 GMT  
		Size: 11.6 MB (11608379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc0b9a863e98c14918ccb64a93d6eb936ee2116d7017d434fd65f435b6109b2a`  
		Last Modified: Thu, 15 Apr 2021 02:56:26 GMT  
		Size: 7.2 KB (7160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422d515561d977cb6df6dac9d2cfe33e0f682d2d84f4cf8f7b60205c6b06ba2b`  
		Last Modified: Thu, 15 Apr 2021 02:56:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa3a8bfc6f8dab3f1bb66d23de27b5a5d9d3ef979497f3c5a1fdabf3d759423`  
		Last Modified: Thu, 15 Apr 2021 02:56:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f845d14345e6b0c70787cc711070cf41b2296afb4e4fa6c81b317d5ca73b9f68`  
		Last Modified: Thu, 15 Apr 2021 02:56:26 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8645cfd8aebdc3d232b7ce2fe0b05dc2aba2aad37de805cd19af7671c6bed262`  
		Last Modified: Thu, 15 Apr 2021 02:56:26 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
