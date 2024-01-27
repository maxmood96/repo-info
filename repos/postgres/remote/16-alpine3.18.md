## `postgres:16-alpine3.18`

```console
$ docker pull postgres@sha256:37182f02e7b8e0e8278d5a77b046d5d08f3e4daca44945bd743ca69a517a8835
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

### `postgres:16-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:be23329b4a1bb7e457f13477ee63ecf2fcb7a2870691605f1a466709066930e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94259930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b467784150b4277be95973c59cc8c0f42f5d7c50c0b71c99b02b0be9ee2fcf13`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:1471daf455ea89c888c0c3f074af7748c7c7348f33c87035f9b27cecfe6e1e76`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b8e370acd07516dd9e90399c12d5c0c948b971be902f0b905b182a89dac23d`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04bf16d3630d45e0da4048cb4299dafd4c4bdf64ca4c3334c43845023856df0`  
		Last Modified: Sat, 27 Jan 2024 00:57:21 GMT  
		Size: 90.8 MB (90840551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d096409f68e112d9aaf0920f7e80aaa1ccc0da99ae719737754a06505883f5c2`  
		Last Modified: Sat, 27 Jan 2024 00:57:20 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e8b153868a1695bd6155a59f439306db723f4a72de5b77b3b64c0fefce1fed`  
		Last Modified: Sat, 27 Jan 2024 00:57:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4fb7fe2cd42b2334826ebcdd39217fba275bcadb06c7ef449884c9124e73b7`  
		Last Modified: Sat, 27 Jan 2024 00:57:20 GMT  
		Size: 167.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc48a70337d9cb125f26ee70ce0c78d43dccb85703cf002fd9a6dda2e9530020`  
		Last Modified: Sat, 27 Jan 2024 00:57:21 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b06acc36daa76386e63641e469e26fccd6c0cbb9dbd74416e455db533879e9`  
		Last Modified: Sat, 27 Jan 2024 00:57:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:3857154f8b52c757dc1f14d0ccf2c7a914e150bac76c28ae5e28c8413156aab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.9 KB (843944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77718435b2c0170167681f6ec51299035b8ce7de5df105f8dcfe14f42ade709`

```dockerfile
```

-	Layers:
	-	`sha256:71ce9c7e3f3ebdf8cb05bcaa33378a155d4a2edf9b9b25e5ef42be09891bfbaf`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 806.5 KB (806494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4adecb9ff5e0edb860af00902d69d89e6d23a5c63a0f1a35db31f8646bf2a765`  
		Last Modified: Sat, 27 Jan 2024 00:57:19 GMT  
		Size: 37.5 KB (37450 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:cfa8d83e8b0b2ed51e54fd260dac3a6e2236a3b97f14a2b34f56946f20c6fd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92894553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8681640d60df7313ce3b81362b1ded5cc5ccdbc632c8db74ff825cebbbe2bb13`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:ed2bcd998f24ef331a98c6df196cdd722dc8c0a2f223024d0feeddbd592e0f40`  
		Last Modified: Sat, 06 Jan 2024 15:03:14 GMT  
		Size: 89.7 MB (89730840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77547209d6a57c1743ed96c821960785ef0db26c9beb9ef42a78b515b605844f`  
		Last Modified: Sat, 06 Jan 2024 15:03:12 GMT  
		Size: 9.6 KB (9565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26cebe866cd73051d70a6ee097e81932b60d766c884ee19a1077994fcb2c0f9`  
		Last Modified: Sat, 06 Jan 2024 15:03:13 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880e5dab84a31a8f5e68612ef48be76a8f5a22b56169e2deb386570ef4aec029`  
		Last Modified: Sat, 06 Jan 2024 15:03:13 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa22c82ef0e127c57445b05ed1b75b6296df32dee48b0b65f482977bd4d2277`  
		Last Modified: Sat, 06 Jan 2024 15:03:13 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887ba1fbe3bb39af8359682bcb8105310de0f58a6982d72f4312e94a93d56729`  
		Last Modified: Sat, 06 Jan 2024 15:03:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:76d5d73165128f294bff57754d4ff7ef858a7f3c3a72345895e2fe76f79809de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57f586e5c67ba0f83b4dd3680be1d86c9e4d667b77466329401d793295145fa2`

```dockerfile
```

-	Layers:
	-	`sha256:85e26d2bb68c787749965113a89ead584f5830375d0de0599574283787e8768d`  
		Last Modified: Sat, 06 Jan 2024 15:03:11 GMT  
		Size: 37.4 KB (37376 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:7134f95fd6fbddcbeb3becda6b2233fe86c53d2021d18f4f46e7190a573c2096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87537724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91464cee2a45d12f00aba38b067fccf240924d276cb8a1083f81c609645f494`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:28 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Thu, 30 Nov 2023 22:49:29 GMT
CMD ["/bin/sh"]
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV LANG=en_US.utf8
# Fri, 22 Dec 2023 00:27:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c815d47e00d2d70d22df505cd75fee458db7a056e91cea2be9e903be7b3cf887`  
		Last Modified: Wed, 13 Dec 2023 01:53:29 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc211333283e058626a589bb51c6eea6895cc4988e59b83890811a76d7be3a1`  
		Last Modified: Wed, 13 Dec 2023 01:53:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bcc7cbad1f562c541e23d6ec52717b2c49ceaf88e535fb7d7e9501316f0fc54`  
		Last Modified: Wed, 13 Dec 2023 01:53:32 GMT  
		Size: 84.6 MB (84619870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aaa0d637011f4e4715941b8ad30f8ff177128978cf6a8c0bc673831d717ab7d`  
		Last Modified: Wed, 13 Dec 2023 01:53:29 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c0cdf1d5ec3c1316e174cb38b2c88641af332280497a5ddf826e6aa784fd60`  
		Last Modified: Wed, 13 Dec 2023 01:53:30 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aff6cccaba07f1abf3e8a3623c238fb015dcde5dee20d17c723d7e8352abea0`  
		Last Modified: Wed, 13 Dec 2023 01:53:30 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90263a4f437543904d26a1b465b7ecd8db780bb5f6f76849c59598e73ac2392`  
		Last Modified: Fri, 05 Jan 2024 03:31:11 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2380e62cc0716abc634b8c05f0469be1540ede361ff05194361b3c3f4ff5468c`  
		Last Modified: Fri, 05 Jan 2024 03:31:12 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:68e767fa5dd065537fe99ed10cce9713dfbbcf9b01e88e757e957cd54087faf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.9 KB (843947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fc54bfbc46d5339ac4babfadb83b1c06867646e5511233b2aae93733cc79b8`

```dockerfile
```

-	Layers:
	-	`sha256:b36878313e1b77edebde80c26817dea04b470ba6eead02339e5d211918f39aac`  
		Last Modified: Fri, 05 Jan 2024 03:31:11 GMT  
		Size: 806.5 KB (806522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97109b3ead4f8dbd0b48c09ba9b07b10e30035e36832e216ca0b4b95ec96e128`  
		Last Modified: Fri, 05 Jan 2024 03:31:11 GMT  
		Size: 37.4 KB (37425 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:56c7c4a8b6b6b6bed6bda2ad61e3d9700b358499d0c02c3e24a551e0dd2286d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93202370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af24b19b8a2cb2196f1be51a29e06c5a1aa65479a2874428457de08f9bbda1ec`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:f3aa49f43d2325dcd2ea85b08b44a7bb660db13a09e65b63d2cb3cbd51b7149b`  
		Last Modified: Wed, 13 Dec 2023 03:03:05 GMT  
		Size: 89.9 MB (89852488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66a5ab8125ab10899fd42c8d424b7a4aeca07351aaf0520e4a2d96f345c2c0a`  
		Last Modified: Wed, 13 Dec 2023 03:03:02 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779fd16670501c3098e5ee16237d336412708dfc65643d180b531fa4e4e4917`  
		Last Modified: Wed, 13 Dec 2023 03:03:03 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eaf998d605de6262c48142125f2cb207223f53aecaaed50e5828d697085b6a`  
		Last Modified: Wed, 13 Dec 2023 03:03:04 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f32f074166b7442bd5063a393e029bcf0c2dd04d597f40c505133640b56f58`  
		Last Modified: Fri, 05 Jan 2024 02:25:40 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6791ab54d7f6c42d6bee1d4efc999418a4b285b19dda31df3732013c2f724c3`  
		Last Modified: Fri, 05 Jan 2024 02:25:40 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:d75891ebe17cf8958dd54edaea13e6f5eaae72d0d59d1d131ef19c0c8d4fa597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.8 KB (843795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6836725e54be657486f0fbc3b58c6797dbcb8bc5d864ff6608b21733eb3eb760`

```dockerfile
```

-	Layers:
	-	`sha256:12b52fa53175de9938fd642aaf07ca1f4fa7f65b35f423e5a412c92292fce3b4`  
		Last Modified: Fri, 05 Jan 2024 02:25:40 GMT  
		Size: 806.5 KB (806503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd4200b9a12b31d2ae8d05395d89e561ac78700ba3b62130a14c44e2a2ecd7ac`  
		Last Modified: Fri, 05 Jan 2024 02:25:40 GMT  
		Size: 37.3 KB (37292 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:d65ec2d3ed261eba492fb900104610ae8b3b14a36a8363a75eff4008c792a510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99237999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36e546e27c65fa6da25f1120146694703bd6deb012e3835f0d2f305411e197d`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:9c78428caec6b2fdbb9879c01897cd24641eb6a735d6a3a2fb8f212384f436db`  
		Last Modified: Sat, 27 Jan 2024 01:58:20 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56311d723e2987a7b51329c7b4fb14ff0a24546eb32c0eea37635287a1805063`  
		Last Modified: Sat, 27 Jan 2024 01:58:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a306bd96ce9299b2529e27270247465deca5c66edfd8dc6cd1f477358dbbcd`  
		Last Modified: Sat, 27 Jan 2024 01:58:22 GMT  
		Size: 96.0 MB (95982097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f17fe3bd2de598f3d997f2125f68fbc0f4de280048af0054b4f15a4fcf6c86d`  
		Last Modified: Sat, 27 Jan 2024 01:58:20 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bdedf64b4b1d5d6accb1226c04b05cb2658c4c307e23d22193a4956b89e9b21`  
		Last Modified: Sat, 27 Jan 2024 01:58:21 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731c26ed9a7dacbf7564973b1070269ed221ea97ccfe3bbea8d816f5a7e0560`  
		Last Modified: Sat, 27 Jan 2024 01:58:21 GMT  
		Size: 166.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b5790c33d1e256266979d5153abcac601f01c961386f4b7676d83b206cb1a8`  
		Last Modified: Sat, 27 Jan 2024 01:58:21 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cd2aff53d06fe3a03d14fb23b3bac22e8de7ee1506d4c7d8a994e29245acbd`  
		Last Modified: Sat, 27 Jan 2024 01:58:22 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:deeeb4307d1b898730accac966892ae0c230aa850785cd172a57e354796a7c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.9 KB (843889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ae6c959f5b4b65772b923a138089caf12647a6ad3ef24e872fafb2e2305d1bc`

```dockerfile
```

-	Layers:
	-	`sha256:089c238d72fd6a50cf42d56a2281867fe5df70891c193375bf3fa17f1316ea34`  
		Last Modified: Sat, 27 Jan 2024 01:58:20 GMT  
		Size: 806.5 KB (806474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ee2f3b67f4e07a8cb4b9ce004c3805418eba18ce838bbe5070cc973c315b39`  
		Last Modified: Sat, 27 Jan 2024 01:58:20 GMT  
		Size: 37.4 KB (37415 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:298e51f17d2078b45acd855113ed0e237ca2c1cdfd4904a402bf95eb71b9742b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99976049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f86a2df013a5f794acdd8e3081d00782fcb9d4892f6f840a6f3758cf14a3cc3e`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:9d14f64022b41519bda9f47b8d875b9a3e7a094f5894f3eb86d22cd1c4f81975`  
		Last Modified: Sat, 27 Jan 2024 10:17:22 GMT  
		Size: 96.6 MB (96610716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403657f21712e71cf7276c1a9482ba23eff25beabd3ec58577d88f3483944b56`  
		Last Modified: Sat, 27 Jan 2024 10:17:20 GMT  
		Size: 9.6 KB (9566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8588cc60a18035ae6e7e5ca7c675be78952156a74494ed594d37e46306514125`  
		Last Modified: Sat, 27 Jan 2024 10:17:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f73b40ab56840c239d19395306953cc9d5d5b09fbaf9fadf50bc42aaaf1a420`  
		Last Modified: Sat, 27 Jan 2024 10:17:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b540aebcbc2c75be0ead97b0d0fa2a9110329277314f9255c48ec70c84db71a`  
		Last Modified: Sat, 27 Jan 2024 10:17:21 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336b5c9d9ba9d5772472edacbee62e2ecc7b02267eaaaa57c22d769cda2db274`  
		Last Modified: Sat, 27 Jan 2024 10:17:21 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:c44469983427f2083076751aea4f5b3ab2e6c300b030394a78fac22dcfba8280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.8 KB (840800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df387608b90e5e8be23bb207297a6ba419b29a360dac91415549e0cdcea39d4c`

```dockerfile
```

-	Layers:
	-	`sha256:85e47ad0aee9c09fa77570574d43b30541782d6b0abf867f42846804f54d0c31`  
		Last Modified: Sat, 27 Jan 2024 10:17:20 GMT  
		Size: 803.5 KB (803471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:945e652b3258ffc3dab7ef81aa320d8d62217278d81ffa28123d048d4b16072b`  
		Last Modified: Sat, 27 Jan 2024 10:17:19 GMT  
		Size: 37.3 KB (37329 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:16-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:51d37f24e078c4a1e646a9634db179bd111379cde238f0e05c9127ed69d6d747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95917793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f69859c8ced43a48cf7fd53df937666b1609397f0eb776f6dbd5df482e1d93f`
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
ENV PG_MAJOR=16
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_VERSION=16.1
# Fri, 22 Dec 2023 00:27:15 GMT
ENV PG_SHA256=ce3c4d85d19b0121fe0d3f8ef1fa601f71989e86f8a66f7dc3ad546dd5564fec
# Fri, 22 Dec 2023 00:27:15 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 22 Dec 2023 00:27:15 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:0cead63ae84b93f86e0859449a310c8f05cfefe2a6987e5ac3051c209e72f8de`  
		Last Modified: Wed, 13 Dec 2023 01:10:53 GMT  
		Size: 92.7 MB (92683481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab17958c1031062ecdb9bb47ec374fdbc9911127a3afc78fc40ef5cdc66a9c39`  
		Last Modified: Wed, 13 Dec 2023 01:10:52 GMT  
		Size: 9.6 KB (9570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbe45538fed15568c76cdb961d09212141515ff406bae311e01143f550cb6b8`  
		Last Modified: Wed, 13 Dec 2023 01:10:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c63236f9cf20be039c9ff2cec010ed07d9e1950e80e3da9193b4381e64e3d2`  
		Last Modified: Wed, 13 Dec 2023 01:10:52 GMT  
		Size: 168.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f27698fa27d17507e10a98f66779c069e88fda52c9c2ce4fcc62ec99698e62`  
		Last Modified: Fri, 05 Jan 2024 02:08:47 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90bf7a12e837fee7c13d36b34d0e268cdaa06fe8e2dc7985760f3176be34382`  
		Last Modified: Fri, 05 Jan 2024 02:08:47 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:16-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:c1ab52a04bc804edc755932297993864bec281d692153331344510a5fbac2c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **842.1 KB (842143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf61beee654a1b745f4cd257718a34897a01295d78537738649f89ef9be9fc5`

```dockerfile
```

-	Layers:
	-	`sha256:0b6ffaa7ab03ce9b1b35d128bb2c5042ebbbf64dfb327a7044da0bc7da5cc0fc`  
		Last Modified: Fri, 05 Jan 2024 02:08:47 GMT  
		Size: 804.9 KB (804858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a03b1e31eeedfd80d2a14bd52bd65d0583cd500f9927f90c012ebbaf2a580db`  
		Last Modified: Fri, 05 Jan 2024 02:08:47 GMT  
		Size: 37.3 KB (37285 bytes)  
		MIME: application/vnd.in-toto+json
