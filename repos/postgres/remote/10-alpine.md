## `postgres:10-alpine`

```console
$ docker pull postgres@sha256:3e9c845b90b14d9a73be73258d1ae8c97f5db2e475ad9dce900b46b392bd0124
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

### `postgres:10-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:7ced77a458b7d6f4f3e4abfa55d6428fdcd0016e1926cb7463250b54b06480a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28603395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ac6f3b3b4d7f6dd371f7beae18e7370100e099cbecc96b58332cf4ac40cb52`
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
# Thu, 15 Apr 2021 04:06:51 GMT
ENV PG_MAJOR=10
# Thu, 15 Apr 2021 04:06:51 GMT
ENV PG_VERSION=10.16
# Thu, 15 Apr 2021 04:06:52 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 15 Apr 2021 04:11:53 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 04:11:56 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 04:11:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 04:11:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 04:12:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 04:12:01 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 04:12:01 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:12:03 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 04:12:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:12:04 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 04:12:04 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 04:12:04 GMT
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
	-	`sha256:51004fcfa27e9b9e02f833d4a3a9dd03d80ac9a98f96619c10b38eae287365ea`  
		Last Modified: Thu, 15 Apr 2021 04:22:41 GMT  
		Size: 25.8 MB (25777771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a4d008a73f93e873d417352eaab9cf723bd290e7296d46bf5367583cbe1da4`  
		Last Modified: Thu, 15 Apr 2021 04:22:33 GMT  
		Size: 7.3 KB (7349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2508a3fd8e171e9c7b1df121b4abf470b22960dfe8f5abcf719cb4028832d91`  
		Last Modified: Thu, 15 Apr 2021 04:22:33 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526e324160da248dba632ccb302989c98c24c02d7618250bca65dd7a1fc89cd5`  
		Last Modified: Thu, 15 Apr 2021 04:22:33 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53e39df381f6129776e1836b6ce51a8a528f1ac9fb4d97b1c611d78f653132b`  
		Last Modified: Thu, 15 Apr 2021 04:22:33 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86d189fde92be19c820f56ef802c7c80615862e7d69351eef5a0d2c7ade8adb`  
		Last Modified: Thu, 15 Apr 2021 04:22:33 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:a2babd9a8c9ebf9f4bb0e8d3f1821c8339b85f40da4ce64d148566d475fd0a1a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27731623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e199821729140c2ea576cea6d6f23998eedd9d4452d2a46d4ce9e179eebe64d1`
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
# Thu, 15 Apr 2021 02:59:18 GMT
ENV PG_MAJOR=10
# Thu, 15 Apr 2021 02:59:19 GMT
ENV PG_VERSION=10.16
# Thu, 15 Apr 2021 02:59:20 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 15 Apr 2021 03:03:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 03:03:20 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 03:03:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 03:03:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 03:03:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 03:03:25 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 03:03:26 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 03:03:30 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 03:03:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 03:03:34 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 03:03:35 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 03:03:36 GMT
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
	-	`sha256:63aef3cfbba837400bfcd230481adc3e30e115778fff1ad7dc80d3235df55258`  
		Last Modified: Thu, 15 Apr 2021 03:13:55 GMT  
		Size: 25.1 MB (25095829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdc869f19357057d0072b1d3bf4462f506f2f7da63ba91abfeb536b48042a85`  
		Last Modified: Thu, 15 Apr 2021 03:13:42 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c486f115c89f44b4088d13ee0821b5c341e5ce31fcad6d822617fc9106cfbf9c`  
		Last Modified: Thu, 15 Apr 2021 03:13:42 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88937e8b64d9853499e4a55cd53d74e6c048ac38376ce5dc882340ce3394811`  
		Last Modified: Thu, 15 Apr 2021 03:13:42 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90df361a4bfd6be962ffd13a6d9d9351937056024603a4a6f54b2f6f93592ad`  
		Last Modified: Thu, 15 Apr 2021 03:13:42 GMT  
		Size: 4.4 KB (4403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ae2f7d14e3d17751b42fb954f06d0dba0cef6868bde70427c3835d08b196e8`  
		Last Modified: Thu, 15 Apr 2021 03:13:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b9763a3680a557f7155f810cabcaddda3015bef9ddcb7ae860f23e1569c050c6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26665637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd711781631e3a237f0a13bfb001f5691053b6e916f02c16f5d20a54363a79c`
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
# Thu, 15 Apr 2021 03:59:18 GMT
ENV PG_MAJOR=10
# Thu, 15 Apr 2021 03:59:20 GMT
ENV PG_VERSION=10.16
# Thu, 15 Apr 2021 03:59:22 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 15 Apr 2021 04:02:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 04:02:30 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 04:02:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 04:02:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 04:02:36 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 04:02:39 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 04:02:41 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 04:02:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 04:02:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 04:02:48 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 04:02:48 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 04:02:49 GMT
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
	-	`sha256:b68e40454d768bab1a70f6915097747e6d2bfd3813bbc37bab97c2df663fa1e8`  
		Last Modified: Thu, 15 Apr 2021 04:12:19 GMT  
		Size: 24.2 MB (24227831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b9de813866fc37a228bf77b00a45cd1a047674940bf4698e5ef92949d9c2322`  
		Last Modified: Thu, 15 Apr 2021 04:12:10 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c840e4627714c35eb4cc9440165b2fc9b2e5c3a4d4b3a9464770f7f0015a56`  
		Last Modified: Thu, 15 Apr 2021 04:12:10 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff18a832d003a1f3ba9ee711ffa154fc791e5ebfb428dc74a42e5ee72e5c66de`  
		Last Modified: Thu, 15 Apr 2021 04:12:10 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86778dc7a72db31db715eaa50f5165c8b013bb9295e2dd7b2f7fd0db10774f89`  
		Last Modified: Thu, 15 Apr 2021 04:12:10 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63a7f32b4f6ab9da21949cb6cd3d8e04d7fb29b5aaf2bf80f07420ad185b2ce`  
		Last Modified: Thu, 15 Apr 2021 04:12:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:2f4622b21f8de2790e52f1c4a1bb65531e25e48643eea64135b9def466d922c0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28310149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9c1c496b4c3fa2ef0fd93b7e150fffe956088f3052d361e83ba545c567c960`
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
# Thu, 01 Apr 2021 15:47:03 GMT
ENV PG_MAJOR=10
# Thu, 01 Apr 2021 15:47:04 GMT
ENV PG_VERSION=10.16
# Thu, 01 Apr 2021 15:47:05 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 01 Apr 2021 15:50:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 15:50:13 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 15:50:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 15:50:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 15:50:20 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 15:50:21 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 15:50:22 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 15:50:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 01 Apr 2021 15:50:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 15:50:27 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 15:50:28 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 15:50:29 GMT
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
	-	`sha256:3ef9e2a25c6adebeb55a25fd6b32745b55968b2911add651ce15ccfeef505647`  
		Last Modified: Thu, 01 Apr 2021 15:59:20 GMT  
		Size: 25.6 MB (25584575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac34d320ebc07d28efa8ae1b8002286b1dd9b6956267bc5ee66d579e90b00ed`  
		Last Modified: Thu, 01 Apr 2021 15:59:13 GMT  
		Size: 7.4 KB (7352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d348de737332c684aa05bbb05706cf43981087040ef72ae896097e6dc8eb10f4`  
		Last Modified: Thu, 01 Apr 2021 15:59:13 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb1457cbe8c19403a3b909ac2b02b58f23304e598512edba6713b91cde259ff`  
		Last Modified: Thu, 01 Apr 2021 15:59:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab692230cb78e77286451cd72cfb0e4df08e10fcddeddb5e23c43665d8643ebf`  
		Last Modified: Thu, 01 Apr 2021 15:59:13 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599f5f0a9f696eb32eae33113938f06aef43be06eb892d95d973ca1269fa9c2a`  
		Last Modified: Thu, 01 Apr 2021 15:59:12 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; 386

```console
$ docker pull postgres@sha256:e476a236dba031b0776a928b4fc511fdd8a8d5dc25e2830bedf193e0bc394351
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29535509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46faa0ea2aae01cd07424010321143984903aa5a37b96feee07b2e6e18363540`
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
# Thu, 01 Apr 2021 05:51:29 GMT
ENV PG_MAJOR=10
# Thu, 01 Apr 2021 05:51:29 GMT
ENV PG_VERSION=10.16
# Thu, 01 Apr 2021 05:51:29 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 01 Apr 2021 05:55:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 01 Apr 2021 05:55:36 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 01 Apr 2021 05:55:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 01 Apr 2021 05:55:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 01 Apr 2021 05:55:37 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 01 Apr 2021 05:55:38 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 01 Apr 2021 05:55:38 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 01 Apr 2021 05:55:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 01 Apr 2021 05:55:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Apr 2021 05:55:39 GMT
STOPSIGNAL SIGINT
# Thu, 01 Apr 2021 05:55:39 GMT
EXPOSE 5432
# Thu, 01 Apr 2021 05:55:40 GMT
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
	-	`sha256:40570228533a87f0c52a5e79fcdb57613edf950b0616b33e5ccef3bc40f422da`  
		Last Modified: Thu, 01 Apr 2021 06:06:48 GMT  
		Size: 26.7 MB (26703051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9325d2b06c11fd358294497557f73416c578b3470ad63e06d1208163fad7692`  
		Last Modified: Thu, 01 Apr 2021 06:06:39 GMT  
		Size: 7.3 KB (7350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372d550376bf570ae04d1abd6181646f02820a3159232c0bc6fea94ca6c9d7db`  
		Last Modified: Thu, 01 Apr 2021 06:06:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5d2b4ebb8ba3a817130de595e024a17c6cab5b8528e3157d94b055f2ef3052`  
		Last Modified: Thu, 01 Apr 2021 06:06:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2039812b75de7f59d197b7d4ae92237917325b7686249dca85784a31ab3893b8`  
		Last Modified: Thu, 01 Apr 2021 06:06:39 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac4f1ed557d0231a97522e48e0e1942eb34d09448d997382b63675a7b9a3b51`  
		Last Modified: Thu, 01 Apr 2021 06:06:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:0b6ceb0fb723ecf15b39eeb854fd363dd9a498665b288b9af1b5d51b22843080
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29798398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be7b966ea5d1fc24fc33b779a96e4b095f4fc927016f75c69a3fecb1d9ed5db`
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
# Fri, 02 Apr 2021 00:18:21 GMT
ENV PG_MAJOR=10
# Fri, 02 Apr 2021 00:18:28 GMT
ENV PG_VERSION=10.16
# Fri, 02 Apr 2021 00:18:33 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Fri, 02 Apr 2021 00:21:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 02 Apr 2021 00:21:45 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 02 Apr 2021 00:21:55 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 02 Apr 2021 00:22:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 02 Apr 2021 00:22:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 02 Apr 2021 00:22:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 02 Apr 2021 00:22:18 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 02 Apr 2021 00:22:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 02 Apr 2021 00:22:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Apr 2021 00:22:41 GMT
STOPSIGNAL SIGINT
# Fri, 02 Apr 2021 00:22:45 GMT
EXPOSE 5432
# Fri, 02 Apr 2021 00:22:51 GMT
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
	-	`sha256:78930d28bcf7149a5d9def7670439af18bbd4a0add17ac4c3cfb4936f4ef2aa9`  
		Last Modified: Fri, 02 Apr 2021 00:36:31 GMT  
		Size: 27.0 MB (26971519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b753b70d6e6479dc7b7b392b327fedfce1b209d1c6764c6eb7ab17a40b7624b4`  
		Last Modified: Fri, 02 Apr 2021 00:36:22 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b2545d228eb16b0d4858d45d154624fe4fba79152674eb46c83b6397ea4aa`  
		Last Modified: Fri, 02 Apr 2021 00:36:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fa7f52f77acf72445b04ea404898e41275d427ebeb3061985480dbbecd3bc4`  
		Last Modified: Fri, 02 Apr 2021 00:36:22 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce4bf98aa39129126797804f99ab4bb5ee5bd3c09f1d560f961b9160aa6acc2`  
		Last Modified: Fri, 02 Apr 2021 00:36:24 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4dea125ec4dce05ee302508b0a60b47da317370965cf565ab792c1e36a4869`  
		Last Modified: Fri, 02 Apr 2021 00:36:22 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:3d71820db291c228991d05c373e89520b5e6661103b530515c0ee8b8f220e59c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28460190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed24312621616f61a20b36086967845886ac8e2dec517b88a3275708c5ec277e`
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
# Thu, 15 Apr 2021 02:47:22 GMT
ENV PG_MAJOR=10
# Thu, 15 Apr 2021 02:47:22 GMT
ENV PG_VERSION=10.16
# Thu, 15 Apr 2021 02:47:22 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 15 Apr 2021 02:50:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 15 Apr 2021 02:50:13 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 15 Apr 2021 02:50:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 15 Apr 2021 02:50:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 15 Apr 2021 02:50:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 15 Apr 2021 02:50:15 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 15 Apr 2021 02:50:16 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 15 Apr 2021 02:50:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 15 Apr 2021 02:50:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 02:50:17 GMT
STOPSIGNAL SIGINT
# Thu, 15 Apr 2021 02:50:17 GMT
EXPOSE 5432
# Thu, 15 Apr 2021 02:50:17 GMT
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
	-	`sha256:850af248a3afe843b5742f9748c467b5e1b7ef2715c7766d78c0a20c958089e0`  
		Last Modified: Thu, 15 Apr 2021 02:56:21 GMT  
		Size: 25.8 MB (25843880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c3e0dab51c8098eeb025aa35636489b6b8ccba478d1ab986e918aaacf6ebd8`  
		Last Modified: Thu, 15 Apr 2021 02:56:16 GMT  
		Size: 7.4 KB (7356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc198782f37dd4847d76fbdd7c8c8fc876db9a9a44f14025a7a4e50fdca72e8`  
		Last Modified: Thu, 15 Apr 2021 02:56:17 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bde4002a934dddbcf54e53d168b134e6c52403e2defb98c810883e730dce4b`  
		Last Modified: Thu, 15 Apr 2021 02:56:16 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5dd6c1d309a74535ef8508a95e3bd4f4591388a5c447e502c5732eea86cf1c`  
		Last Modified: Thu, 15 Apr 2021 02:56:16 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f2ecd3dfd26b436588fb27b593825ba49d34d0f03ef82d2c2fe5016568bf45`  
		Last Modified: Thu, 15 Apr 2021 02:56:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
