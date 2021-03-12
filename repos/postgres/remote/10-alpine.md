## `postgres:10-alpine`

```console
$ docker pull postgres@sha256:047f16b9ac0f7525b9b795a9f650062b661ab9a496ce4d1f737421a5419d6bda
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
$ docker pull postgres@sha256:19cd61536b88e163958b909d04a33edc03511cb8f8b52fe6744c0eaf00c6fdd7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.6 MB (28603117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7b2c46fa5926b7e1e0a325dc467288ee2f1ced74d98fe9c42f93642c611a8df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 21:19:54 GMT
ADD file:80bf8bd014071345b1c0364eeb0a5e48f3fb0d87f9c31cb990e57caa652b59b8 in / 
# Wed, 17 Feb 2021 21:19:54 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 15:26:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Mar 2021 15:26:36 GMT
ENV LANG=en_US.utf8
# Fri, 12 Mar 2021 15:26:37 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Mar 2021 15:49:31 GMT
ENV PG_MAJOR=10
# Fri, 12 Mar 2021 15:49:31 GMT
ENV PG_VERSION=10.16
# Fri, 12 Mar 2021 15:49:31 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Fri, 12 Mar 2021 15:53:56 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Mar 2021 15:53:58 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Mar 2021 15:54:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Mar 2021 15:54:01 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Mar 2021 15:54:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Mar 2021 15:54:03 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Mar 2021 15:54:04 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 12 Mar 2021 15:54:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Mar 2021 15:54:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Mar 2021 15:54:07 GMT
STOPSIGNAL SIGINT
# Fri, 12 Mar 2021 15:54:07 GMT
EXPOSE 5432
# Fri, 12 Mar 2021 15:54:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ba3557a56b150f9b813f9d02274d62914fd8fce120dd374d9ee17b87cf1d277d`  
		Last Modified: Wed, 17 Feb 2021 21:20:25 GMT  
		Size: 2.8 MB (2811657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba41e371f09ceda8ea570b685d8f7db61c8615eadf30756d81a62f7d61289a74`  
		Last Modified: Fri, 12 Mar 2021 16:06:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ca07debf1d3613aa92cbe55cf0578603c9c9ae5c089c320f890ce41820f58a`  
		Last Modified: Fri, 12 Mar 2021 16:06:01 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf974a756dc9caf12d30292e20aff96bbfba79bb94efb27743b89e2c13cf1be5`  
		Last Modified: Fri, 12 Mar 2021 16:08:43 GMT  
		Size: 25.8 MB (25777799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3c682c8006db0f44bcae6f193e580c04268ff5a5e4439c1cabe352d27c9ad9`  
		Last Modified: Fri, 12 Mar 2021 16:08:35 GMT  
		Size: 7.3 KB (7350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a21d061b4179c76fb1a54e6ba634c69e9debf47eb856ebf4fc37e17cd5e6d8`  
		Last Modified: Fri, 12 Mar 2021 16:08:35 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171ec6c84bf975c5bdedfdaca57cbea2ce7c1971c3d7c02cb89ab8798b29247f`  
		Last Modified: Fri, 12 Mar 2021 16:08:35 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f21661538293246f4791990255c86e02bdf49e43f7e4b39e89c37cff05ee5`  
		Last Modified: Fri, 12 Mar 2021 16:08:35 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fbe9abac3615440dd230ae9ca1a2311469b8fa83a8e5eef340cac070b06549`  
		Last Modified: Fri, 12 Mar 2021 16:08:35 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:5dd81de2f77bac14e7b1df254d906c968d0e56eb18c6d625a8b381541eeb4982
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 MB (27731356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af8d1812535aac59d47115aa8457943f864465ca8c952dcfd88c922ab4ef954`
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
# Wed, 17 Feb 2021 23:17:14 GMT
ENV PG_MAJOR=10
# Wed, 17 Feb 2021 23:17:15 GMT
ENV PG_VERSION=10.16
# Wed, 17 Feb 2021 23:17:17 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Wed, 17 Feb 2021 23:20:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:20:07 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:20:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:20:10 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:20:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:20:13 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:20:15 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:20:20 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 23:20:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:20:24 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:20:27 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:20:29 GMT
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
	-	`sha256:e5b3474c7579dec68e68a99e93ce8e19f69509102e8c3e06e0e7c7e26fec318b`  
		Last Modified: Wed, 17 Feb 2021 23:28:35 GMT  
		Size: 25.1 MB (25095654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc14f683c32d2e9cff8b035f019e9480660d12a86a286aff444f155985f053c`  
		Last Modified: Wed, 17 Feb 2021 23:28:25 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c347266be0ce874bc389ab71a4df82d643bd4cd1355908fd4105d45b30bf90a7`  
		Last Modified: Wed, 17 Feb 2021 23:28:25 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0af9a1837964336209cd3e1a6214ffee5bef9ee5f3808dcf46a31c33d41ccc9`  
		Last Modified: Wed, 17 Feb 2021 23:28:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8630e796a6cd30524dda857874ef34606e0a5c5ddef6ded9df8ad60699a1b9b1`  
		Last Modified: Wed, 17 Feb 2021 23:28:25 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718cdf8f5cd50714f2d4459a27d59ef3a9cb09e3193e130ad9c301e17d29f1fe`  
		Last Modified: Wed, 17 Feb 2021 23:28:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7462158693df6c80c088283a46491bf13682c81a0173ba21021f4f400677a7d2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26665567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f5f1b5fc3d438b06bc6d3c777b7fae30cf75ead1bc5eaa0a6d46c68ff8cbd9`
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
# Wed, 17 Feb 2021 23:49:51 GMT
ENV PG_MAJOR=10
# Wed, 17 Feb 2021 23:49:52 GMT
ENV PG_VERSION=10.16
# Wed, 17 Feb 2021 23:49:53 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Wed, 17 Feb 2021 23:52:36 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:52:40 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:52:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:52:43 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:52:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:52:46 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:52:46 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:52:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 23:52:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:52:51 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:52:51 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:52:52 GMT
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
	-	`sha256:e1e452e300e8c74ec145d44e78b2f1ea7fc9da3cbd6271494c6103070fa96733`  
		Last Modified: Thu, 18 Feb 2021 00:02:03 GMT  
		Size: 24.2 MB (24228024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aafbce3ed0ded2898fac4e436730c5b064c319200628385c6dbe26b2746afd`  
		Last Modified: Thu, 18 Feb 2021 00:01:54 GMT  
		Size: 7.3 KB (7347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56956bec494b68dfd3718b2d8c5eed040e1db4d409324ffa4722d5246578a4e4`  
		Last Modified: Thu, 18 Feb 2021 00:01:54 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25213d7b73ce5c6eeffb21893a38adc913f06d2d551b66f62ec145e80b52627`  
		Last Modified: Thu, 18 Feb 2021 00:01:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ba1ad8d4d7e1b124383d8c7004d535cc2b9c269d87459e179021fe4b5531d0`  
		Last Modified: Thu, 18 Feb 2021 00:01:54 GMT  
		Size: 4.4 KB (4402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c55b3a22c0f1cca3b48ab73201f3b6317d6308daabd589c13cd19c6bdce1273`  
		Last Modified: Thu, 18 Feb 2021 00:01:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:730e6e580c902ec98560f279769a8434bc792ce47adcd75eba46a1ace125120d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.3 MB (28309862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5a15791dc0013b54d6665ffe683b0242337aca858dbcfad1315085f09b4b13`
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
# Wed, 17 Feb 2021 23:28:34 GMT
ENV PG_MAJOR=10
# Wed, 17 Feb 2021 23:28:34 GMT
ENV PG_VERSION=10.16
# Wed, 17 Feb 2021 23:28:35 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Wed, 17 Feb 2021 23:31:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 17 Feb 2021 23:31:27 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 17 Feb 2021 23:31:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 17 Feb 2021 23:31:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 17 Feb 2021 23:31:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 17 Feb 2021 23:31:35 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 17 Feb 2021 23:31:36 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Wed, 17 Feb 2021 23:31:38 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 17 Feb 2021 23:31:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Feb 2021 23:31:40 GMT
STOPSIGNAL SIGINT
# Wed, 17 Feb 2021 23:31:41 GMT
EXPOSE 5432
# Wed, 17 Feb 2021 23:31:41 GMT
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
	-	`sha256:43567d0f384a86ad8b86005c8413f2cee28eeed54cb8964318603e437e9099fe`  
		Last Modified: Wed, 17 Feb 2021 23:40:13 GMT  
		Size: 25.6 MB (25584625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6f066f0a6a4c0b4a44845fa96ac842be528c5e08ba3086f4f1648aeccec06`  
		Last Modified: Wed, 17 Feb 2021 23:40:06 GMT  
		Size: 7.4 KB (7354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41d5a95a80dba99c7bbdcd11445bd9712c1840da557e82ab63c8c28baae3330`  
		Last Modified: Wed, 17 Feb 2021 23:40:05 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48d1cfc58394f45587e7d91b2045991498b5baf8fe9f3b828e55f2ebf36643b`  
		Last Modified: Wed, 17 Feb 2021 23:40:05 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4773017028d9502e05a648a7cec4061059b240b0f74845100fe16908c2a5e3f7`  
		Last Modified: Wed, 17 Feb 2021 23:40:05 GMT  
		Size: 4.4 KB (4406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982b2ed72c47349130209c719c1d160b9178f4c48eba8b778a5bc1e283a2f696`  
		Last Modified: Wed, 17 Feb 2021 23:40:05 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; 386

```console
$ docker pull postgres@sha256:7effe30549e31eb025472757f8e6b1bde14cc511a41453800cb14d4526c7564f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 MB (29534857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71037a7d5f13f60152f95c89bee3531542193be52a40d7b517ae4a3dfcc0400`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 20:22:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Mar 2021 20:22:43 GMT
ENV LANG=en_US.utf8
# Fri, 12 Mar 2021 20:22:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Mar 2021 20:49:36 GMT
ENV PG_MAJOR=10
# Fri, 12 Mar 2021 20:49:36 GMT
ENV PG_VERSION=10.16
# Fri, 12 Mar 2021 20:49:36 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Fri, 12 Mar 2021 20:54:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Mar 2021 20:54:33 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Mar 2021 20:54:34 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Mar 2021 20:54:34 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Mar 2021 20:54:35 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Mar 2021 20:54:35 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Mar 2021 20:54:36 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Fri, 12 Mar 2021 20:54:36 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Fri, 12 Mar 2021 20:54:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Mar 2021 20:54:37 GMT
STOPSIGNAL SIGINT
# Fri, 12 Mar 2021 20:54:37 GMT
EXPOSE 5432
# Fri, 12 Mar 2021 20:54:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e729ac31be078df1147e7d573e4eae1419b7e8af9e15f0a1d1c82ca4e57e8b0f`  
		Last Modified: Fri, 12 Mar 2021 21:06:54 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8d26371d9431aa45553c82bf8bd7314116c124e7aa94a92da6992533c2ec16`  
		Last Modified: Fri, 12 Mar 2021 21:06:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0112fb3231cc312909c44b6455fbc8eee2d0ede417c0757dd0a6938443e14e2d`  
		Last Modified: Fri, 12 Mar 2021 21:10:23 GMT  
		Size: 26.7 MB (26703022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c458994fdc5c69669eb962b91a343e110881af399d492b9928a72f142aeb605c`  
		Last Modified: Fri, 12 Mar 2021 21:10:15 GMT  
		Size: 7.3 KB (7350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a27f7e9f61e40692df404f1ebc0bc0ca8806ac62d798aaa0c1edcf8e97df31a`  
		Last Modified: Fri, 12 Mar 2021 21:10:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666f66bc50105e84c723d827162fa8e9730733627cebf61898072fbab32c89d1`  
		Last Modified: Fri, 12 Mar 2021 21:10:15 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4dfa497a46b89bc93178ecc088c75f371a0cc58c5f3fbfd0daaa2a84d6b4276`  
		Last Modified: Fri, 12 Mar 2021 21:10:15 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1e11980b205140fc281b892d65f6b7f43c02dfc06374a66e621185baa452c7`  
		Last Modified: Fri, 12 Mar 2021 21:10:16 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:15aa8672d09a7b1e3c247f33f0edd98c85514d8aa0cc4c4c8177a2cf24a714f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29798543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78166ecbdea23138d53baeaa43d6da34e1a5aced6d54705f92c3a2bb0855a10c`
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
# Thu, 18 Feb 2021 00:01:04 GMT
ENV PG_MAJOR=10
# Thu, 18 Feb 2021 00:01:10 GMT
ENV PG_VERSION=10.16
# Thu, 18 Feb 2021 00:01:16 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 18 Feb 2021 00:04:24 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 18 Feb 2021 00:04:44 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 18 Feb 2021 00:04:54 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 18 Feb 2021 00:04:59 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Feb 2021 00:05:19 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 18 Feb 2021 00:05:24 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Feb 2021 00:05:29 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 18 Feb 2021 00:05:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 18 Feb 2021 00:05:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 00:05:50 GMT
STOPSIGNAL SIGINT
# Thu, 18 Feb 2021 00:05:55 GMT
EXPOSE 5432
# Thu, 18 Feb 2021 00:06:00 GMT
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
	-	`sha256:58334dec4b1da80dddf65b87a1b4972fc1c821963bb7ae7262b73f8116aaa4ab`  
		Last Modified: Thu, 18 Feb 2021 00:18:18 GMT  
		Size: 27.0 MB (26971804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf3866957cced1efd49079f85d31b7eb507b60f560d0b3f4ca23b844478cae8`  
		Last Modified: Thu, 18 Feb 2021 00:18:09 GMT  
		Size: 7.4 KB (7351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f70f34ecb198daec83ed6ed4a9c573045422f8feb924932124477d2bd66a5970`  
		Last Modified: Thu, 18 Feb 2021 00:18:09 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6dfcb1d3e7df04f475c80bbdc3cfc155dede3de74b1420cb806a7eb21b97a7a`  
		Last Modified: Thu, 18 Feb 2021 00:18:09 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7171009608744ae99ef83fb1349d28cc45dc26bca993ba77be9254123ef9513`  
		Last Modified: Thu, 18 Feb 2021 00:18:09 GMT  
		Size: 4.4 KB (4405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e4ab15fb7e465f2793eecc7e36ca438021dc9741dbbffef40785ce5b88474c`  
		Last Modified: Thu, 18 Feb 2021 00:18:10 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:10-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:8c995072f17f57f9d5dd5f21385cd2e22b78ac5542cd1fc9872c745332ce090b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28459860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ffbd1487c3a87a3b4f4d4be04aa85d1c68ea17a73bffd343bc55e9f70bde6d`
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
# Thu, 18 Feb 2021 02:05:02 GMT
ENV PG_MAJOR=10
# Thu, 18 Feb 2021 02:05:02 GMT
ENV PG_VERSION=10.16
# Thu, 18 Feb 2021 02:05:02 GMT
ENV PG_SHA256=a35c718b1b6690e01c69626d467edb933784f8d1d6741e21fe6cce0738467bb3
# Thu, 18 Feb 2021 02:06:54 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 18 Feb 2021 02:06:55 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 18 Feb 2021 02:06:56 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 18 Feb 2021 02:06:56 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 18 Feb 2021 02:06:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 18 Feb 2021 02:06:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 18 Feb 2021 02:06:57 GMT
COPY file:ad28506adc606e446eefc263bc99d4cb809e608d4f550956143bf13c82c91f85 in /usr/local/bin/ 
# Thu, 18 Feb 2021 02:06:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 18 Feb 2021 02:06:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Feb 2021 02:06:58 GMT
STOPSIGNAL SIGINT
# Thu, 18 Feb 2021 02:06:59 GMT
EXPOSE 5432
# Thu, 18 Feb 2021 02:06:59 GMT
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
	-	`sha256:1748b3e2ee2bec6a029a6e42aa1cc8a335a837a19b11f995333a92e6e1f211e8`  
		Last Modified: Thu, 18 Feb 2021 02:12:08 GMT  
		Size: 25.8 MB (25843825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb70de6f79f7452604e768f9222c6c0251726cc266ecba7decf23c1dfff6956`  
		Last Modified: Thu, 18 Feb 2021 02:12:03 GMT  
		Size: 7.3 KB (7350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b9188d5af7fbc005bbc155ec18ee98e035090870db5d0c483fcb1c4124c25`  
		Last Modified: Thu, 18 Feb 2021 02:12:03 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618b0d7f23ad30d61c1cb7fcee2fc5fe6dbf18f52ab50670fed3ab6788e3a672`  
		Last Modified: Thu, 18 Feb 2021 02:12:03 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd5a04b6ad19edbc1fe819964854d74daa7d9f6c40d3fdbe387ac0413142358`  
		Last Modified: Thu, 18 Feb 2021 02:12:03 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6776dbaa62be6e3ec5c025daf7febb389889eb52f60e906eaafa8de92d1c8a`  
		Last Modified: Thu, 18 Feb 2021 02:12:03 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
