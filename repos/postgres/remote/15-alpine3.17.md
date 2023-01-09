## `postgres:15-alpine3.17`

```console
$ docker pull postgres@sha256:df2eb226944dd353cb7f1a47e41b68609b349b4f5f77c424af5dca91137a7055
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
$ docker pull postgres@sha256:69bd7cc493f84c970cf0af442dbf1ed15315b63c3a1cd2f8556dc9e98004a11f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94091691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8428074961ed299e3897ae0737f21761f64e29a473de2d5ebcda117ff443760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 19:21:00 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 09 Jan 2023 19:21:00 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jan 2023 19:21:01 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 09 Jan 2023 19:21:01 GMT
ENV PG_MAJOR=15
# Mon, 09 Jan 2023 19:21:01 GMT
ENV PG_VERSION=15.1
# Mon, 09 Jan 2023 19:21:01 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Mon, 09 Jan 2023 19:23:55 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Mon, 09 Jan 2023 19:23:56 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 09 Jan 2023 19:23:57 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 09 Jan 2023 19:23:57 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 09 Jan 2023 19:23:58 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 09 Jan 2023 19:23:58 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 09 Jan 2023 19:23:58 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Mon, 09 Jan 2023 19:23:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 19:23:58 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jan 2023 19:23:58 GMT
EXPOSE 5432
# Mon, 09 Jan 2023 19:23:58 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb286326f602388731b6b7d5ea90c1396c25225841d81c9a1e28c6020be1e322`  
		Last Modified: Mon, 09 Jan 2023 19:36:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63139c77dd7e81ef958b7ecd822c2f71cfa0a9920fd8f46a9bc6e98569b4c5b6`  
		Last Modified: Mon, 09 Jan 2023 19:36:00 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9743166247fbb7f2e001913930aabdb2e4e783cd9c50606faaaae0c224fda3f`  
		Last Modified: Mon, 09 Jan 2023 19:36:11 GMT  
		Size: 90.7 MB (90705042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74511a0f4fffc0d44775fa0313b4eee028b1fa0185cb1e885ec19c14efbd6eb4`  
		Last Modified: Mon, 09 Jan 2023 19:35:58 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff50ec8f35d169ce9d6cf010a34b62267716eb242564a6e4cce4976c882cdc86`  
		Last Modified: Mon, 09 Jan 2023 19:35:58 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a3210db3fb75bc4a7573075b53d51a5d9bf4ef518fbbbf068dd9b931da0d35`  
		Last Modified: Mon, 09 Jan 2023 19:35:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a297527e76d0ea48af68a00b0fa883116354017232e32f3c8d02bdb41320f27`  
		Last Modified: Mon, 09 Jan 2023 19:35:58 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; arm variant v6

```console
$ docker pull postgres@sha256:ed0702cac5adfda8a28f468fe611f141bcf343f335365046b4bfb5c0baef8fb5
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91901900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b2cdba498f4cb28387dac375e1df040fc42cb12d47ce535baa9d3e5c259e46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Wed, 30 Nov 2022 21:10:19 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Wed, 30 Nov 2022 21:10:19 GMT
ENV LANG=en_US.utf8
# Wed, 30 Nov 2022 21:10:20 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 30 Nov 2022 21:10:20 GMT
ENV PG_MAJOR=15
# Wed, 30 Nov 2022 21:10:20 GMT
ENV PG_VERSION=15.1
# Wed, 30 Nov 2022 21:10:20 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Fri, 23 Dec 2022 00:52:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Fri, 23 Dec 2022 00:52:33 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Fri, 23 Dec 2022 00:52:33 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Fri, 23 Dec 2022 00:52:33 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 23 Dec 2022 00:52:34 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Fri, 23 Dec 2022 00:52:34 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 23 Dec 2022 00:52:34 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Fri, 23 Dec 2022 00:52:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Dec 2022 00:52:34 GMT
STOPSIGNAL SIGINT
# Fri, 23 Dec 2022 00:52:34 GMT
EXPOSE 5432
# Fri, 23 Dec 2022 00:52:35 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd022df475c75e388b1fd7a4163f33c0ff1b1d74fdc20b70d7997fe03aa044af`  
		Last Modified: Wed, 30 Nov 2022 21:27:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed70ce3a42bb46bc919e74b0e65503324722dcbef23cf71e04c33adf27e1835`  
		Last Modified: Wed, 30 Nov 2022 21:27:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ee5026b5cde3a4e0f24fc02286f600edd12c020df65bd9bfd17b2b422caff3`  
		Last Modified: Fri, 23 Dec 2022 01:07:28 GMT  
		Size: 88.8 MB (88778860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f140138b1f4c2b9752a40d27e80da6496b970e30e49268d85ab2508d419b3dc`  
		Last Modified: Fri, 23 Dec 2022 01:07:13 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2749657a57d77bd294d8574e6d5d70ad887cc0306b8bbde122dbde47b38dc730`  
		Last Modified: Fri, 23 Dec 2022 01:07:13 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64834020362d140d1ca56bea0cfd5a95a310c0c5793be7a8f58dbc814cc556b8`  
		Last Modified: Fri, 23 Dec 2022 01:07:13 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85e0cce2e8bcf87748d4ab56702ea8324c5d38e0572f7a15426573b5d23a184`  
		Last Modified: Fri, 23 Dec 2022 01:07:13 GMT  
		Size: 4.8 KB (4781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; arm variant v7

```console
$ docker pull postgres@sha256:02f865334942734ce529973f920d04df89b4580a2788e1f25ec9ca926e1bbf97
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86528313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5ee7cf480248a0e8fdf8bbf296bb5733d4aeaaedd3406077d698e32f45f4ef`
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
# Mon, 09 Jan 2023 21:46:30 GMT
ENV PG_VERSION=15.1
# Mon, 09 Jan 2023 21:46:31 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Mon, 09 Jan 2023 21:49:21 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Mon, 09 Jan 2023 21:49:23 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 09 Jan 2023 21:49:24 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 09 Jan 2023 21:49:24 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 09 Jan 2023 21:49:24 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 09 Jan 2023 21:49:24 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 09 Jan 2023 21:49:25 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Mon, 09 Jan 2023 21:49:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 21:49:25 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jan 2023 21:49:25 GMT
EXPOSE 5432
# Mon, 09 Jan 2023 21:49:25 GMT
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
	-	`sha256:2dfdb13be29539b5c0a2827c91e3f593a6616878ec09273fb2848593198a74ed`  
		Last Modified: Mon, 09 Jan 2023 22:04:11 GMT  
		Size: 83.6 MB (83647207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a40cc4fad57733e51312bb787001866dbb29986375c4bc463c52d292ccb47f3`  
		Last Modified: Mon, 09 Jan 2023 22:03:58 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160d5917a22c6d193626829436e37e5c592391a38bd57c1bda229b70285688ec`  
		Last Modified: Mon, 09 Jan 2023 22:04:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafcb59d991d78014a9ff75e3622c554ee3b633b8b331f3d8abfc2df239d9e42`  
		Last Modified: Mon, 09 Jan 2023 22:03:58 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b11b1213e039f71ffbaa6c057c57fadeaf6216b6ae2e6bbaa0823a0f308b4ba3`  
		Last Modified: Mon, 09 Jan 2023 22:03:58 GMT  
		Size: 4.8 KB (4781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:bb62224a7a69cf9c7f99823a6e224d61401c54a159b79e3e8f9337d1f42dfa9d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91810215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c930beec93df56849c09efb842c50efb548c1fb61deda574bf893c9f08037a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jan 2023 17:04:48 GMT
ADD file:3080f19f39259a4b77cc53975de0184c78d4335ceb9ffb77a2838d0539ad6f85 in / 
# Mon, 09 Jan 2023 17:04:49 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:48:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 09 Jan 2023 18:48:08 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jan 2023 18:48:08 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 09 Jan 2023 18:48:08 GMT
ENV PG_MAJOR=15
# Mon, 09 Jan 2023 18:48:08 GMT
ENV PG_VERSION=15.1
# Mon, 09 Jan 2023 18:48:09 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Mon, 09 Jan 2023 18:50:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Mon, 09 Jan 2023 18:50:14 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 09 Jan 2023 18:50:14 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 09 Jan 2023 18:50:14 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 09 Jan 2023 18:50:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 09 Jan 2023 18:50:15 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 09 Jan 2023 18:50:15 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:50:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:50:15 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jan 2023 18:50:15 GMT
EXPOSE 5432
# Mon, 09 Jan 2023 18:50:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:a9eaa45ef418e883481a13c7d84fa9904f2ec56789c52a87ba5a9e6483f2b74f`  
		Last Modified: Mon, 09 Jan 2023 17:05:12 GMT  
		Size: 3.3 MB (3259241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6004074ad02a4a75a55e9f9de3d1384503d5aaaeeaac87e22ef67302f57a7397`  
		Last Modified: Mon, 09 Jan 2023 18:59:54 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690395976a322335d42ab9b0d16f50a759c5f6fb5ffca7e4df22ee42c859325b`  
		Last Modified: Mon, 09 Jan 2023 18:59:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16c16c48e64b6786c687745e0b792e6494616a8a71986300068156188d520b5`  
		Last Modified: Mon, 09 Jan 2023 19:00:01 GMT  
		Size: 88.5 MB (88534954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7b4dc281d025cea6a01f2cac38d07b42ac6a2409ccb0365e0250c2a7c3cfa8`  
		Last Modified: Mon, 09 Jan 2023 18:59:52 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230023af7758e441a66a1c86974e75d598558b96f629fbfd0d8adb0fc2996886`  
		Last Modified: Mon, 09 Jan 2023 18:59:52 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ef3435c70b6836584707727b27291bdb58bf4e39e489051be2355973dc4aaf`  
		Last Modified: Mon, 09 Jan 2023 18:59:52 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3916e03a26374430229b37e512ad5ff9758140488a4bc41ebfdd4a8afeb455ea`  
		Last Modified: Mon, 09 Jan 2023 18:59:52 GMT  
		Size: 4.8 KB (4780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; 386

```console
$ docker pull postgres@sha256:a00c19cdd0cfbc9ebcbcc88454cef2261bbb150eac849e6fa9d3c724c43b8cde
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98924522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6eb81d553be8d89f97851ff9a91bc7e2c8c5b0d0c3339c77d4c18931d6fd33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:00 GMT
ADD file:d03619a0ef81726c34189e849b80cc92da908eb36e116f28275d5765e6d0919a in / 
# Mon, 09 Jan 2023 17:05:00 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 18:36:20 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 09 Jan 2023 18:36:21 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jan 2023 18:36:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 09 Jan 2023 18:36:23 GMT
ENV PG_MAJOR=15
# Mon, 09 Jan 2023 18:36:24 GMT
ENV PG_VERSION=15.1
# Mon, 09 Jan 2023 18:36:25 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Mon, 09 Jan 2023 18:39:25 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Mon, 09 Jan 2023 18:39:26 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 09 Jan 2023 18:39:26 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 09 Jan 2023 18:39:27 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 09 Jan 2023 18:39:28 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 09 Jan 2023 18:39:29 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 09 Jan 2023 18:39:31 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Mon, 09 Jan 2023 18:39:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 18:39:32 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jan 2023 18:39:33 GMT
EXPOSE 5432
# Mon, 09 Jan 2023 18:39:34 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:40e5b0b2e2bde18974628cadecd8a2f190f45f06c32846c16885d69b2908bf68`  
		Last Modified: Mon, 09 Jan 2023 17:05:42 GMT  
		Size: 3.4 MB (3408318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093d697a6418eb05c03bd1f2ec776ef43f3366c0b203e0b233d9e5fb3e07af37`  
		Last Modified: Mon, 09 Jan 2023 18:53:16 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ef2d146cf2212827af5cf49a06f3ae223b858fc14efa4eef4a3544e262d439`  
		Last Modified: Mon, 09 Jan 2023 18:53:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9ca5cc959ec392fafa4e5afc910e1c8660625a3ba4716cd6d8e211df621baa`  
		Last Modified: Mon, 09 Jan 2023 18:53:25 GMT  
		Size: 95.5 MB (95500307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5207fd804c9ba356f167a188029f80f49d4ece4013569bdd29d6937a40979ba8`  
		Last Modified: Mon, 09 Jan 2023 18:53:14 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5ab8c53867806a26511766af504348cdce1ff75f72e2a72291ae19cb7258f34`  
		Last Modified: Mon, 09 Jan 2023 18:53:14 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f1e1dc463a65f74ffc69a47cc86e23ddc9646a0d88286fd96b6bc8c128fd9b`  
		Last Modified: Mon, 09 Jan 2023 18:53:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f4241df19a98d71d76acdce350cc6ade6fe1cab5cee72034f087c738adc733`  
		Last Modified: Mon, 09 Jan 2023 18:53:14 GMT  
		Size: 4.8 KB (4781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; ppc64le

```console
$ docker pull postgres@sha256:6ed8b3830a4a50fb74160097f6f2c382214a778198e2c1d532fda5c0d1909bd9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99940789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f8bbcab52d9f1cbe1a2d85518fa1cf008e39bcb57873fa9a4dfbdfe594e297`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:13 GMT
ADD file:9a1d27fdc0c915f387f2446c85193d5215b18020b313114f0bf2799efcc1baae in / 
# Mon, 09 Jan 2023 17:05:13 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 22:29:04 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 09 Jan 2023 22:29:05 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jan 2023 22:29:06 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 09 Jan 2023 22:29:06 GMT
ENV PG_MAJOR=15
# Mon, 09 Jan 2023 22:29:07 GMT
ENV PG_VERSION=15.1
# Mon, 09 Jan 2023 22:29:07 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Mon, 09 Jan 2023 22:32:32 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Mon, 09 Jan 2023 22:32:36 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 09 Jan 2023 22:32:37 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 09 Jan 2023 22:32:37 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 09 Jan 2023 22:32:38 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 09 Jan 2023 22:32:39 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 09 Jan 2023 22:32:39 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Mon, 09 Jan 2023 22:32:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 22:32:40 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jan 2023 22:32:40 GMT
EXPOSE 5432
# Mon, 09 Jan 2023 22:32:41 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f45bfda3aa14e255d9eb4c9a108eb3d8c6721946b4aa2e5808e5092242344a1c`  
		Last Modified: Mon, 09 Jan 2023 17:05:56 GMT  
		Size: 3.4 MB (3384562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1151129ee425b166e8a582e89a68f81d3abc38c488b7c2bc3df173fc6a7b0d`  
		Last Modified: Mon, 09 Jan 2023 22:48:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29c12e4681195d016bcf82fe4146b0530e49b0e81a229e7ed4581d30bd1bc76`  
		Last Modified: Mon, 09 Jan 2023 22:48:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f088a332310bd8f5764c3b689ea7adb92645752d81eb46e66451184cc96241`  
		Last Modified: Mon, 09 Jan 2023 22:49:02 GMT  
		Size: 96.5 MB (96540201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b02e7dc9ac09ed264a4610ea57eed95e6eaaa73e97894e781f65fe781c0995`  
		Last Modified: Mon, 09 Jan 2023 22:48:40 GMT  
		Size: 9.5 KB (9454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6519b25180326071c699eb954bf0038df3a3bc78f4c1574c1646ecb977c9dda3`  
		Last Modified: Mon, 09 Jan 2023 22:48:40 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0741135c2bf342f49d090651b91441a828c47ef3cc19c923a952592df4e49c`  
		Last Modified: Mon, 09 Jan 2023 22:48:40 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064833db01a85c92f70f6aa56b159b2f355502bfa310590594a8ae7f38ec5859`  
		Last Modified: Mon, 09 Jan 2023 22:48:40 GMT  
		Size: 4.8 KB (4783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postgres:15-alpine3.17` - linux; s390x

```console
$ docker pull postgres@sha256:e85bba0235c711dccbc37face0ee3d52c1dd75e46abc46568618f68e3ab7587a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94671133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d864e03a367194246fd902bec25cfba3c3eff586e0e2269c62a19325288a853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:44 GMT
ADD file:eabe7c3c368e65478b53ac35c1daf3b703f2bca4ecdab2d080a65e8b981d7d4a in / 
# Mon, 09 Jan 2023 17:05:46 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 22:19:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql
# Mon, 09 Jan 2023 22:19:13 GMT
ENV LANG=en_US.utf8
# Mon, 09 Jan 2023 22:19:15 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Mon, 09 Jan 2023 22:19:16 GMT
ENV PG_MAJOR=15
# Mon, 09 Jan 2023 22:19:16 GMT
ENV PG_VERSION=15.1
# Mon, 09 Jan 2023 22:19:17 GMT
ENV PG_SHA256=64fdf23d734afad0dfe4077daca96ac51dcd697e68ae2d3d4ca6c45cb14e21ae
# Mon, 09 Jan 2023 22:23:31 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		bison 		coreutils 		dpkg-dev dpkg 		flex 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		llvm-dev clang g++ 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 	./configure 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-krb5 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version
# Mon, 09 Jan 2023 22:23:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample
# Mon, 09 Jan 2023 22:23:42 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 2777 /var/run/postgresql
# Mon, 09 Jan 2023 22:23:42 GMT
ENV PGDATA=/var/lib/postgresql/data
# Mon, 09 Jan 2023 22:23:43 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 777 "$PGDATA"
# Mon, 09 Jan 2023 22:23:44 GMT
VOLUME [/var/lib/postgresql/data]
# Mon, 09 Jan 2023 22:23:44 GMT
COPY file:8532d121e17f2ce9a5f749e2bb1c2800d41f880daad16051150ea9824a2ed88f in /usr/local/bin/ 
# Mon, 09 Jan 2023 22:23:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jan 2023 22:23:45 GMT
STOPSIGNAL SIGINT
# Mon, 09 Jan 2023 22:23:46 GMT
EXPOSE 5432
# Mon, 09 Jan 2023 22:23:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:ae982806674c51a962c0fdd6e19f464ebd673df529c5cfb7c1d049e0b618d384`  
		Last Modified: Mon, 09 Jan 2023 17:06:50 GMT  
		Size: 3.2 MB (3170744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662a09d3140efd92c8236e927cd76468e6a9e6ec85e642c8be853af8115fc86b`  
		Last Modified: Mon, 09 Jan 2023 22:43:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5fdcfa24c97962c73bfbc6153d69d967abd53e8d047f34419139a3f3802614`  
		Last Modified: Mon, 09 Jan 2023 22:43:21 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54aaeeefab30cb0743c1a05e4b4475302a35cf6868737f78e9cb4ae5a12bd12d`  
		Last Modified: Mon, 09 Jan 2023 22:43:32 GMT  
		Size: 91.5 MB (91484369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cf73cc375ade2904808b21193c52d8e31a9ca2b4b56fbeb3e9cd33a49faa23`  
		Last Modified: Mon, 09 Jan 2023 22:43:20 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461b3d9ef6f65cbd6b81284b75daa2d60589ecce044a614518e46f445f89f3a0`  
		Last Modified: Mon, 09 Jan 2023 22:43:20 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cce71156228d41e75e39dc11585e3c8df73729dba657f432b2bd60c09735878`  
		Last Modified: Mon, 09 Jan 2023 22:43:20 GMT  
		Size: 192.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653b8d78e230d2146e771c391aab429236980ad47aac06de840d8feeb0b8efca`  
		Last Modified: Mon, 09 Jan 2023 22:43:20 GMT  
		Size: 4.8 KB (4784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
