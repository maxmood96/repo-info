## `postgres:12-alpine`

```console
$ docker pull postgres@sha256:e5c80ed43fc48ccec716bdf43341c4dddf29a99b3aaceca6a87ff2ccbd05324f
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
$ docker pull postgres@sha256:5f6747957adaaa303ad07234aa24ade985eba56805991f9be32783de485a9adb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61611937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0766dd0f9d460940d7dc9d5b615917a39bdc0c3089cf274257544a2eeef1a838`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Fri, 29 Jan 2021 02:53:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 29 Jan 2021 02:53:55 GMT
ENV LANG=en_US.utf8
# Fri, 29 Jan 2021 02:53:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 29 Jan 2021 03:01:35 GMT
ENV PG_MAJOR=12
# Fri, 12 Feb 2021 19:29:18 GMT
ENV PG_VERSION=12.6
# Fri, 12 Feb 2021 19:29:19 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Fri, 12 Feb 2021 19:35:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Feb 2021 19:35:35 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Feb 2021 19:35:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Feb 2021 19:35:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Feb 2021 19:35:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Feb 2021 19:35:37 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Feb 2021 19:35:37 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 12 Feb 2021 19:35:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Feb 2021 19:35:38 GMT
STOPSIGNAL SIGINT
# Fri, 12 Feb 2021 19:35:38 GMT
EXPOSE 5432
# Fri, 12 Feb 2021 19:35:38 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff5918c11c3ab1f2763192c7c033f5dfe60b30d369a8aa483d65326974b637a`  
		Last Modified: Fri, 29 Jan 2021 03:42:07 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c393806625cde0c68d6881aaeb6a8305d841ad1ec4e6152fe5dde27a6c7b4af8`  
		Last Modified: Fri, 29 Jan 2021 03:42:07 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7a0286f83b77e1a001a64ce0e2ef0d867b6049a5b51a9eee7306a240eef69c`  
		Last Modified: Fri, 12 Feb 2021 20:07:11 GMT  
		Size: 58.8 MB (58786314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c872f603583c8c2c1e94e0800b74f9aaec6d000e5ed859c51f92d6cd115bd2`  
		Last Modified: Fri, 12 Feb 2021 20:07:00 GMT  
		Size: 8.2 KB (8242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26985cbf083890237509234948fc87f9360728564e6098584e08c1363e273e80`  
		Last Modified: Fri, 12 Feb 2021 20:07:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aff2a6ce899ead776ac4b7edc66357196072f0e5beef7c2e2c2ad75ef89d943`  
		Last Modified: Fri, 12 Feb 2021 20:06:59 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f736273838bbf6ac3d5b9ddfe192ea199cb82c210496967d75a29251afdb1a5`  
		Last Modified: Fri, 12 Feb 2021 20:07:00 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:95ee5993459f57dddd1e42d0c11adf8363172b3828f94ed7a5ecac74da0e8ec4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59991073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed4f937f06c2c04ab29bfddef0fd163a5a78f43a5ab8e01c1684d9bc7ecd0e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:03:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:03:42 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:03:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:08:14 GMT
ENV PG_MAJOR=12
# Wed, 17 Feb 2021 23:08:15 GMT
ENV PG_VERSION=12.6
# Wed, 17 Feb 2021 23:08:16 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Wed, 17 Feb 2021 23:12:13 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:12:16 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:12:18 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:12:19 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:12:20 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:12:21 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:12:22 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:12:23 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:12:24 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:12:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70c466870a71b73094e5a73a7e0fdf9e0fc7a2def8525ea7665bc5b3e382f8b4`  
		Last Modified: Wed, 17 Feb 2021 23:27:05 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:754cb30576f658b66484126890351d63b0bbecd0aff43d7ff597325359d00112`  
		Last Modified: Wed, 17 Feb 2021 23:27:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb257749d2f4a5358dbb2fc385cb9668353bb8ce59ed660729a59852d6f064b1`  
		Last Modified: Wed, 17 Feb 2021 23:27:47 GMT  
		Size: 57.4 MB (57354601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7510c046e28daf1b7e3e8468ed50754b005f63325f5e794183a55afd9eeea1`  
		Last Modified: Wed, 17 Feb 2021 23:27:27 GMT  
		Size: 8.2 KB (8245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ee2db18d91dfe90a8998d35700b77fe142eb2fc92124a52bd0cb63e94d3440`  
		Last Modified: Wed, 17 Feb 2021 23:27:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15dbbc28c8a89ca3678f85a18118a230ab33a3a1369a61c762b717b0c2edadd`  
		Last Modified: Wed, 17 Feb 2021 23:27:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb8d7da12cf4ec74d1a827c0d2a156808ed114421160a068caa488f65917db`  
		Last Modified: Wed, 17 Feb 2021 23:27:27 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:959d288e4d301dc5f0be28c9976b27e4ff77dbd1106ba8adc7f0989c4dde3009
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57041391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e76174d97fae083b99667fd836a829b83a7656d2ccdedfbc4f5f5c67436686`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:57:36 GMT
ADD file:efdd39e5243eaf378f12ad5a85d2222b44930850a90263e5f17e8a6b5e9bc9b8 in / 
# Wed, 17 Feb 2021 20:57:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:38:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:38:06 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:38:08 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:42:15 GMT
ENV PG_MAJOR=12
# Wed, 17 Feb 2021 23:42:16 GMT
ENV PG_VERSION=12.6
# Wed, 17 Feb 2021 23:42:17 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Wed, 17 Feb 2021 23:45:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:45:34 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:45:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:45:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:45:39 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:45:40 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:45:41 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:45:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:45:42 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:45:43 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:45:44 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f55b840e27d3dbe27e44497103a4397f043749f933eb0433d29e2f104b3435ef`  
		Last Modified: Wed, 17 Feb 2021 20:58:14 GMT  
		Size: 2.4 MB (2423892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a02e78d0690510cbbcaf122beefdfd0be6106291820f5db4dcc3b6d0e28dfc8`  
		Last Modified: Thu, 18 Feb 2021 00:00:39 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c6d1d98c310b550014b6a6f6f5e38df97f28413e21c08391b2771130a5c74`  
		Last Modified: Thu, 18 Feb 2021 00:00:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48068f8901fa8508c24052a3fccd41616bb5bad88cb73354bcbb3dd6341238e8`  
		Last Modified: Thu, 18 Feb 2021 00:01:19 GMT  
		Size: 54.6 MB (54603071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b233052aba08ee3bd4f92580a4a8017573e63d91e9c9eb60fdcd4bb41cccf28`  
		Last Modified: Thu, 18 Feb 2021 00:01:04 GMT  
		Size: 8.2 KB (8242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980d0b6da1c8d59709d88f2e8f1a1621ea0ac5c4bb89d5a982cd31325ee263c2`  
		Last Modified: Thu, 18 Feb 2021 00:01:04 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ea0a789837731a0921c0b3316bd56dedf7f1752976fdeb5f0465ff08135fb4`  
		Last Modified: Thu, 18 Feb 2021 00:01:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651feb8fc071a5d67316734d17e69814bf06a743a23d2943d7887ade2388d206`  
		Last Modified: Thu, 18 Feb 2021 00:01:04 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:e776b76f1dad0192f0cac2f1fb95a3187cc6274c84ecc6a770852294e14320fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60924243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99bb74959d0872c24e21405c0438b0738f9491460655784e2eb507c40169232`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:39:29 GMT
ADD file:3bf1497bd250cf7c73c12231dc4ebe3a3a67f2cd99e35bce47ef6674683aeb1d in / 
# Wed, 17 Feb 2021 20:39:30 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:15:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:15:05 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:15:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:19:29 GMT
ENV PG_MAJOR=12
# Wed, 17 Feb 2021 23:19:30 GMT
ENV PG_VERSION=12.6
# Wed, 17 Feb 2021 23:19:31 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Wed, 17 Feb 2021 23:23:16 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:23:20 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:23:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:23:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:23:27 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:23:28 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:23:29 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:23:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:23:30 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:23:31 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:23:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:069a56d6d07f6b186fbb82e4486616b9be9a37ce32a63013af6cddcb65898182`  
		Last Modified: Wed, 17 Feb 2021 20:40:04 GMT  
		Size: 2.7 MB (2711572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ea767c0e0b823455a91d082e4db47af65e6aa51a78df49f9700eb9e21245f8d`  
		Last Modified: Wed, 17 Feb 2021 23:38:53 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65dac6dbfdc3c658a4293d3279f8b00d5ba7fb3b2793c0e984f39a0a25d8b34`  
		Last Modified: Wed, 17 Feb 2021 23:38:53 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73cb843cade0fc5ee817b22aa7f706c51b3d1c89039f967b854b66db4c199c7c`  
		Last Modified: Wed, 17 Feb 2021 23:39:33 GMT  
		Size: 58.2 MB (58198242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef54af71f233926c47992d61759b39490cbd7fae645567340724c319e28d141`  
		Last Modified: Wed, 17 Feb 2021 23:39:19 GMT  
		Size: 8.2 KB (8242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10408444f83517328e15bc8f3e1d27041986f8114bb57df1bc51ae791424578`  
		Last Modified: Wed, 17 Feb 2021 23:28:43 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cad4cfbff5879bc0c41e508544513a8c8bb9d02bfe2b7821dedeec23491d9af`  
		Last Modified: Wed, 17 Feb 2021 23:28:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494c30f7abe04940c2b837cc0bfce875f42e3a30011ac3e2ed049902b931e28d`  
		Last Modified: Wed, 17 Feb 2021 23:39:20 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; 386

```console
$ docker pull postgres@sha256:75e897f15b780152bbdfd7a6b460b4d734fe987792c7d167394f8a596b568026
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65158856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c9abca37b0fad60a39dbd626228fb9cf9f748cdf09e1f5480ca5b60224c3f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:32:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 18 Feb 2021 01:32:39 GMT
ENV LANG=en_US.utf8
# Thu, 18 Feb 2021 01:32:40 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 18 Feb 2021 01:46:10 GMT
ENV PG_MAJOR=12
# Thu, 18 Feb 2021 01:46:11 GMT
ENV PG_VERSION=12.6
# Thu, 18 Feb 2021 01:46:11 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 18 Feb 2021 01:54:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 18 Feb 2021 01:54:22 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 18 Feb 2021 01:54:24 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 18 Feb 2021 01:54:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Feb 2021 01:54:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 18 Feb 2021 01:54:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Feb 2021 01:54:27 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 18 Feb 2021 01:54:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 01:54:28 GMT
STOPSIGNAL SIGINT
# Thu, 18 Feb 2021 01:54:28 GMT
EXPOSE 5432
# Thu, 18 Feb 2021 01:54:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d4c403e47c591ecc6f278761afe2bdc05fc908d7374e6c71047a30a7e551e2`  
		Last Modified: Thu, 18 Feb 2021 02:26:53 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad33d01c73fd25a7034659df599f6de2cc035bea845f7bc6addd58c2c442eaa6`  
		Last Modified: Thu, 18 Feb 2021 02:26:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de721f3d19b24c6e34add9408bc38f97e83bd5f616953142735ed9c4282c5bd5`  
		Last Modified: Thu, 18 Feb 2021 02:27:37 GMT  
		Size: 62.3 MB (62326377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9cd20896ad5ae735546876939ebf9ee1f5c0e2996e72b70096e7fef9e6e344`  
		Last Modified: Thu, 18 Feb 2021 02:27:21 GMT  
		Size: 8.2 KB (8237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0cdba3f1b66d7a920c959eebb8197316a56f398b1fa5c3af910de19f54c267b`  
		Last Modified: Thu, 18 Feb 2021 02:27:21 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852aa26ec6ad383b26471830968162fdbbaaafc3b7c06735b9c83ef234ed4a27`  
		Last Modified: Thu, 18 Feb 2021 02:27:21 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b992686f8f7dce558aadac6d3d8f891e54c1f7df602dbead784173d70408709a`  
		Last Modified: Thu, 18 Feb 2021 02:27:21 GMT  
		Size: 4.4 KB (4408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:0c197ae599c5c1614f64e810936e44fdc099da4033f41b6c0ae4015dc2eb70f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.0 MB (63999803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f55dec780d87fd7ba91fe6986a276573fe2bd08117cb5d857bd80e36db33f46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 21:17:29 GMT
ADD file:28f4377c61c0f8eb43a6b36e6a24ef5893f51d405d25b62e364988223537ae0b in / 
# Wed, 17 Feb 2021 21:17:37 GMT
CMD ["/bin/sh"]
# Wed, 17 Feb 2021 23:40:39 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 17 Feb 2021 23:40:45 GMT
ENV LANG=en_US.utf8
# Wed, 17 Feb 2021 23:40:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 17 Feb 2021 23:46:51 GMT
ENV PG_MAJOR=12
# Wed, 17 Feb 2021 23:46:56 GMT
ENV PG_VERSION=12.6
# Wed, 17 Feb 2021 23:47:00 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Wed, 17 Feb 2021 23:51:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:51:22 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:51:51 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:51:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:52:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:52:32 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:52:39 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:52:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:53:05 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:53:19 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:53:25 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:cb672e0375a8f9bb3d33049ceb372ffa49b959bfc84fe6f72bfb97b682a608c8`  
		Last Modified: Wed, 17 Feb 2021 21:18:10 GMT  
		Size: 2.8 MB (2813081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62347ea12b2b66d9d40b3e5b53079b8dab0d76d44bc63abf4361dde7a9d2fd6`  
		Last Modified: Thu, 18 Feb 2021 00:16:49 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e195dedf606bdd9ff225564397fb91e0bfd068b1e74cb7c243e7a9026192471`  
		Last Modified: Thu, 18 Feb 2021 00:16:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e279b7dc9a55cd5d61550bb7a3c87ce2d421781b290a0871e3b12191a4c5185f`  
		Last Modified: Thu, 18 Feb 2021 00:17:27 GMT  
		Size: 61.2 MB (61172291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f79f9b059df3be68b2cf081dd42f39c6760da6a17fa422bdafd89bf0b8488f1`  
		Last Modified: Thu, 18 Feb 2021 00:17:15 GMT  
		Size: 8.2 KB (8242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50d7ee0dfb04d24d20772a01e6c736b08b1740d150b3ebd37316140a899c916`  
		Last Modified: Thu, 18 Feb 2021 00:17:15 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e424fc77cf5d3b7bd850643af3c05be3d3c20e3354d3cd95801a713103d6b59`  
		Last Modified: Thu, 18 Feb 2021 00:17:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bedeacbbab7fdd882be27e857013603d06fa6700c0da868f0a6d31437edfedc9`  
		Last Modified: Thu, 18 Feb 2021 00:17:15 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:12-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:2d6ccebf01f9fe5fc62d2d61f327ade53bddbc3672c99a8a8fc4792df6b58231
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64236153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57295681e7b8ccc87f2084720aee1e280d3126de27e23e72f97abb8045dd6fea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 20:41:27 GMT
ADD file:630c66f8d774d75b51e32aff812b438d377ebd3389c4aa6c324fdf8c03b6fa13 in / 
# Wed, 17 Feb 2021 20:41:27 GMT
CMD ["/bin/sh"]
# Thu, 18 Feb 2021 01:54:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 18 Feb 2021 01:54:30 GMT
ENV LANG=en_US.utf8
# Thu, 18 Feb 2021 01:54:31 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 18 Feb 2021 01:57:52 GMT
ENV PG_MAJOR=12
# Thu, 18 Feb 2021 01:57:52 GMT
ENV PG_VERSION=12.6
# Thu, 18 Feb 2021 01:57:52 GMT
ENV PG_SHA256=df7dd98d5ccaf1f693c7e1d0d084e9fed7017ee248bba5be0167c42ad2d70a09
# Thu, 18 Feb 2021 02:01:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm10-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 18 Feb 2021 02:01:04 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 18 Feb 2021 02:01:05 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 18 Feb 2021 02:01:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Feb 2021 02:01:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 18 Feb 2021 02:01:07 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Feb 2021 02:01:07 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 18 Feb 2021 02:01:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 02:01:08 GMT
STOPSIGNAL SIGINT
# Thu, 18 Feb 2021 02:01:08 GMT
EXPOSE 5432
# Thu, 18 Feb 2021 02:01:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ff5e8cb87555e9fa38a441f5cf0414e91353e2cd21cdb48d48b7de5bb39ce674`  
		Last Modified: Wed, 17 Feb 2021 20:41:58 GMT  
		Size: 2.6 MB (2602381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da53daa845ee16c5cb762996a474aa4ecac04e53b3578031254225e63f573164`  
		Last Modified: Thu, 18 Feb 2021 02:11:15 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05dfcde47a8d8d175de0042dd1d418474b9ff7acfa08d97a3d46ba82ea562c8e`  
		Last Modified: Thu, 18 Feb 2021 02:11:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dfc9a5fe367d18c37512e47ed3565b870cec5a074f1552df14306704734c15`  
		Last Modified: Thu, 18 Feb 2021 02:11:37 GMT  
		Size: 61.6 MB (61619342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d08dc6f8bc0316d8569622119d04fda92fd3783194271ccbacea32d418b1ba8`  
		Last Modified: Thu, 18 Feb 2021 02:11:29 GMT  
		Size: 8.2 KB (8244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a85c2832c86307125e132314dd935a88b9dd1fed101889d6425e5619bb468cd`  
		Last Modified: Thu, 18 Feb 2021 02:11:29 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5d8d768583e990b951f79d782de746061eb1be70c97d4aee48d7ae4bd508783`  
		Last Modified: Thu, 18 Feb 2021 02:11:29 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b0a8c500852ee329920b6d9ef9f58a09c45d75b043d3e416c8c9d660a7d225`  
		Last Modified: Thu, 18 Feb 2021 02:11:29 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
