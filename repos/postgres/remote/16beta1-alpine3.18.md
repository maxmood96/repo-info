## `postgres:16beta1-alpine3.18`

```console
$ docker pull postgres@sha256:71e5693b455bf042cf8ec3ca42127c8d523d2f12fae544e752a5b646c05db7a5
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

### `postgres:16beta1-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:a29ad701f41387ee02f17558dbf7dc2e312288d30cd86c7a2c4d00cfc9d46046
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.2 MB (94228608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25bf131c8ffa06b9baaead91f89fedfc79182da809df7919b6e8d5b7f11ea4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:10:06 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:10:06 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:10:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:10:07 GMT
ENV PG_MAJOR=16
# Wed, 14 Jun 2023 21:10:07 GMT
ENV PG_VERSION=16beta1
# Wed, 14 Jun 2023 21:10:07 GMT
ENV PG_SHA256=59e248d434aa515fa2d31c0d161c4148f30d511dcde91f6e888684823b6849a8
# Wed, 14 Jun 2023 21:10:07 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:12:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:12:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:12:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:12:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:12:57 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:12:57 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:12:57 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:12:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:12:57 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:12:58 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:12:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7c8ef16402f7d0f3d3c7c581b33d4ab851efed851826633154d90c08d5e1f89`  
		Last Modified: Wed, 14 Jun 2023 21:46:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cb57831f5201e337de1dd5b1fb077701af0afe39fd7fa8143f9e552eb6ae20`  
		Last Modified: Wed, 14 Jun 2023 21:46:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32f20c22c763a7e7eaa70aea5009c95dec78a6b29ac08577fa94251b7f00e4a`  
		Last Modified: Wed, 14 Jun 2023 21:47:03 GMT  
		Size: 90.8 MB (90814571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31c232d9f0f7de4f2815e272338e94f19aea4ef512aa2a1bd3d538fb2c6ccc`  
		Last Modified: Wed, 14 Jun 2023 21:46:52 GMT  
		Size: 9.6 KB (9571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c37159d6992646468d6998ea8096de61ff2aa487f8f4a497d1bcc35fae18cab`  
		Last Modified: Wed, 14 Jun 2023 21:46:52 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22494d20836b055e751a90e001eb5d2bbb218bec7643b7377cc44ca00dbf499f`  
		Last Modified: Wed, 14 Jun 2023 21:46:52 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d92cd174773365ed66c9ce825387c83a7d810be5151df320c4310bea6090c2bb`  
		Last Modified: Wed, 14 Jun 2023 21:46:52 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta1-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:92a2ef3fb8ce256d5fa27397722cf3b74cedd32f7850e295c94a7cd32060215e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92855726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264faed68cf574d242e11affa9b1ea222abcb9e249bbe9151e187f037ce20ee1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:20 GMT
ADD file:4213782693bf27a9a6de23bc924ef0c4fb6b2d56010fc07b25f81edeba83b0d4 in / 
# Wed, 14 Jun 2023 18:49:20 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 18:56:23 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 18:56:23 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 18:56:24 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 18:56:24 GMT
ENV PG_MAJOR=16
# Wed, 14 Jun 2023 18:56:24 GMT
ENV PG_VERSION=16beta1
# Wed, 14 Jun 2023 18:56:24 GMT
ENV PG_SHA256=59e248d434aa515fa2d31c0d161c4148f30d511dcde91f6e888684823b6849a8
# Wed, 14 Jun 2023 18:56:24 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 18:59:20 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 18:59:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 18:59:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 18:59:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 18:59:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 18:59:23 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 18:59:23 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 18:59:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 18:59:23 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 18:59:23 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 18:59:24 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:7836be94d3024e2042069c1095caba0b391f70c4b3d34a0475a503239d73dfba`  
		Last Modified: Wed, 14 Jun 2023 18:49:46 GMT  
		Size: 3.1 MB (3143353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd788ea942919017d4b7ef0045f6562b5dedeeea5929dde74db00394b9effd7`  
		Last Modified: Wed, 14 Jun 2023 19:34:49 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3230cb44ffa2c0e180c66587eea332cbdfa3f7b41a5ed589836a7c1924851766`  
		Last Modified: Wed, 14 Jun 2023 19:34:49 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c829cd0f139dc6159eb3e52e74da2de9efeb87ab838d806cac655137cc68067f`  
		Last Modified: Wed, 14 Jun 2023 19:35:01 GMT  
		Size: 89.7 MB (89696212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbfe63b7b646fc88b31d980331c4ab9b6d5de17b4d6936cd08d75b0d399a9aa`  
		Last Modified: Wed, 14 Jun 2023 19:34:48 GMT  
		Size: 9.6 KB (9575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475ee0ea2c254cdf64dddb79d44a5559c418d2c6d143e9a626b343fe702e68eb`  
		Last Modified: Wed, 14 Jun 2023 19:34:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc728ab39f2cc3b0b5aa80de397bc29d3fb8f1a4e5ae925390438340e7d5a8ba`  
		Last Modified: Wed, 14 Jun 2023 19:34:47 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baeefb29df543136b49cabedd94f096c823c6801b8875657017851ffdb93af40`  
		Last Modified: Wed, 14 Jun 2023 19:34:47 GMT  
		Size: 4.8 KB (4792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta1-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:3b57980283af972f0b069c29e4db25f87e42879a768c998ccfbcc2e4eb112911
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87529124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465246eac3c55ba2a5267f16647d4163621af7382dc5ef9f52843206dbff4c32`
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
# Wed, 31 May 2023 02:50:50 GMT
ENV PG_MAJOR=16
# Wed, 31 May 2023 02:50:50 GMT
ENV PG_VERSION=16beta1
# Wed, 31 May 2023 02:50:50 GMT
ENV PG_SHA256=59e248d434aa515fa2d31c0d161c4148f30d511dcde91f6e888684823b6849a8
# Wed, 31 May 2023 02:50:50 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 31 May 2023 02:53:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 31 May 2023 02:53:16 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 31 May 2023 02:53:16 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 31 May 2023 02:53:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 31 May 2023 02:53:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 31 May 2023 02:53:17 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 31 May 2023 02:53:17 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 31 May 2023 02:53:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 May 2023 02:53:17 GMT
STOPSIGNAL SIGINT
# Wed, 31 May 2023 02:53:18 GMT
EXPOSE 5432
# Wed, 31 May 2023 02:53:18 GMT
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
	-	`sha256:96d3edb574c5c6854cfcc768ac9413f14765f4518f6c364c577f3ba6dc32db04`  
		Last Modified: Wed, 31 May 2023 02:57:22 GMT  
		Size: 84.6 MB (84601848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3fab05fb4c1b0e8b5804bda305e4e2b2ceeab3c3934696b1c608e4f91dba147`  
		Last Modified: Wed, 31 May 2023 02:57:12 GMT  
		Size: 9.6 KB (9572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7c56f3d35e9d89a9f692da83f20bac5591b98e8551fba3945cad4943922aa9`  
		Last Modified: Wed, 31 May 2023 02:57:12 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ebed38c7f555397fa44058cf87238bdd8ce08f369b041df971546049c9ac79`  
		Last Modified: Wed, 31 May 2023 02:57:12 GMT  
		Size: 202.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a2150a4ffe23b4e789a71ce1a6ae2ee2ab51b1082483766fcf636b8af14c2b`  
		Last Modified: Wed, 31 May 2023 02:57:12 GMT  
		Size: 4.8 KB (4790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3a90b5071dd8655ab6fb2fe72015a986ef5602a198ae6018eaa82cc61b7b9746
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93160787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20dc0687aa3730487af159a0253eac0630415d5630b0ff8798d2429a66fe2643`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 21:02:16 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 14 Jun 2023 21:02:16 GMT
ENV LANG=en_US.utf8
# Wed, 14 Jun 2023 21:02:16 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 14 Jun 2023 21:02:16 GMT
ENV PG_MAJOR=16
# Wed, 14 Jun 2023 21:02:17 GMT
ENV PG_VERSION=16beta1
# Wed, 14 Jun 2023 21:02:17 GMT
ENV PG_SHA256=59e248d434aa515fa2d31c0d161c4148f30d511dcde91f6e888684823b6849a8
# Wed, 14 Jun 2023 21:02:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 14 Jun 2023 21:04:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 14 Jun 2023 21:04:32 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 14 Jun 2023 21:04:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 14 Jun 2023 21:04:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 14 Jun 2023 21:04:33 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 14 Jun 2023 21:04:33 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 14 Jun 2023 21:04:33 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 14 Jun 2023 21:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 21:04:33 GMT
STOPSIGNAL SIGINT
# Wed, 14 Jun 2023 21:04:33 GMT
EXPOSE 5432
# Wed, 14 Jun 2023 21:04:33 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d285f268e220aa1ae37b8ad4f59c7c59f60c721d1f433c9c58e4f9e52e814f61`  
		Last Modified: Wed, 14 Jun 2023 21:31:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4388b4d68d1c49bc6e6b54f3d73762850870a8281138568a35e656553686e84`  
		Last Modified: Wed, 14 Jun 2023 21:31:17 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b11ffa1184a2b8a7fb31042ff64b070b600b9590fed4a55a034ae0effff01cc`  
		Last Modified: Wed, 14 Jun 2023 21:31:24 GMT  
		Size: 89.8 MB (89815377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df75672790e037e5c0110bb9cface1ccf0cd26b796b0b32a88e98cdd05b53a01`  
		Last Modified: Wed, 14 Jun 2023 21:31:15 GMT  
		Size: 9.6 KB (9575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b77e78054b3bfbe857aec14655219bef5da2e74ea2c84241685423feabab902`  
		Last Modified: Wed, 14 Jun 2023 21:31:15 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7d039e365e74825bc6828a5a15c18172e2305096c3d4ac5605d64de9b2145b`  
		Last Modified: Wed, 14 Jun 2023 21:31:15 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20f739ea56511f101973d2be0b05f625016ac71def124bbf3647e39d31a585e`  
		Last Modified: Wed, 14 Jun 2023 21:31:15 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta1-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:d5527d39c7c95d451816ebeb69995f85e93d7fc6b76d32ce60f350604750d9ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101129829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5286d16a53e8cbdb94f3334080b22148aa09d078aef705a27b5760f32daf80e`
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
# Wed, 31 May 2023 01:40:06 GMT
ENV PG_MAJOR=16
# Wed, 31 May 2023 01:40:06 GMT
ENV PG_VERSION=16beta1
# Wed, 31 May 2023 01:40:06 GMT
ENV PG_SHA256=59e248d434aa515fa2d31c0d161c4148f30d511dcde91f6e888684823b6849a8
# Wed, 31 May 2023 01:40:06 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 31 May 2023 01:45:30 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 31 May 2023 01:45:31 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 31 May 2023 01:45:32 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 31 May 2023 01:45:32 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 31 May 2023 01:45:32 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 31 May 2023 01:45:33 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 31 May 2023 01:45:33 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 31 May 2023 01:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 May 2023 01:45:33 GMT
STOPSIGNAL SIGINT
# Wed, 31 May 2023 01:45:33 GMT
EXPOSE 5432
# Wed, 31 May 2023 01:45:33 GMT
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
	-	`sha256:f77f66c2973e156165292309d2323a67df426ffe6f3ffa1a52845f02b51c15bf`  
		Last Modified: Wed, 31 May 2023 01:52:37 GMT  
		Size: 97.8 MB (97848811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e74f94fedd582316b474506aa83a7741ad4b2b7af68d9dc60b6348b66fc8d3`  
		Last Modified: Wed, 31 May 2023 01:52:20 GMT  
		Size: 9.6 KB (9572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6393882c93d6a04e2ac541fae5092b95ae37e88b37678d599523919c9cb355d5`  
		Last Modified: Wed, 31 May 2023 01:52:20 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c8979f5a05388b2cb924cf8aa4216d555c62316221e3c4ea8b7e9dc8d210c2`  
		Last Modified: Wed, 31 May 2023 01:52:20 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b668b15e180247128de0455fcafd94baeedbb302c4a0e30330aa4f48cd633f3`  
		Last Modified: Wed, 31 May 2023 01:52:20 GMT  
		Size: 4.8 KB (4788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta1-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:ca28a261d14c503b0d1a5b1d775bc4bbb0506e6236b228d9529a5f0109fccdb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101921993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0917237976084e9f0330931e5192eb7fe4b31e71d295dbd22751788d2a96a9f`
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
# Wed, 31 May 2023 02:36:52 GMT
ENV PG_MAJOR=16
# Wed, 31 May 2023 02:36:52 GMT
ENV PG_VERSION=16beta1
# Wed, 31 May 2023 02:36:52 GMT
ENV PG_SHA256=59e248d434aa515fa2d31c0d161c4148f30d511dcde91f6e888684823b6849a8
# Wed, 31 May 2023 02:36:53 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 31 May 2023 02:40:38 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 31 May 2023 02:40:42 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 31 May 2023 02:40:43 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 31 May 2023 02:40:44 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 31 May 2023 02:40:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 31 May 2023 02:40:46 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 31 May 2023 02:40:46 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 31 May 2023 02:40:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 May 2023 02:40:47 GMT
STOPSIGNAL SIGINT
# Wed, 31 May 2023 02:40:47 GMT
EXPOSE 5432
# Wed, 31 May 2023 02:40:48 GMT
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
	-	`sha256:370f2ebb918cc5a425df36d04f12394e679f5cf74bf10b7ff3431fc2fc20d03e`  
		Last Modified: Wed, 31 May 2023 02:47:22 GMT  
		Size: 98.5 MB (98520198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87894194c58a3065fce33a3e9b9d1b023ca3a5cde4c21762287d6349d0fc756`  
		Last Modified: Wed, 31 May 2023 02:47:00 GMT  
		Size: 9.6 KB (9577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b529e2d7197df4dd06aed01101a5298085e047518b6228016611d78bb9e05bf6`  
		Last Modified: Wed, 31 May 2023 02:47:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036b641c5cc88c61b1ac4ea9bb8f51c45570735cb155e29f9f8bfed75fa32a8b`  
		Last Modified: Wed, 31 May 2023 02:47:01 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0a299cf1c861647b81f0d0e492cf4f2e634421a756ea17fde698a212dd213e`  
		Last Modified: Wed, 31 May 2023 02:47:00 GMT  
		Size: 4.8 KB (4793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:16beta1-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:1a4c7db68f86982d9c8cb03a424ef2010c34123bad2667a9c3aeb3e4c6ba2aab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97710054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d737775a34cc0c745c20f92d80d76ba7e646008f31dda87cd40936a94884f0b3`
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
# Wed, 31 May 2023 02:48:29 GMT
ENV PG_MAJOR=16
# Wed, 31 May 2023 02:48:30 GMT
ENV PG_VERSION=16beta1
# Wed, 31 May 2023 02:48:30 GMT
ENV PG_SHA256=59e248d434aa515fa2d31c0d161c4148f30d511dcde91f6e888684823b6849a8
# Wed, 31 May 2023 02:48:30 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Wed, 31 May 2023 02:51:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Wed, 31 May 2023 02:51:22 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Wed, 31 May 2023 02:51:22 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql
# Wed, 31 May 2023 02:51:22 GMT
ENV PGDATA=/var/lib/postgresql/data
# Wed, 31 May 2023 02:51:23 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA"
# Wed, 31 May 2023 02:51:23 GMT
VOLUME [/var/lib/postgresql/data]
# Wed, 31 May 2023 02:51:23 GMT
COPY file:e635913e9467265f505455bc3f08bed37d67ce6597a1f10365f8faf79f09b654 in /usr/local/bin/ 
# Wed, 31 May 2023 02:51:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 31 May 2023 02:51:23 GMT
STOPSIGNAL SIGINT
# Wed, 31 May 2023 02:51:23 GMT
EXPOSE 5432
# Wed, 31 May 2023 02:51:23 GMT
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
	-	`sha256:a67179ace23cd46a987c34ea9d3bb9b12a9425fd1c5f8f4ee10a4aefe8427d48`  
		Last Modified: Wed, 31 May 2023 02:57:05 GMT  
		Size: 94.5 MB (94467594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb8c0a9a5945cdf973679d3d8877cb0aca6681e3b8c09c405fc703d8d37c802`  
		Last Modified: Wed, 31 May 2023 02:56:54 GMT  
		Size: 9.6 KB (9572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa4aaa07c3c0b07c72bf1cefb92c75a16604f77d1aeb4b0b1963bc645b6558b`  
		Last Modified: Wed, 31 May 2023 02:56:54 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d48ea028cee84de32bb3102313e576ad84954e21b5a066559b75efbd18121d5`  
		Last Modified: Wed, 31 May 2023 02:56:54 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f66161abb3be061465c44bfe7a03c535c386ca4f1920f8d4e784b4c2005d14`  
		Last Modified: Wed, 31 May 2023 02:56:54 GMT  
		Size: 4.8 KB (4789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
