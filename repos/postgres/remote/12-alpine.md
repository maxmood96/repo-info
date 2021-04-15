## `postgres:12-alpine`

```console
$ docker pull postgres@sha256:f95a8d36ffab00a2113d0e607b2a3d928aacd59f6cd61b0d7c9b6fc265458341
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

### `postgres:12-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:faf54a67a58ecf4d21e3e68b9a3b33f81a11e8a786530044c4ee80d51b148e05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61612755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc493ea5711b2b577de577e5c9073e3ce46458cc3ce377a238e5c16d75d5fc68`
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
# Thu, 15 Apr 2021 03:52:19 GMT
ENV PG_MAJOR=12
# Thu, 15 Apr 2021 03:52:19 GMT
ENV PG_VERSION=12.6
# Thu, 15 Apr 2021 03:52:19 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 15 Apr 2021 03:58:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 03:58:59 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 03:59:01 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 03:59:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 03:59:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 03:59:04 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 03:59:04 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:59:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:59:05 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 03:59:05 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 03:59:06 GMT
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
	-	`sha256:d20618766abceaed37866a438aaae27cf8c078ebe48ab8b344c431f897fb0fca`  
		Last Modified: Thu, 15 Apr 2021 04:21:56 GMT  
		Size: 58.8 MB (58786355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae1c0be05666280b920b09e0001229ebfd3020441fff0bd84ee430548147589`  
		Last Modified: Thu, 15 Apr 2021 04:21:44 GMT  
		Size: 8.2 KB (8245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a4454a31c09e13caa1763a82a1eee1dc53e4c006486240e48079483ae2a83f`  
		Last Modified: Thu, 15 Apr 2021 04:21:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eac2512a47368d299f00a03bceafbda50ee334d9edcbf7055480eb3e7126651`  
		Last Modified: Thu, 15 Apr 2021 04:21:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f832862b0135118555545789a45b2d1086cb6ea4d9f1fa0bb131de9c95e756`  
		Last Modified: Thu, 15 Apr 2021 04:21:44 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:7188338fdd4ce5f79867a5dffb41d5086355577796b2c91620b078d989953c22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59991013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccccdee61f87be71e2d11c62fe86391b016192ab0dde09ecd17d952232d2470`
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
# Thu, 15 Apr 2021 02:47:59 GMT
ENV PG_MAJOR=12
# Thu, 15 Apr 2021 02:48:00 GMT
ENV PG_VERSION=12.6
# Thu, 15 Apr 2021 02:48:02 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 15 Apr 2021 02:52:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:52:35 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:52:38 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:52:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:52:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:52:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:52:47 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:52:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:52:49 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:52:50 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:52:51 GMT
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
	-	`sha256:12f70915ba72f88cb46b8cb8f1aae20fcb1fc00643bd5ea369f96c6d8acb5271`  
		Last Modified: Thu, 15 Apr 2021 03:13:07 GMT  
		Size: 57.4 MB (57354452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f373f77db9aba064999ea35440c359b6cd093c344a7878ec59c33464744582f9`  
		Last Modified: Thu, 15 Apr 2021 03:12:51 GMT  
		Size: 8.2 KB (8242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc1979b1f58ea455ac7182836ccd6a414c8040102d9b35165d4549241592abe`  
		Last Modified: Thu, 15 Apr 2021 03:12:52 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f828e659ffd74cd634f69841b8cbce8191f2e0738e4fdd0e5d240188c4ffd1`  
		Last Modified: Thu, 15 Apr 2021 03:12:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7543842ea611ad8d8882d435523c13021b8b953afc13178f95e5e8604ec896f8`  
		Last Modified: Thu, 15 Apr 2021 03:12:52 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:828344f6b7ee4a05cfd42a12bfe13a40549df9a2c5578a6ca58b140d43ebcd7a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57041655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffec5a7a7c6ba0ae33eb27077be8f7db3fc53b290d8601b1df99f2efa0ab20ec`
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
# Thu, 15 Apr 2021 03:50:36 GMT
ENV PG_MAJOR=12
# Thu, 15 Apr 2021 03:50:37 GMT
ENV PG_VERSION=12.6
# Thu, 15 Apr 2021 03:50:37 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 15 Apr 2021 03:53:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 03:53:52 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 03:53:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 03:53:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 03:53:59 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 03:54:00 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 03:54:02 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:54:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:54:05 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 03:54:09 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 03:54:11 GMT
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
	-	`sha256:2d04a177f8ec8cf2f360d9f21f9393c5139e7d6cd38d41ac9c37ca015ccec0da`  
		Last Modified: Thu, 15 Apr 2021 04:11:29 GMT  
		Size: 54.6 MB (54603079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b256a492c102efa5d6ca8030adacd1359876fc8cc7e072fdbb06a53b281da32`  
		Last Modified: Thu, 15 Apr 2021 04:11:13 GMT  
		Size: 8.2 KB (8245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75de1c8edaf9de9f3323d8943083b36e617261d25ec9abc9377960c74dfe2ae9`  
		Last Modified: Thu, 15 Apr 2021 04:11:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a548ceaa22842453e287e9741a809f0c40807aa3242b7a24bcf5fccecf1513`  
		Last Modified: Thu, 15 Apr 2021 04:11:13 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ffe68aa7381fe88d6e540b912572adb564fa579c0b70f31eda0a7d56597459`  
		Last Modified: Thu, 15 Apr 2021 04:11:13 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:ebeb1f885ed3543e9d5569ae00c53619266f7aa3be7e984233ea642e19081c59
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60924398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00667eedffe8815eeadf1adc5e72bd0fe59754e49ac56d992dee5a224a3ed7d`
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
# Thu, 01 Apr 2021 15:38:42 GMT
ENV PG_MAJOR=12
# Thu, 01 Apr 2021 15:38:42 GMT
ENV PG_VERSION=12.6
# Thu, 01 Apr 2021 15:38:43 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 01 Apr 2021 15:42:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 15:42:12 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 15:42:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 15:42:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 15:42:22 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 15:42:23 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 15:42:24 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 15:42:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 15:42:26 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 15:42:27 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 15:42:28 GMT
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
	-	`sha256:d0be9c550d4a3074434e37acff8e07973685ab3dea88a4a5c0b39b8eeb7e8bd6`  
		Last Modified: Thu, 01 Apr 2021 15:58:33 GMT  
		Size: 58.2 MB (58198054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8f89c26208574d698cfb07c47c7dadd91988da05c4a2d8666a4e54d0d86f21`  
		Last Modified: Thu, 01 Apr 2021 15:58:20 GMT  
		Size: 8.2 KB (8240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eef5a8be705481bb9f0cf032abaf6dc3284f2f55d47a6cb9dcfca8e67d5e4a`  
		Last Modified: Thu, 01 Apr 2021 15:58:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2adcf61ebf5e4ca4a02a6c2f8c00f8fe5f79c7b1c55df26a8e1753984dfa27c`  
		Last Modified: Thu, 01 Apr 2021 15:58:20 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba281175e19d23f48c336d403a69b36d5e369fd2949e348e5ca362c71c52b2d`  
		Last Modified: Thu, 01 Apr 2021 15:58:20 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; 386

```console
$ docker pull postgres@sha256:a2cb754b9b8497bf57920c84debf6a5a2f7c9513cee515780cda737979d94bef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65159937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f3043423ef39ab492b521742e841c00f6b621a869960b2c3ac65f827f61d08`
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
# Thu, 01 Apr 2021 05:37:22 GMT
ENV PG_MAJOR=12
# Thu, 01 Apr 2021 05:37:22 GMT
ENV PG_VERSION=12.6
# Thu, 01 Apr 2021 05:37:23 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 01 Apr 2021 05:44:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 05:44:01 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 05:44:02 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 05:44:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 05:44:04 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 05:44:04 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 05:44:04 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 05:44:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 05:44:05 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 05:44:05 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 05:44:05 GMT
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
	-	`sha256:6edc450a1ef6f349045e9f7db050d3f6ceb137827becd387ec7e9c2d9086159c`  
		Last Modified: Thu, 01 Apr 2021 06:05:45 GMT  
		Size: 62.3 MB (62326714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28332642d01efbdbf42b736719d1738915d68ab89657cd346def0c377987e743`  
		Last Modified: Thu, 01 Apr 2021 06:05:33 GMT  
		Size: 8.2 KB (8236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f6d0c96beb4c9d0d497facef0a78fc40d0aa15eb3f27a6f489c37f5c3094a7`  
		Last Modified: Thu, 01 Apr 2021 06:05:33 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197256130fba98a9d8be3f96ad43be669fc2b25caf2ee956bde9757af9643efc`  
		Last Modified: Thu, 01 Apr 2021 06:05:33 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72c3b149c9784cb89c5d6d1b9ceab5317cb72fc0d328141df48345364f147791`  
		Last Modified: Thu, 01 Apr 2021 06:05:33 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:67849e2221e6d9f4cfef6aea7b6c3da30fd434b9602b041f2d476b606eefa9d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a92be76da60ac9874e65f1399eb86e421cbd8bc2c11a6c6b21b99e2100daf2`
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
# Fri, 02 Apr 2021 00:03:23 GMT
ENV PG_MAJOR=12
# Fri, 02 Apr 2021 00:03:30 GMT
ENV PG_VERSION=12.6
# Fri, 02 Apr 2021 00:03:40 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Fri, 02 Apr 2021 00:08:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 02 Apr 2021 00:08:30 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 02 Apr 2021 00:09:01 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 02 Apr 2021 00:09:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 02 Apr 2021 00:09:48 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 02 Apr 2021 00:09:55 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 02 Apr 2021 00:09:59 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 02 Apr 2021 00:10:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Apr 2021 00:10:21 GMT
STOPSIGNAL SIGINT
# Fri, 02 Apr 2021 00:10:28 GMT
EXPOSE 5432
# Fri, 02 Apr 2021 00:10:38 GMT
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
	-	`sha256:d398809c1007a38b362579a2cfb39db1055e257cbdd39269f769a8707e748336`  
		Last Modified: Fri, 02 Apr 2021 00:35:37 GMT  
		Size: 61.2 MB (61172184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d6d71cec7ba75187cb4ac03cd27e9d9f06ea5a25b9cdfb412de34a0761998a`  
		Last Modified: Fri, 02 Apr 2021 00:35:24 GMT  
		Size: 8.2 KB (8238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ce2b58e7d030d58d5eee18db7ef05655a60d222e10522e527cc9d042abdf31`  
		Last Modified: Fri, 02 Apr 2021 00:35:24 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae709a4309a336d8b77f1d031398e94f8adb88142f77d0531fc4d76c92d6cd3`  
		Last Modified: Fri, 02 Apr 2021 00:35:24 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13eaf99cd56f7b09bf01171a259415c9b7f81343e579f9a266b1ccb80bb755fe`  
		Last Modified: Fri, 02 Apr 2021 00:35:24 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:a37cf0142d4c2f19e450b549058a60705c2a5ec5fcbe31bb9aaf83951c67c25e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64236304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b043a78d91e237dd9a343aa3feb8168ba05a09089880dda130852949fe11b275`
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
# Thu, 15 Apr 2021 02:39:22 GMT
ENV PG_MAJOR=12
# Thu, 15 Apr 2021 02:39:23 GMT
ENV PG_VERSION=12.6
# Thu, 15 Apr 2021 02:39:23 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 15 Apr 2021 02:43:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:43:12 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:43:13 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:43:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:43:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:43:14 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:43:14 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:43:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:43:15 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:43:15 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:43:15 GMT
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
	-	`sha256:e7ae9a5b11e5aa3dc815e6e30d69da17a903209e4c874864c65540ccca04be65`  
		Last Modified: Thu, 15 Apr 2021 02:55:51 GMT  
		Size: 61.6 MB (61619236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad60a4ec65380c2b7f2729e282ceb12d5c3b8067af54663c9678bcddcf54f00`  
		Last Modified: Thu, 15 Apr 2021 02:55:43 GMT  
		Size: 8.2 KB (8236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba4ad182707f80f62367b5151e561d5995d94edaa428362d31fb4559f2b05d3`  
		Last Modified: Thu, 15 Apr 2021 02:55:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a529480521cc68884c477f9fab74c075becb0b06b91edfb15f1a100a4ef492b5`  
		Last Modified: Thu, 15 Apr 2021 02:55:44 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00e1191132ad69c4118b8bccf54a5bf551f66390f830bed417bc261b030e40d`  
		Last Modified: Thu, 15 Apr 2021 02:55:43 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
