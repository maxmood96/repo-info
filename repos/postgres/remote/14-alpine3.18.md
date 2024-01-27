## `postgres:14-alpine3.18`

```console
$ docker pull postgres@sha256:b67536ea03961475922cccb926d6deb0f0383bcae01c99dd86ccf827cd2643cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:14-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:d713b425436e91da0c2d45ed2a63f2ed0809f94759537bccb939c17055a1b2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92752019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d20fe884f9ea58db3f4f7adb8adab4a2ec7d68858dbfb276d0409e8f90d774f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=14
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=14.10
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=c99431c48e9d470b0d0ab946eb2141a3cd19130c2fb4dc4b3284a7774ecc8399
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330b7ebafa5820228e91eee845269fbec0a9e67080285a71266c8dba1ad7a0f6`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a317eb750470ccd90c37bd6b6a045250a846ce55b6c0b3f2730080bd05fd51`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427face4b6af9edd6ff8d1233a4d30a5a2f4b15813785d40d2fa7c0921e16ccd`  
		Last Modified: Sat, 27 Jan 2024 00:57:21 GMT  
		Size: 89.3 MB (89333000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed207720fd4987097e6ecaad460a7ac557b5242ed4b4ae99cbd00823df0e57b`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb698be67a125c6784a1cc1444e9fd565e739744df50ff30b9c37d032f556d3`  
		Last Modified: Sat, 27 Jan 2024 00:57:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c90e1eaa381162edc9ca4fee2fa8a3183e9ba848c152224ef3fb24d7d15b468`  
		Last Modified: Sat, 27 Jan 2024 00:57:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c862d87326bfd784a478fb1d58c0ff9f40bdb532e44b4ff716a075bacb6dd1a`  
		Last Modified: Sat, 27 Jan 2024 00:57:20 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83ec7f5dbd35807aae399fca79d6020dc9ea22d657fcc1e7b8bd1ccd5f52d14c`  
		Last Modified: Sat, 27 Jan 2024 00:57:21 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:61015780063be263c7b98142d12e61b9c43989abb986c2766ac22044e114293b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f15e8ed3db65816b810657e8c4ad5defb3506b10a24b27b47a843bbe5100368`

```dockerfile
```

-	Layers:
	-	`sha256:72948b605242cdafe3f83ff2c92bb08783aac234ebdea97f88a63715699bc7d5`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 806.2 KB (806188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74a8d5d93846e09e8f128e2eb536a7d4e885468f5257c7c67c95b821eaf77831`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 36.9 KB (36913 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:39612d3661900cd62e8c6d3559d01270c344a33b636867c8c5270458e8cd0002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91447133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b18d6aa9819d3a8eabcf873725b6d8b954cb211a8c3ad61fd4f794f96ec4020`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=14
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=14.10
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=c99431c48e9d470b0d0ab946eb2141a3cd19130c2fb4dc4b3284a7774ecc8399
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2005880f0a8d3c4d23e45c16fdaa58cb4377636fcd3d162307d11bebfd27facf`  
		Last Modified: Sat, 06 Jan 2024 15:03:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a947db43f66e2ba9dc7d21d7f9ad1fd2472652795e4ff560358a2bdc892de0af`  
		Last Modified: Sat, 06 Jan 2024 15:03:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c58330a2e7b87a3296e41aa8490057d67c7843ed8d6508b5f13a50ee3ece30`  
		Last Modified: Sun, 07 Jan 2024 03:36:03 GMT  
		Size: 88.3 MB (88283781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0c094dc5e72660383ec53ba7202fc17b3d507ae327cd66c23ae02cc412f68e`  
		Last Modified: Sun, 07 Jan 2024 03:36:00 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa9b814595db31a39b85d1ce1769d344345d417b0e32cca5536343dd8d97db`  
		Last Modified: Sun, 07 Jan 2024 03:36:00 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c9c4d2e5ec3968e2251b0e2245f1a1ef3a16f57467c1e898ab89da1e8864b3`  
		Last Modified: Sun, 07 Jan 2024 03:36:00 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7048f51c57ff8d61c4e77cb374a7196c7abafa84505d0d6e36e5e057b5821fc`  
		Last Modified: Sun, 07 Jan 2024 03:36:01 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c9810e534e7a756520cb7f686d64d8b960726ebce6686951053bac55567f8d`  
		Last Modified: Sun, 07 Jan 2024 03:36:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:d45861d0e182b1ccf6fcbb785bee543f30db211b776067d9c709178f87fe6366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f68c917fc76042935e618dd570743faceed21b9e826edcaa1396cd8f618d061`

```dockerfile
```

-	Layers:
	-	`sha256:6def22c4b667f8473af74e4eded4c5a29b75dcfa40e59bcfb1491a501c64baa9`  
		Last Modified: Sun, 07 Jan 2024 03:36:00 GMT  
		Size: 36.7 KB (36664 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7e98df27ecb71e57805192cfbac8e3a43abc8bf548b462c527ba84ccf57d05db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86120894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b009fd37b912f79328c28d1da5828fb11684a1d711faafcb3bd9446780780d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=14
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=14.10
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=c99431c48e9d470b0d0ab946eb2141a3cd19130c2fb4dc4b3284a7774ecc8399
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee793a8dd1ca22a66ebbb05c284efb9f864b9604841787848ee3f0014bd6cbe`  
		Last Modified: Sat, 27 Jan 2024 16:48:53 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662e46b68fafa16500a341d3f119c8776a2c9330794b9052ab010587645f0a7f`  
		Last Modified: Sat, 27 Jan 2024 16:48:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c65608430ee85b486208949b03b4d992948d5a411a4451abc4031ef42340e5`  
		Last Modified: Sat, 27 Jan 2024 17:44:33 GMT  
		Size: 83.2 MB (83203022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46f97eaf40da224e8101039d392ade21a490e45486605fa20decb328d55781a`  
		Last Modified: Sat, 27 Jan 2024 17:44:30 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09af4482c4c3ffd7ce945f3bc04814aaae34839cb4e55721c2e779ab0d1742c2`  
		Last Modified: Sat, 27 Jan 2024 17:44:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737d9b78ef0afeaa9e7c7bb37fb9323f26eb1874f3ec64656080ba1231b71af8`  
		Last Modified: Sat, 27 Jan 2024 17:44:30 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb89666be4e22c74ab5c7b14970be255a9a0c1265817dae8dee0bb16c6f9c8bc`  
		Last Modified: Sat, 27 Jan 2024 17:44:31 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78adce697d21478565de9e87319334a3937eefc027d49e89fd43fde38f8a41a3`  
		Last Modified: Sat, 27 Jan 2024 17:44:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:eee187dd79095554de4a31a104e4bcd6e20d8fda99730edff6f5422dab1577d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1f35d8321cf0907bcf6afc1f7520fb916f2490a6fdba4442796660f9e4a75d`

```dockerfile
```

-	Layers:
	-	`sha256:267a884f10edfeeed6d8f3582487931d290441fd4283d892ef2093c37e668476`  
		Last Modified: Sat, 27 Jan 2024 17:44:30 GMT  
		Size: 806.2 KB (806208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca569fc356b994693476a9bda439bc3c0fb756b3fa893bbbfb5b443d36009ba`  
		Last Modified: Sat, 27 Jan 2024 17:44:30 GMT  
		Size: 36.9 KB (36879 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:94f574a80088742f2e5da15c08839a5c2738169e1aa492e8e4eb401f35cc5ff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91690615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03173addee961298dd00bba376443c9735627bd139f7b93ebb0c8d2f298b623`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=14
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=14.10
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=c99431c48e9d470b0d0ab946eb2141a3cd19130c2fb4dc4b3284a7774ecc8399
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f976195ad28258b2cce8a3feff1817f99cc57aaba200954d184c38814d91795`  
		Last Modified: Wed, 13 Dec 2023 03:03:02 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03936fc3c66b1d124f91e7128a308d9c4de24f1374198667f3b5dcf9c8a0c88c`  
		Last Modified: Wed, 13 Dec 2023 03:03:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57d2eb43c9d225e1c23fd4b00ba43111a3b0523f42b963b53e68406653c22e9`  
		Last Modified: Wed, 13 Dec 2023 04:15:11 GMT  
		Size: 88.3 MB (88341091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec8b2fc98246232402ebf2d00fe00932b3474e835be5e6ab2b50867a940cab4`  
		Last Modified: Wed, 13 Dec 2023 04:15:08 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32d4311c321432b8c47990ffe1d15a6b96a38f90890b75dfc02588093279d49`  
		Last Modified: Wed, 13 Dec 2023 04:15:08 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebada864a5a3a60e237ea039d91bb50f7b0b6b15d197c104cd0898369c476c8`  
		Last Modified: Wed, 13 Dec 2023 04:15:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0448f79e824420ae8f5feb7bbac438c85deda3292bc8bc0b9d8cc78edf665587`  
		Last Modified: Fri, 05 Jan 2024 02:30:08 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899eff895e40867050e8554b3c40edb73c7fdd7ed894ba0349e8d0d8d52843a2`  
		Last Modified: Fri, 05 Jan 2024 02:30:08 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:a01556b7c6c06f93f686e0c7403a0d569204e2b7844153430d7929592b6bba7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.9 KB (842948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df6c194d70d2da2ba51c24d1cd4c2c1bc4152c0abfa6e7a00a25eeeef974000`

```dockerfile
```

-	Layers:
	-	`sha256:2734123e962ecbfa1bb1fe54ddbec43cdf839c9fecd6ff479ca47fea8560d3ba`  
		Last Modified: Fri, 05 Jan 2024 02:30:08 GMT  
		Size: 806.2 KB (806195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a495c4bed9fc59ace4cc15149fb7cf94f6d3f4249f13f47254997c1513fd7bd3`  
		Last Modified: Fri, 05 Jan 2024 02:30:08 GMT  
		Size: 36.8 KB (36753 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:6e60c344921bc683eb24db0dad260dbfc6c2f9c9c08c9d200930841a82abca2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97735967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74d88a2c931203ae52b3334ef62c7baa5bf5e60f35f2d49f9ae783a54b422fe6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=14
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=14.10
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=c99431c48e9d470b0d0ab946eb2141a3cd19130c2fb4dc4b3284a7774ecc8399
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe6c4f7e7b726bba957179def6211645b0e67470f2e5dd48ecf912bd8cfb564`  
		Last Modified: Sat, 27 Jan 2024 01:58:16 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd21fc1dc9dff2a8d1324df5ce4517d5857d092ca8ef5625bcae4ffca9f6c0fd`  
		Last Modified: Sat, 27 Jan 2024 01:58:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e383e84ad8ca80f49909ca9badc584423f179c086cfd05104a9c005382e0712`  
		Last Modified: Sat, 27 Jan 2024 01:58:18 GMT  
		Size: 94.5 MB (94480429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1283eddecf26d4f743077a06de99fcc5366b40d715721fc89128fd869ac7210c`  
		Last Modified: Sat, 27 Jan 2024 01:58:16 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ff89922ce233774892678be59806f24bf35abb762fe36074ee7cefe1159ba7`  
		Last Modified: Sat, 27 Jan 2024 01:58:17 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c043750a5eccac39147d4246aa493bf66b97e7ec5fcab0a0f01f6eca7272b79`  
		Last Modified: Sat, 27 Jan 2024 01:58:17 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727b88997af5c672b035ce4371fe35629164dfd7169646cad51fc33fc35a1a35`  
		Last Modified: Sat, 27 Jan 2024 01:58:17 GMT  
		Size: 5.4 KB (5417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb69c11c59e1ea3f2fedbd5675c59273ea1021808af5d8989186b79a6ef9b08`  
		Last Modified: Sat, 27 Jan 2024 01:58:17 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:b7da8f732f86825fb46b544e92875e1a621db8149958637fe3b37012eb11751b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.1 KB (843055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89a40b534ad41de229917175a656873e4b688f34d3eae4d163456640b01e649`

```dockerfile
```

-	Layers:
	-	`sha256:583cc2460404f0dc4ed1097bc895462675bb6f75b058d11e41e383e6e39065be`  
		Last Modified: Sat, 27 Jan 2024 01:58:16 GMT  
		Size: 806.2 KB (806173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921c5c815bb19c78c33c52ed0d353cc95bf34682438039d2735a36d83a39cd66`  
		Last Modified: Sat, 27 Jan 2024 01:58:16 GMT  
		Size: 36.9 KB (36882 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:aa0d5fb9aabb055a0445abfadff91032aa2ea92633ae81a6709702c0c9389bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98381864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ccb02c8b9ff9feb8d90f26720b538e9415bc9e51c50782ce421e9287799c46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 22 Dec 2023 00:27:15 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=14
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=14.10
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=c99431c48e9d470b0d0ab946eb2141a3cd19130c2fb4dc4b3284a7774ecc8399
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d4e1f043d7d605723903297bf782bdc880c196eda3fe11e4246a234fc0a04e`  
		Last Modified: Sat, 27 Jan 2024 10:17:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43a3563625547593d82964e1003937876728a971f59a85e17dbe2a78201e6eb`  
		Last Modified: Sat, 27 Jan 2024 10:17:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d3ae5805207532e64f876be3194c705e24c20209f76aa8089a8ddd2e22cd4`  
		Last Modified: Sat, 27 Jan 2024 10:29:39 GMT  
		Size: 95.0 MB (95016890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596bccbad9d4b94059332a57be20086dab87af8983e9ab638ff1522baf5ecef3`  
		Last Modified: Sat, 27 Jan 2024 10:29:36 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a0a0dbe8ac6b8090b8796f7326a3baa665b09a1648c3e935e33b80e448d880`  
		Last Modified: Sat, 27 Jan 2024 10:29:36 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1645839be4702f9a8291378e4ce8c399500405d4afa2854637d55918515af3b`  
		Last Modified: Sat, 27 Jan 2024 10:29:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b598a22a7f636eb5968d48943b7fdb8a148666596fbbdbf7f1a36ac4244882b`  
		Last Modified: Sat, 27 Jan 2024 10:29:37 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6959af3cc9ba1d91fda869209be85bf0d158f8cef22d956bb900678c9cbf2fec`  
		Last Modified: Sat, 27 Jan 2024 10:29:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:97dafb024db7be068413af05a8ccd098028bab1f0ec88f9ea40c5357eb1198f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.9 KB (839944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edea223c5f823d11d374041222e3ceace3f4cf6e444ed546cc692046f3e44762`

```dockerfile
```

-	Layers:
	-	`sha256:9d911ef0e27defe9eb9132647e4ae1804b39990192bf3ab26a78ff55338c96e4`  
		Last Modified: Sat, 27 Jan 2024 10:29:36 GMT  
		Size: 803.2 KB (803159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b6c6e5735ad184e90beb39490dc4b56b4e2e7d414d574a78473a5d1e46bd27`  
		Last Modified: Sat, 27 Jan 2024 10:29:36 GMT  
		Size: 36.8 KB (36785 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:1c41801b3c1277f0e4add1728d8948ff2ed466625072c3bfb26dcde8400d9b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94394589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5e37cfddbf9cbb73a4064472a60873dd5c7a3b0374eaa5fdbbbe083181f8cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 30 Nov 2023 22:42:08 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Thu, 30 Nov 2023 22:42:09 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=14
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=14.10
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=c99431c48e9d470b0d0ab946eb2141a3cd19130c2fb4dc4b3284a7774ecc8399
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 22 Dec 2023 00:27:15 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
STOPSIGNAL SIGINT
# Fri, 22 Dec 2023 00:27:15 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 22 Dec 2023 00:27:15 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d9eca7e3578b4c16792649c73fb65141bee2d048a99d88a9450e527a42ff6c9`  
		Last Modified: Wed, 13 Dec 2023 01:10:51 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd2ac5a1eda861bfa4578d408f9e37fb3e11394e1c790c366377d9f15578e1c`  
		Last Modified: Wed, 13 Dec 2023 01:10:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589a2054c601c34f4f224c49a8ecb750a78b3fc104408909d0a62c9b9f7e9faa`  
		Last Modified: Wed, 13 Dec 2023 01:26:17 GMT  
		Size: 91.2 MB (91160647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dfd7512fbaf6cc6ebacda99c6c62958bc5d0cea345a7758b0db15a9867f41aa`  
		Last Modified: Wed, 13 Dec 2023 01:26:16 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199c7555c0346115304f0d5f09a935e295ce343f0398bd223eaee792a0546a9a`  
		Last Modified: Wed, 13 Dec 2023 01:26:16 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c538ab414ededf0046dcdb88dccbd02afa55697f6e6bcc414ea4ca54c8e3ba71`  
		Last Modified: Wed, 13 Dec 2023 01:26:16 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da5b9c52d584c05e0ca5519067ca729e3cbfd949232fa23dcd1ff1f4d10db52`  
		Last Modified: Fri, 05 Jan 2024 02:15:09 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d413d59965b9e1287fac47e26162ffc5dd958dd3fb24e6e8ec5fdd70f293d664`  
		Last Modified: Fri, 05 Jan 2024 02:15:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:b59e8d4505b652cf405b95c6389e7e5617ac3c93738ab948a2104a107cf5b600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.3 KB (841298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b08aaf12c15f96c934d07b9869d9f3febf9b11b0166c180c341bdf10cdf7ce4`

```dockerfile
```

-	Layers:
	-	`sha256:3c93ae114ed68b77f9afc6d2a50cab8c9809cadbcfa08bc20e8e74919efe874c`  
		Last Modified: Fri, 05 Jan 2024 02:15:09 GMT  
		Size: 804.6 KB (804552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e808a7040667642055bdae8f7b6d9870c21b26c08dc6dd25bbec1c6afe2ad30f`  
		Last Modified: Fri, 05 Jan 2024 02:15:09 GMT  
		Size: 36.7 KB (36746 bytes)  
		MIME: application/vnd.in-toto+json
