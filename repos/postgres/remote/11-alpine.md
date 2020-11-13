## `postgres:11-alpine`

```console
$ docker pull postgres@sha256:f4d9b01d9ce0f501b8361cf370770b9eb561eb2829dad3c325e339a6b9d48069
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

### `postgres:11-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:eee4444474afacff2b9d12e8f636c3b08f665e138c94a65484704e2f73aba798
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61df677592b3859a1957657f896792bc6fb062faa03b43d4fbb7a57b6d6c16e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:55:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 07:55:14 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 07:55:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 08:06:44 GMT
ENV PG_MAJOR=11
# Fri, 13 Nov 2020 02:35:49 GMT
ENV PG_VERSION=11.10
# Fri, 13 Nov 2020 02:35:49 GMT
ENV PG_SHA256=13e6d2f80662fe463bc7718cdf0de6a9ec67fc78afcc7a3ae66b9ea19bb97899
# Fri, 13 Nov 2020 02:41:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:41:33 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:41:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:41:35 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:41:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:41:37 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:41:37 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:41:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Nov 2020 02:41:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:41:41 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:41:43 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:41:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f1d1b70e7fa650fd6229086120f763219adce9e33e8b20bdfbf8452ab69847`  
		Last Modified: Thu, 22 Oct 2020 08:21:53 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4f01476d2b86761cdb0414c4a583b89af3b5d0b67022cfc0d378743307f7e3`  
		Last Modified: Thu, 22 Oct 2020 08:21:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26efaa0f51b7c93995a862f2e4aeb979c6c66d93ad816bf0244d8f092465bbd4`  
		Last Modified: Fri, 13 Nov 2020 03:02:36 GMT  
		Size: 57.5 MB (57478447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e42c6cc447317ad050b6740972baac741faf753896c3f4946d8cf91e94b8a04`  
		Last Modified: Fri, 13 Nov 2020 03:02:22 GMT  
		Size: 7.6 KB (7570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67ca0e3d5a37287bbe622cc273a0db91b0e3eb74e4b97f18d8382d49f437af3`  
		Last Modified: Fri, 13 Nov 2020 03:02:22 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6870e165868cf625dfb97ca694ecb9bb4238b9989350e41200bf7d64af6e6e13`  
		Last Modified: Fri, 13 Nov 2020 03:02:21 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25664bc9a7fe0b8d066c6b287fb094d33cf51236f90ca3cdfce5bc20b77b827`  
		Last Modified: Fri, 13 Nov 2020 03:02:21 GMT  
		Size: 4.3 KB (4260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56242e85e0be25e878fea4752f5da6c4b767c9915b3408839bcd3ffb74fea300`  
		Last Modified: Fri, 13 Nov 2020 03:02:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e3bd446df798f9591717a29a95e1ccb6027b55805c9eb37f968f2f196fa91e70
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58488357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7d0386b6c77438a13e82d7a2c3e4a43505db1c99c2e53250dbfe5c744e18f0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 08:55:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 08:55:00 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 08:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 09:04:59 GMT
ENV PG_MAJOR=11
# Fri, 13 Nov 2020 03:02:06 GMT
ENV PG_VERSION=11.10
# Fri, 13 Nov 2020 03:02:08 GMT
ENV PG_SHA256=13e6d2f80662fe463bc7718cdf0de6a9ec67fc78afcc7a3ae66b9ea19bb97899
# Fri, 13 Nov 2020 03:06:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 03:06:22 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 03:06:24 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 03:06:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 03:06:32 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 03:06:35 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 03:06:36 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 03:06:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Nov 2020 03:06:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 03:06:41 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 03:06:42 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 03:06:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54bc8a79538fa79db3e734327f2a73654bc80285dc55b7e4d8d206161ec79a9`  
		Last Modified: Thu, 22 Oct 2020 09:19:19 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30574d1822b9e42c2a6da5e4a8f52ab65d88be941e497b4565382967ebd326f8`  
		Last Modified: Thu, 22 Oct 2020 09:19:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba84cd9b87c2ce235d2634fedbfa7c50cfea3cacb7639702a0574c63a42981a5`  
		Last Modified: Fri, 13 Nov 2020 03:18:44 GMT  
		Size: 55.9 MB (55872714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b265b1b30dc92e5113c99bb24864024451286a88749043ebdac6adae3a84e8ba`  
		Last Modified: Fri, 13 Nov 2020 03:18:24 GMT  
		Size: 7.6 KB (7568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c218bce8f5dc7b6d2bc4394b94be03dae4582664b85c88c59b0d04b0dca51292`  
		Last Modified: Fri, 13 Nov 2020 03:18:24 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179ea2bdd1373b9ee8679a31153bbaa84d199121969ec23d21e4b9365c86e556`  
		Last Modified: Fri, 13 Nov 2020 03:18:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e2103896eba0f10e9d6787e4fcb18e417b629c9459f354a1f9b0e601c52982`  
		Last Modified: Fri, 13 Nov 2020 03:18:24 GMT  
		Size: 4.3 KB (4262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b6a08ed7c797788a5595a41cc23b6e50f274735813e4d6f7622d2753795d6fe`  
		Last Modified: Fri, 13 Nov 2020 03:18:24 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:ac3bf6bd9afb1e32d31d18edc45d29cd90e2a1a5fecbab858a756bfb2469cadd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55674782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdac71f8334773ad13d2386db8ff595e506381740697c21c28e0c62189d8196`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 08:56:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 08:56:03 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 08:56:05 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 09:04:07 GMT
ENV PG_MAJOR=11
# Thu, 22 Oct 2020 09:04:08 GMT
ENV PG_VERSION=11.9
# Thu, 22 Oct 2020 09:04:09 GMT
ENV PG_SHA256=35618aa72e0372091f923c42389c6febd07513157b4fbb9408371706afbb6635
# Thu, 22 Oct 2020 09:07:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 09:07:20 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 09:07:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 09:07:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 09:07:25 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 09:07:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 09:07:27 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Thu, 22 Oct 2020 09:07:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 09:07:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 09:07:30 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 09:07:30 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 09:07:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7eedf40b1ca3ca0c12781ef9399626d49e7898eb4dc6bf3888a3add86c9ee2`  
		Last Modified: Thu, 22 Oct 2020 09:17:08 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2cc4a27e16f2350721162545664e1c967b92e8a0ecffb90828c979f0bc3ac6`  
		Last Modified: Thu, 22 Oct 2020 09:17:08 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8744965d85a887a1a7a3dced6f0202ead4d55efa0b7588528f7735586c3b5683`  
		Last Modified: Thu, 22 Oct 2020 09:18:18 GMT  
		Size: 53.3 MB (53255369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a06383560e1db5eac489179766919bc67da0f176d9160c272b1146b7278e8d`  
		Last Modified: Thu, 22 Oct 2020 09:18:01 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be62bea1696e58983b8d9c43c605c50a423c6bbc40813ab47fc5fb0d67a9cc5`  
		Last Modified: Thu, 22 Oct 2020 09:18:01 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d0d783ebbf14db0c1817b13cf9e9f9f9a7755c4621234da376fa849860282d`  
		Last Modified: Thu, 22 Oct 2020 09:18:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f2fe42f6b532ccae3c1aee2136e59777b73fcb03fae56366c0c14398bbdb2b`  
		Last Modified: Thu, 22 Oct 2020 09:18:01 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29147edddff1f66375d08dc6df6c1681e26699760f8e37dbae1ff786e5615d54`  
		Last Modified: Thu, 22 Oct 2020 09:18:01 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3ab21a2131d6becdfbaeaae1988a8ce31a72205b48db98ee97edbf872691efb9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59855172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f42ba4208d66ccfcd26e6eae35bc43f8e2c62b834f558f8774b873189fd7e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 08:21:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 08:21:49 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 08:21:51 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 08:30:28 GMT
ENV PG_MAJOR=11
# Thu, 22 Oct 2020 08:30:30 GMT
ENV PG_VERSION=11.9
# Thu, 22 Oct 2020 08:30:31 GMT
ENV PG_SHA256=35618aa72e0372091f923c42389c6febd07513157b4fbb9408371706afbb6635
# Thu, 22 Oct 2020 08:33:41 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 08:33:45 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 08:33:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 08:33:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 08:33:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 08:33:49 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 08:33:50 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Thu, 22 Oct 2020 08:33:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 22 Oct 2020 08:33:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 08:33:53 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 08:33:54 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 08:33:57 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46b3b77440641e62ecc741cdb44f0f558d15c3f3b6d506be26f8c285f7a36ff`  
		Last Modified: Thu, 22 Oct 2020 08:44:00 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85615d5b5e22de086f665265885eae6f4cb41a63e5ed6910df6d0d03d0e90c5`  
		Last Modified: Thu, 22 Oct 2020 08:43:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e62537e567035c5999657615bd736409c64f41e942b3f87e615c66ae52a8cb`  
		Last Modified: Thu, 22 Oct 2020 08:45:03 GMT  
		Size: 57.1 MB (57134879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23fb5551ecc716a44734ad6358e1e78e7e79c98a3a9f96de760c29cb33890c5`  
		Last Modified: Thu, 22 Oct 2020 08:44:48 GMT  
		Size: 7.6 KB (7574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7baa45aa7871810c573597f945354762e83b06811f6d056d0ab88464a510059b`  
		Last Modified: Thu, 22 Oct 2020 08:44:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4f31d3813ec635ab947d8920d2f5c647368804aaa6daf6534a2c760881cf88`  
		Last Modified: Thu, 22 Oct 2020 08:44:47 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda57f6651ce34adfa7b1c188d1d9db8089308598f50a74690d4c7ece8abc5db`  
		Last Modified: Thu, 22 Oct 2020 08:44:47 GMT  
		Size: 4.3 KB (4259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8953d6050ea0981260cd058299c4cdf3393cbec496c99879bd52cbcfb9702ae9`  
		Last Modified: Thu, 22 Oct 2020 08:44:47 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; 386

```console
$ docker pull postgres@sha256:c4163e6baf9178fe26f05df524f821f8daf87cd6f9d8cc167d6996bb8fc48319
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63739377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7632549d9f50d8cb9a080d4ef585a406200bb5b088b11adc1e41e4c6063f24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 09:38:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 09:38:39 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 09:38:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 09:56:33 GMT
ENV PG_MAJOR=11
# Fri, 13 Nov 2020 03:03:48 GMT
ENV PG_VERSION=11.10
# Fri, 13 Nov 2020 03:03:48 GMT
ENV PG_SHA256=13e6d2f80662fe463bc7718cdf0de6a9ec67fc78afcc7a3ae66b9ea19bb97899
# Fri, 13 Nov 2020 03:10:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 03:10:33 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 03:10:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 03:10:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 03:10:35 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 03:10:35 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 03:10:36 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 03:10:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Nov 2020 03:10:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 03:10:37 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 03:10:37 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 03:10:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596122efb908f979efd1794c09ae9c7a15ac0e4d53f2c181fd646d9f32565d9a`  
		Last Modified: Thu, 22 Oct 2020 10:20:51 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeb7bd791d51cd161cadd22b53bd066e70998ebd55dd5ba92760d35f1ab9e8b`  
		Last Modified: Thu, 22 Oct 2020 10:20:51 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77218a2362ce017a4760108d2183c2ebc928db4918a961ace422d2185bd29dcf`  
		Last Modified: Fri, 13 Nov 2020 03:26:37 GMT  
		Size: 60.9 MB (60934357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e8312b025b3be60aaea2c59e0fae1421dbef7058baacdecdb85126fd9a8965`  
		Last Modified: Fri, 13 Nov 2020 03:26:22 GMT  
		Size: 7.6 KB (7574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688f3d3251ced09eada8d76b36efc0193e96c200c674dde135b46ad38c035f3e`  
		Last Modified: Fri, 13 Nov 2020 03:26:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7446de091671966afe5abf8c26dd57614157a90273bf1963dcf5b29e696920b0`  
		Last Modified: Fri, 13 Nov 2020 03:26:22 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5601092a9302f019b9653a00204e2fb94cb507104ec782b75e2c0bd8ab89f32`  
		Last Modified: Fri, 13 Nov 2020 03:26:22 GMT  
		Size: 4.3 KB (4262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2e95404a388669a0608d3eac45079fbd2bf244554c6721bd0d7a211038b3db`  
		Last Modified: Fri, 13 Nov 2020 03:26:23 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:bd85c320a2818205465c91fa0a817595439081faadd6db686a090294163bcad0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62606713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860df6f9f93f1620ff9c5cc1c4637eacf24aaeb8bbd7b805f229e703902d5700`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 23:06:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 23:06:17 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 23:06:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 23:18:56 GMT
ENV PG_MAJOR=11
# Fri, 13 Nov 2020 02:46:46 GMT
ENV PG_VERSION=11.10
# Fri, 13 Nov 2020 02:46:52 GMT
ENV PG_SHA256=13e6d2f80662fe463bc7718cdf0de6a9ec67fc78afcc7a3ae66b9ea19bb97899
# Fri, 13 Nov 2020 02:51:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:52:01 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:52:19 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:52:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:52:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:52:45 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:52:49 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:53:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Nov 2020 02:53:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:53:23 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:53:30 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:53:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f40cba28bb2e7e5449306ade2eb73dd95379370b59f2eac45aa9f62aa4d376b1`  
		Last Modified: Thu, 22 Oct 2020 23:41:44 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b145001d871735701a01931a308a05fafba12a34115cac00163359d3ed8cf19`  
		Last Modified: Thu, 22 Oct 2020 23:41:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b47e924ed9ac402458d3be3182bdad77dd8301feb2f8f49154e76deb4df2fe`  
		Last Modified: Fri, 13 Nov 2020 03:13:33 GMT  
		Size: 59.8 MB (59789753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bcf746c293bb7653e8d1f655365509a29f6677c2df8754c97e8c5e5bc249f5`  
		Last Modified: Fri, 13 Nov 2020 03:13:16 GMT  
		Size: 7.6 KB (7576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d404b7512f5834ac49381865e7f414af3cd4809aef89c3e8d8c255f68dadd5`  
		Last Modified: Fri, 13 Nov 2020 03:13:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5aea35bf0b70966b1a4fe13f73b42c71e8842e900151cc1c366beb282351754`  
		Last Modified: Fri, 13 Nov 2020 03:13:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e858ee738c46856bc7a56869d4d2dfe17d262978b8689d808d595eb0763258b`  
		Last Modified: Fri, 13 Nov 2020 03:13:16 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a34673a7f05d6a23b1d6525c85e67436aa72a6db996c84f6bb5dae3ee4d5d8`  
		Last Modified: Fri, 13 Nov 2020 03:13:15 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:1bb37b77b5cdd1a1482125b94908aba423f71d251607f3ca77a887f03371bb29
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62300391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76ebb4e9ee22b6df7022d6338625699a905d37a197dcb4b668befaf0b03e001`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 22 Oct 2020 01:59:08 GMT
ADD file:e07d6f40b1afc3d3eff230bc89e84704eb762706a373a60c6bea6a45b2287464 in / 
# Thu, 22 Oct 2020 01:59:09 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 09:05:49 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 22 Oct 2020 09:05:49 GMT
ENV LANG=en_US.utf8
# Thu, 22 Oct 2020 09:05:50 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 22 Oct 2020 09:15:07 GMT
ENV PG_MAJOR=11
# Fri, 13 Nov 2020 03:13:13 GMT
ENV PG_VERSION=11.10
# Fri, 13 Nov 2020 03:13:14 GMT
ENV PG_SHA256=13e6d2f80662fe463bc7718cdf0de6a9ec67fc78afcc7a3ae66b9ea19bb97899
# Fri, 13 Nov 2020 03:17:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 03:17:16 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 03:17:18 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 03:17:18 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 03:17:20 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 03:17:20 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 03:17:21 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 03:17:22 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 13 Nov 2020 03:17:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 03:17:23 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 03:17:23 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 03:17:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a4c84ece3d2b98927d25f13a4f367bfd96cbfae272f6ff1117d74c84b92d11d3`  
		Last Modified: Thu, 22 Oct 2020 01:59:37 GMT  
		Size: 2.6 MB (2565829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4788b366e4c5d5f3b69b31ae06b2811fe54eb39bd4fd8b6107985f9982ab150a`  
		Last Modified: Thu, 22 Oct 2020 09:29:06 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eed686015d5efd53e62cc5b3f61833711a48184edf03c7d21f021b34f23095`  
		Last Modified: Thu, 22 Oct 2020 09:29:07 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dc25696bfcf2b2aa20a9f500056f2d65b21022e5afc5dce20df79af2e1b0e2`  
		Last Modified: Fri, 13 Nov 2020 03:27:11 GMT  
		Size: 59.7 MB (59720826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f505769723950b9f39e92a4b8d68f7772476398247fed1396f24594e300c5ef9`  
		Last Modified: Fri, 13 Nov 2020 03:27:01 GMT  
		Size: 7.6 KB (7574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1a56b0b800c9927b1ea7efb7adccf485904004c04ac7955860a609f5dcd4a3`  
		Last Modified: Fri, 13 Nov 2020 03:27:01 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c11caa69c6428fda23368e179b63a5681487bacff40255d122fd3f552d7b407`  
		Last Modified: Fri, 13 Nov 2020 03:27:01 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e659aed4546491f18bf69c67eaea7dd729bc3d38e04d285d8c147600e810bba`  
		Last Modified: Fri, 13 Nov 2020 03:27:00 GMT  
		Size: 4.3 KB (4264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c0cefd8f5bcb4d43c38cdaf033d7f71edd0cc4f7dee1634e1719e07869548d`  
		Last Modified: Fri, 13 Nov 2020 03:27:01 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
