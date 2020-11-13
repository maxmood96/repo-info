## `postgres:13-alpine`

```console
$ docker pull postgres@sha256:7e8ff2786a49ad44ef2fcecf49f76667a9636971b46b25e0b2e536c11520f012
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

### `postgres:13-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:0c163c1c5901c5d46784c57ffc4c49f39994dadda3b672aa1ed11c5c207eaba7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62019961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770f846caccea499131403039925f7b71078985f92c4cdc5706604fe87dbc665`
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
# Thu, 22 Oct 2020 07:55:15 GMT
ENV PG_MAJOR=13
# Fri, 13 Nov 2020 02:22:32 GMT
ENV PG_VERSION=13.1
# Fri, 13 Nov 2020 02:22:32 GMT
ENV PG_SHA256=12345c83b89aa29808568977f5200d6da00f88a035517f925293355432ffe61f
# Fri, 13 Nov 2020 02:28:09 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:28:10 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:28:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:28:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:28:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:28:13 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:28:13 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:28:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:28:13 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:28:13 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:28:13 GMT
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
	-	`sha256:354372ef1765461a4557d9c373a723ba3c9c523f834ee5b89fc3d7dff7388a02`  
		Last Modified: Fri, 13 Nov 2020 03:01:01 GMT  
		Size: 59.2 MB (59208643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2c2c47ed522a99623c02b4cee13f2a4ae31e42f7373d41332747ee3ca02c34`  
		Last Modified: Fri, 13 Nov 2020 03:00:49 GMT  
		Size: 8.5 KB (8538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a51019c173774438da98769d9c15d6772ec538fdf7e59cb58ba2d37bd1d5f85`  
		Last Modified: Fri, 13 Nov 2020 03:00:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73459c934bad5a75445ef85cd005b51097a2f0f749e2ce2a1e599895801d11b`  
		Last Modified: Fri, 13 Nov 2020 03:00:49 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a02dcc4168bcc05f83ae2ad8e7cbcb576ac3ea281dd946934027217c34d9e6`  
		Last Modified: Fri, 13 Nov 2020 03:00:49 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:d03ca4d8180a022d42b3df57a121207d7929b8944698a49488f2d985d1a1aec0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60196835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2887fce14791585d53865df6937e7b057ca81707641e6b2dd27810765284c94b`
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
# Thu, 22 Oct 2020 08:55:03 GMT
ENV PG_MAJOR=13
# Fri, 13 Nov 2020 02:52:49 GMT
ENV PG_VERSION=13.1
# Fri, 13 Nov 2020 02:52:50 GMT
ENV PG_SHA256=12345c83b89aa29808568977f5200d6da00f88a035517f925293355432ffe61f
# Fri, 13 Nov 2020 02:56:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:57:02 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:57:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:57:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:57:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:57:07 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:57:08 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:57:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:57:09 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:57:10 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:57:11 GMT
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
	-	`sha256:31c25babd2e6ad05bdc27df0070d4089b1001e40ce178afb407fe431669a960d`  
		Last Modified: Fri, 13 Nov 2020 03:17:53 GMT  
		Size: 57.6 MB (57580335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef55b8b836a9708c2e84e072517c216faea9a8bb8d3a4846e0e496875e9b17b8`  
		Last Modified: Fri, 13 Nov 2020 03:17:36 GMT  
		Size: 8.5 KB (8544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98099ba340681047f0216239e4a5a025fef7533e2cdc761603de2ec163efdfdb`  
		Last Modified: Fri, 13 Nov 2020 03:17:36 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff86c4f96666dcdc8d87a270d2aedddeba16889d368020da904e508625865b51`  
		Last Modified: Fri, 13 Nov 2020 03:17:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d2e6cc158e96a6b25a578abf8dd1b8583e42f1e04561e52f5d3dfeeb77b0948`  
		Last Modified: Fri, 13 Nov 2020 03:17:36 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:36ed8010aa7cb12ba66b1e4db0b8085fe08a61fc4f20b14c9dc5cf48f49fe391
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.3 MB (57304236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d095d11ad7acb1affe24fc9e4de91bbd54cb60004fd5315f80de26809f170dc7`
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
# Thu, 22 Oct 2020 08:56:06 GMT
ENV PG_MAJOR=13
# Thu, 22 Oct 2020 08:56:08 GMT
ENV PG_VERSION=13.0
# Thu, 22 Oct 2020 08:56:10 GMT
ENV PG_SHA256=80e750be8d436b54197636a02636f8fd3263ba6779bf865b04832495ea592296
# Thu, 22 Oct 2020 08:59:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 08:59:43 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 08:59:47 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 08:59:48 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 08:59:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 08:59:51 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 08:59:52 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Thu, 22 Oct 2020 08:59:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 08:59:53 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 08:59:54 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 08:59:54 GMT
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
	-	`sha256:3d9e1fc344fdc1be9247f34eb1533fd8a223cbab00b5bf4aa7459424df790ea4`  
		Last Modified: Thu, 22 Oct 2020 09:17:22 GMT  
		Size: 54.9 MB (54883977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65080db56689834b20ad68241bde5ccfa334bf0c2f80db744db6186238d2c89d`  
		Last Modified: Thu, 22 Oct 2020 09:17:06 GMT  
		Size: 8.5 KB (8540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3d3a7196b2ada5397485bfe080afd7d743d37f68d526f285b6a57887087e78`  
		Last Modified: Thu, 22 Oct 2020 09:17:06 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba4958fec54abe667c1f75d7c7f24dd84d87711ae546e91a16344740aeab57b`  
		Last Modified: Thu, 22 Oct 2020 09:17:06 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0fabe1fbf3b332a3379ec29ec509a3f837c46f5aac0601b8ee836c80fb9029`  
		Last Modified: Thu, 22 Oct 2020 09:17:06 GMT  
		Size: 4.3 KB (4264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b6399aef923e0529a4f2a5874e8860d29cef3726ab7079883f3368aaa2a9f29c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61557698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b98a8adac19738d6d88e76787142368522635722706e167bdfb7e3756f615b2`
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
# Thu, 22 Oct 2020 08:21:52 GMT
ENV PG_MAJOR=13
# Thu, 22 Oct 2020 08:21:52 GMT
ENV PG_VERSION=13.0
# Thu, 22 Oct 2020 08:21:53 GMT
ENV PG_SHA256=80e750be8d436b54197636a02636f8fd3263ba6779bf865b04832495ea592296
# Thu, 22 Oct 2020 08:25:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 22 Oct 2020 08:25:19 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 22 Oct 2020 08:25:25 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 22 Oct 2020 08:25:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 22 Oct 2020 08:25:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 22 Oct 2020 08:25:32 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 22 Oct 2020 08:25:33 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Thu, 22 Oct 2020 08:25:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Oct 2020 08:25:35 GMT
STOPSIGNAL SIGINT
# Thu, 22 Oct 2020 08:25:37 GMT
EXPOSE 5432
# Thu, 22 Oct 2020 08:25:39 GMT
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
	-	`sha256:3399ca8ba311608fce7edea2b4b7c56e3a15651820560e526d7e892a45d9a694`  
		Last Modified: Thu, 22 Oct 2020 08:44:11 GMT  
		Size: 58.8 MB (58836563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37765dcba1abe0ee860486e0de0391cb6816ed272cea1886bc75908efac1cf77`  
		Last Modified: Thu, 22 Oct 2020 08:43:58 GMT  
		Size: 8.5 KB (8539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2093493e16e25a2e3387389fa691fab3e9a5815dd691af0c7b6f055110d738f`  
		Last Modified: Thu, 22 Oct 2020 08:43:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e2815f4ac9a0a90fcaf51162bacb8adcd984d8958d89c016d82c79d5291fb3`  
		Last Modified: Thu, 22 Oct 2020 08:43:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58df26ccc1cae9303c03384992f898557df12827808b6800a3ac24718d80dbc9`  
		Last Modified: Thu, 22 Oct 2020 08:43:58 GMT  
		Size: 4.3 KB (4259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; 386

```console
$ docker pull postgres@sha256:e1f57dc77d3bc8e819a48f6a09b90ec7f284b61372d3354fe6627424270223b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65610760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bceb707849eb1f485f0465e9680d2ec792f12266a041680b0b1b0493a0d27a`
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
# Thu, 22 Oct 2020 09:38:40 GMT
ENV PG_MAJOR=13
# Fri, 13 Nov 2020 02:40:52 GMT
ENV PG_VERSION=13.1
# Fri, 13 Nov 2020 02:40:52 GMT
ENV PG_SHA256=12345c83b89aa29808568977f5200d6da00f88a035517f925293355432ffe61f
# Fri, 13 Nov 2020 02:51:59 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:52:01 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:52:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:52:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:52:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:52:05 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:52:06 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:52:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:52:06 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:52:07 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:52:07 GMT
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
	-	`sha256:1a5b7ed6791e02b199da7734ad695aa18cc1617047e303c6553d53ecf354ad6a`  
		Last Modified: Fri, 13 Nov 2020 03:25:11 GMT  
		Size: 62.8 MB (62804899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c04caf8800ad9eaccc9a4b7f2733c7fec69bedce1f574d12404b310e37d866d`  
		Last Modified: Fri, 13 Nov 2020 03:24:57 GMT  
		Size: 8.5 KB (8534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eae48fe9955d2c8bafe1585ad14e89eb63d5999d8e7e60c1d896218f5c9b193`  
		Last Modified: Fri, 13 Nov 2020 03:24:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded556513bea9d093d94d442d7a881146cd6abaedd0619a1041ed30565cbebf8`  
		Last Modified: Fri, 13 Nov 2020 03:24:57 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdda5418d28998f6beb7370bc957c865566d1b823256f9ef24f148dfede65dd7`  
		Last Modified: Fri, 13 Nov 2020 03:24:57 GMT  
		Size: 4.3 KB (4263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:02b0dc104026b0fe4cb41231d8bfda6395c704d42b3b332a668cc8a5922f832a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.4 MB (64419384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17d6b08465f68fd7b757fada0b14e47ac91409468ca0d2a2d145a327026fa9e`
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
# Thu, 22 Oct 2020 23:06:26 GMT
ENV PG_MAJOR=13
# Fri, 13 Nov 2020 02:27:53 GMT
ENV PG_VERSION=13.1
# Fri, 13 Nov 2020 02:27:58 GMT
ENV PG_SHA256=12345c83b89aa29808568977f5200d6da00f88a035517f925293355432ffe61f
# Fri, 13 Nov 2020 02:33:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:33:44 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:33:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:34:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:34:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:34:20 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:34:23 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:34:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:34:36 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:34:40 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:34:43 GMT
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
	-	`sha256:045c1f17cd5993fe4dca236d24cfb272b14e52f2253b7aadf5c14d2ea24553d7`  
		Last Modified: Fri, 13 Nov 2020 03:11:53 GMT  
		Size: 61.6 MB (61601574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5039642f1af2a6df26cb664f224ecb4ec661e17db552930716e0b4fdde4719c`  
		Last Modified: Fri, 13 Nov 2020 03:11:40 GMT  
		Size: 8.5 KB (8543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec5eaad90ecef1ac7fe5e93478f37fdcb742b6be4cbcd7615712c563f56799b`  
		Last Modified: Fri, 13 Nov 2020 03:11:39 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec49e0e3726956b6850c55150e73f0462a15ccf40d5d4229626bb5a855cdaab4`  
		Last Modified: Fri, 13 Nov 2020 03:11:39 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef6b3d0fb0076ad72f050c759de39a87dc9bde76313e342ca717ae469669c08`  
		Last Modified: Fri, 13 Nov 2020 03:11:40 GMT  
		Size: 4.3 KB (4265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:914ef1b7e1b7a0190fc6d73d8e5484feb760a34e4cc968d57749040235c64c2d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64477496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82846d1dfd4834b88c2d620f7d4df0e961436361c885a72ffbe3519cb6fa773`
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
# Thu, 22 Oct 2020 09:05:51 GMT
ENV PG_MAJOR=13
# Fri, 13 Nov 2020 02:54:32 GMT
ENV PG_VERSION=13.1
# Fri, 13 Nov 2020 02:54:33 GMT
ENV PG_SHA256=12345c83b89aa29808568977f5200d6da00f88a035517f925293355432ffe61f
# Fri, 13 Nov 2020 02:58:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 13 Nov 2020 02:58:54 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 13 Nov 2020 02:58:55 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 13 Nov 2020 02:58:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 13 Nov 2020 02:58:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 13 Nov 2020 02:58:57 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 13 Nov 2020 02:58:58 GMT
COPY file:8f542efd076b9b67ef64928f3c0185ed50bfcbbc3572436a7222e879810d747f in /usr/local/bin/ 
# Fri, 13 Nov 2020 02:58:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Nov 2020 02:58:59 GMT
STOPSIGNAL SIGINT
# Fri, 13 Nov 2020 02:59:00 GMT
EXPOSE 5432
# Fri, 13 Nov 2020 02:59:00 GMT
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
	-	`sha256:bb3cb9ca968b593f2565e27a71b7477a66b7715c3a0052d3d6467cfed2d4704c`  
		Last Modified: Fri, 13 Nov 2020 03:26:17 GMT  
		Size: 61.9 MB (61897089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1169c766412164696474fb413078e4d71a75103ab1dddb507284608241c57973`  
		Last Modified: Fri, 13 Nov 2020 03:26:09 GMT  
		Size: 8.5 KB (8536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395651407fd45f6c04f6f2ae6c8d5bb2d43f7d2dd99f521c7f10892c172182b3`  
		Last Modified: Fri, 13 Nov 2020 03:26:08 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e32ebae1ad10387e707a349a195aa8d0748fe85a836f5d9e97e4f77dd1fb7b`  
		Last Modified: Fri, 13 Nov 2020 03:26:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad20ffc55ea878db7e2e74e281766fd3482e4588bab2ab35cafde4ef7c73692d`  
		Last Modified: Fri, 13 Nov 2020 03:26:09 GMT  
		Size: 4.3 KB (4262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
