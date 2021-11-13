## `postgres:11-alpine3.14`

```console
$ docker pull postgres@sha256:15b5d350c9a4b27fcac4ff729dcacead715c19308801084e5af665f7b4593393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `postgres:11-alpine3.14` - linux; amd64

```console
$ docker pull postgres@sha256:94007d6e3dd932e7aa4d4493637ce34b54731540dec174b031699757028a4a66
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74120235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cec9c179882cf222c5f4791f786711584dab77948929d052d536adcebfb340d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 22:48:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 27 Aug 2021 22:48:02 GMT
ENV LANG=en_US.utf8
# Fri, 27 Aug 2021 22:48:03 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 27 Aug 2021 23:09:50 GMT
ENV PG_MAJOR=11
# Thu, 11 Nov 2021 22:39:34 GMT
ENV PG_VERSION=11.14
# Thu, 11 Nov 2021 22:39:35 GMT
ENV PG_SHA256=965c7f4be96fb64f9581852c58c4f05c3812d4ad823c0f3e2bdfe777c162f999
# Thu, 11 Nov 2021 22:44:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm11-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 11 Nov 2021 22:44:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 11 Nov 2021 22:44:50 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Thu, 11 Nov 2021 22:44:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 Nov 2021 22:44:51 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Thu, 11 Nov 2021 22:44:51 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 Nov 2021 22:44:51 GMT
COPY file:7bb2d643a5007a2573ce85b55b80b2ddaa7af3a038cba459ffbf2e367376ca53 in /usr/local/bin/ 
# Thu, 11 Nov 2021 22:44:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Nov 2021 22:44:51 GMT
STOPSIGNAL SIGINT
# Thu, 11 Nov 2021 22:44:52 GMT
EXPOSE 5432
# Thu, 11 Nov 2021 22:44:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5034a66b99e67db609bf6b4f82bea915e39a42e6f03d11889f7406b4de9e99da`  
		Last Modified: Fri, 27 Aug 2021 23:28:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e9eb77798bd506a06a9adab733c822c718be829c54d514b5789b07c0f1c164`  
		Last Modified: Fri, 27 Aug 2021 23:28:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eebe42d4e7d84b2912330731928878655ec63646f9341ce701a786b2d51c869`  
		Last Modified: Thu, 11 Nov 2021 22:59:20 GMT  
		Size: 71.3 MB (71291293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d7e4e2fb73889b67c2ed54e781abfe5ff34b08c7633e41f226214f86c4b224`  
		Last Modified: Thu, 11 Nov 2021 22:59:10 GMT  
		Size: 8.0 KB (7986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5401d4966a922228ae557173781b7ab5e3522fc443a324af3265e2e999502d2e`  
		Last Modified: Thu, 11 Nov 2021 22:59:10 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbb8722432895a52b7c127a155b5f27832b13e74924482973f35cf154376da7`  
		Last Modified: Thu, 11 Nov 2021 22:59:10 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3a40682d5b914efb10c2b541b61b423649252eb0d1d7d88b3b040d0dc9c6cd`  
		Last Modified: Thu, 11 Nov 2021 22:59:10 GMT  
		Size: 4.7 KB (4723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.14` - linux; arm variant v6

```console
$ docker pull postgres@sha256:4a59d57953e5e5a368d29935f8aa44f8ea3b4206a241121c3b0808596b9e4549
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72679840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b75591ba0f10f2f063f788d1811d5d4eaec8c6c615e283fe64ab67b1ae890a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 00:23:41 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 13 Nov 2021 00:23:42 GMT
ENV LANG=en_US.utf8
# Sat, 13 Nov 2021 00:23:43 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 13 Nov 2021 00:39:41 GMT
ENV PG_MAJOR=11
# Sat, 13 Nov 2021 00:39:42 GMT
ENV PG_VERSION=11.14
# Sat, 13 Nov 2021 00:39:43 GMT
ENV PG_SHA256=965c7f4be96fb64f9581852c58c4f05c3812d4ad823c0f3e2bdfe777c162f999
# Sat, 13 Nov 2021 00:44:19 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm11-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 13 Nov 2021 00:44:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 13 Nov 2021 00:44:23 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 13 Nov 2021 00:44:23 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 13 Nov 2021 00:44:25 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 13 Nov 2021 00:44:26 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 13 Nov 2021 00:44:26 GMT
COPY file:7bb2d643a5007a2573ce85b55b80b2ddaa7af3a038cba459ffbf2e367376ca53 in /usr/local/bin/ 
# Sat, 13 Nov 2021 00:44:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 00:44:27 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 00:44:27 GMT
EXPOSE 5432
# Sat, 13 Nov 2021 00:44:28 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0306bf867c1af5e86348eac10e572e5bbf7b1df7161b3237e6dbf067420ba562`  
		Last Modified: Sat, 13 Nov 2021 00:54:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b273647972e23088da4f0aa3896b1e39e9c26c17f7239fe3fa6ca165b5190765`  
		Last Modified: Sat, 13 Nov 2021 00:54:50 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0872f286a37b3d60b9c165ff13a85dc2a70a7580019e9f4167894362ff858266`  
		Last Modified: Sat, 13 Nov 2021 00:58:30 GMT  
		Size: 70.0 MB (70029945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec2974b5528793c01bbe54816e4d5cd0d1f45d209e57f459a89f146a417df8c1`  
		Last Modified: Sat, 13 Nov 2021 00:58:02 GMT  
		Size: 8.0 KB (7994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc3cb92c1c4b3c2f8629ca92b577045216cabd7595f01eabe9a911fa5c172f7`  
		Last Modified: Sat, 13 Nov 2021 00:58:02 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea71d37a661622539f08d3a7cb5208e16666434637881e77af9354a31ebc335`  
		Last Modified: Sat, 13 Nov 2021 00:58:02 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f869fa999cde4fb341b83394935a563dbe6e5e9273de667755026346ccf22ac`  
		Last Modified: Sat, 13 Nov 2021 00:58:02 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.14` - linux; arm variant v7

```console
$ docker pull postgres@sha256:86452b38a609bc2300de615fce99dbf8984d7b2015a3655ade495547ba80bab3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68459495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a01b0122682191405831a29c681dd1f2897247c5ad27982d7cda28ee4a10675d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 12 Nov 2021 16:57:35 GMT
ADD file:03e0720458c3475758bf4394afa56f2165198eb91e6e9581f7768e433744dd9b in / 
# Fri, 12 Nov 2021 16:57:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 20:25:42 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Nov 2021 20:25:42 GMT
ENV LANG=en_US.utf8
# Fri, 12 Nov 2021 20:25:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Nov 2021 20:41:33 GMT
ENV PG_MAJOR=11
# Fri, 12 Nov 2021 20:41:34 GMT
ENV PG_VERSION=11.14
# Fri, 12 Nov 2021 20:41:34 GMT
ENV PG_SHA256=965c7f4be96fb64f9581852c58c4f05c3812d4ad823c0f3e2bdfe777c162f999
# Fri, 12 Nov 2021 20:46:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm11-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Nov 2021 20:46:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Nov 2021 20:46:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Nov 2021 20:46:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Nov 2021 20:46:09 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Nov 2021 20:46:10 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Nov 2021 20:46:10 GMT
COPY file:7bb2d643a5007a2573ce85b55b80b2ddaa7af3a038cba459ffbf2e367376ca53 in /usr/local/bin/ 
# Fri, 12 Nov 2021 20:46:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 20:46:11 GMT
STOPSIGNAL SIGINT
# Fri, 12 Nov 2021 20:46:12 GMT
EXPOSE 5432
# Fri, 12 Nov 2021 20:46:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:764d2e53e1a607f2d8261522185d5b9021ade3ec1a595664ee90308c00176899`  
		Last Modified: Fri, 12 Nov 2021 16:59:33 GMT  
		Size: 2.4 MB (2438618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65aac23bae9dde4628b949f53b16460bf45bbe0cb93feb0ca4e699560ec405be`  
		Last Modified: Fri, 12 Nov 2021 20:59:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c82e83b49adac505e95de3db74b7b3d754078880f57793b8cd1a81d5c456289`  
		Last Modified: Fri, 12 Nov 2021 20:59:27 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec5eb50fec0c70b07424a3eb2b3592a83e2b9c01e50033aad2912661ed20682`  
		Last Modified: Fri, 12 Nov 2021 21:03:15 GMT  
		Size: 66.0 MB (66006374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b1158f15b4c889d440e1d5fbfaf1c9753b66275bf56c027f4ca19539192318`  
		Last Modified: Fri, 12 Nov 2021 21:02:40 GMT  
		Size: 8.0 KB (7994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e11204ceb81c7c7b6f66ff77433a4b90067b636773f4e258024ea623a1900ed`  
		Last Modified: Fri, 12 Nov 2021 21:02:41 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f76d1dcbcc1c2c1aaca9f7c0e54c1b601145f67c1c6c9c92f2539303aa541d`  
		Last Modified: Fri, 12 Nov 2021 21:02:40 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690a94221405575836620df9e2059d7faeab4f752b6a0924acbd7e0324520d08`  
		Last Modified: Fri, 12 Nov 2021 21:02:40 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.14` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:9abec6f335481fde15a5926f2dd576a6b18add089c8f23b728262bb2ddfae92f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73037610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae71794e83794e82875ef4b9c06464c214e27422f991d3d2bed2567d30d3aaa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 23:41:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Nov 2021 23:41:52 GMT
ENV LANG=en_US.utf8
# Fri, 12 Nov 2021 23:41:53 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Nov 2021 23:56:47 GMT
ENV PG_MAJOR=11
# Fri, 12 Nov 2021 23:56:48 GMT
ENV PG_VERSION=11.14
# Fri, 12 Nov 2021 23:56:49 GMT
ENV PG_SHA256=965c7f4be96fb64f9581852c58c4f05c3812d4ad823c0f3e2bdfe777c162f999
# Sat, 13 Nov 2021 00:00:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm11-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 13 Nov 2021 00:00:43 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 13 Nov 2021 00:00:44 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 13 Nov 2021 00:00:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 13 Nov 2021 00:00:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 13 Nov 2021 00:00:47 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 13 Nov 2021 00:00:49 GMT
COPY file:7bb2d643a5007a2573ce85b55b80b2ddaa7af3a038cba459ffbf2e367376ca53 in /usr/local/bin/ 
# Sat, 13 Nov 2021 00:00:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 00:00:50 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 00:00:51 GMT
EXPOSE 5432
# Sat, 13 Nov 2021 00:00:52 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736fbb41a17a3d331434d1ced1bbefaf60ce58df545c90a6d1dbfeec5eb9af41`  
		Last Modified: Sat, 13 Nov 2021 00:10:26 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99566057aebae6d994d20c6ed9fa0b7e7cd103f58ddce64c9096b244ec9905a0`  
		Last Modified: Sat, 13 Nov 2021 00:10:26 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3547cebbcffc1cb70dcf657ecb8901c6dcbdf133e51e8b6fd0df6075e1f98b15`  
		Last Modified: Sat, 13 Nov 2021 00:12:09 GMT  
		Size: 70.3 MB (70305531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f1e8c991a00f6d92c1ccf06ce5f163d835a1e5923cbd51e81a237b6b1998097`  
		Last Modified: Sat, 13 Nov 2021 00:11:59 GMT  
		Size: 8.0 KB (7989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea555fb6b5b34e8c64f30f3db2dca8c7e698906926f839b967558a7c98d0ea4e`  
		Last Modified: Sat, 13 Nov 2021 00:11:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49da9892c0b5f1d099c522c7ea4a9bc1ea2c3e9f33d7835186bd5b27dc38da07`  
		Last Modified: Sat, 13 Nov 2021 00:12:00 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dec33c501fd9c3912079194c245b913dde759f4057b204bb37a4e6eb0962d3f`  
		Last Modified: Sat, 13 Nov 2021 00:11:59 GMT  
		Size: 4.7 KB (4722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.14` - linux; 386

```console
$ docker pull postgres@sha256:47fb2bd480fdb640ec8948625a80fc65ebc60350a774002f903534aebb1b0ff2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78729518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5486a244deed7f4061437f2d96bdffcc0ab4ba8a3817b587b82a438aba22c1a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 23:55:01 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Nov 2021 23:55:01 GMT
ENV LANG=en_US.utf8
# Fri, 12 Nov 2021 23:55:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 13 Nov 2021 00:19:15 GMT
ENV PG_MAJOR=11
# Sat, 13 Nov 2021 00:19:15 GMT
ENV PG_VERSION=11.14
# Sat, 13 Nov 2021 00:19:16 GMT
ENV PG_SHA256=965c7f4be96fb64f9581852c58c4f05c3812d4ad823c0f3e2bdfe777c162f999
# Sat, 13 Nov 2021 00:26:29 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm11-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 13 Nov 2021 00:26:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 13 Nov 2021 00:26:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 13 Nov 2021 00:26:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 13 Nov 2021 00:26:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 13 Nov 2021 00:26:34 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 13 Nov 2021 00:26:34 GMT
COPY file:7bb2d643a5007a2573ce85b55b80b2ddaa7af3a038cba459ffbf2e367376ca53 in /usr/local/bin/ 
# Sat, 13 Nov 2021 00:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 00:26:35 GMT
STOPSIGNAL SIGINT
# Sat, 13 Nov 2021 00:26:35 GMT
EXPOSE 5432
# Sat, 13 Nov 2021 00:26:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69c9882c88ce94760f0d36deed4d8f55228d1df726a3bc33021031f8922aa5a`  
		Last Modified: Sat, 13 Nov 2021 00:41:13 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2788bc110cff8f1594e3fabf8ae849a646240d7e3c7ce77b566583c4a66b5467`  
		Last Modified: Sat, 13 Nov 2021 00:41:13 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6a0944013799db0a0dfe4a079149c6fd0defb40949c6b012cb900303ec0228`  
		Last Modified: Sat, 13 Nov 2021 00:43:53 GMT  
		Size: 75.9 MB (75884079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6395c46d83abc7f6a5ee16ac4a3a364869073493dde7a36a2fa47ac6d763938b`  
		Last Modified: Sat, 13 Nov 2021 00:43:34 GMT  
		Size: 8.0 KB (7985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d3a16f60318bd1ed3090de57165980b6c3e459ac735d91b5d3609f99cca847`  
		Last Modified: Sat, 13 Nov 2021 00:43:34 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90510323434d4a91e6af02075c9388e5c48af2aa0cd1fa285cc4219c9569d895`  
		Last Modified: Sat, 13 Nov 2021 00:43:34 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1d6e3e127c3a5cc048d3d695ef1f73b97f79f54fceef09df44494535da3f86`  
		Last Modified: Sat, 13 Nov 2021 00:43:34 GMT  
		Size: 4.7 KB (4720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.14` - linux; ppc64le

```console
$ docker pull postgres@sha256:b9a69db56ac2ecb58301fa9ab6e26ffa0aba759b251ab8c9dfd8dc3289984971
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78947601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc856ae6232c77c75b114477fe688ed0ddc3ce28bd2da13e0bc6e143fb017bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 27 Aug 2021 19:39:54 GMT
ADD file:d213c56ffc24a5051e8060fd0fec1a0520367c10d88ab16321c36336b6c66098 in / 
# Fri, 27 Aug 2021 19:39:59 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 21:43:37 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 27 Aug 2021 21:43:39 GMT
ENV LANG=en_US.utf8
# Fri, 27 Aug 2021 21:43:48 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 27 Aug 2021 22:01:25 GMT
ENV PG_MAJOR=11
# Fri, 12 Nov 2021 02:17:26 GMT
ENV PG_VERSION=11.14
# Fri, 12 Nov 2021 02:17:30 GMT
ENV PG_SHA256=965c7f4be96fb64f9581852c58c4f05c3812d4ad823c0f3e2bdfe777c162f999
# Fri, 12 Nov 2021 02:21:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm11-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Nov 2021 02:21:41 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Nov 2021 02:21:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Nov 2021 02:21:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Nov 2021 02:21:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Nov 2021 02:22:00 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Nov 2021 02:22:01 GMT
COPY file:7bb2d643a5007a2573ce85b55b80b2ddaa7af3a038cba459ffbf2e367376ca53 in /usr/local/bin/ 
# Fri, 12 Nov 2021 02:22:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 02:22:09 GMT
STOPSIGNAL SIGINT
# Fri, 12 Nov 2021 02:22:11 GMT
EXPOSE 5432
# Fri, 12 Nov 2021 02:22:14 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:63da8ca98f7b4b94381aed56862a60aecf355d9428b9aeb7c61d5bd017100c18`  
		Last Modified: Fri, 27 Aug 2021 19:41:06 GMT  
		Size: 2.8 MB (2812284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b84363c8c0f2373e8b665451df1c6a11a9415fd4f1c773e8ce7aaafa836248`  
		Last Modified: Fri, 27 Aug 2021 22:17:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7f2722689cf013f5f6333bf25f2c1fa26b298e09468166e2cbade7a81c0817c`  
		Last Modified: Fri, 27 Aug 2021 22:17:38 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce939f760ff8f30419fa5471b46f9824efde7d63f72db1dbf8b3a5009b27493e`  
		Last Modified: Fri, 12 Nov 2021 03:06:43 GMT  
		Size: 76.1 MB (76120817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c37c00f4f6171ee5a323456644b392c699570eb8d84ab9d78f94395e91cefa9`  
		Last Modified: Fri, 12 Nov 2021 03:02:44 GMT  
		Size: 8.0 KB (7992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92fce6f3c556961da544eceb372ab3c114aea8e35687a2966e970de79ec34023`  
		Last Modified: Fri, 12 Nov 2021 03:02:44 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cd7e1f2bb039cdf8df86956b865c583cc0296c7dffded85d20ee5f780ed0231`  
		Last Modified: Fri, 12 Nov 2021 03:02:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15549f279baebc9933ca8c599290996afafc78f2f2030aeaf7be0bd58d01036`  
		Last Modified: Fri, 12 Nov 2021 03:02:44 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:11-alpine3.14` - linux; s390x

```console
$ docker pull postgres@sha256:72b329e1145d7cefcfcc7d816de6c433df7e23dcbc43fd285fbd9fbd4999f1b0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75230585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae6b63795851c4fef1329d6a28d3c36f8d5fe9f5a8dc25155e60c2b163ca77b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 12 Nov 2021 16:41:35 GMT
ADD file:7e0cf02b3f015b1a0f867c03b2902b85f2140be1cee7af63c23f367a487e4577 in / 
# Fri, 12 Nov 2021 16:41:36 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 19:02:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Fri, 12 Nov 2021 19:02:11 GMT
ENV LANG=en_US.utf8
# Fri, 12 Nov 2021 19:02:12 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Fri, 12 Nov 2021 19:11:14 GMT
ENV PG_MAJOR=11
# Fri, 12 Nov 2021 19:11:14 GMT
ENV PG_VERSION=11.14
# Fri, 12 Nov 2021 19:11:14 GMT
ENV PG_SHA256=965c7f4be96fb64f9581852c58c4f05c3812d4ad823c0f3e2bdfe777c162f999
# Fri, 12 Nov 2021 19:13:43 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm11-dev clang g++ 		make 		openssl-dev 		perl-utils 		perl-ipc-run 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 				--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 12 Nov 2021 19:13:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 12 Nov 2021 19:13:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 12 Nov 2021 19:13:47 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 12 Nov 2021 19:13:47 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 12 Nov 2021 19:13:47 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 12 Nov 2021 19:13:47 GMT
COPY file:7bb2d643a5007a2573ce85b55b80b2ddaa7af3a038cba459ffbf2e367376ca53 in /usr/local/bin/ 
# Fri, 12 Nov 2021 19:13:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 19:13:48 GMT
STOPSIGNAL SIGINT
# Fri, 12 Nov 2021 19:13:48 GMT
EXPOSE 5432
# Fri, 12 Nov 2021 19:13:48 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:817a13b0e05928f7491adbf1d2cf261ec35079112247bd03469bbe31156aca7c`  
		Last Modified: Fri, 12 Nov 2021 16:42:44 GMT  
		Size: 2.6 MB (2609278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c11d0e178e11b961bdeb7fbf4c5d37bdf95bead1a94bf7cb11c22318da7b0408`  
		Last Modified: Fri, 12 Nov 2021 19:19:45 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013949685d6dbf2034fe35128fa32dead6dda85c74b516d4e075450693ad8cd7`  
		Last Modified: Fri, 12 Nov 2021 19:19:45 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6649d512a994535ac422ef96566798ada332ffe4eeeae1321bb2e6a713fe90f`  
		Last Modified: Fri, 12 Nov 2021 19:21:05 GMT  
		Size: 72.6 MB (72606810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c77e5e3cb44be7404546507f9a68e7b97b98750caf42d11c0d249e08021e6a`  
		Last Modified: Fri, 12 Nov 2021 19:20:57 GMT  
		Size: 8.0 KB (7990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6351c0501d0f38b245c47812012d83ab8d4a108cefead294c1abfbbaab7718de`  
		Last Modified: Fri, 12 Nov 2021 19:20:57 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66cec70f118736dbf9a40e77e6bc5a4016fa2739a726fe2fc1d45604a18e23ce`  
		Last Modified: Fri, 12 Nov 2021 19:20:57 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba52cf5058b572b56180d57bfea9915df5330e3ed70575c309dedfda4a50295`  
		Last Modified: Fri, 12 Nov 2021 19:20:57 GMT  
		Size: 4.7 KB (4717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
