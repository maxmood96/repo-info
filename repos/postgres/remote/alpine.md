## `postgres:alpine`

```console
$ docker pull postgres@sha256:7e9d7316bdeed0179344e09a5a0b872a3d7ab40e17583ccf4449295c92c27c04
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

### `postgres:alpine` - linux; amd64

```console
$ docker pull postgres@sha256:3335d0494b62ae52f0c18a1e4176a83991c9d3727fe67d8b1907b569de2f6175
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62271088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e43172f9204f3f2ec21165200338d5d918a86e2984b2c75a36b18cffd9a948b4`
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
# Thu, 15 Apr 2021 03:44:33 GMT
ENV PG_MAJOR=13
# Thu, 15 Apr 2021 03:44:34 GMT
ENV PG_VERSION=13.2
# Thu, 15 Apr 2021 03:44:34 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Thu, 15 Apr 2021 03:52:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 03:52:03 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 03:52:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 03:52:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 03:52:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 03:52:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 03:52:08 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:52:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:52:08 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 03:52:09 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 03:52:09 GMT
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
	-	`sha256:74e3b91ca207933c4263573de4f7068728b71af3de813e333c4ee441044eb6a8`  
		Last Modified: Thu, 15 Apr 2021 04:21:28 GMT  
		Size: 59.4 MB (59444370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c8cceb594b920cea48c417e53be414df4a8c4cb4c835587e85efaa0f35eb34`  
		Last Modified: Thu, 15 Apr 2021 04:21:17 GMT  
		Size: 8.6 KB (8562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63418dfbd97fdcaeda2890ad4628843dbba44aa21aa4180714fa5c229a28e6f`  
		Last Modified: Thu, 15 Apr 2021 04:21:17 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8adc73d3af8212747784e0debf0aa5e0551399854bf502136435255b898baa`  
		Last Modified: Thu, 15 Apr 2021 04:21:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a2a57ca5f851230bf8485d6b6188f55a37412a0f720aa4d9f298d9ef69d3c7`  
		Last Modified: Thu, 15 Apr 2021 04:21:17 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5724c3217149590baadb9d982e4e1c30bfe0ff49fcd9c80e8506b55cae47c2b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60576006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5244fbe9f4369d67c445ce3a74891fc93f1f1bdb9bc77e43c0f75ac035fde57`
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
# Thu, 15 Apr 2021 02:39:50 GMT
ENV PG_MAJOR=13
# Thu, 15 Apr 2021 02:39:53 GMT
ENV PG_VERSION=13.2
# Thu, 15 Apr 2021 02:39:54 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Thu, 15 Apr 2021 02:44:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:44:41 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:45:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:45:26 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:46:36 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:46:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:47:10 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:47:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:47:21 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:47:30 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:47:38 GMT
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
	-	`sha256:1a9d8499b6e9e8c2c5ed995a2671811533ed393ce5e711ee31618ea293155c1e`  
		Last Modified: Thu, 15 Apr 2021 03:12:41 GMT  
		Size: 57.9 MB (57939118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00684a87abeabba407f80bd5340e365fd48173670f93c3187b608dbf068407c9`  
		Last Modified: Thu, 15 Apr 2021 03:12:21 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a6f7bf404f13903acbae2c14d0f4fd3385e0ebcd28027df62df3ad81320acb`  
		Last Modified: Thu, 15 Apr 2021 03:12:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bfa883a567f896d138578aa79bb5af169cdb785bd1d24046a559b42751c595`  
		Last Modified: Thu, 15 Apr 2021 03:12:21 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeed68755c947cf32af4be4c40762060adcf58dab2b9638b25f42c37f4ee8abc`  
		Last Modified: Thu, 15 Apr 2021 03:12:21 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:efb6dceb9a8262863b75146e5b29aa6b238b79b55bb275e3a6b6b2f0573fefd8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57608722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020e4d948fa9f2709e07fe8b9789f690bbe1ee21f55bfdbffdc49c85ba35b355`
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
# Thu, 15 Apr 2021 03:45:36 GMT
ENV PG_MAJOR=13
# Thu, 15 Apr 2021 03:45:38 GMT
ENV PG_VERSION=13.2
# Thu, 15 Apr 2021 03:45:39 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Thu, 15 Apr 2021 03:49:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 03:49:58 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 03:50:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 03:50:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 03:50:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 03:50:13 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 03:50:15 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:50:19 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 03:50:20 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 03:50:22 GMT
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
	-	`sha256:9a56ba0e3ceb3ef8455d3fb33d36f8a121aa607653fb47fe8df1e33ec86701f4`  
		Last Modified: Thu, 15 Apr 2021 04:11:03 GMT  
		Size: 55.2 MB (55169822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538a94b8e7debb4b462f058eaedf6c097700e9f7ae4e4ee33bd824dc786a160d`  
		Last Modified: Thu, 15 Apr 2021 04:10:47 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c230624ff515cd06b20372da44a1795ff536dc2c8fcd79db4d063a52335e88be`  
		Last Modified: Thu, 15 Apr 2021 04:10:47 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91137073100ed8efdd03ec8c5549ce41fcdd691dcc7304c81e92f0f934c19eef`  
		Last Modified: Thu, 15 Apr 2021 04:10:46 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d86f9e7eace98b46ddcccd4a660e3cb6de16ece5e0b3581c8fc4da724340800`  
		Last Modified: Thu, 15 Apr 2021 04:10:46 GMT  
		Size: 4.4 KB (4408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:aae89ba887088258b5d86f103aaa57dea8ee10add042f4c430ca02a586a0a3a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61543441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab06dfb53dcd23fa28ed1bd4894d70212de6434c9411112244061dea1b09d202`
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
# Thu, 01 Apr 2021 15:34:36 GMT
ENV PG_MAJOR=13
# Thu, 01 Apr 2021 15:34:37 GMT
ENV PG_VERSION=13.2
# Thu, 01 Apr 2021 15:34:37 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Thu, 01 Apr 2021 15:38:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 15:38:14 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 15:38:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 15:38:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 15:38:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 15:38:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 15:38:26 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 15:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 15:38:28 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 15:38:29 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 15:38:29 GMT
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
	-	`sha256:04461ab421a4a92273f650ce7aadcdc461966c3f9abe938426ec792db9bf5ab3`  
		Last Modified: Thu, 01 Apr 2021 15:58:04 GMT  
		Size: 58.8 MB (58816774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15d35193c33fe45816a927148befa9187f0cbcb8200157c18e50fd14430f1a6`  
		Last Modified: Thu, 01 Apr 2021 15:57:50 GMT  
		Size: 8.6 KB (8562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88d0ec0cffb1b4da838c286488721a019691ad58d73d5dc07ce679e58b61f4bf`  
		Last Modified: Thu, 01 Apr 2021 15:57:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9429e1f43f89838188b418537a8d852f53950e7cd9d0e2374eb62ac923734da6`  
		Last Modified: Thu, 01 Apr 2021 15:57:48 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379fbaf5bd325d6a2105ddb01e26924481b4b4135ed10094b373b88fc47bb844`  
		Last Modified: Thu, 01 Apr 2021 15:57:49 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; 386

```console
$ docker pull postgres@sha256:0e2aae69079b868dad8439364a62401e8896816472d41e40ddbaaaab6b8dc0e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65851892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31ca3ba54aa9b3d5abaa0b859336819f451a24729e091d93c8650f7aef91692`
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
# Thu, 01 Apr 2021 05:30:18 GMT
ENV PG_MAJOR=13
# Thu, 01 Apr 2021 05:30:18 GMT
ENV PG_VERSION=13.2
# Thu, 01 Apr 2021 05:30:18 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Thu, 01 Apr 2021 05:36:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 05:36:54 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 05:36:55 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 05:36:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 05:36:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 05:36:56 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 05:36:56 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 05:36:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 05:36:57 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 05:36:57 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 05:36:57 GMT
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
	-	`sha256:702137ed04b008e0ae3b9e1be4833c983e25e0ce6be1356b795145f55d89d3d1`  
		Last Modified: Thu, 01 Apr 2021 06:05:11 GMT  
		Size: 63.0 MB (63018344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e03a739c495ea77837cb8aac46280eaff0e153dfdd26d3c25a4b429f92a952`  
		Last Modified: Thu, 01 Apr 2021 06:04:56 GMT  
		Size: 8.6 KB (8564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4521a99e81c1d9166762d8fff1e034d2f3b4cb73540c1b373c192db8248513aa`  
		Last Modified: Thu, 01 Apr 2021 06:04:55 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d37c1109b6c886c643edc3d300116de3a96d8d3938f03bf05be5fe3858c8f4`  
		Last Modified: Thu, 01 Apr 2021 06:04:58 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb786bcef319cd4b10d9fcc334d5434ef597209a68ff1d4f572821ad80afbcd4`  
		Last Modified: Thu, 01 Apr 2021 06:04:56 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:7e50472c45ba248103827b90604629d38fa007711807547d3c34d2b522cf45ac
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64694239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e555d59effb2727f0b7260cb0357428a1139d60ae20220559f0631892231e57c`
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
# Thu, 01 Apr 2021 23:55:18 GMT
ENV PG_MAJOR=13
# Thu, 01 Apr 2021 23:55:23 GMT
ENV PG_VERSION=13.2
# Thu, 01 Apr 2021 23:55:32 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Fri, 02 Apr 2021 00:00:01 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 02 Apr 2021 00:00:40 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 02 Apr 2021 00:01:21 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 02 Apr 2021 00:01:29 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 02 Apr 2021 00:01:56 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 02 Apr 2021 00:02:06 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 02 Apr 2021 00:02:12 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 02 Apr 2021 00:02:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Apr 2021 00:02:35 GMT
STOPSIGNAL SIGINT
# Fri, 02 Apr 2021 00:02:43 GMT
EXPOSE 5432
# Fri, 02 Apr 2021 00:02:54 GMT
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
	-	`sha256:262ba91babd241346f9807acb666697b6089afa6a3cbc8b44a279e019da8a2c0`  
		Last Modified: Fri, 02 Apr 2021 00:35:07 GMT  
		Size: 61.9 MB (61866269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e65a451c704137b1ec415136b050f5403564b15dc15ac38a098b0be9dea6ce9`  
		Last Modified: Fri, 02 Apr 2021 00:34:53 GMT  
		Size: 8.6 KB (8564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cf2dcc928062f6c009661f9f972dbca7eabaf710558e3a39d5e55180b4ef7a`  
		Last Modified: Fri, 02 Apr 2021 00:34:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec60c1643b9fa0dcc720bb924bbf84f9c8f4efe1c28274b3f1b6d3de066c4dcc`  
		Last Modified: Fri, 02 Apr 2021 00:34:53 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b6fd4f0793f073ad3c543c7aec64a5ba40965344c870822107e39bec0e6194d`  
		Last Modified: Fri, 02 Apr 2021 00:34:54 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; s390x

```console
$ docker pull postgres@sha256:53c93fa77f8cdcfe6225b07f2ce4f5dc03b7325cadd9193ece8321e3dcda2357
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65021080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47539d4eb660826b58fc15a75e28732979a0deaebc74eb9ba05dfc2f12347b9`
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
# Thu, 15 Apr 2021 02:35:27 GMT
ENV PG_MAJOR=13
# Thu, 15 Apr 2021 02:35:28 GMT
ENV PG_VERSION=13.2
# Thu, 15 Apr 2021 02:35:28 GMT
ENV PG_SHA256=5fd7fcd08db86f5b2aed28fcfaf9ae0aca8e9428561ac547764c2a2b0f41adfc
# Thu, 15 Apr 2021 02:39:07 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:39:10 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:39:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:39:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:39:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:39:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:39:12 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:39:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:39:13 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:39:13 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:39:13 GMT
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
	-	`sha256:8881001efd9e26d59df540c8bf660be9a51bf8dc52ddd7434c13b3b6db5f38bd`  
		Last Modified: Thu, 15 Apr 2021 02:55:34 GMT  
		Size: 62.4 MB (62403684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3606bd65cbbe39ae39be8a4ffce2ca69fa6ea7cfb25c4b5af66c4ca6db081e1f`  
		Last Modified: Thu, 15 Apr 2021 02:55:26 GMT  
		Size: 8.6 KB (8561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b902d00923a34c4468e4a845f223f86a8dd04fb373ab043a1a452b24e38ea0`  
		Last Modified: Thu, 15 Apr 2021 02:55:26 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5573da465d50870ecac670ceffa656dbbdca753a68f0fa655ca78dbdc3295137`  
		Last Modified: Thu, 15 Apr 2021 02:55:26 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb50772e74ec79de1c9331578fe5084abda795e3028e5d7e9d7db67558f2c8`  
		Last Modified: Thu, 15 Apr 2021 02:55:26 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
