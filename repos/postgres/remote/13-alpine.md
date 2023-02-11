## `postgres:13-alpine`

```console
$ docker pull postgres@sha256:54ff49d5aa3cc5360b765ea06cf1605c5b2b8da96c3d6b962750f536859d2c87
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

### `postgres:13-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:0c4fe80cf04859e175ba0e57c2b974fb33f4afb1f86a0151920fc633b9a5e145
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91999298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f14697b527cdb3269ce0e7b3a7dc7e886282b17c3c8ae1ff1fa09d930cbf35`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:02:45 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 11 Feb 2023 05:02:45 GMT
ENV LANG=en_US.utf8
# Sat, 11 Feb 2023 05:02:46 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 11 Feb 2023 05:09:19 GMT
ENV PG_MAJOR=13
# Sat, 11 Feb 2023 05:09:19 GMT
ENV PG_VERSION=13.10
# Sat, 11 Feb 2023 05:09:20 GMT
ENV PG_SHA256=5bbcf5a56d85c44f3a8b058fb46862ff49cbc91834d07e295d02e6de3c216df2
# Sat, 11 Feb 2023 05:11:51 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 05:11:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 05:11:52 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 05:11:52 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 05:11:53 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 05:11:53 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 05:11:53 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 05:11:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:11:53 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 05:11:54 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 05:11:54 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c441836541d936a780ab5a18cf835d5ae7199cb588cec248614c06418dc7d74c`  
		Last Modified: Sat, 11 Feb 2023 05:19:26 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49de1a24361effb80661c973c1fcf863dca0564eec7667a9be5b9981501e6a4`  
		Last Modified: Sat, 11 Feb 2023 05:19:26 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c609d08dc3c06bf716770f3e0c5d102efbb0b998f7af8c33cfad99bd919cce8`  
		Last Modified: Sat, 11 Feb 2023 05:21:26 GMT  
		Size: 88.6 MB (88609255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e801cecfb07c483cb37c1bd8c2f9069af40ad155dd7597486859fc4a78a02701`  
		Last Modified: Sat, 11 Feb 2023 05:21:14 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98756d4318400cee9bdce78662c064ae80c15c8f21221917fec93583a196d9cd`  
		Last Modified: Sat, 11 Feb 2023 05:21:14 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d991736c9c5adbb6c7a3978ae0c28151246e065f390d43dcf45e24319a912984`  
		Last Modified: Sat, 11 Feb 2023 05:21:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708ebe2e647dd2aa997b443c5cb0db10850bbfd16c9abcdb2ee7575abbcf59e`  
		Last Modified: Sat, 11 Feb 2023 05:21:14 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:c984d6132a4f6a5d06153ab25fff3c3b40c1ced7c85a28a7664b7fb0d1b82df8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91533317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd042281357f3afc5ca9e5c4b3b4cdef6748e3566a0bfb84a37909062c72b71d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:54 GMT
ADD file:b15fd8e9f996815394e25f20c8459bfb4c2a8c4074592d6f4c75f4fe79ce537e in / 
# Mon, 09 Jan 2023 17:04:55 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 23:30:27 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 09 Jan 2023 23:30:27 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jan 2023 23:30:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 09 Jan 2023 23:37:38 GMT
ENV PG_MAJOR=13
# Fri, 10 Feb 2023 18:56:23 GMT
ENV PG_VERSION=13.10
# Fri, 10 Feb 2023 18:56:23 GMT
ENV PG_SHA256=5bbcf5a56d85c44f3a8b058fb46862ff49cbc91834d07e295d02e6de3c216df2
# Fri, 10 Feb 2023 18:59:18 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 10 Feb 2023 18:59:20 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 10 Feb 2023 18:59:20 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 10 Feb 2023 18:59:21 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 10 Feb 2023 18:59:21 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 10 Feb 2023 18:59:21 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 10 Feb 2023 18:59:21 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Fri, 10 Feb 2023 18:59:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 18:59:22 GMT
STOPSIGNAL SIGINT
# Fri, 10 Feb 2023 18:59:22 GMT
EXPOSE 5432
# Fri, 10 Feb 2023 18:59:22 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0269c10e600f3a375f36ddabdbd264ce9503a455f0d0969ce8a00f24eaecc032`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.1 MB (3107243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909c72a9df3baa262940fa4442cb689b379ea4290fcf09350e2be758d22abf63`  
		Last Modified: Mon, 09 Jan 2023 23:47:30 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0351a3586f66e0818c6c33de9468bf6f24569571ba6aa82f79d8b9d00413826`  
		Last Modified: Mon, 09 Jan 2023 23:47:29 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b441857ef87ca4ec631e9453d46c67cab06038d6578138b7ca23802a2652837`  
		Last Modified: Fri, 10 Feb 2023 19:08:31 GMT  
		Size: 88.4 MB (88410602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83e730c576d14184fbf1b7173a996d300911329847333e49c8e54df7b1933547`  
		Last Modified: Fri, 10 Feb 2023 19:08:16 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb660a41455e139f739e108f294ed90b12b7d6c8cd6f12ed00ffdd937cc6381`  
		Last Modified: Fri, 10 Feb 2023 19:08:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c02ccc6f611f886c75a2ad02eaf5bd555fafaae81e40bbb90f6a0dd69d03d05`  
		Last Modified: Fri, 10 Feb 2023 19:08:16 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d952fd94cc5f0fe210dea2bbbcc2d1d35d13bee1d2ae62c14aa2cfe243b09bc4`  
		Last Modified: Fri, 10 Feb 2023 19:08:17 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:db76afd767d865c543589641df1a1c482343dcf0e7f55cb28220c5e02ecf6f0b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86101162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9c1ea48399b60d72818b40ac85efeaf2e490d4e7ab978fc0d6475bf5f4be0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jan 2023 17:06:27 GMT
ADD file:4696f25d0f019b27457c55b3b128b70bf153f38e3e4eb5bdfc21058543313e94 in / 
# Mon, 09 Jan 2023 17:06:27 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 21:46:30 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 09 Jan 2023 21:46:30 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jan 2023 21:46:30 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 09 Jan 2023 21:53:03 GMT
ENV PG_MAJOR=13
# Fri, 10 Feb 2023 19:49:48 GMT
ENV PG_VERSION=13.10
# Fri, 10 Feb 2023 19:49:48 GMT
ENV PG_SHA256=5bbcf5a56d85c44f3a8b058fb46862ff49cbc91834d07e295d02e6de3c216df2
# Fri, 10 Feb 2023 19:52:34 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 10 Feb 2023 19:52:35 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 10 Feb 2023 19:52:36 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 10 Feb 2023 19:52:36 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 10 Feb 2023 19:52:36 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 10 Feb 2023 19:52:37 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 10 Feb 2023 19:52:37 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Fri, 10 Feb 2023 19:52:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 19:52:37 GMT
STOPSIGNAL SIGINT
# Fri, 10 Feb 2023 19:52:37 GMT
EXPOSE 5432
# Fri, 10 Feb 2023 19:52:37 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c527615e4ffa2d5b9b777fd469b3b5ba7c1b1e9201c065be2c43569de48a3754`  
		Last Modified: Mon, 09 Jan 2023 17:07:17 GMT  
		Size: 2.9 MB (2865208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd4157fd012b33b3e7ad71ecb79e6bed245bc640c620f0976b111fc558b9afa2`  
		Last Modified: Mon, 09 Jan 2023 22:04:00 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4a6cf5c34a0f5b36fbe4cb9ff9e7a04f57e2c06d6b6e46a114bff6f6473005`  
		Last Modified: Mon, 09 Jan 2023 22:04:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ae0db428ba8623d52dad781031cc87e6b93e296583e19e2c74bae851194002`  
		Last Modified: Fri, 10 Feb 2023 20:29:12 GMT  
		Size: 83.2 MB (83220479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a01c40a8a72f9fa21c6f03dfd2a741ac05a42219fc1195aad44262f899b464`  
		Last Modified: Fri, 10 Feb 2023 20:28:59 GMT  
		Size: 9.0 KB (9028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead01e6bd6fcd03b6945ac423d623fecb2ba56aeaa0f51840c7bcf35a1e9fddb`  
		Last Modified: Fri, 10 Feb 2023 20:28:59 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153ac3452c26c1845ec7a896916ee2f16715238f46ca1c6b75c720c35383065d`  
		Last Modified: Fri, 10 Feb 2023 20:28:59 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab8e06c47e9aa538393b23792608be9becf127c059a59907ac9e63b59a532c3`  
		Last Modified: Fri, 10 Feb 2023 20:28:59 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b4fe9d0d4fcf8dd04a328f7bd171c6f41bf7dc067aa1076256bc703aa86c354f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89766150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fca7d7fd865f33f16a95c820408bc7dac051c41fabb6f264eaf6ff0b9aed372`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:07:58 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 11 Feb 2023 03:07:58 GMT
ENV LANG=en_US.utf8
# Sat, 11 Feb 2023 03:07:59 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 11 Feb 2023 03:12:17 GMT
ENV PG_MAJOR=13
# Sat, 11 Feb 2023 03:12:17 GMT
ENV PG_VERSION=13.10
# Sat, 11 Feb 2023 03:12:17 GMT
ENV PG_SHA256=5bbcf5a56d85c44f3a8b058fb46862ff49cbc91834d07e295d02e6de3c216df2
# Sat, 11 Feb 2023 03:14:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 03:14:09 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 03:14:09 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 03:14:09 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 03:14:10 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 03:14:10 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 03:14:10 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 03:14:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 03:14:10 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 03:14:10 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 03:14:10 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71286d2ce0cc0803a31c93bdd02c2974bcf648b2587eab598a95d3304821b328`  
		Last Modified: Sat, 11 Feb 2023 03:18:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b82afe47906a58fdc251da4eba9d943f6f1aa95833f128935ffac4ee84c4ef75`  
		Last Modified: Sat, 11 Feb 2023 03:18:57 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12505865e74b1de5e5401120fb30f45a33ccfeccb53d058b4c4596383592c9a`  
		Last Modified: Sat, 11 Feb 2023 03:19:56 GMT  
		Size: 86.5 MB (86488595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c68d9979ca88e74d5bfe523c61529e8b5ec32f900a9999ea1682dd89f2516443`  
		Last Modified: Sat, 11 Feb 2023 03:19:48 GMT  
		Size: 9.0 KB (9024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506ff9c88f58669341ad89a1ba464fa13511f28a7144738195dca053d8b35ba4`  
		Last Modified: Sat, 11 Feb 2023 03:19:48 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d446aee04be8035a6c0703b17559d6e809ea52869dad0cb69dc23abaa663bda`  
		Last Modified: Sat, 11 Feb 2023 03:19:48 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4756cfff679ed0c809b850aaba1bdbf2d69428c1009a13ef0f9a07073808ad`  
		Last Modified: Sat, 11 Feb 2023 03:19:48 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; 386

```console
$ docker pull postgres@sha256:9004ecb06fba6137ce0e932944ddd8fbc224c4f976070c2dd3f1f01b387e84c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96770432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf85cfef01ceaf41df3b9bf3950e7115d8dbc045b90b7f382eab7b825b678c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:23 GMT
ADD file:125f3514520a5cd29df2830a409aa026a2bc06a77a7a5d150133436404b33d41 in / 
# Fri, 10 Feb 2023 21:24:24 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 00:19:34 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 11 Feb 2023 00:19:35 GMT
ENV LANG=en_US.utf8
# Sat, 11 Feb 2023 00:19:36 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 11 Feb 2023 00:26:05 GMT
ENV PG_MAJOR=13
# Sat, 11 Feb 2023 00:26:06 GMT
ENV PG_VERSION=13.10
# Sat, 11 Feb 2023 00:26:07 GMT
ENV PG_SHA256=5bbcf5a56d85c44f3a8b058fb46862ff49cbc91834d07e295d02e6de3c216df2
# Sat, 11 Feb 2023 00:30:10 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 00:30:10 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 00:30:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 00:30:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 00:30:13 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 00:30:14 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 00:30:16 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 00:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 00:30:17 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 00:30:18 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 00:30:19 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:b3e346c15c2377ec0e75cc9efa98baecd58b0e9bb92f0ec07eeda0bcc7e67fc7`  
		Last Modified: Fri, 10 Feb 2023 21:25:13 GMT  
		Size: 3.4 MB (3412353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f692279d70e546549132ad9e3cae75f2decb7f64e52867935ae59c7d8b160c1`  
		Last Modified: Sat, 11 Feb 2023 00:37:55 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7501feb79631a909e9f88bb3f5f5d4218524231f2494e59ffb4e4d5f3b3bfe`  
		Last Modified: Sat, 11 Feb 2023 00:37:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3134f649d9b8ac6c2b9ea3ed29bf9758c3a9228fc83c842dabecaa521464df`  
		Last Modified: Sat, 11 Feb 2023 00:39:12 GMT  
		Size: 93.3 MB (93342599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d3ac8bda428270e9882e80f0fe0112705168cfc34ae7864f004946a59e63e1`  
		Last Modified: Sat, 11 Feb 2023 00:39:01 GMT  
		Size: 9.0 KB (9027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cb769d24a014b4b72b98bc659bb0dfca8f999dd80676aafec8ec5a2c64ac45`  
		Last Modified: Sat, 11 Feb 2023 00:39:01 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee6bd62ef5a2a5a7909e016ac5a8ece731cd9f7e875e3913b2a3b8ad3732aedb`  
		Last Modified: Sat, 11 Feb 2023 00:39:01 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e442d719b0ae58f42733f6e0c9eadf2bb8fd096961cf2bf6dc502afdc4151cd7`  
		Last Modified: Sat, 11 Feb 2023 00:39:01 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:e3ae6781629f2c2b13cb954336860c59302879762f937cc1dee78bf8933be528
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97697841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb97aff5e685626d20b150d330f52e6fe2317faca2314c4359fdfb9ff9288cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:36 GMT
ADD file:ec037a0d4b462d12963ac20d9ec49bb73b4bcaf84d4bc7b364ebf93667e585b0 in / 
# Fri, 10 Feb 2023 21:20:36 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:24:55 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 11 Feb 2023 04:24:56 GMT
ENV LANG=en_US.utf8
# Sat, 11 Feb 2023 04:24:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 11 Feb 2023 04:33:26 GMT
ENV PG_MAJOR=13
# Sat, 11 Feb 2023 04:33:27 GMT
ENV PG_VERSION=13.10
# Sat, 11 Feb 2023 04:33:27 GMT
ENV PG_SHA256=5bbcf5a56d85c44f3a8b058fb46862ff49cbc91834d07e295d02e6de3c216df2
# Sat, 11 Feb 2023 04:36:50 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 04:36:55 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 04:36:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 04:36:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 04:36:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 04:36:59 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 04:36:59 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 04:37:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 04:37:01 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 04:37:01 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 04:37:02 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:aa3c56f9c6f127b6c8f628c95db165741ca400d19bdaef2752d80f093e47451e`  
		Last Modified: Fri, 10 Feb 2023 21:21:37 GMT  
		Size: 3.4 MB (3390750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d7704dad0718e44953e6e5377507fc3cb2a9980ace972b76c8f08076991b04`  
		Last Modified: Sat, 11 Feb 2023 04:46:58 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fcb5e7a550e7b18e05838b48f571c1d54c7bce3624373e7b334a691305b0c30`  
		Last Modified: Sat, 11 Feb 2023 04:46:58 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e52132f862df2603332660df6e3cbc24e4ff49af24fe9904337659adf6dd92d`  
		Last Modified: Sat, 11 Feb 2023 04:48:52 GMT  
		Size: 94.3 MB (94291493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820c3e2c6bcf9d352e878a758d7a364424a1460104457f91fc9f86b371f3e2e8`  
		Last Modified: Sat, 11 Feb 2023 04:48:29 GMT  
		Size: 9.0 KB (9028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f504713e4fed92b12f0bd8fe68be366a258565f88c4194d59435d72348d2e4c7`  
		Last Modified: Sat, 11 Feb 2023 04:48:29 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1044b953173b0e79e97010c1310cb3760372d684f131e50c4b0dd56a7326d7f4`  
		Last Modified: Sat, 11 Feb 2023 04:48:29 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfff83eb30343c9cbb0d1c6b151cf3647ea4ed2814ae9abef07eb263be23d363`  
		Last Modified: Sat, 11 Feb 2023 04:48:29 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:13-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:d6696cc72b2fc99d51f6cad0b44075ead1281cb97430fdaf9f3a57375cf39212
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92546863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248b7c6aa8eb2c695bb4a00cbf1352471688cb9d8827db8abacd2e6cabc00ec6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:25 GMT
ADD file:03b2fb4d732a294329449ff55c5d84f7d2735e6510985718979469994f3a607b in / 
# Fri, 10 Feb 2023 21:41:26 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 04:39:56 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Sat, 11 Feb 2023 04:39:56 GMT
ENV LANG=en_US.utf8
# Sat, 11 Feb 2023 04:39:57 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Sat, 11 Feb 2023 04:46:04 GMT
ENV PG_MAJOR=13
# Sat, 11 Feb 2023 04:46:05 GMT
ENV PG_VERSION=13.10
# Sat, 11 Feb 2023 04:46:05 GMT
ENV PG_SHA256=5bbcf5a56d85c44f3a8b058fb46862ff49cbc91834d07e295d02e6de3c216df2
# Sat, 11 Feb 2023 04:49:22 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 04:49:27 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 04:49:27 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 04:49:28 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 04:49:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 04:49:28 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 04:49:28 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 04:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 04:49:29 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 04:49:29 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 04:49:29 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:24c4f8de3549a39c64b0edc2cfa68769b373f35138d0f13725100160bb32d4e2`  
		Last Modified: Fri, 10 Feb 2023 21:42:16 GMT  
		Size: 3.2 MB (3175116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98c4bc67df93b58de2a395f9131065d574c703299c6bab4946c78b3f528fa23`  
		Last Modified: Sat, 11 Feb 2023 05:11:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e9d012299f4104ac3fef850a121e9a8e314a6b63f740b0f9ca843e0b57f55e`  
		Last Modified: Sat, 11 Feb 2023 05:11:46 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def2cc9cfa794b11853d4ad459d5b4fd7b46989a923c2db0777ebfea135ae878`  
		Last Modified: Sat, 11 Feb 2023 05:12:53 GMT  
		Size: 89.4 MB (89356148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:138a4f2774e9b4a9df30642af842fb8e1558341847e471dcb4488216f89e73ce`  
		Last Modified: Sat, 11 Feb 2023 05:12:42 GMT  
		Size: 9.0 KB (9025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c39b4a620e9aa6561051d82940ea752b7dee9b943be139fcae0236b77d94a5`  
		Last Modified: Sat, 11 Feb 2023 05:12:42 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c70673e8e13be987738308609a3699c37ecd635b5fae4fd4d030ac0732581ce`  
		Last Modified: Sat, 11 Feb 2023 05:12:42 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5f85e5cfecc7ab9910d87daff96ff5bac7354f8d3acf787e64ab707995592`  
		Last Modified: Sat, 11 Feb 2023 05:12:42 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
