## `postgres:9-alpine`

```console
$ docker pull postgres@sha256:5c0bbae3a3fe5c0300d377f307c98d49a6c37892f48bb17d79e681c454447e1f
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
$ docker pull postgres@sha256:4d5972a9ba861a7fdc9a0be9ee50b169207b4ad070b69a50d0316d34e3206dbf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14937696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e25d1ad8712238101166337b6e6058d3b85694a15a4f008ae097d7014fa3e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 15 Jan 2021 02:23:51 GMT
ADD file:edbe213ae0c825a5bfbe569928cf20f683f334f93a093ccd0a3a014b7428e760 in / 
# Fri, 15 Jan 2021 02:23:51 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:35:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 21 Jan 2021 19:35:15 GMT
ENV LANG=en_US.utf8
# Thu, 21 Jan 2021 19:35:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Jan 2021 20:01:03 GMT
ENV PG_MAJOR=9.6
# Thu, 21 Jan 2021 20:01:03 GMT
ENV PG_VERSION=9.6.20
# Thu, 21 Jan 2021 20:01:03 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Thu, 21 Jan 2021 20:04:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 21 Jan 2021 20:04:44 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 21 Jan 2021 20:04:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 21 Jan 2021 20:04:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Jan 2021 20:04:48 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 21 Jan 2021 20:04:48 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Jan 2021 20:04:48 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 21 Jan 2021 20:04:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 21 Jan 2021 20:04:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Jan 2021 20:04:51 GMT
STOPSIGNAL SIGINT
# Thu, 21 Jan 2021 20:04:51 GMT
EXPOSE 5432
# Thu, 21 Jan 2021 20:04:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:596ba82af5aaa3e2fd9d6f955b8b94f0744a2b60710e3c243ba3e4a467f051d1`  
		Last Modified: Fri, 15 Jan 2021 02:08:10 GMT  
		Size: 2.8 MB (2810825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8271b35503fb62bfa2f68a3a5f2f051276650964585403ee69453c552ecf5838`  
		Last Modified: Thu, 21 Jan 2021 20:13:16 GMT  
		Size: 1.2 KB (1248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fde607c214b2eb1f39958d85758ee4a83c5caab88fd4deefb7e2e8d2985ce20`  
		Last Modified: Thu, 21 Jan 2021 20:13:16 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb13ead9f9ccade20b9d67327277d6d3bf0f68e3996f2884c7ef6868de06ef62`  
		Last Modified: Thu, 21 Jan 2021 20:15:29 GMT  
		Size: 12.1 MB (12113538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2c04ace0b35a53f33bdcf227842f00c8caf5d2ff73baa47c59611dfa64cb47`  
		Last Modified: Thu, 21 Jan 2021 20:15:23 GMT  
		Size: 7.2 KB (7152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c055340aae6b4af9079425c4cc1cb69779b3e468489f2eae014808e3fd402e9`  
		Last Modified: Thu, 21 Jan 2021 20:15:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce32fc8719a24c13d11394ed74b12d16a2af3fa9f150b2a280928e68289c4f`  
		Last Modified: Thu, 21 Jan 2021 20:15:24 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed0fbbcbe2ea7452554863bc158959a84b0a0feeeb8c59fae46715cd4414174`  
		Last Modified: Thu, 21 Jan 2021 20:15:24 GMT  
		Size: 4.4 KB (4404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f551754aba2663daa9b26b8cc07a9d7215bd1993de16a57b7bf2723b6bb1fb`  
		Last Modified: Thu, 21 Jan 2021 20:15:25 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:36bfe9991d830564d73dbabf36443f295266ae523c8edcac9d6b19182e74b8ec
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14321946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9b19fb3ac239eacd2d03164a3057a6a6623237807038cee3a3f77e0dbdb925`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 15 Jan 2021 01:51:19 GMT
ADD file:f2665ccfd90cf53580dc87c3e57db7c223147c686554b1d6e3fc166cce818b3e in / 
# Fri, 15 Jan 2021 01:51:20 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:14:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 21 Jan 2021 19:14:20 GMT
ENV LANG=en_US.utf8
# Thu, 21 Jan 2021 19:14:23 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Jan 2021 19:30:29 GMT
ENV PG_MAJOR=9.6
# Thu, 21 Jan 2021 19:30:30 GMT
ENV PG_VERSION=9.6.20
# Thu, 21 Jan 2021 19:30:31 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Thu, 21 Jan 2021 19:32:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 21 Jan 2021 19:32:55 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 21 Jan 2021 19:32:58 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 21 Jan 2021 19:33:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Jan 2021 19:33:02 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 21 Jan 2021 19:33:04 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Jan 2021 19:33:05 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:33:08 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 21 Jan 2021 19:33:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Jan 2021 19:33:11 GMT
STOPSIGNAL SIGINT
# Thu, 21 Jan 2021 19:33:12 GMT
EXPOSE 5432
# Thu, 21 Jan 2021 19:33:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b550170d5d44558603032e2371fa7a2fb3575b38b2c64ad8be4ab798bcad44d3`  
		Last Modified: Fri, 15 Jan 2021 01:52:01 GMT  
		Size: 2.6 MB (2621576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d448e33e6bbf937388e1317851d5b4a9b18f803f906acfe3dde0ac64bb61697`  
		Last Modified: Thu, 21 Jan 2021 19:36:34 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7df0858d3f1f356d20ed21ced80cc18a075092bce592c17bb60dc14b42497b1`  
		Last Modified: Thu, 21 Jan 2021 19:36:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e62025433d56044177572186df6279edc33cfdcb6624cce8f880703f39bcb3`  
		Last Modified: Thu, 21 Jan 2021 19:38:29 GMT  
		Size: 11.7 MB (11686899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3a5bec00c03fc912b432fa17c83637a49efda1c2f9e9dac19d39fbe7fae27c`  
		Last Modified: Thu, 21 Jan 2021 19:38:20 GMT  
		Size: 7.2 KB (7160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fac64b8dda9a331a3507594c39525166d882dc1b9768b715450243131468d3`  
		Last Modified: Thu, 21 Jan 2021 19:38:20 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a7fbb589e950ad6955193369b7c8ae220af9d0999cabb50ef9b2e501cebcef`  
		Last Modified: Thu, 21 Jan 2021 19:38:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fd1a7d3673dfe15bd5d42787fae26cbb4d87793fa7b11884266152753f35c4`  
		Last Modified: Thu, 21 Jan 2021 19:38:21 GMT  
		Size: 4.4 KB (4407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1c240a2f853945e3048e1d6be0d047f183debe29cd06a5180e0cefe764b5a4`  
		Last Modified: Thu, 21 Jan 2021 19:38:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:949a944bca821d3c16fcdd9f0613b3cb606f39d1e8e0c7df651ac5af6cc098bf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.4 MB (13438909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8900fe92c58f9d8f455f7aaf613618e60bd008a72775b6f3aecf6ab25ccf76e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 15 Jan 2021 01:58:27 GMT
ADD file:718d7c24a8d6ff0feb2843cf8c3ca4b7ef1fb523a45dea568404259a7b4e6f10 in / 
# Fri, 15 Jan 2021 01:58:29 GMT
CMD ["/bin/sh"]
# Thu, 21 Jan 2021 19:33:26 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 21 Jan 2021 19:33:27 GMT
ENV LANG=en_US.utf8
# Thu, 21 Jan 2021 19:33:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 21 Jan 2021 19:48:58 GMT
ENV PG_MAJOR=9.6
# Thu, 21 Jan 2021 19:48:59 GMT
ENV PG_VERSION=9.6.20
# Thu, 21 Jan 2021 19:49:00 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Thu, 21 Jan 2021 19:51:33 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 21 Jan 2021 19:51:36 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 21 Jan 2021 19:51:39 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 21 Jan 2021 19:51:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 21 Jan 2021 19:51:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 21 Jan 2021 19:51:44 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 21 Jan 2021 19:51:46 GMT
COPY file:e881105b30bb0f1591c0f7f6dfe19bf5351d029d5babae597d2698e04a16ec8b in /usr/local/bin/ 
# Thu, 21 Jan 2021 19:51:49 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Thu, 21 Jan 2021 19:51:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 21 Jan 2021 19:51:53 GMT
STOPSIGNAL SIGINT
# Thu, 21 Jan 2021 19:51:54 GMT
EXPOSE 5432
# Thu, 21 Jan 2021 19:51:55 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0f34ce5da94097b8c334f6b2065a010aced9855c3532e4462e9bd1b0a4c4b3f6`  
		Last Modified: Fri, 15 Jan 2021 01:59:13 GMT  
		Size: 2.4 MB (2422744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf09b586dfdfa5ab7c32f77d7b47d5cbe837f3bb208ff5d8a1aff7e6319cd68`  
		Last Modified: Thu, 21 Jan 2021 19:56:21 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb68f76f06b0f78f7efb32a0e3ef242626ed667717e56fe28f2e2d4adf84c8a6`  
		Last Modified: Thu, 21 Jan 2021 19:56:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea67c5cddf98044052b11955868040ea58e9dba599e7a64485fbe29a049f77fc`  
		Last Modified: Thu, 21 Jan 2021 19:59:08 GMT  
		Size: 11.0 MB (11002705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2208e7f11ebd6718af97656c386db59f23a496e567c89be744cce3460fc35e`  
		Last Modified: Thu, 21 Jan 2021 19:59:00 GMT  
		Size: 7.2 KB (7156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eeff0d3f90ff3d26459212dac7e6ab94f45ef70f19956c90ad5117590353ef1`  
		Last Modified: Thu, 21 Jan 2021 19:59:01 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56787bfa15644fc715ce75432239331489ab7ae54ad1aaed80688319d2563f`  
		Last Modified: Thu, 21 Jan 2021 19:59:00 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec6385b012f2b89161c730657e81d1f6d45a8c194e13019e88d9b696ded3d6d`  
		Last Modified: Thu, 21 Jan 2021 19:59:00 GMT  
		Size: 4.4 KB (4401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28caeccda53aafca11560e02fd69bf4779521c2fc4cfe429835a8cd29447ebc2`  
		Last Modified: Thu, 21 Jan 2021 19:59:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:93d8a27afa2a6c63bfed7d162c5dbb6b36987b58e3c8c4fc592bbf2e11c0eee7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 MB (14240784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27997dc924b5919ebaac7d9be741432c81aad77f8d76e622cedc65206d92d625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:01:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Dec 2020 04:01:19 GMT
ENV LANG=en_US.utf8
# Thu, 17 Dec 2020 04:01:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Dec 2020 04:20:22 GMT
ENV PG_MAJOR=9.6
# Thu, 17 Dec 2020 04:20:23 GMT
ENV PG_VERSION=9.6.20
# Thu, 17 Dec 2020 04:20:25 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Thu, 17 Dec 2020 04:22:52 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 17 Dec 2020 04:22:57 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 17 Dec 2020 04:23:03 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Dec 2020 04:23:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Dec 2020 04:23:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Dec 2020 04:23:08 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Dec 2020 00:45:34 GMT
COPY file:d98720f44754747f666c604efdd82f7c897ce6bdbdfb328f1b7ffc977a4060b7 in /usr/local/bin/ 
# Wed, 30 Dec 2020 00:45:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 30 Dec 2020 00:45:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Dec 2020 00:45:49 GMT
STOPSIGNAL SIGINT
# Wed, 30 Dec 2020 00:45:55 GMT
EXPOSE 5432
# Wed, 30 Dec 2020 00:45:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20223af9aac4511a0a9a78463ff758585620e621be0678319eba90176b7e615`  
		Last Modified: Thu, 17 Dec 2020 04:28:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2482f57ac4ab8ff038d0589f0507eea54d56adf3da98ff95df25c6beb575c1e4`  
		Last Modified: Thu, 17 Dec 2020 04:28:04 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46d87c6b8167ffac1b89447901d049264255ebed26c7e544bb8b0c97ac0df1a`  
		Last Modified: Thu, 17 Dec 2020 04:29:57 GMT  
		Size: 11.5 MB (11518273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8952926e929de220a0d4daf8f607b7f7ac56bc0f4cf34ac929250dc061f42c5a`  
		Last Modified: Thu, 17 Dec 2020 04:29:51 GMT  
		Size: 7.2 KB (7163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00907a241881e56ce6afb9a41fcc6a72391843b3526902f3f1dadd742faa186b`  
		Last Modified: Thu, 17 Dec 2020 04:29:51 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54db1106eb6ce25010a4ce79be3a5a132f5298530ebab86cefc3128759a3f179`  
		Last Modified: Thu, 17 Dec 2020 04:29:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c048d7d94646cacc5f2e0de0195544f087175a97f583107ca8d2f10683431d93`  
		Last Modified: Wed, 30 Dec 2020 00:48:42 GMT  
		Size: 4.4 KB (4393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61cd284405de8263ace80bbf6c4f1b1f8334cc0d9522c7bd1adfcca7e7635c5`  
		Last Modified: Wed, 30 Dec 2020 00:48:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; 386

```console
$ docker pull postgres@sha256:3914c000740ee1540afe736d5c6b56194b91c3aa83cba76cfffd4e0f08d6bc62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15113683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91da971ba4bccbe72f56994255a99f273c81cf8b72f69e80611853f1e728b96f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:32 GMT
ADD file:de33fda50a142403e842620d20bc4404e66fc4ace16edc6946c4539e8a797458 in / 
# Thu, 17 Dec 2020 00:38:32 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 05:49:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Dec 2020 05:49:56 GMT
ENV LANG=en_US.utf8
# Thu, 17 Dec 2020 05:49:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Dec 2020 06:03:30 GMT
ENV PG_MAJOR=9.6
# Thu, 17 Dec 2020 06:03:30 GMT
ENV PG_VERSION=9.6.20
# Thu, 17 Dec 2020 06:03:30 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Fri, 18 Dec 2020 20:50:14 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 18 Dec 2020 20:50:15 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 18 Dec 2020 20:50:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 18 Dec 2020 20:50:16 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 18 Dec 2020 20:50:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 18 Dec 2020 20:50:17 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Dec 2020 00:41:56 GMT
COPY file:d98720f44754747f666c604efdd82f7c897ce6bdbdfb328f1b7ffc977a4060b7 in /usr/local/bin/ 
# Wed, 30 Dec 2020 00:41:57 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 30 Dec 2020 00:41:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Dec 2020 00:41:58 GMT
STOPSIGNAL SIGINT
# Wed, 30 Dec 2020 00:41:58 GMT
EXPOSE 5432
# Wed, 30 Dec 2020 00:41:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:455793c72b878001f0905634ed52a2524ba51796e7377bf00683a85123f7dce9`  
		Last Modified: Thu, 17 Dec 2020 00:39:18 GMT  
		Size: 2.8 MB (2794130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5305178ae8cb85c448e0963870f5425a527c36dae59155568c8da341f4173b82`  
		Last Modified: Thu, 17 Dec 2020 06:07:45 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3614159f507682c618782d96e8e35ed8b175b4dff44e39ef793184e39ba180`  
		Last Modified: Thu, 17 Dec 2020 06:07:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a33958ae23a3ee135349d61f8d01c38a05870913ce45d0c547cc8b75db7b3b1`  
		Last Modified: Fri, 18 Dec 2020 20:56:15 GMT  
		Size: 12.3 MB (12306231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e9195bb494783bdbdd0660882c11db048eb86877e2b1a25aecbb0f2f3f4ff4`  
		Last Modified: Fri, 18 Dec 2020 20:56:11 GMT  
		Size: 7.2 KB (7156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf1c9bc2a6141b5757cb4fbcd71d18d39e2076fdb03eacd8ca366360053bd45`  
		Last Modified: Fri, 18 Dec 2020 20:56:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1bb804d5d1d34a9c351b9f62eef3a38b45b496c9a1a9aa84b4617852db3e67b`  
		Last Modified: Fri, 18 Dec 2020 20:56:10 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677dd4b16a6ed6f020b89a1a82af28a6d42b0487b7e10658476be71d11e5b5a6`  
		Last Modified: Wed, 30 Dec 2020 00:43:35 GMT  
		Size: 4.4 KB (4392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ed346e0aa19e0087b2c6757f9af2192c5d5ba6769d0394a654b830892fd773`  
		Last Modified: Wed, 30 Dec 2020 00:43:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:1ec6d0541da759e7bf35f562aeea0106092d1bc09312507cd0ada318e721fe34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15439028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9655e8da4ea7a50492d5225f880546088393e0092dc8b6cf4472a10a0380551`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 17 Dec 2020 00:20:42 GMT
ADD file:0a38c9b4955f8faa79627c166fca80ef342e443a16ce2925a30eeae317bbd786 in / 
# Thu, 17 Dec 2020 00:20:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 08:27:05 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Dec 2020 08:27:07 GMT
ENV LANG=en_US.utf8
# Thu, 17 Dec 2020 08:27:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Dec 2020 08:47:26 GMT
ENV PG_MAJOR=9.6
# Thu, 17 Dec 2020 08:47:32 GMT
ENV PG_VERSION=9.6.20
# Thu, 17 Dec 2020 08:47:36 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Thu, 17 Dec 2020 08:49:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 17 Dec 2020 08:50:05 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 17 Dec 2020 08:50:10 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 17 Dec 2020 08:50:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 17 Dec 2020 08:50:18 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 17 Dec 2020 08:50:22 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Dec 2020 01:20:59 GMT
COPY file:d98720f44754747f666c604efdd82f7c897ce6bdbdfb328f1b7ffc977a4060b7 in /usr/local/bin/ 
# Wed, 30 Dec 2020 01:21:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 30 Dec 2020 01:21:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Dec 2020 01:21:13 GMT
STOPSIGNAL SIGINT
# Wed, 30 Dec 2020 01:21:17 GMT
EXPOSE 5432
# Wed, 30 Dec 2020 01:21:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a9d343b7bcc225fe7ac17d96a81329510ab7f31a50472311cafe7168d3107317`  
		Last Modified: Thu, 17 Dec 2020 00:21:33 GMT  
		Size: 2.8 MB (2805226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9020dece47a455612905a0f9d5608b39b5cfa68bf304d4473bbbee3f085dce3e`  
		Last Modified: Thu, 17 Dec 2020 08:55:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd7a09fca54bf573268df0318667b22454de76b77537ce6968b9a9e3a5bd2b7`  
		Last Modified: Thu, 17 Dec 2020 08:55:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15893102c7418bd27c2c0082ad7742ae5d0e69b3242eed5bc81408cdabd8ab67`  
		Last Modified: Thu, 17 Dec 2020 08:57:11 GMT  
		Size: 12.6 MB (12620345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c3900046078572db0a950e71210da625a7948bb75e80b1b3bfe2a332761797`  
		Last Modified: Thu, 17 Dec 2020 08:57:04 GMT  
		Size: 7.2 KB (7158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e05efdc5674bcc241ee4db4cc0ff9df2d70a09b11c74d5bef7816944d7846d`  
		Last Modified: Thu, 17 Dec 2020 08:57:04 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d78661e48176d17518ece3d2f6f0f1c83788bc0202f7a60b9d35c3b8e18af3`  
		Last Modified: Thu, 17 Dec 2020 08:57:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49bf9a7b78f97aa3f29113fdf30dd615615cab62a8c6932ac5c2b9e18592b15b`  
		Last Modified: Wed, 30 Dec 2020 01:23:40 GMT  
		Size: 4.4 KB (4396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116ce8672c12482dd61649c907abc75f28cf05c7938885bccb452dacf1c07ac2`  
		Last Modified: Wed, 30 Dec 2020 01:23:39 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:9-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:1f90ffd8e1ed90dc01970b8ce21c645a0617b693355f554ffa317e4f87a0c7f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14072210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe09f3107645b442a47010a74cc0cccd3934dcab0c6fc866605cbae547cb0db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:37 GMT
ADD file:3ad3856d165e8760af85574a8ffa75ca44b7e1b97b64d1d6d4608445efa4b860 in / 
# Wed, 16 Dec 2020 23:41:37 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 09:43:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 17 Dec 2020 09:43:57 GMT
ENV LANG=en_US.utf8
# Thu, 17 Dec 2020 09:43:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 17 Dec 2020 10:01:48 GMT
ENV PG_MAJOR=9.6
# Thu, 17 Dec 2020 10:01:49 GMT
ENV PG_VERSION=9.6.20
# Thu, 17 Dec 2020 10:01:50 GMT
ENV PG_SHA256=3d08cba409d45ab62d42b24431a0d55e7537bcd1db2d979f5f2eefe34d487bb6
# Fri, 18 Dec 2020 23:01:37 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 18 Dec 2020 23:01:41 GMT
RUN sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 18 Dec 2020 23:01:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 18 Dec 2020 23:01:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 18 Dec 2020 23:01:45 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 18 Dec 2020 23:01:46 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 30 Dec 2020 00:46:27 GMT
COPY file:d98720f44754747f666c604efdd82f7c897ce6bdbdfb328f1b7ffc977a4060b7 in /usr/local/bin/ 
# Wed, 30 Dec 2020 00:46:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh / # backwards compat
# Wed, 30 Dec 2020 00:46:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 30 Dec 2020 00:46:30 GMT
STOPSIGNAL SIGINT
# Wed, 30 Dec 2020 00:46:30 GMT
EXPOSE 5432
# Wed, 30 Dec 2020 00:46:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ee52640a49e15b8b7c8edb66c2d048b26abdee8d828d6e5ef4e10a28cb15a84f`  
		Last Modified: Wed, 16 Dec 2020 23:42:15 GMT  
		Size: 2.6 MB (2567018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec909f7d148e1f5c76f40f0fe4cec25c8a0f55dee05e382db0c692d59f7c084f`  
		Last Modified: Fri, 18 Dec 2020 23:05:49 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fadc63f7954f50d02abf819a5f8693cf92f86873d00c4dd5108f7dbbf5e0c48`  
		Last Modified: Fri, 18 Dec 2020 23:05:48 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5176239b5867b77edf4396755a17204392b966860718ec133488dac7729599`  
		Last Modified: Fri, 18 Dec 2020 23:07:21 GMT  
		Size: 11.5 MB (11491731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e3824f15275868bc5c9e66971a7fe3c24d29d1a2abf82840d52a54cbd7e343`  
		Last Modified: Fri, 18 Dec 2020 23:07:18 GMT  
		Size: 7.2 KB (7160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e411a35f99101ee655e0b393ff618781421d9847bbe8e9b39099011580a0545`  
		Last Modified: Fri, 18 Dec 2020 23:07:18 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63961fb349454d857ad0a65569bff82021db9aa9aa206260497bc8f0c76a7ac1`  
		Last Modified: Fri, 18 Dec 2020 23:07:18 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eabfbae595b89fb552a2329bfcc2a8e3b1daa5267ae3d2b5f14892f172cd1acf`  
		Last Modified: Wed, 30 Dec 2020 00:48:28 GMT  
		Size: 4.4 KB (4393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b64a0e4cfa470808be18c02abad6087c16438dbc6b870c22f6f4fa151d0cbb2`  
		Last Modified: Wed, 30 Dec 2020 00:48:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
