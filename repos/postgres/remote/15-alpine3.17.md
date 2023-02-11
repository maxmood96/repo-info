## `postgres:15-alpine3.17`

```console
$ docker pull postgres@sha256:4ff023196ab87fe155d471f7f3db5cc914f472ea8d5e3acf5b957579999fad5a
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

### `postgres:15-alpine3.17` - linux; amd64

```console
$ docker pull postgres@sha256:53a02ecbe9d18ff6476e6651c34811da39f054424c725fc15d2b480fc3fab877
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94097015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a35e2c987a69cd37f078e911ea336e0576d980fa5c3eceac3e24e3b3e90eeb1`
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
# Sat, 11 Feb 2023 05:02:46 GMT
ENV PG_MAJOR=15
# Sat, 11 Feb 2023 05:02:46 GMT
ENV PG_VERSION=15.2
# Sat, 11 Feb 2023 05:02:46 GMT
ENV PG_SHA256=99a2171fc3d6b5b5f56b757a7a3cb85d509a38e4273805def23941ed2b8468c7
# Sat, 11 Feb 2023 05:05:28 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 05:05:29 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 05:05:30 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 05:05:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 05:05:30 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 05:05:30 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 05:05:31 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 05:05:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 05:05:31 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 05:05:31 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 05:05:31 GMT
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
	-	`sha256:b95308fc3d317f9d902bc98ab7ca5a4ae14f2e1fdc9082050e37f6d09ad34623`  
		Last Modified: Sat, 11 Feb 2023 05:19:36 GMT  
		Size: 90.7 MB (90706544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0668417a86c843812fee781d9f862a180d1d35fa8936ff1062e4e1b6d1622af`  
		Last Modified: Sat, 11 Feb 2023 05:19:24 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fc954fc7aab68d8c9bbfb55b3a500024b85c0f9126767e8c4b65b494af092e`  
		Last Modified: Sat, 11 Feb 2023 05:19:25 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f84ed83d814338eda02e9941d478da5dd2c7f14594bcaa2601d3192af46867`  
		Last Modified: Sat, 11 Feb 2023 05:19:24 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e42e95b14320acc58478673bad0b2a24e5a15ca8dc1b004b1bc2a4c69193fd`  
		Last Modified: Sat, 11 Feb 2023 05:19:24 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:c06192502a8c502337dd7636d27c538e8e8af7a7d6e2f59b04a188daefc2baf3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93612417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44a35c3214e308667dba147e4117d1e8126503e556e3fcc7043c8952af43ca5`
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
# Mon, 09 Jan 2023 23:30:28 GMT
ENV PG_MAJOR=15
# Fri, 10 Feb 2023 18:49:45 GMT
ENV PG_VERSION=15.2
# Fri, 10 Feb 2023 18:49:45 GMT
ENV PG_SHA256=99a2171fc3d6b5b5f56b757a7a3cb85d509a38e4273805def23941ed2b8468c7
# Fri, 10 Feb 2023 18:52:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 10 Feb 2023 18:52:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 10 Feb 2023 18:52:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 10 Feb 2023 18:52:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 10 Feb 2023 18:52:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 10 Feb 2023 18:52:58 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 10 Feb 2023 18:52:58 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Fri, 10 Feb 2023 18:52:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 18:52:58 GMT
STOPSIGNAL SIGINT
# Fri, 10 Feb 2023 18:52:58 GMT
EXPOSE 5432
# Fri, 10 Feb 2023 18:52:58 GMT
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
	-	`sha256:64d75f951b84c3d8de851a23e7391600c3b19a59c2d7b5974d3797eb576c8273`  
		Last Modified: Fri, 10 Feb 2023 19:07:18 GMT  
		Size: 90.5 MB (90489275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d38a3a302cf6e8e5555763a6f92dbb833cc7f24cfc6a046ea30379a783f1ca2`  
		Last Modified: Fri, 10 Feb 2023 19:07:04 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140545ef9a75b99bb57720a1f69063686a3be554096f1dbb353bc446a457b865`  
		Last Modified: Fri, 10 Feb 2023 19:07:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f0737c51d9b6e0a8ab3bcfd0399316c4762675a36ac942317f3d7730bd09bf`  
		Last Modified: Fri, 10 Feb 2023 19:07:04 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3985b4f7983b85bcea2cffa1f7a82fb88dd845a6ed804a9648178d9cc25732ea`  
		Last Modified: Fri, 10 Feb 2023 19:07:04 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:11dbce8cc9364bf037690c2e1179906e28759978c910ad32f19f452f51a343d0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88139394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4419c3b4bfe7734dc3721bcff5d44562ae73b806e202f9f05afc28e357b342b4`
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
# Mon, 09 Jan 2023 21:46:30 GMT
ENV PG_MAJOR=15
# Fri, 10 Feb 2023 19:16:16 GMT
ENV PG_VERSION=15.2
# Fri, 10 Feb 2023 19:16:16 GMT
ENV PG_SHA256=99a2171fc3d6b5b5f56b757a7a3cb85d509a38e4273805def23941ed2b8468c7
# Fri, 10 Feb 2023 19:19:04 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 10 Feb 2023 19:19:05 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 10 Feb 2023 19:19:06 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 10 Feb 2023 19:19:06 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 10 Feb 2023 19:19:06 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 10 Feb 2023 19:19:06 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 10 Feb 2023 19:19:07 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Fri, 10 Feb 2023 19:19:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 19:19:07 GMT
STOPSIGNAL SIGINT
# Fri, 10 Feb 2023 19:19:07 GMT
EXPOSE 5432
# Fri, 10 Feb 2023 19:19:07 GMT
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
	-	`sha256:2a9f1d661d98a8546d3bd67582f437f1ce54384ce0161a193caa3ff8c2075fbe`  
		Last Modified: Fri, 10 Feb 2023 20:26:55 GMT  
		Size: 85.3 MB (85258291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a759bf28f7d36b7043d56e0d7e47ff36a939ca6f7681ca56b0f6a051f3bdbd`  
		Last Modified: Fri, 10 Feb 2023 20:26:42 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f123b6bcca9bc0ecddfbfce687aa798a8c6065392be7b6b27288cf3a4d8e5f3`  
		Last Modified: Fri, 10 Feb 2023 20:26:42 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1604f462211106a13a0e6ca22f9d13c0d49514bdd9374ada7a39e5a420ca13bf`  
		Last Modified: Fri, 10 Feb 2023 20:26:42 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db225b71930c82205bbb197c5896aa9c8fa4957b759fa56a578c904e72e074ad`  
		Last Modified: Fri, 10 Feb 2023 20:26:42 GMT  
		Size: 4.8 KB (4781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:57e2ee1c020ca08ce251c3bf2ffbe95fb76ea106073471629f9d546286dc418d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91831640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68d4a8d9d3d9275239b87ed097ab5afcd294349e96c1a1d30b4528ae43614204`
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
# Sat, 11 Feb 2023 03:07:59 GMT
ENV PG_MAJOR=15
# Sat, 11 Feb 2023 03:07:59 GMT
ENV PG_VERSION=15.2
# Sat, 11 Feb 2023 03:07:59 GMT
ENV PG_SHA256=99a2171fc3d6b5b5f56b757a7a3cb85d509a38e4273805def23941ed2b8468c7
# Sat, 11 Feb 2023 03:09:58 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 03:09:59 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 03:10:00 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 03:10:00 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 03:10:00 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 03:10:00 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 03:10:00 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 03:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 03:10:01 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 03:10:01 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 03:10:01 GMT
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
	-	`sha256:75d514bb4aa7956b346ecec7a4c6de3f35335b7c721e4135fd2579ca1d64c576`  
		Last Modified: Sat, 11 Feb 2023 03:19:04 GMT  
		Size: 88.6 MB (88553650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217da6f41d9e722df36d3afa17845c285df3cdf7ad86e4dfdbbc724af8997bfb`  
		Last Modified: Sat, 11 Feb 2023 03:18:56 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a3f48231261b6c34da7b341ba73922e72466c291daa3fd89ec4b26682e66de`  
		Last Modified: Sat, 11 Feb 2023 03:18:56 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6571a6afccc930a7f3aee356c5cd6bc3e42841b540a24ba2171b119238bcac`  
		Last Modified: Sat, 11 Feb 2023 03:18:56 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae7d38f54c4c995a4bdfbb25601547118fef3e811501f5d0a1ba49ce42abb2d`  
		Last Modified: Sat, 11 Feb 2023 03:18:56 GMT  
		Size: 4.8 KB (4786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:e15cb3abd2c85fe4ae20cfc6c983837fb1cb96e442998e5f1ed399126f8a20d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98948618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e40e67914eddf1734e386eb33a29fff956c8e5e042d9ef0b6900f841abe967b`
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
# Sat, 11 Feb 2023 00:19:37 GMT
ENV PG_MAJOR=15
# Sat, 11 Feb 2023 00:19:38 GMT
ENV PG_VERSION=15.2
# Sat, 11 Feb 2023 00:19:39 GMT
ENV PG_SHA256=99a2171fc3d6b5b5f56b757a7a3cb85d509a38e4273805def23941ed2b8468c7
# Sat, 11 Feb 2023 00:22:27 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 00:22:28 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 00:22:29 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 00:22:30 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 00:22:31 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 00:22:32 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 00:22:34 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 00:22:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 00:22:35 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 00:22:36 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 00:22:37 GMT
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
	-	`sha256:853319dfdd5057c36738b10c0705cd524c9ddd43c4ae99e9d47ec46febb78a07`  
		Last Modified: Sat, 11 Feb 2023 00:38:05 GMT  
		Size: 95.5 MB (95520368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3efae35f72f0e222da8c7166d3e8aa2671c9b1a23fb15152cd380f6867d7eb8`  
		Last Modified: Sat, 11 Feb 2023 00:37:53 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff06529c1ab78dfeaad824511ef6845e5458d476db806427dcfcebf7954dcb4`  
		Last Modified: Sat, 11 Feb 2023 00:37:53 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8f300dda1aa6b3cc2e48e9df9211eda6bb4675c8d15cb4f48494fb6a306db8`  
		Last Modified: Sat, 11 Feb 2023 00:37:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffb3f445f9fe1596ede1c18ef84da33130e70082e4cbf4c81cc1b0d25d05be9`  
		Last Modified: Sat, 11 Feb 2023 00:37:53 GMT  
		Size: 4.8 KB (4781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:c0d0474df18029c723dc06b695cba3a81ebf71d897570e3cedacadb96ad34137
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99949054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ce2043af328fb77eee6f1fdc3c90c1f364c11456cdf706e9da774ddde4a706`
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
# Sat, 11 Feb 2023 04:24:58 GMT
ENV PG_MAJOR=15
# Sat, 11 Feb 2023 04:24:59 GMT
ENV PG_VERSION=15.2
# Sat, 11 Feb 2023 04:24:59 GMT
ENV PG_SHA256=99a2171fc3d6b5b5f56b757a7a3cb85d509a38e4273805def23941ed2b8468c7
# Sat, 11 Feb 2023 04:28:47 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 04:28:52 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 04:28:53 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 04:28:54 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 04:28:55 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 04:28:56 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 04:28:56 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 04:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 04:28:57 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 04:28:58 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 04:28:58 GMT
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
	-	`sha256:c2a4b4f920130dd4575347fa4a7dc616542d4312751cce2538b3b6c34407168c`  
		Last Modified: Sat, 11 Feb 2023 04:47:19 GMT  
		Size: 96.5 MB (96542277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4fe5673d0f68f70c6b5efced25d1e5db563677ad475352db2d96ddc7a72ac27`  
		Last Modified: Sat, 11 Feb 2023 04:46:55 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8318dcc714355ecd243dcae3d299519ec0748ed82c4e82a4d7d73dd36e186f78`  
		Last Modified: Sat, 11 Feb 2023 04:46:55 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf6a7dbbaaa88e602fe37e7d9648c25d37bc5e92d5514502fe93758a59e1b14`  
		Last Modified: Sat, 11 Feb 2023 04:46:55 GMT  
		Size: 193.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70900759c41b19e437b9718fbfb744f9965e9f22cfee34a0add45b423ba23c6a`  
		Last Modified: Sat, 11 Feb 2023 04:46:55 GMT  
		Size: 4.8 KB (4785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:7b579c47e222d36074e802a154f43b22cf7fc9c303c4cfc9243a287b16ccd17d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94693919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e40f6fe3aa381b3da6cc332d703bf9fefabdc5910db2ce89b8fc47d6b1e9656`
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
# Sat, 11 Feb 2023 04:39:57 GMT
ENV PG_MAJOR=15
# Sat, 11 Feb 2023 04:39:58 GMT
ENV PG_VERSION=15.2
# Sat, 11 Feb 2023 04:39:58 GMT
ENV PG_SHA256=99a2171fc3d6b5b5f56b757a7a3cb85d509a38e4273805def23941ed2b8468c7
# Sat, 11 Feb 2023 04:42:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Sat, 11 Feb 2023 04:42:45 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Sat, 11 Feb 2023 04:42:45 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Sat, 11 Feb 2023 04:42:45 GMT
ENV PGDATA=/var/lib/postgresql/data
# Sat, 11 Feb 2023 04:42:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Sat, 11 Feb 2023 04:42:46 GMT
VOLUME [/var/lib/postgresql/data]
# Sat, 11 Feb 2023 04:42:46 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Sat, 11 Feb 2023 04:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 11 Feb 2023 04:42:46 GMT
STOPSIGNAL SIGINT
# Sat, 11 Feb 2023 04:42:46 GMT
EXPOSE 5432
# Sat, 11 Feb 2023 04:42:46 GMT
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
	-	`sha256:4d6bb6419e2c9374fd0661bc402a5f1bc4e89c40b6f8281bf7107c5ecb0b9792`  
		Last Modified: Sat, 11 Feb 2023 05:11:56 GMT  
		Size: 91.5 MB (91502778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8e4aad40673ceff3b2b64ace84e6658c7ff26ec5bd5f15957ff8fb5a8c4ae2`  
		Last Modified: Sat, 11 Feb 2023 05:11:45 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ec1a5cd6d720278f50ec36d5a5cc23b04a41140905fd06e4433ecf25b952af`  
		Last Modified: Sat, 11 Feb 2023 05:11:45 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8934aa4d823bd6f8876dcafdfdb85b65080bbbf5caa7d4d437d3c5ee16e830eb`  
		Last Modified: Sat, 11 Feb 2023 05:11:45 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada0b8c598cac2a50690bc05e6df37cc88d464e32398414a1b14dc5fcc5683b9`  
		Last Modified: Sat, 11 Feb 2023 05:11:45 GMT  
		Size: 4.8 KB (4782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
