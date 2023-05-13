## `postgres:15-alpine3.18`

```console
$ docker pull postgres@sha256:c8310fe84064f88438df71f4827e1adebd7c09aa7aef2246fcb7527a5b24cddd
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

### `postgres:15-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:dffb08c444a0c711059eac2e9caf2cea8188d286050acc16ecca303429429f76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96098026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6681122a1de4dd256bb36913057f73b479f64e40914785b0deefa6f86e9f4e52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 May 2023 23:11:10 GMT
ADD file:7625ddfd589fb824ee39f1b1eb387b98f3676420ff52f26eb9d975151e889667 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 22:17:02 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 11 May 2023 22:17:02 GMT
ENV LANG=en_US.utf8
# Thu, 11 May 2023 22:17:02 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 11 May 2023 22:17:02 GMT
ENV PG_MAJOR=15
# Thu, 11 May 2023 22:17:02 GMT
ENV PG_VERSION=15.3
# Thu, 11 May 2023 22:17:03 GMT
ENV PG_SHA256=ffc7d4891f00ffbf5c3f4eab7fbbced8460b8c0ee63c5a5167133b9e6599d932
# Thu, 11 May 2023 22:19:48 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 11 May 2023 22:19:49 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 11 May 2023 22:19:50 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 11 May 2023 22:19:50 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 May 2023 22:19:50 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 11 May 2023 22:19:50 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 May 2023 22:19:51 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 11 May 2023 22:19:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 22:19:51 GMT
STOPSIGNAL SIGINT
# Thu, 11 May 2023 22:19:51 GMT
EXPOSE 5432
# Thu, 11 May 2023 22:19:51 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8a49fdb3b6a5ff2bd8ec6a86c05b2922a0f7454579ecc07637e94dfd1d0639b6`  
		Last Modified: Tue, 09 May 2023 23:11:26 GMT  
		Size: 3.4 MB (3397490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397880efeff2e0a94cc49f859780ff532955c8778d655e68a67b1d609a6bfb45`  
		Last Modified: Thu, 11 May 2023 22:33:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7981ad2d616c5a6eb0618199d194500533df0f0e223f3679527c52722611a98e`  
		Last Modified: Thu, 11 May 2023 22:33:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de3742230e10a39b4d9257c913307bd58584227f0a569d6158bab241dc8bbb3a`  
		Last Modified: Thu, 11 May 2023 22:33:38 GMT  
		Size: 92.7 MB (92684485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0f8c4115566f608b349fcf878231c77a78dd3922bde3311baf9b7682259c5b`  
		Last Modified: Thu, 11 May 2023 22:33:27 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6cc3640e52090083f16843cc48d50566bf3b572dfe011f5646a6b4defa54d56`  
		Last Modified: Thu, 11 May 2023 22:33:27 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b4004b1ece670250c4499819878a340eecd8b11d56903caef99d282c729148`  
		Last Modified: Thu, 11 May 2023 22:33:27 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2b0e3c4896388fa01a15db76aa352e2343aa533d2e475e62b046ee7ab8bba0`  
		Last Modified: Thu, 11 May 2023 22:33:27 GMT  
		Size: 4.8 KB (4794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:073f071d07120c5485aad53b26264838aa1edd7b7cb48455ec0012358595a6d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92095724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be4d70f6ccba1f17ce02c95fd2e686680d4eb554e77b6f2653bf30e71fb9435`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 May 2023 23:11:04 GMT
ADD file:f87a991e2e9f185fd4a88569d86a9b8e5bc07182e7fa613b95acab25986f2a6c in / 
# Tue, 09 May 2023 23:11:04 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 21:28:28 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 11 May 2023 21:28:29 GMT
ENV LANG=en_US.utf8
# Thu, 11 May 2023 21:28:29 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 11 May 2023 21:28:30 GMT
ENV PG_MAJOR=15
# Thu, 11 May 2023 21:28:30 GMT
ENV PG_VERSION=15.3
# Thu, 11 May 2023 21:28:30 GMT
ENV PG_SHA256=ffc7d4891f00ffbf5c3f4eab7fbbced8460b8c0ee63c5a5167133b9e6599d932
# Sat, 13 May 2023 01:18:56 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Sat, 13 May 2023 01:21:45 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 13 May 2023 01:21:48 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 13 May 2023 01:21:49 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Sat, 13 May 2023 01:21:49 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 13 May 2023 01:21:49 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Sat, 13 May 2023 01:21:49 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 13 May 2023 01:21:49 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Sat, 13 May 2023 01:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 May 2023 01:21:50 GMT
STOPSIGNAL SIGINT
# Sat, 13 May 2023 01:21:50 GMT
EXPOSE 5432
# Sat, 13 May 2023 01:21:50 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:015ee8d9fb3dca1b18815f1e4ee0d325d1f40cde6f2df4dd307918f7b69167d7`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.2 MB (3155679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a504b2c539d53246a983f3a350d68c383c09b673da982199911c098186d3f0`  
		Last Modified: Thu, 11 May 2023 21:42:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8cc37774d9571823ff4ecbcd6dfcb2b1016d2a5c6071cf1a5a9bad5ecec6593`  
		Last Modified: Thu, 11 May 2023 21:42:52 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d710eeacd21c8c9d2b34d80d01514a5418323da500d06f70e5868e8d2ac885b`  
		Last Modified: Sat, 13 May 2023 01:32:12 GMT  
		Size: 88.9 MB (88924007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c980b89a3a11801916021a0594df5fbe258f8cf91e6bac91fc4104f69c92063`  
		Last Modified: Sat, 13 May 2023 01:32:00 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04422776bf8b51dcd508182ba4f366e5a1b18d61ebb57409fb22c442e46c4acd`  
		Last Modified: Sat, 13 May 2023 01:32:00 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454d6bd032faee672f47d6d304e667379723256cb820711496f11601f3dc35b5`  
		Last Modified: Sat, 13 May 2023 01:32:00 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7b3ca53aef7ed42c9c40746d4de866660111c8753a3452128411a7a9dddbcb`  
		Last Modified: Sat, 13 May 2023 01:32:00 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:8800e170e2a8eef55e86d7f1bb99728284b3b2a42842f7f042096cf3b8cc0041
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89425179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482a2c1fd242057ff5b18931c005d9eb4d07e4bff9be5ac9212e0e92dd82ae34`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 May 2023 22:57:32 GMT
ADD file:eb6b6a885e8ac9bccbf44a5c673b8542c8144bba927376688240446c2f413b10 in / 
# Tue, 09 May 2023 22:57:32 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 21:57:24 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 11 May 2023 21:57:24 GMT
ENV LANG=en_US.utf8
# Thu, 11 May 2023 21:57:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 11 May 2023 21:57:25 GMT
ENV PG_MAJOR=15
# Thu, 11 May 2023 21:57:25 GMT
ENV PG_VERSION=15.3
# Thu, 11 May 2023 21:57:25 GMT
ENV PG_SHA256=ffc7d4891f00ffbf5c3f4eab7fbbced8460b8c0ee63c5a5167133b9e6599d932
# Thu, 11 May 2023 22:00:02 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 11 May 2023 22:00:04 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 11 May 2023 22:00:04 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 11 May 2023 22:00:04 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 May 2023 22:00:05 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 11 May 2023 22:00:05 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 May 2023 22:00:05 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 11 May 2023 22:00:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 22:00:05 GMT
STOPSIGNAL SIGINT
# Thu, 11 May 2023 22:00:05 GMT
EXPOSE 5432
# Thu, 11 May 2023 22:00:05 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:e14425cf8fb9304b9ad4a9d1250e0d4c22e507a334ff747fa69b804500afc113`  
		Last Modified: Tue, 09 May 2023 22:57:50 GMT  
		Size: 2.9 MB (2911117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3adc0c81db83b2090838aafa2da0e4991bb8cf968b3608a2454dd607bc9a25`  
		Last Modified: Thu, 11 May 2023 22:57:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d98d649e4d405cf332db6211ca9a75ee7df775caee96a4090601b28a3d95d3`  
		Last Modified: Thu, 11 May 2023 22:57:30 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf028a7398c3e31b3b3926ee3d3a5db637a9bea1136e1a497eb0a89f43b841f`  
		Last Modified: Thu, 11 May 2023 22:57:38 GMT  
		Size: 86.5 MB (86498026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d65a516417138d8f61afdf5fe7d8a9c3351ac522a1e3ce08940bb50ff99dc0`  
		Last Modified: Thu, 11 May 2023 22:57:27 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0dae15e349174e69bb8804f61a2566eb2093baddc138ecf80fa88cb4f98a9da`  
		Last Modified: Thu, 11 May 2023 22:57:28 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81949c6ba1f1a8c6267dc2afe7f32e6335d396da7e7e48f01541ad275a0aaf7`  
		Last Modified: Thu, 11 May 2023 22:57:28 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df16e84d9b3238be7f5bbc30f0ad4e8dd749d9b86e2e0ce413069d4e6046669`  
		Last Modified: Thu, 11 May 2023 22:57:28 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:65e40b052c300045e822ca35ef39647613468ede48b7af98f1cf658d40b8c813
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92311870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9033d8d76ec13484da357e3557ead138fb12e9b431dfdd952fe1def000519c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 May 2023 23:11:08 GMT
ADD file:df7fccc3453b6ec1401d27a1295b0882a83e731fde8f23db9d3f687a2b6b4e70 in / 
# Tue, 09 May 2023 23:11:08 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 22:52:14 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 11 May 2023 22:52:14 GMT
ENV LANG=en_US.utf8
# Thu, 11 May 2023 22:52:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 11 May 2023 22:52:15 GMT
ENV PG_MAJOR=15
# Thu, 11 May 2023 22:52:15 GMT
ENV PG_VERSION=15.3
# Thu, 11 May 2023 22:52:15 GMT
ENV PG_SHA256=ffc7d4891f00ffbf5c3f4eab7fbbced8460b8c0ee63c5a5167133b9e6599d932
# Sat, 13 May 2023 02:07:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Sat, 13 May 2023 02:10:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 13 May 2023 02:10:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 13 May 2023 02:10:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Sat, 13 May 2023 02:10:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 13 May 2023 02:10:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Sat, 13 May 2023 02:10:07 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 13 May 2023 02:10:07 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Sat, 13 May 2023 02:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 May 2023 02:10:07 GMT
STOPSIGNAL SIGINT
# Sat, 13 May 2023 02:10:07 GMT
EXPOSE 5432
# Sat, 13 May 2023 02:10:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08409d4172603f40b56eb6b76240a1e6bd78baa0e96590dc7ff76c5f1a093af2`  
		Last Modified: Tue, 09 May 2023 23:11:23 GMT  
		Size: 3.3 MB (3342848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6450d4e89514cf973218c2acf337dd514874b584b24721dc8039c2e5d9bb46e6`  
		Last Modified: Thu, 11 May 2023 23:05:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb127fe040bfe4d77bcfce7123f88f4f3a88be02bb64d3dc68e39956ef046330`  
		Last Modified: Thu, 11 May 2023 23:05:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8af074c92cc049f746b7a7c6ebc1e2325f8bd88d4b19272b8cd36af2a59198`  
		Last Modified: Sat, 13 May 2023 02:19:22 GMT  
		Size: 89.0 MB (88952988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bcb1f7eaed0d2b718c7b94724fc3c6812c543af66a5bfed2f14212245d95b5f`  
		Last Modified: Sat, 13 May 2023 02:19:14 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc817d17a567cf4cb64a81730f2aa378343ca5fa78ea067fd5d048b9f350f2c`  
		Last Modified: Sat, 13 May 2023 02:19:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1d9b0faa846ac90d2306437ec5cc371465cea997e040a92820acb8d7ea6b1f`  
		Last Modified: Sat, 13 May 2023 02:19:14 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee6a28490ffebc871a7b2faaf7dc079fd9953dc6c4f3856aac0eaeddae544b6`  
		Last Modified: Sat, 13 May 2023 02:19:14 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:2d7b09a2f8e2b28d3813dc7c622898a8e0d649138b90e9a34ca10583693e16b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98394260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1915a7e5a4a6e7c57f808b9401a43cacf498e6fcdb3fef216a0ef6728e249e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 May 2023 23:11:03 GMT
ADD file:cfe47ebe49c4a75094234cafa52aa13aa26abcdad49b89293585884b3a8faeae in / 
# Tue, 09 May 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 23:39:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 11 May 2023 23:39:12 GMT
ENV LANG=en_US.utf8
# Thu, 11 May 2023 23:39:13 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 11 May 2023 23:39:13 GMT
ENV PG_MAJOR=15
# Thu, 11 May 2023 23:39:13 GMT
ENV PG_VERSION=15.3
# Thu, 11 May 2023 23:39:13 GMT
ENV PG_SHA256=ffc7d4891f00ffbf5c3f4eab7fbbced8460b8c0ee63c5a5167133b9e6599d932
# Sat, 13 May 2023 02:12:28 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Sat, 13 May 2023 02:18:05 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 13 May 2023 02:18:06 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 13 May 2023 02:18:07 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Sat, 13 May 2023 02:18:07 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 13 May 2023 02:18:07 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Sat, 13 May 2023 02:18:07 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 13 May 2023 02:18:07 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Sat, 13 May 2023 02:18:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 May 2023 02:18:08 GMT
STOPSIGNAL SIGINT
# Sat, 13 May 2023 02:18:08 GMT
EXPOSE 5432
# Sat, 13 May 2023 02:18:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:613767c5530f4016482e81288d0efdca4e58c62031252130d8fccd6f6260a068`  
		Last Modified: Tue, 09 May 2023 23:11:20 GMT  
		Size: 3.3 MB (3264862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b67179174838decafe9bbca3aa6fee7eab28a0ceccd6b34cc420607c17dd64f`  
		Last Modified: Fri, 12 May 2023 01:00:25 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf7f6c786daa9fb0ca80c8070b7f0f50e907f82fc656d530f4f40e0e39515b66`  
		Last Modified: Fri, 12 May 2023 01:00:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d938acede4b463d2caf76a65c17944c5e322684932352ef296a7eba28506d7`  
		Last Modified: Sat, 13 May 2023 02:38:16 GMT  
		Size: 95.1 MB (95113362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36febf7ac0fbbe6c9494742a091093eb5962b3bc5651b700dc9dafdd0786b19c`  
		Last Modified: Sat, 13 May 2023 02:37:59 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501a528e429c18771bdb2ccd4a2b6b7e42b0cbb30ebcaf264044fa57fd0fff1`  
		Last Modified: Sat, 13 May 2023 02:37:59 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedd7423be604321de84a1d2edbf6e00815b3c7a8c4715762ab6bc9156063aaf`  
		Last Modified: Sat, 13 May 2023 02:37:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7c35cf655ed3187dccec7889be37b22bad7f84b569573859fbdb762d3ffb14`  
		Last Modified: Sat, 13 May 2023 02:37:59 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:14f976912ce05217fa9abe4148a012f3707f59831fa4909b9c5f2d7410b63aec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102010002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d1e3b399848694dadd9808f1ece24e69c1894f474c3336bb92b66c037d73b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 May 2023 23:11:09 GMT
ADD file:0a227602737a24c596923d3fd0a7c8b7d9000dbc6b80561473def09abbebbfa6 in / 
# Tue, 09 May 2023 23:11:10 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 20:34:51 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 11 May 2023 20:34:51 GMT
ENV LANG=en_US.utf8
# Thu, 11 May 2023 20:34:52 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 11 May 2023 20:34:53 GMT
ENV PG_MAJOR=15
# Thu, 11 May 2023 20:34:53 GMT
ENV PG_VERSION=15.3
# Thu, 11 May 2023 20:34:53 GMT
ENV PG_SHA256=ffc7d4891f00ffbf5c3f4eab7fbbced8460b8c0ee63c5a5167133b9e6599d932
# Thu, 11 May 2023 20:38:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 11 May 2023 20:38:54 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 11 May 2023 20:38:55 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 11 May 2023 20:38:55 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 May 2023 20:38:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 11 May 2023 20:38:57 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 May 2023 20:38:57 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 11 May 2023 20:38:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 20:38:58 GMT
STOPSIGNAL SIGINT
# Thu, 11 May 2023 20:38:58 GMT
EXPOSE 5432
# Thu, 11 May 2023 20:38:59 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:5c0986f188e93dd7e76a4dc49a9170da2cd124709f5e1590b378e31a2b0d9587`  
		Last Modified: Tue, 09 May 2023 23:11:31 GMT  
		Size: 3.4 MB (3385631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9b471158165ffbcbb4bf3c45f9ba33918076f85db77a01729c1ad05ddf0ea16`  
		Last Modified: Thu, 11 May 2023 21:02:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb96bbe9f79ed5a7dc1e2dc3e0239477816e809b77a95c81a856311487cda12a`  
		Last Modified: Thu, 11 May 2023 21:02:24 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9020ee5d9e97e3df5b025f0a2c12cc16173a443e7f9909d8ab507fb6bddafd`  
		Last Modified: Thu, 11 May 2023 21:02:53 GMT  
		Size: 98.6 MB (98608328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243d6fdbd093192cf5ac8c28e2ddc1918316e78ab50997cce41c78bd83fe95ab`  
		Last Modified: Thu, 11 May 2023 21:02:22 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d46a801d4fb956718c027d5eaa41c80528a7e1527904881800f0ae2992275e`  
		Last Modified: Thu, 11 May 2023 21:02:22 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4d2a5550e3f98a42d55e65e7106d6be089ecdfedf5e87d04f3818bd11d13a3`  
		Last Modified: Thu, 11 May 2023 21:02:22 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd5e98238989a4250e35de13d6ffe80ce84a6e767cabc057f76e49c14cec65c`  
		Last Modified: Thu, 11 May 2023 21:02:22 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:cfea790f821f374ed7e00f479e2c2b76d13229a09bce7c7911afb9a5954fc83e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.9 MB (97924227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5a7f705dbebc4dcef891dd295c26e3cd89db73f8eb397b37dfa8409b971c4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 09 May 2023 23:11:06 GMT
ADD file:89d6e366e8ab41011a5866f8ca43aac6cfef00edffebad565918ab632a6d6210 in / 
# Tue, 09 May 2023 23:11:07 GMT
CMD ["/bin/sh"]
# Thu, 11 May 2023 22:18:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Thu, 11 May 2023 22:18:34 GMT
ENV LANG=en_US.utf8
# Thu, 11 May 2023 22:18:35 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Thu, 11 May 2023 22:18:35 GMT
ENV PG_MAJOR=15
# Thu, 11 May 2023 22:18:35 GMT
ENV PG_VERSION=15.3
# Thu, 11 May 2023 22:18:35 GMT
ENV PG_SHA256=ffc7d4891f00ffbf5c3f4eab7fbbced8460b8c0ee63c5a5167133b9e6599d932
# Thu, 11 May 2023 22:21:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Thu, 11 May 2023 22:21:25 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Thu, 11 May 2023 22:21:25 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Thu, 11 May 2023 22:21:25 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 11 May 2023 22:21:26 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Thu, 11 May 2023 22:21:26 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 11 May 2023 22:21:26 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Thu, 11 May 2023 22:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 May 2023 22:21:27 GMT
STOPSIGNAL SIGINT
# Thu, 11 May 2023 22:21:27 GMT
EXPOSE 5432
# Thu, 11 May 2023 22:21:27 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:25da54cc0a08f4ca602c6bcd3e52d70082eb8a25ee022bc9f1dda019de49197a`  
		Last Modified: Tue, 09 May 2023 23:11:35 GMT  
		Size: 3.2 MB (3226303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319ad51e75272fd6a79ef5d464ac891cc259bc7d83a22465172d13aa0fcb8078`  
		Last Modified: Thu, 11 May 2023 22:36:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0478d56e3d75cfd7130836b30b279ccfe2a84ede863193ac154424689b33ef8`  
		Last Modified: Thu, 11 May 2023 22:36:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b2a3a68ac40dbeee72213685b8d9d6596e4e0c740faf87eab23a1d452134a3`  
		Last Modified: Thu, 11 May 2023 22:36:36 GMT  
		Size: 94.7 MB (94681892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b30be9be417e20898f2bfdc81f7be4f27860313018d387e4cb747c0aafd4c40`  
		Last Modified: Thu, 11 May 2023 22:36:25 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b41bed333ce0698556136d32920c33513e9c0644a6745c261a265c69deb3a7d`  
		Last Modified: Thu, 11 May 2023 22:36:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ca5723b2dff835315da5f18e6f10b11453a2b2d031bd0c44d7cccbedbeafa0`  
		Last Modified: Thu, 11 May 2023 22:36:25 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0374c9bb08ca1584bfc98d434827428a14a9600ae5eec0e1a5a96d2f463ae559`  
		Last Modified: Thu, 11 May 2023 22:36:25 GMT  
		Size: 4.8 KB (4791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
