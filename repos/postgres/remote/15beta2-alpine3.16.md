## `postgres:15beta2-alpine3.16`

```console
$ docker pull postgres@sha256:aa87acaaccedd43a0a1098ecbaf06917d01adf15e500b80ef6a77d8c72686a6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `postgres:15beta2-alpine3.16` - linux; arm variant v6

```console
$ docker pull postgres@sha256:384819e78757b0977014e04b5f8528c376131fb8a21f142a681c978199778215
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.9 MB (84881150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afebda393c67b5007a803e538d7eac00ef1d1cf89143c544607d46a98a3a89c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 May 2022 19:49:32 GMT
ADD file:f7cee617575b5e5a7672d298a519bb8d8b5098efb90aa2a5d7b0510003457d52 in / 
# Mon, 23 May 2022 19:49:33 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 22:54:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 25 May 2022 22:54:04 GMT
ENV LANG=en_US.utf8
# Wed, 25 May 2022 22:54:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 25 May 2022 22:54:06 GMT
ENV PG_MAJOR=15
# Fri, 01 Jul 2022 00:51:06 GMT
ENV PG_VERSION=15beta2
# Fri, 01 Jul 2022 00:51:06 GMT
ENV PG_SHA256=2fedbc58b370f30e5f59fb0dcc8128a2ef9a922b50fa931b442e4fa27ca98830
# Fri, 01 Jul 2022 00:57:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 01 Jul 2022 00:57:30 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 01 Jul 2022 00:57:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Jul 2022 00:57:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Jul 2022 00:57:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Jul 2022 00:57:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Jul 2022 00:57:35 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Fri, 01 Jul 2022 00:57:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Jul 2022 00:57:35 GMT
STOPSIGNAL SIGINT
# Fri, 01 Jul 2022 00:57:36 GMT
EXPOSE 5432
# Fri, 01 Jul 2022 00:57:36 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:79a25ccaf940855872635c06e7614d9b27dd38ffb5a8adfdb9274dfdc0ea0d87`  
		Last Modified: Mon, 23 May 2022 19:08:47 GMT  
		Size: 2.6 MB (2606142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ce185d2eacd6b0f61082b66474ba45a2f13ff27bbae2c58ee0b2da085db2db`  
		Last Modified: Wed, 25 May 2022 23:32:05 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c88d0d1f7487195d34ca2fb5493567418f60bf6dc33e0a43e6c3338928710e5`  
		Last Modified: Wed, 25 May 2022 23:32:06 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62f0a8a7feb04cc0b49ea140924c8f793020aba145924e184df246871da1509`  
		Last Modified: Fri, 01 Jul 2022 01:01:14 GMT  
		Size: 82.3 MB (82259057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a98b1e39beb2f950b7c20ff9032d4830317df7e7e63cd1429e9739ddf4db1ac`  
		Last Modified: Fri, 01 Jul 2022 01:00:26 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cf2768b34531f38a905e4499f1a1768d76d75c244b69beabd4b41dd7afe1a2`  
		Last Modified: Fri, 01 Jul 2022 01:00:26 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e39554716a6d318bd28a5528151f79e9a66ac0ea759f4cac1763aace11c340`  
		Last Modified: Fri, 01 Jul 2022 01:00:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b4a19f1035aed9153000b29f905efc9944d6a9aa33b3aa2012dc41aa691964`  
		Last Modified: Fri, 01 Jul 2022 01:00:26 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta2-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b3ccc4e8f4453e2c73614cd4e652925092cd7058e88782bd31ac00b54dab7384
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85719497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b198309a9ffdfbd1e2560e8b8cfb18fd4c356bbc28f73c7b2cc4e609ec389ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 21:33:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 25 May 2022 21:33:05 GMT
ENV LANG=en_US.utf8
# Wed, 25 May 2022 21:33:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 25 May 2022 21:33:07 GMT
ENV PG_MAJOR=15
# Fri, 01 Jul 2022 00:47:38 GMT
ENV PG_VERSION=15beta2
# Fri, 01 Jul 2022 00:47:39 GMT
ENV PG_SHA256=2fedbc58b370f30e5f59fb0dcc8128a2ef9a922b50fa931b442e4fa27ca98830
# Fri, 01 Jul 2022 00:51:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 01 Jul 2022 00:51:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 01 Jul 2022 00:51:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Jul 2022 00:51:13 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Jul 2022 00:51:14 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Jul 2022 00:51:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Jul 2022 00:51:17 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Fri, 01 Jul 2022 00:51:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Jul 2022 00:51:18 GMT
STOPSIGNAL SIGINT
# Fri, 01 Jul 2022 00:51:19 GMT
EXPOSE 5432
# Fri, 01 Jul 2022 00:51:20 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428d3642719badb326ee04030ea97839d69d5a82b8306924e5ebcf3a65b191dc`  
		Last Modified: Wed, 25 May 2022 21:55:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd66d73c4e4594a6a582481c08b74269a6bda983845fb5018e8ff8e00fb5ec1`  
		Last Modified: Wed, 25 May 2022 21:55:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7c655eb9457c589a4d394024e023bc4e2ed511e418b5616dfeece84c8a1140`  
		Last Modified: Fri, 01 Jul 2022 00:54:41 GMT  
		Size: 83.0 MB (83009195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75740a582eac84007b69c19abdfa9f4f4a3f52f91e9bfe0696a1b1e5cd1282e`  
		Last Modified: Fri, 01 Jul 2022 00:54:30 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7dc53f8b685d6e30e9ef525f92d5c927b26d617bffee690ca4cf7a7d93e9bb`  
		Last Modified: Fri, 01 Jul 2022 00:54:30 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f081766cd927bdcae94f062036970272316625ca2cc8f907b0cdf1850e8888`  
		Last Modified: Fri, 01 Jul 2022 00:54:30 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40597212e9f1cfcf90417e829f829a6c1d44957ab6ad839d26f1f51afdeb7a43`  
		Last Modified: Fri, 01 Jul 2022 00:54:30 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta2-alpine3.16` - linux; 386

```console
$ docker pull postgres@sha256:46f56966a3267051d91db29fa5096129f8281bae4cf37d86755e919103b09e66
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92347776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:796982e8d3442e5875eac01b4ec04227be4ce2fb914afbe93a33368f56069de8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 May 2022 19:38:20 GMT
ADD file:1750ccfabfe93636015070d51a6e824cbd738056223421c69d8aaabc38041b18 in / 
# Mon, 23 May 2022 19:38:20 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 22:22:31 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 25 May 2022 22:22:32 GMT
ENV LANG=en_US.utf8
# Wed, 25 May 2022 22:22:33 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 25 May 2022 22:22:34 GMT
ENV PG_MAJOR=15
# Fri, 01 Jul 2022 00:52:59 GMT
ENV PG_VERSION=15beta2
# Fri, 01 Jul 2022 00:53:00 GMT
ENV PG_SHA256=2fedbc58b370f30e5f59fb0dcc8128a2ef9a922b50fa931b442e4fa27ca98830
# Fri, 01 Jul 2022 00:57:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 01 Jul 2022 00:57:03 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 01 Jul 2022 00:57:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Jul 2022 00:57:05 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Jul 2022 00:57:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Jul 2022 00:57:07 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Jul 2022 00:57:09 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Fri, 01 Jul 2022 00:57:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Jul 2022 00:57:10 GMT
STOPSIGNAL SIGINT
# Fri, 01 Jul 2022 00:57:11 GMT
EXPOSE 5432
# Fri, 01 Jul 2022 00:57:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bb638a3869eed698f88775c7a48f36f8e22e7c6bbaa98fa1d5678966b619b859`  
		Last Modified: Mon, 23 May 2022 19:09:25 GMT  
		Size: 2.8 MB (2801887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6b536300ebf44ca3d811d15e76a960dacddafea21867a310b2bc9d308d382e`  
		Last Modified: Wed, 25 May 2022 22:48:02 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c973fe6785aafb3f812e17ca4088d67ed9081ac155d8340dfbfb27e6af6fd4f1`  
		Last Modified: Wed, 25 May 2022 22:48:02 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1eb6dd8edb16a4bcf41488b41b034b92732a0644908a5647833c4246149271d`  
		Last Modified: Fri, 01 Jul 2022 01:00:39 GMT  
		Size: 89.5 MB (89530049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195c86bdef420bf7dce413e53f50a1c7917e97c97e18b5d741154eebea1559ff`  
		Last Modified: Fri, 01 Jul 2022 01:00:28 GMT  
		Size: 9.5 KB (9461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3ca6600bb6c959a853c8001cce54a9c4f0b4aff573b05b8aa0131d33948c4e`  
		Last Modified: Fri, 01 Jul 2022 01:00:28 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e42753f9195162b55d3b21efbd6f30bad25642c6b56ebb44101e527ac2a5b855`  
		Last Modified: Fri, 01 Jul 2022 01:00:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdcecfe859742759d1add574bf0b00d6aa6400f68ca85473aca01cbc365ed12`  
		Last Modified: Fri, 01 Jul 2022 01:00:28 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15beta2-alpine3.16` - linux; s390x

```console
$ docker pull postgres@sha256:80c4ba8a1868f9fd6162adbb777d30ff95b24985f7beb03ae1bc49c583bd9ef5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87970088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d692307366b8a193b0817304f1f1e0971ef4e14da259381690e878d085524bb7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 23 May 2022 19:41:59 GMT
ADD file:e1852d8ef555a0d3ef6d0b74a898720c82bb9f491430b06a0dd0499497ce118e in / 
# Mon, 23 May 2022 19:42:10 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 21:18:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 25 May 2022 21:18:56 GMT
ENV LANG=en_US.utf8
# Wed, 25 May 2022 21:18:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 25 May 2022 21:18:57 GMT
ENV PG_MAJOR=15
# Fri, 01 Jul 2022 00:51:37 GMT
ENV PG_VERSION=15beta2
# Fri, 01 Jul 2022 00:51:37 GMT
ENV PG_SHA256=2fedbc58b370f30e5f59fb0dcc8128a2ef9a922b50fa931b442e4fa27ca98830
# Fri, 01 Jul 2022 00:56:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 01 Jul 2022 00:56:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 01 Jul 2022 00:56:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 01 Jul 2022 00:56:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 01 Jul 2022 00:56:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 01 Jul 2022 00:56:16 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 01 Jul 2022 00:56:17 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Fri, 01 Jul 2022 00:56:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Jul 2022 00:56:17 GMT
STOPSIGNAL SIGINT
# Fri, 01 Jul 2022 00:56:17 GMT
EXPOSE 5432
# Fri, 01 Jul 2022 00:56:18 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af1ac1a73384e058591d04d19bc05a06781cc32d52d4593b468d6cb95eda9858`  
		Last Modified: Mon, 23 May 2022 19:43:36 GMT  
		Size: 2.6 MB (2580494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39251492e62d811aa94961c8e28a32e2d839aff833e8cb7d038d68cfa1b31b1`  
		Last Modified: Wed, 25 May 2022 21:48:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c159c69cfc44c287422fdef78cc8dbc8c6a88fd4f24d04b8efc313da9b72eda0`  
		Last Modified: Wed, 25 May 2022 21:48:39 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c379a05ff4bd0aa60cb599e099f87bc15d6aa1c803d6258261eb75f437f4e3`  
		Last Modified: Fri, 01 Jul 2022 00:59:48 GMT  
		Size: 85.4 MB (85373651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcf04d99c87388605798a41eea959cc5f7918e08e2ab19c0bbba758ef979b64`  
		Last Modified: Fri, 01 Jul 2022 00:59:39 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea97ba1e2854aa8e137709146729d8a7da4842b3a01912e1462cb48b8caccc8`  
		Last Modified: Fri, 01 Jul 2022 00:59:39 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262f6d9beef3729ce1882ebe5d211b9b0b7f85306a3a58a542fa85dee80a5002`  
		Last Modified: Fri, 01 Jul 2022 00:59:39 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e20db32c29c0cb3040029ffa882b1c6d4605f52f3f53df65ee0fdcc0954614`  
		Last Modified: Fri, 01 Jul 2022 00:59:39 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
