## `postgres:10-alpine3.14`

```console
$ docker pull postgres@sha256:398ee1f310c86bf98e0689cad1154e540f4c341354ae6e57fa75381b00c6af8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `postgres:10-alpine3.14` - linux; amd64

```console
$ docker pull postgres@sha256:495e562be0d613f96814b534c91ee693aefde58e44f0c38ce810f742cc36d280
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.7 MB (28654582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a78c4ea2b0a1fc84e937ab4725aa5a652ef0b3e81c74b40245a0e4c60f377f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 20:09:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 06 Aug 2021 20:09:36 GMT
ENV LANG=en_US.utf8
# Fri, 06 Aug 2021 20:09:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 06 Aug 2021 20:38:34 GMT
ENV PG_MAJOR=10
# Fri, 06 Aug 2021 20:38:34 GMT
ENV PG_VERSION=10.17
# Fri, 06 Aug 2021 20:38:35 GMT
ENV PG_SHA256=5af28071606c9cd82212c19ba584657a9d240e1c4c2da28fc1f3998a2754b26c
# Fri, 06 Aug 2021 20:44:00 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 06 Aug 2021 20:44:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 06 Aug 2021 20:44:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 06 Aug 2021 20:44:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Aug 2021 20:44:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 06 Aug 2021 20:44:05 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Aug 2021 20:44:05 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 06 Aug 2021 20:44:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 20:44:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 20:44:07 GMT
STOPSIGNAL SIGINT
# Fri, 06 Aug 2021 20:44:07 GMT
EXPOSE 5432
# Fri, 06 Aug 2021 20:44:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f8a1ea71cb44639c871a69f095baa1737555205a3ea7ce92b116c1462ffc37`  
		Last Modified: Fri, 06 Aug 2021 20:49:45 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d8912b293dcd54c830c025ee7d3c1e3774037bc917800fc4db4a04959855ca`  
		Last Modified: Fri, 06 Aug 2021 20:49:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca32792aa1cb63c253b5e12146748c6c8c0e5327131f24602f7ef330a7795a99`  
		Last Modified: Fri, 06 Aug 2021 20:52:03 GMT  
		Size: 25.8 MB (25827528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d02a6c0c16ad57001f1ae18a6ecf4bf7fec53418762fa0271c2ad570a5f8c61c`  
		Last Modified: Fri, 06 Aug 2021 20:51:55 GMT  
		Size: 7.7 KB (7731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14697e215b1b4768585b953be75bbb8b55dcb0f450a7345964df5de347ac283f`  
		Last Modified: Fri, 06 Aug 2021 20:51:55 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5938b4e5c466370427a06342600690ee0addfda35018aa1a44d5fd4658d3aa08`  
		Last Modified: Fri, 06 Aug 2021 20:51:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926f8cf12cf405846b56df8b92f3fd94e795e8eae5529287b2a81344b7f9a01f`  
		Last Modified: Fri, 06 Aug 2021 20:51:55 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbc924c7ffcc634534b8f4e840b3f8bc8fac5b8e88366ad71b85b361d5eb190`  
		Last Modified: Fri, 06 Aug 2021 20:51:55 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine3.14` - linux; arm variant v6

```console
$ docker pull postgres@sha256:2cd8c3a649fb36c55823ffbca2bfe0e4d0b5fc06d2a64c6921bb2c7a9c8e0428
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27799077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5c686f208555c3df495801e811bd298f1b6aaebbc901a3c927a04da4d0e1ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:34:10 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 06 Aug 2021 21:34:11 GMT
ENV LANG=en_US.utf8
# Fri, 06 Aug 2021 21:34:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 06 Aug 2021 21:55:17 GMT
ENV PG_MAJOR=10
# Fri, 06 Aug 2021 21:55:18 GMT
ENV PG_VERSION=10.17
# Fri, 06 Aug 2021 21:55:18 GMT
ENV PG_SHA256=5af28071606c9cd82212c19ba584657a9d240e1c4c2da28fc1f3998a2754b26c
# Fri, 06 Aug 2021 21:58:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 06 Aug 2021 21:58:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 06 Aug 2021 21:58:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 06 Aug 2021 21:58:58 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Aug 2021 21:59:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 06 Aug 2021 21:59:00 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Aug 2021 21:59:01 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 06 Aug 2021 21:59:02 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 21:59:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 21:59:03 GMT
STOPSIGNAL SIGINT
# Fri, 06 Aug 2021 21:59:04 GMT
EXPOSE 5432
# Fri, 06 Aug 2021 21:59:04 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9894594f46e7a2d9314f2f96a83a8a4d069c1c3d3bd1f20f7378ea4a36eb000`  
		Last Modified: Fri, 06 Aug 2021 22:05:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d885209ac2857981e19ce7ccfb1852b335ed57fd0d8020badbc76323c3a5c3`  
		Last Modified: Fri, 06 Aug 2021 22:05:04 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ba11c3d005e91c99eb12877162542d7b5d748c61cf8d8397dc694af617f30ed`  
		Last Modified: Fri, 06 Aug 2021 22:09:27 GMT  
		Size: 25.2 MB (25158678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee9a6f6fe3a09cb7a8cf0361d963c285674905cc88daeee188e8a2c1b48fe52`  
		Last Modified: Fri, 06 Aug 2021 22:09:09 GMT  
		Size: 7.7 KB (7731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c63b8e60e33f284d337841a4b6786130d97619b45f99b66f3545878b2c470e`  
		Last Modified: Fri, 06 Aug 2021 22:09:10 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8427fe8b81522c5b026455448e1a761e8b0a64c46551fb1080f1ae98ea5a3d00`  
		Last Modified: Fri, 06 Aug 2021 22:09:09 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5519c79e8d396163a2d758349ea2a9fd1f26a6ed50630a608eac3b8cbecde2`  
		Last Modified: Fri, 06 Aug 2021 22:09:10 GMT  
		Size: 4.4 KB (4408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add7270837da9aaf5f8f68cc7f5f3a4eb4bebebfbacde32aebe9f2455c6ac000`  
		Last Modified: Fri, 06 Aug 2021 22:09:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine3.14` - linux; arm variant v7

```console
$ docker pull postgres@sha256:11632d615137566c45ea7f99f49fd82ddf555720f4e0c0a93d6a0db2bd94f54c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26721210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9831133338a1435b6ee4151334a4b7d3be142b6aaa4dd716a90ea2d6aacc8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 30 Jul 2021 18:36:19 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Fri, 30 Jul 2021 18:36:20 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 08:46:13 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 31 Jul 2021 08:46:14 GMT
ENV LANG=en_US.utf8
# Sat, 31 Jul 2021 08:46:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 31 Jul 2021 09:07:23 GMT
ENV PG_MAJOR=10
# Sat, 31 Jul 2021 09:07:23 GMT
ENV PG_VERSION=10.17
# Sat, 31 Jul 2021 09:07:23 GMT
ENV PG_SHA256=5af28071606c9cd82212c19ba584657a9d240e1c4c2da28fc1f3998a2754b26c
# Sat, 31 Jul 2021 09:10:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 31 Jul 2021 09:11:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 31 Jul 2021 09:11:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 31 Jul 2021 09:11:03 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 31 Jul 2021 09:11:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 31 Jul 2021 09:11:06 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 31 Jul 2021 09:11:07 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Sat, 31 Jul 2021 09:11:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 09:11:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 09:11:10 GMT
STOPSIGNAL SIGINT
# Sat, 31 Jul 2021 09:11:10 GMT
EXPOSE 5432
# Sat, 31 Jul 2021 09:11:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb35baa25c11884b4612eb293d3c04919a6b81cb8bd498efd53277e8af230a1`  
		Last Modified: Sat, 31 Jul 2021 09:19:40 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51e9449fda7b836d81f89b815e2250c46f73f87ce2e2d82171983d06a25a25b`  
		Last Modified: Sat, 31 Jul 2021 09:19:40 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5ac87740e80f97b0079899ac01f3072b0fa8cbf9b113b47a52aa4eaef5d6824`  
		Last Modified: Sat, 31 Jul 2021 09:24:17 GMT  
		Size: 24.3 MB (24279252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0466a926e0128a2a32130be37432288f1e8d1ff976f5912030cf57cc5df747b8`  
		Last Modified: Sat, 31 Jul 2021 09:24:00 GMT  
		Size: 7.7 KB (7729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d4e8c5ae84f58528336d60d67da8b63413df0a6cfc96780e1ab262b215eae4`  
		Last Modified: Sat, 31 Jul 2021 09:24:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02cb73ed855dac7fae5a56523dd0a1ce03ac150373fa78ff5ede15a05a88e7a`  
		Last Modified: Sat, 31 Jul 2021 09:24:00 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d3cc5a3ad7b581288b9624acb4b56773057d54f496480ad1b903df572aa0c8`  
		Last Modified: Sat, 31 Jul 2021 09:24:00 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2727deb44fba790606f7a3ea15de444e981896e2d807a8c6e20e919b91ea1f5c`  
		Last Modified: Sat, 31 Jul 2021 09:24:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:a2874bdb0d2ace3a5186f2145718818fb9c4dbd6c0abb97b0560f82b1487b8e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.4 MB (28359334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d28712cac4ad7951d14749077c6970fb194bf453c363489c696bef3a5199a41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 23:08:22 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 16 Jun 2021 23:08:23 GMT
ENV LANG=en_US.utf8
# Wed, 16 Jun 2021 23:08:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 16 Jun 2021 23:33:54 GMT
ENV PG_MAJOR=10
# Wed, 16 Jun 2021 23:33:54 GMT
ENV PG_VERSION=10.17
# Wed, 16 Jun 2021 23:33:54 GMT
ENV PG_SHA256=5af28071606c9cd82212c19ba584657a9d240e1c4c2da28fc1f3998a2754b26c
# Fri, 25 Jun 2021 19:12:35 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 25 Jun 2021 19:12:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 25 Jun 2021 19:12:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 25 Jun 2021 19:12:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 25 Jun 2021 19:12:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 25 Jun 2021 19:12:38 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 25 Jun 2021 19:12:39 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 25 Jun 2021 19:12:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 25 Jun 2021 19:12:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 25 Jun 2021 19:12:40 GMT
STOPSIGNAL SIGINT
# Fri, 25 Jun 2021 19:12:40 GMT
EXPOSE 5432
# Fri, 25 Jun 2021 19:12:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014ca0527e174cf1bce26a8ba236f17ca0ffd4ebd97fd99b18dd76c382ea5bca`  
		Last Modified: Fri, 25 Jun 2021 19:17:39 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9ed2adb5ac9aa385033227091a3f86d6ea0b74ea30e6ee625da34db4ca5a20`  
		Last Modified: Fri, 25 Jun 2021 19:17:39 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc0a8caeb230a5ef4854b032480facbf08fab1f01e9415ae6bb0d3fa552170f`  
		Last Modified: Fri, 25 Jun 2021 19:19:15 GMT  
		Size: 25.6 MB (25635661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac49140592fd255ec25d79d4f3940303928594ebb204da8f359cc2b26c62749c`  
		Last Modified: Fri, 25 Jun 2021 19:19:08 GMT  
		Size: 7.7 KB (7730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69728477d3881d1b4a115f5e330bc3eb6a8b6478c1b806a70bb49f45bc398a04`  
		Last Modified: Fri, 25 Jun 2021 19:19:08 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc032a91f7b898cbaa9e19cfa4acf7113279f519c4c8b5918944706e09582d94`  
		Last Modified: Fri, 25 Jun 2021 19:19:08 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f370cec689ae0a64590c7241239b9fea1ed48ef7122283e0ffd7190c5d9842`  
		Last Modified: Fri, 25 Jun 2021 19:19:08 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce79edd0f0eb58ca135607b774306d70b7d650ed6a8d6011aece1e18a0a61b28`  
		Last Modified: Fri, 25 Jun 2021 19:19:08 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine3.14` - linux; 386

```console
$ docker pull postgres@sha256:7c8d3d056216d8639ca64d40666f6fcd45f1d824f8d6127d709636c97e6ab675
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.6 MB (29557873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f05f4276ef0e51c6ce40e6091c27872e0d55e0c849ac64047057e8a9b6bbf2da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 06 Aug 2021 17:38:26 GMT
ADD file:bafaec4a54d6cef99b5f3660d074a3d2251e4d4bd09df9ea65f33e9bffb7d88d in / 
# Fri, 06 Aug 2021 17:38:26 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 21:44:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 06 Aug 2021 21:44:57 GMT
ENV LANG=en_US.utf8
# Fri, 06 Aug 2021 21:44:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 06 Aug 2021 22:12:59 GMT
ENV PG_MAJOR=10
# Fri, 06 Aug 2021 22:13:00 GMT
ENV PG_VERSION=10.17
# Fri, 06 Aug 2021 22:13:00 GMT
ENV PG_SHA256=5af28071606c9cd82212c19ba584657a9d240e1c4c2da28fc1f3998a2754b26c
# Fri, 06 Aug 2021 22:17:06 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 06 Aug 2021 22:17:07 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 06 Aug 2021 22:17:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 06 Aug 2021 22:17:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 06 Aug 2021 22:17:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 06 Aug 2021 22:17:11 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 06 Aug 2021 22:17:12 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 06 Aug 2021 22:17:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 06 Aug 2021 22:17:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Aug 2021 22:17:14 GMT
STOPSIGNAL SIGINT
# Fri, 06 Aug 2021 22:17:15 GMT
EXPOSE 5432
# Fri, 06 Aug 2021 22:17:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:935703e1179e32e201e4a36d5664d58299dc8e7bcac197b70c295c0a59216db1`  
		Last Modified: Fri, 06 Aug 2021 17:39:15 GMT  
		Size: 2.8 MB (2821910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c05efe598158ae45c83841ac5ec7934faa5d733f5fcfe85b0261cf9c987262`  
		Last Modified: Fri, 06 Aug 2021 22:25:16 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf37feeefc8b50739451550bcd2f9738e9369d3eea1e7c8fe5fbd0ee22ba530`  
		Last Modified: Fri, 06 Aug 2021 22:25:15 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04f3471f60cb11dd4c9b6368ae793b1ddc1e468f33d8310d2206d978301eb9ff`  
		Last Modified: Fri, 06 Aug 2021 22:27:59 GMT  
		Size: 26.7 MB (26721914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd3b29d108509cd2bfee98101d29ce700254be75a691179851172f92bdd257`  
		Last Modified: Fri, 06 Aug 2021 22:27:51 GMT  
		Size: 7.7 KB (7732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a22e7213d35c2d3cbc2a7d1a2654335eb97b87cdc34a131db331f8ea8620eca`  
		Last Modified: Fri, 06 Aug 2021 22:27:52 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372b2ebcb9bc77a696131cb4950cb0f16ec65e855e28cfbe4b914e223f0aac73`  
		Last Modified: Fri, 06 Aug 2021 22:27:51 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd28e4515fa18992bb0909519803ec67e57d3ab6f00b76e2a80dfd47897f25a6`  
		Last Modified: Fri, 06 Aug 2021 22:27:51 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e9edb490f8fe786c7fd4a035594ae77145061ff7a7a77a51b4e99eb9409d43`  
		Last Modified: Fri, 06 Aug 2021 22:27:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine3.14` - linux; ppc64le

```console
$ docker pull postgres@sha256:3f2be8f370840a58fec543e0e5ffe325436d5ca1c486ca1e7ed1b7056a07ad7c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.9 MB (29949195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85fee73521156bcbb657909387d91c9eb5a39dead4763d720ac97b234483510e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 30 Jul 2021 17:24:32 GMT
ADD file:0075aad7a94f0496483442bb2d9fdaa13e9c23087b90638d014b4bc263aa3861 in / 
# Fri, 30 Jul 2021 17:24:37 GMT
CMD ["/bin/sh"]
# Sat, 31 Jul 2021 04:50:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 31 Jul 2021 04:50:29 GMT
ENV LANG=en_US.utf8
# Sat, 31 Jul 2021 04:50:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 31 Jul 2021 05:12:55 GMT
ENV PG_MAJOR=10
# Sat, 31 Jul 2021 05:13:01 GMT
ENV PG_VERSION=10.17
# Sat, 31 Jul 2021 05:13:05 GMT
ENV PG_SHA256=5af28071606c9cd82212c19ba584657a9d240e1c4c2da28fc1f3998a2754b26c
# Sat, 31 Jul 2021 05:15:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 31 Jul 2021 05:16:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 31 Jul 2021 05:16:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 31 Jul 2021 05:16:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 31 Jul 2021 05:16:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 31 Jul 2021 05:16:21 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 31 Jul 2021 05:16:22 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Sat, 31 Jul 2021 05:16:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Sat, 31 Jul 2021 05:16:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 31 Jul 2021 05:16:35 GMT
STOPSIGNAL SIGINT
# Sat, 31 Jul 2021 05:16:38 GMT
EXPOSE 5432
# Sat, 31 Jul 2021 05:16:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:baf144cfb66ebe9df1969f3b90f1c448beff98edc84de1ccb5d6346195a070d4`  
		Last Modified: Tue, 15 Jun 2021 22:27:38 GMT  
		Size: 2.8 MB (2810478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5f794a079d1d5ec0aa9085986653d7caa23aa1abe999799df2ccfb9f0c85d4`  
		Last Modified: Sat, 31 Jul 2021 05:22:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39fc1a74a4b6fbe04c448f2a92565605cbf2302b989835cdf98b4345478b473e`  
		Last Modified: Sat, 31 Jul 2021 05:22:34 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ed4034fa5706d75a24c2866fce3872d610a2cae370710bba53f325813765e0`  
		Last Modified: Sat, 31 Jul 2021 05:24:56 GMT  
		Size: 27.1 MB (27124673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcc655b1ffff3905d35dcef12fec8355c913eae3a73687a6be44df6a76f7f5c`  
		Last Modified: Sat, 31 Jul 2021 05:24:47 GMT  
		Size: 7.7 KB (7729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29df65e451041be13fed24ae509c35a3f75ff8f3ce8dc43e922b40bf79fe9839`  
		Last Modified: Sat, 31 Jul 2021 05:24:47 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9cc374b7b8200bf136b6f66cb1218684ea3c69e17d1a0286c77325498e26fe`  
		Last Modified: Sat, 31 Jul 2021 05:24:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eeec0f62a8e9dd68da5993e2856b19774ecebe165a17fba05ea5ba3b5b6da6f`  
		Last Modified: Sat, 31 Jul 2021 05:24:47 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c56b308faf4084f74200c828bcbc1e85404495ab94870e91a5044de3b2d2703`  
		Last Modified: Sat, 31 Jul 2021 05:24:48 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
