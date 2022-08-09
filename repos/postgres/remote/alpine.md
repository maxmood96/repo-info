## `postgres:alpine`

```console
$ docker pull postgres@sha256:5799375c646333dc1861a65662fbe998f2cad0d04e757f77d93c83f5555363a4
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

### `postgres:alpine` - linux; amd64

```console
$ docker pull postgres@sha256:7d6403121b12c9d29c13c9873bc0f76da8ff51f6c89fae10b99dc890807e27ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84683553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cd24e8c51bfe2a56fbe1577c41f5160692de3092d7ba0f2e0a622c57724fc3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 01:37:18 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 19 Jul 2022 01:37:18 GMT
ENV LANG=en_US.utf8
# Tue, 19 Jul 2022 01:37:19 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 19 Jul 2022 01:41:13 GMT
ENV PG_MAJOR=14
# Tue, 19 Jul 2022 01:41:13 GMT
ENV PG_VERSION=14.4
# Tue, 19 Jul 2022 01:41:14 GMT
ENV PG_SHA256=c23b6237c5231c791511bdc79098617d6852e9e3bdf360efd8b5d15a1a3d8f6a
# Tue, 19 Jul 2022 01:44:39 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 19 Jul 2022 01:44:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 19 Jul 2022 01:44:41 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 19 Jul 2022 01:44:41 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 Jul 2022 01:44:41 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 19 Jul 2022 01:44:41 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 Jul 2022 01:44:42 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 19 Jul 2022 01:44:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 01:44:42 GMT
STOPSIGNAL SIGINT
# Tue, 19 Jul 2022 01:44:42 GMT
EXPOSE 5432
# Tue, 19 Jul 2022 01:44:42 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915bf02ec4105a810e064257cd9ce9cbf90be2ec069bf0f87d12f98038d07c56`  
		Last Modified: Tue, 19 Jul 2022 01:58:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b026a0cf3c97e00c74281e123e212ce0517eee48fbd9a1086027c4684f6f5517`  
		Last Modified: Tue, 19 Jul 2022 01:58:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88659e2107f6c19018c4e187da12c1d25804ea415012db2800349a24303c3f58`  
		Last Modified: Tue, 19 Jul 2022 01:59:19 GMT  
		Size: 81.9 MB (81869047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33960a1e9871a67fd4cdc90215bb1e3002ec7fac9e5ffa3d9729f1632f659f91`  
		Last Modified: Tue, 19 Jul 2022 01:59:07 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bbc907277f07d68b85d7eab8d131447831f84eaac4d1bf2421ff2e6139ea7c`  
		Last Modified: Tue, 19 Jul 2022 01:59:07 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e545c6230ec7e1d72b3d7fdfae81ebfa9d1ee7ab1fb165b956202376cafe277`  
		Last Modified: Tue, 19 Jul 2022 01:59:07 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5428d6e942832c77d8b941f2a66f721abc27bb010a93d9a60a933df9e51dc4`  
		Last Modified: Tue, 19 Jul 2022 01:59:07 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:56d258a75a7862cb319cfd52cc3bf174f78b9f4d242cfdd98cfbe78c1a506ca6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82779681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba42fabb5665ba1fc8b66d76e712164047f5115a59208c01facc932ca6986a8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 21:06:36 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 18 Jul 2022 21:06:36 GMT
ENV LANG=en_US.utf8
# Mon, 18 Jul 2022 21:06:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 18 Jul 2022 21:13:22 GMT
ENV PG_MAJOR=14
# Mon, 18 Jul 2022 21:13:22 GMT
ENV PG_VERSION=14.4
# Mon, 18 Jul 2022 21:13:23 GMT
ENV PG_SHA256=c23b6237c5231c791511bdc79098617d6852e9e3bdf360efd8b5d15a1a3d8f6a
# Mon, 18 Jul 2022 21:19:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Mon, 18 Jul 2022 21:19:13 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 18 Jul 2022 21:19:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 18 Jul 2022 21:19:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 18 Jul 2022 21:19:16 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 18 Jul 2022 21:19:16 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 18 Jul 2022 21:19:17 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Mon, 18 Jul 2022 21:19:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Jul 2022 21:19:18 GMT
STOPSIGNAL SIGINT
# Mon, 18 Jul 2022 21:19:18 GMT
EXPOSE 5432
# Mon, 18 Jul 2022 21:19:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ee135ac0bb04d40f0640b49a624bd7ee2aefe8bfbfc103e187bc2ec33604b8`  
		Last Modified: Mon, 18 Jul 2022 21:44:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f9e567f61e29fde27226359cb09450d6888364eedb70b1144acc08642e6ade`  
		Last Modified: Mon, 18 Jul 2022 21:44:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ab543b24bb036ab693847b178b8ac49a86ca0c46cf043f5125e473cb054c9e`  
		Last Modified: Mon, 18 Jul 2022 21:45:51 GMT  
		Size: 80.2 MB (80157550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7714019fc6f25e85b1bcce6fe19b344aa5c200dd2c223434dce112d7ac62c778`  
		Last Modified: Mon, 18 Jul 2022 21:45:04 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9aaf9a842af3493df009b39d0dbd1703bfb1d564e4f9ec3f00253fe1f7c18e`  
		Last Modified: Mon, 18 Jul 2022 21:45:04 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d60d60f7f3a4c5ae5af3478752f58a20ff3d65fd3aaf59011ea4591f17f6809`  
		Last Modified: Mon, 18 Jul 2022 21:45:04 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f0ae825c0023c72b789af79a5d0c080acfb555ce21e70bd10c57089a26ea30`  
		Last Modified: Mon, 18 Jul 2022 21:45:04 GMT  
		Size: 4.7 KB (4706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7ce18384700276177611c77e6a8fefce198933a42f62ada08fbfc95748a766e9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77896872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb9878dd2dc1cb7e40dce70279367c4a66911fb8219c24a87943586d09df27a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 01:49:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 03 Aug 2022 01:49:56 GMT
ENV LANG=en_US.utf8
# Wed, 03 Aug 2022 01:49:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 03 Aug 2022 02:14:30 GMT
ENV PG_MAJOR=14
# Wed, 03 Aug 2022 02:14:30 GMT
ENV PG_VERSION=14.4
# Wed, 03 Aug 2022 02:14:30 GMT
ENV PG_SHA256=c23b6237c5231c791511bdc79098617d6852e9e3bdf360efd8b5d15a1a3d8f6a
# Wed, 03 Aug 2022 02:22:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 03 Aug 2022 02:22:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 03 Aug 2022 02:22:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 03 Aug 2022 02:22:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Aug 2022 02:22:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 03 Aug 2022 02:22:30 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Aug 2022 02:22:30 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 03 Aug 2022 02:22:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 02:22:30 GMT
STOPSIGNAL SIGINT
# Wed, 03 Aug 2022 02:22:31 GMT
EXPOSE 5432
# Wed, 03 Aug 2022 02:22:31 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33360a646bda42f932e75e42435889ffc8d59c02791d80964924819ec1341dc2`  
		Last Modified: Wed, 03 Aug 2022 03:58:44 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f17786242936cb69b5a2449dae1644bad5fd485824573a50db403a1c8b6943`  
		Last Modified: Wed, 03 Aug 2022 03:58:43 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de945285404c9803aea236ccfc48511af240923fed1b6f355d8a21550281dd6`  
		Last Modified: Wed, 03 Aug 2022 04:00:10 GMT  
		Size: 75.5 MB (75468866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af25066d3003c6f9cbd17eae59892e00609249860e6fb1e5ce8f3d47c48b9bc`  
		Last Modified: Wed, 03 Aug 2022 03:59:54 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d76a92f6142826559cdbe58a8a880fa691b18a6c8109d0917dc2dfdea0ead2`  
		Last Modified: Wed, 03 Aug 2022 03:59:54 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388eb085433112ebdabd4452f29df5f30dfc4e2b48e5abbc8a323cb5934c52f3`  
		Last Modified: Wed, 03 Aug 2022 03:59:54 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2d8208db5c835d6c5d67e1403aab430b05bb35369173355bf8fa24c588b568`  
		Last Modified: Wed, 03 Aug 2022 03:59:54 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:033ba1b6dfd128e81008e98229b1b6d715352f13a14f3ae58539677b9cc79ef8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83524809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054113da34d97ccba36ed9c08e21d2f6e6dd7bf5950aae1e9981b96c3c56c71c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 01:26:38 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 19 Jul 2022 01:26:38 GMT
ENV LANG=en_US.utf8
# Tue, 19 Jul 2022 01:26:39 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 19 Jul 2022 01:30:40 GMT
ENV PG_MAJOR=14
# Tue, 19 Jul 2022 01:30:41 GMT
ENV PG_VERSION=14.4
# Tue, 19 Jul 2022 01:30:42 GMT
ENV PG_SHA256=c23b6237c5231c791511bdc79098617d6852e9e3bdf360efd8b5d15a1a3d8f6a
# Tue, 19 Jul 2022 01:34:03 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 19 Jul 2022 01:34:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 19 Jul 2022 01:34:05 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 19 Jul 2022 01:34:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 Jul 2022 01:34:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 19 Jul 2022 01:34:08 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 Jul 2022 01:34:10 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 19 Jul 2022 01:34:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 01:34:11 GMT
STOPSIGNAL SIGINT
# Tue, 19 Jul 2022 01:34:12 GMT
EXPOSE 5432
# Tue, 19 Jul 2022 01:34:13 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204fa37ad79b6fbdaa6b71115fab75d702735b2da767ca79a34f9ae33d35e456`  
		Last Modified: Tue, 19 Jul 2022 01:49:22 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a550a0032f8399648b092e8dac43bb9b5ac5fd50d67cd74bfe0ad094ba2a535`  
		Last Modified: Tue, 19 Jul 2022 01:49:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb34ecb999918a9201680eaf8c70e6269e8c0d72fa05748ed276eace84fe76e3`  
		Last Modified: Tue, 19 Jul 2022 01:49:56 GMT  
		Size: 80.8 MB (80814513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a2e68b08765d3a07190c21adfc150b2087aff7f3deada0a605d6e455025f92`  
		Last Modified: Tue, 19 Jul 2022 01:49:46 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13dfed150d08c79c112befc24b7668800f0b4c5082871984779d6f824a8255f0`  
		Last Modified: Tue, 19 Jul 2022 01:49:46 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac01d50c1b9b4a340eb93f4f32028c3d16273851c63f4274e12bfb12a5c83171`  
		Last Modified: Tue, 19 Jul 2022 01:49:46 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5590d83d2d1740deaede85637af992e32009b5a0fdbcb63280c0a89feda1a37a`  
		Last Modified: Tue, 19 Jul 2022 01:49:46 GMT  
		Size: 4.7 KB (4704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; 386

```console
$ docker pull postgres@sha256:3554ecbdf87cab14809c85e015c3013fa6696f6f51b86714b8c641f1b16b881d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89985561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6371989ced7d87349e52c9c658b3c3e280c7576987215d968ec601a121c15d6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 20:53:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 09 Aug 2022 20:53:16 GMT
ENV LANG=en_US.utf8
# Tue, 09 Aug 2022 20:53:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 09 Aug 2022 20:57:48 GMT
ENV PG_MAJOR=14
# Tue, 09 Aug 2022 20:57:49 GMT
ENV PG_VERSION=14.4
# Tue, 09 Aug 2022 20:57:50 GMT
ENV PG_SHA256=c23b6237c5231c791511bdc79098617d6852e9e3bdf360efd8b5d15a1a3d8f6a
# Tue, 09 Aug 2022 21:01:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 09 Aug 2022 21:01:38 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 09 Aug 2022 21:01:39 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 09 Aug 2022 21:01:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 09 Aug 2022 21:01:41 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 09 Aug 2022 21:01:42 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 09 Aug 2022 21:01:44 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 09 Aug 2022 21:01:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Aug 2022 21:01:45 GMT
STOPSIGNAL SIGINT
# Tue, 09 Aug 2022 21:01:46 GMT
EXPOSE 5432
# Tue, 09 Aug 2022 21:01:47 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c28e75c4cf92ef72dba94a55ce482cf503fbc49400e209e8c7f918c4c3b738`  
		Last Modified: Tue, 09 Aug 2022 21:18:35 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec2f418c543a35f5a9bd4622f8333170308c8bfc39d60776c46f8cd414f6218`  
		Last Modified: Tue, 09 Aug 2022 21:18:35 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182d8ecb44aef21b6e2d35f2ac4ff9e8ef938999f9d820e9368a2bcc4a7e6a66`  
		Last Modified: Tue, 09 Aug 2022 21:19:10 GMT  
		Size: 87.2 MB (87162865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a2dd5e80615cd82602f676562676f5883c32c982b2c1025b31e2b76ec363da5`  
		Last Modified: Tue, 09 Aug 2022 21:18:59 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541a0f0e29a2aef876b6f50fc29568b23ede3f7e209080b681763376e6723f19`  
		Last Modified: Tue, 09 Aug 2022 21:18:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e7ce463390661f02e2fad99c24096efadb88d8af26d464a911b0825c41edd2`  
		Last Modified: Tue, 09 Aug 2022 21:18:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b47350a7866f3930193363f538cd1619d7af531ee75848dc2833112956bcf28`  
		Last Modified: Tue, 09 Aug 2022 21:18:59 GMT  
		Size: 4.7 KB (4702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:2d8cba7b3057fc5a9b7be922417514f65fab657ee3be0062aaea5aa43fd2596b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.9 MB (90926022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215a8e3b04edbbf0d5d43b257a377d30f383b8cfd3caa796985efaacdfe7bc1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 02:37:43 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 03 Aug 2022 02:37:43 GMT
ENV LANG=en_US.utf8
# Wed, 03 Aug 2022 02:37:44 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 03 Aug 2022 02:43:30 GMT
ENV PG_MAJOR=14
# Wed, 03 Aug 2022 02:43:30 GMT
ENV PG_VERSION=14.4
# Wed, 03 Aug 2022 02:43:30 GMT
ENV PG_SHA256=c23b6237c5231c791511bdc79098617d6852e9e3bdf360efd8b5d15a1a3d8f6a
# Wed, 03 Aug 2022 02:47:57 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 03 Aug 2022 02:48:01 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 03 Aug 2022 02:48:02 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Wed, 03 Aug 2022 02:48:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 03 Aug 2022 02:48:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Wed, 03 Aug 2022 02:48:04 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 03 Aug 2022 02:48:04 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Wed, 03 Aug 2022 02:48:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 02:48:05 GMT
STOPSIGNAL SIGINT
# Wed, 03 Aug 2022 02:48:05 GMT
EXPOSE 5432
# Wed, 03 Aug 2022 02:48:06 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ff041e5ab1725c61c42fff56e7c07df5164981599304940be8e762e0388254`  
		Last Modified: Wed, 03 Aug 2022 03:11:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45689f88b078cb894e9a8cfb35e8bb3e8b1f6f805877273e566f569e1f8d519`  
		Last Modified: Wed, 03 Aug 2022 03:11:20 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b809251bb5833dc604f93dfd2c70d0da84c040e1e270e53ff702bcf14876ee2e`  
		Last Modified: Wed, 03 Aug 2022 03:13:02 GMT  
		Size: 88.1 MB (88120403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ea1ad1b9b3bebe1343252abbbf70a929cf9799a1fbe07b32cfc353bf349d14`  
		Last Modified: Wed, 03 Aug 2022 03:12:42 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2472e448d4e1362d87ef342655764969fa5b237ae2e139df6b6020a2e1f8d4c0`  
		Last Modified: Wed, 03 Aug 2022 03:12:42 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d5310e23252c981ed5d5430d84de229976d7887c3bcbffe6caaeeefec9a7d3`  
		Last Modified: Wed, 03 Aug 2022 03:12:42 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108ec5b149c4325e8a6d765f4081e4a52c6829312269efde792b2ba3c750428f`  
		Last Modified: Wed, 03 Aug 2022 03:12:43 GMT  
		Size: 4.7 KB (4705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:alpine` - linux; s390x

```console
$ docker pull postgres@sha256:a1985a4a2aad2a90ff6cc53178a72cb90f75ab842a51a995202d6a30eea0c7c1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.9 MB (85875682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d6a3b8376393a718c8d60048cded77c8ed709a67a18f62c64f9ada71e58861`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 03:37:54 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Tue, 19 Jul 2022 03:37:55 GMT
ENV LANG=en_US.utf8
# Tue, 19 Jul 2022 03:37:56 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 19 Jul 2022 03:43:25 GMT
ENV PG_MAJOR=14
# Tue, 19 Jul 2022 03:43:25 GMT
ENV PG_VERSION=14.4
# Tue, 19 Jul 2022 03:43:25 GMT
ENV PG_SHA256=c23b6237c5231c791511bdc79098617d6852e9e3bdf360efd8b5d15a1a3d8f6a
# Tue, 19 Jul 2022 03:47:42 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Tue, 19 Jul 2022 03:47:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Tue, 19 Jul 2022 03:48:01 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Tue, 19 Jul 2022 03:48:02 GMT
ENV PGDATA=/var/lib/postgresql/data
# Tue, 19 Jul 2022 03:48:03 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Tue, 19 Jul 2022 03:48:04 GMT
VOLUME [/var/lib/postgresql/data]
# Tue, 19 Jul 2022 03:48:04 GMT
COPY file:232dce6cf487afb0c0cc43d38932ff29614a74b57cd04557dc7398e6d2b93b8f in /usr/local/bin/ 
# Tue, 19 Jul 2022 03:48:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Jul 2022 03:48:05 GMT
STOPSIGNAL SIGINT
# Tue, 19 Jul 2022 03:48:06 GMT
EXPOSE 5432
# Tue, 19 Jul 2022 03:48:07 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef21d7303e7cec444c557678d1d82ed1093485abfa43d752e3b9b3f8ced44c5c`  
		Last Modified: Tue, 19 Jul 2022 04:05:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3215cc8466384c4108c3bfa65989864020c0a98faaca380239e0de7da5e115`  
		Last Modified: Tue, 19 Jul 2022 04:05:59 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b7cc8ffc5ecc93be39fc895e6c7c4e8315283abed324e51938a90310e7d5c5`  
		Last Modified: Tue, 19 Jul 2022 04:06:31 GMT  
		Size: 83.3 MB (83279184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97f5a6b233a34c7f2b4d03d5a9aea31c02f1b1212204c46e5f29c9c4877ce098`  
		Last Modified: Tue, 19 Jul 2022 04:06:21 GMT  
		Size: 9.2 KB (9205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c36d666f826f07a748646cdcf65d144ea0478b35ef440063f36c836d17413c`  
		Last Modified: Tue, 19 Jul 2022 04:06:21 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d90aa99a8cda997999a882a409df260316471859eeddc94d19e7debbbff8beb`  
		Last Modified: Tue, 19 Jul 2022 04:06:21 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0eb26ecd529be727e1ba740d9fe0937671a32df1da185f7e9da4e56de649b0`  
		Last Modified: Tue, 19 Jul 2022 04:06:21 GMT  
		Size: 4.7 KB (4703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
