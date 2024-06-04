## `postgres:14-alpine3.19`

```console
$ docker pull postgres@sha256:2774bcfa6916acb9593c91af0df5cf0c00bf12faf6d8bb9dbcc76d10881deec0
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

### `postgres:14-alpine3.19` - linux; amd64

```console
$ docker pull postgres@sha256:06445325fc7ac2cd6231d6933fac1ce996d99e992b4e984ac27c2e220350f1f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96231059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84c1196166faefecdc6ae092fd2b65d3f5d784784b43462fa2ffaf315c2fab4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=14
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=14.12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3becd19abbb155396552f1ec0b80e51eaaf82b975a77d9851c1a755c8560493b`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9dfbdc19fa057ba2a700170fc5e34c5ee2cdb9f521fd3dfc3a870498c978c2`  
		Last Modified: Mon, 03 Jun 2024 19:06:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b566db55b3a3791bd3dd4140b92a99c46f98621369b0e87b702fac9ae4c079e`  
		Last Modified: Mon, 03 Jun 2024 19:06:13 GMT  
		Size: 92.8 MB (92805834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ccc6e00aa304fc0dd9b2fe05e816e1eaa0d0c58dcf6600c4474a5019fbb977`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0824f57412488c616fe19dafdf1a370a747ffd11628ff267bffa00506e5942`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b246a629aaaae6319e93a0a552dc396d6488e4eed5a62d367377b0221b0436`  
		Last Modified: Mon, 03 Jun 2024 19:06:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62c567e35c84642d32e62ccf83717437d5fc25faa1b8edf3f68f00de15378d1`  
		Last Modified: Mon, 03 Jun 2024 19:06:11 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6617115c01455a1164efd2c0211ee17fb34a089148700254290a890d0070961e`  
		Last Modified: Mon, 03 Jun 2024 19:06:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:eadbe21e03dcab198402bbc81582ca4dc29621bbeded9bcfe5100f669c81f83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.5 KB (993465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f129b4b675694258e6a6673eccb0bda31e75fd495bad834bc0777bc3d6cd7a3f`

```dockerfile
```

-	Layers:
	-	`sha256:237b3c89a8144f8687e4f3be32a4b31ffbcc518be35e4d667e575b18ef0549e9`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 956.7 KB (956694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143073c12619dc0bd27e248075dd70e5102fcb6d285921d4ab7504755857f4d1`  
		Last Modified: Mon, 03 Jun 2024 19:06:10 GMT  
		Size: 36.8 KB (36771 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v6

```console
$ docker pull postgres@sha256:3e97c87c08197d2fe80077283318c355aeed41396912ee181431d589df4c2f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94725420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1ca31eca85136bbef9f6c596d1d56718ec37acf6f2e51d90d874915a7beb87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=14
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=14.12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860e35ae27435bcb376652f33da561573efc82cb903cc30ce3684aff0ca6d38b`  
		Last Modified: Mon, 03 Jun 2024 19:26:27 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a305f8be1993a674347a47e4e4da6dc04c8b7969a73d6830b0cfe4e8de939888`  
		Last Modified: Mon, 03 Jun 2024 19:26:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672ae149d8d84d1b1df4a8a0ddd641292c8d5b753c636f84b222b512f8510d6`  
		Last Modified: Mon, 03 Jun 2024 19:50:08 GMT  
		Size: 91.5 MB (91543527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cebaf0ed8cbc6c6f6583d4672803cd980248b2a71493453bff029dd7e7a4d7c`  
		Last Modified: Mon, 03 Jun 2024 19:50:06 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139a28f612818e1c4c9dc9cfed309c568bfeed2024c6bfb0b97f19163df6f563`  
		Last Modified: Mon, 03 Jun 2024 19:50:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4882afebcb497a2a77b78db7cac0943220497e58f36117b638b9ff98f69a8e8e`  
		Last Modified: Mon, 03 Jun 2024 19:50:07 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e64765b1d66e9c2a95758983c30d87d4771ba5368636cfa77c62fac6e74631e5`  
		Last Modified: Mon, 03 Jun 2024 19:50:07 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6481f5b282f4d9125f97516eb4be23e99383dfeebb1e7d44115da0aff8013d`  
		Last Modified: Mon, 03 Jun 2024 19:50:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:fe48284bdb570b40c827bd786ed42bfaaf0b24349c55e35a6164c8140910d099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 KB (36684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4625527b5f66ca7ec96d3be158252cbfca50182afa1a253eb705b79182dca54`

```dockerfile
```

-	Layers:
	-	`sha256:ee8f7295ec10e8f625a45ae7c6b498d639f57007d00d1ef3229a403a7a836f5e`  
		Last Modified: Mon, 03 Jun 2024 19:50:06 GMT  
		Size: 36.7 KB (36684 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm variant v7

```console
$ docker pull postgres@sha256:79b4c47fbfd8c2cdf838b3e29f2b502af5d98e47f7b489e4b17082fd5c72b5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89063430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb419debcfb3a95a6fc8e2a598a178d575220cc7f6f4fa93c6bf5e91f0f36c15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=14
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=14.12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e4bfd7c0deff5a703442b05eea3fc3238bd197ba703ae949a0a735a738790f`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a6f980339956e09a15f739f93841e0d33b8e50c83f4e1c2c83dd4ead7ef7a6`  
		Last Modified: Mon, 03 Jun 2024 20:42:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acfa537ad218f564c2d5a65f248548947aa47f2f79dd4791613cb56e72fb0d8`  
		Last Modified: Mon, 03 Jun 2024 21:24:48 GMT  
		Size: 86.1 MB (86128038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a7af8262aa4746b6a5823c620e2402715a58094058b103bb6231ab9537af6a`  
		Last Modified: Mon, 03 Jun 2024 21:24:45 GMT  
		Size: 9.2 KB (9203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948cd943e7fc708602b38128dbbe273b687454a6606ac83458bea7baf67e3ae6`  
		Last Modified: Mon, 03 Jun 2024 21:24:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0962678c59e9b4a3f1eadc3d03e8c7ac515c291acbf5dcde784e9664d52e0c03`  
		Last Modified: Mon, 03 Jun 2024 21:24:45 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a99ee8b5a91fb48c2c990514a96ff1315e746ea6e4372be710070ebae0ac6d0`  
		Last Modified: Mon, 03 Jun 2024 21:24:46 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ae96128de17a8a7fd41d8c48223232889e09214c84e361606b65d5ab69d534`  
		Last Modified: Mon, 03 Jun 2024 21:24:46 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:320a041160fdf4660f7d6f684e1ab62128d11e5a58975e08ac1553e396b147a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.6 KB (993615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ebf25e95a200d2a868a18a085700ed8a7831c76158ac45c12f6b8c313b46f7`

```dockerfile
```

-	Layers:
	-	`sha256:20bd18a6e0b648fb1356a45ddfc4c34a6e0a0d50a258b84ed3acdaf55b2225e3`  
		Last Modified: Mon, 03 Jun 2024 21:24:45 GMT  
		Size: 956.7 KB (956714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c78dd84883e5e4aa4ed24d37a22c211109cd350071056065a1ab3f9a97d1d23`  
		Last Modified: Mon, 03 Jun 2024 21:24:45 GMT  
		Size: 36.9 KB (36901 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:b704f2c1a0b8b3031f145f3ee944fa4cdcca41bf1a0ef3a66df3a70f8cf910e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94903743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ea63eaff4818d6a89b3723929f3ef7cf14e3cb14d85c9a5f75362fe44e8bd8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_MAJOR=14
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_VERSION=14.12
# Thu, 09 May 2024 18:31:12 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Thu, 09 May 2024 18:31:12 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:31:12 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:31:12 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:31:12 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:31:12 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:31:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:31:12 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:31:12 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:31:12 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6426790b86128c81359671377728ac209ddd73d25d62a98505f61e0f34e541c2`  
		Last Modified: Thu, 09 May 2024 22:23:47 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2765e6e641bc36e3e37080f48cbbeb6eb6beb085e0a5cc4d749578ec2b27d79`  
		Last Modified: Thu, 09 May 2024 22:23:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06042dbb507e00f914d8604a261e1b1f2526522f345222745ae6b2ee40808598`  
		Last Modified: Thu, 09 May 2024 22:39:07 GMT  
		Size: 91.5 MB (91539543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9036d8625308f3826db6d92baccbb96aab402e7164b27e927a1ca187645c0940`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 9.2 KB (9204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4e5f5618881bc83fa81e8c0cc4938ce6afaa5cfa27c90301503fbec772b688`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e6606ffbd6b44043b71d4c0a9625a6b3cabaa8d8353b30cc4e4def86ae66c2`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb6bfe745c6678a8368ef9b0f0b044eaa6d38331bac6b9044e18827c89a67f0`  
		Last Modified: Thu, 09 May 2024 22:39:06 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190c5164dfbefae3c456aaed4993e5b6b4f23ba5f6d03460ea83e6eb5523a63c`  
		Last Modified: Thu, 09 May 2024 22:39:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:a05c7de9d5646c88f03b1eafcc80b1d7772fef60a969ff2ef33a337dd8c9197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **994.7 KB (994710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93ff5ced05817247d5a235987a57767b92b18477013e3d7829a89ac0808f122`

```dockerfile
```

-	Layers:
	-	`sha256:4665767cf8ccecd45da4a25cd176a0842b235268f8b1e9cd14a19e00ee3151bf`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 957.3 KB (957328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bce73dd0322923624c9e0991b6b0e71d474882110db77d15778c0262d14a1f`  
		Last Modified: Thu, 09 May 2024 22:39:05 GMT  
		Size: 37.4 KB (37382 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; 386

```console
$ docker pull postgres@sha256:17b35bb19859dceea4f3896b441f12daf3c8320381088eea42db8a810c8d6c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101364395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef301481b8bfb3506486dcea0c2fca74242dbf121fb64ef1eb24837967effa4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=14
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=14.12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ae4608ecc31e33228c3c3fece57c4a8759412e8e12da9de2c3be7b31a8f4ac`  
		Last Modified: Mon, 03 Jun 2024 19:06:20 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a980c12f14e25545971db511e10e60ec69ff03d2e01845095ba21860f841437f`  
		Last Modified: Mon, 03 Jun 2024 19:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3dfda5fa1c297b8017d1db5d94923b24d235589370855131cb08757f14da146`  
		Last Modified: Mon, 03 Jun 2024 19:06:22 GMT  
		Size: 98.1 MB (98103818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edfbbed18b5e899c62b09ec2aac05210dd55e2a2a73efae5c229891bef840a4`  
		Last Modified: Mon, 03 Jun 2024 19:06:20 GMT  
		Size: 9.2 KB (9202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94cb6a9b08336a8ba121883b0e7b5ea8b7a467bc3530f2e470f2ea8acf6d6d78`  
		Last Modified: Mon, 03 Jun 2024 19:06:20 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7de83f5d1b5d3cacff37055e6e5265adbef87ed5b4da48f23ff9bd518b9d80`  
		Last Modified: Mon, 03 Jun 2024 19:06:20 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da6b70a6ddbcbff321f6347a3813a6552d80b31f4398336c2da4b83f8f6f925`  
		Last Modified: Mon, 03 Jun 2024 19:06:21 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2168b648e294dc31844abb89ed0fcdc596537a6bc2a4719329f0d6a2674963ec`  
		Last Modified: Mon, 03 Jun 2024 19:06:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:49e9e2aa18e6b3821c18245d6f08feb4ef8b9ce7a40c8c0bc5b0dc249690162b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.4 KB (993419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1e074395c15018ae75d1b0a914e7bfc1bbeb9d3ed4062b972424d2e27a7c40`

```dockerfile
```

-	Layers:
	-	`sha256:2425a2b9e9e5548e081d535b37d6cf0efa1356b0e4e158ffccacdd7afb63e7be`  
		Last Modified: Mon, 03 Jun 2024 19:06:20 GMT  
		Size: 956.7 KB (956679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:124850ed748ab176d7094ceff3ee9986d5f3a9d4c4215a7496d7fa0c8d99c895`  
		Last Modified: Mon, 03 Jun 2024 19:06:19 GMT  
		Size: 36.7 KB (36740 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; ppc64le

```console
$ docker pull postgres@sha256:306a3852663ae981a71bf3d99589052b5f21e48032204d18ecf91c8b062d0c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100682961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292c3e87ff8e65bf28569580117b458bea524e9cc2fc586be25ee50baad14cae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=14
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=14.12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc0a98c9d584f2a67805c2d06416946139d1fc100fbde03f3fb69498d4adc87`  
		Last Modified: Tue, 04 Jun 2024 00:41:59 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46b4079b8ab65d67e0592c39b5171188bfa6367e02f4dd92f69cdf45d9ce755`  
		Last Modified: Tue, 04 Jun 2024 00:41:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe620b01173531249c12aa246f6fb6833497f7191f30009f22f645b9b94f64b1`  
		Last Modified: Tue, 04 Jun 2024 01:22:05 GMT  
		Size: 97.3 MB (97308118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f9383f6aedf98d8133aadfd91ac9948e0997b03bf5eb93016d537bc77eb62`  
		Last Modified: Tue, 04 Jun 2024 01:22:02 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c341c4fde4dcfb86627f77f8b718c9736b614f5c803a2eb32d4fe9738eab34`  
		Last Modified: Tue, 04 Jun 2024 01:22:02 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e9f2cdfd65498c7af1a2d576b99a058ea9545c28c54b1675d6ca2ede0cfefd`  
		Last Modified: Tue, 04 Jun 2024 01:22:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad96597bdedf2faa2b8f8d72b206ecc84da85e613aa352e299edb810914050d`  
		Last Modified: Tue, 04 Jun 2024 01:22:03 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7145db489e473a993a218f5cca10f1563834e7b01971222719a86a4a77dc77e7`  
		Last Modified: Tue, 04 Jun 2024 01:22:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:62e4133ea57d519deb16f6c2194cdd4ec5be09346239bb6edd83ba288d3614c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.0 KB (990049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5adc2d9831e2e5529029ae65e421c2ee1f92fa7076f463ecb51b7d7766e5f84`

```dockerfile
```

-	Layers:
	-	`sha256:59a51371c3a1a00d7c0e1aefc0328c855573076e2e685c8c04ad8d03667baf5c`  
		Last Modified: Tue, 04 Jun 2024 01:22:02 GMT  
		Size: 953.2 KB (953241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d47612df0588a4ca0daa9c6dea55d539ec8e5c04b503bbc384f0dff6da8efb2`  
		Last Modified: Tue, 04 Jun 2024 01:22:02 GMT  
		Size: 36.8 KB (36808 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:14-alpine3.19` - linux; s390x

```console
$ docker pull postgres@sha256:4807e196a852f6af30dd9c529c2208ae8c573dfdd9cc41187fe96fcbbf56575a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.9 MB (104903066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97dcca4b4230b332419d72ba02ee5f62df524fc779168872f8cc8861ec1eab6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=14
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=14.12
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=6118d08f9ddcc1bd83cf2b7cc74d3b583bdcec2f37e6245a8ac003b8faa80923
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PGDATA=/var/lib/postgresql/data
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Fri, 31 May 2024 13:43:40 GMT
VOLUME [/var/lib/postgresql/data]
# Fri, 31 May 2024 13:43:40 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 13:43:40 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 13:43:40 GMT
STOPSIGNAL SIGINT
# Fri, 31 May 2024 13:43:40 GMT
EXPOSE map[5432/tcp:{}]
# Fri, 31 May 2024 13:43:40 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf070e1afb1dfa2858898d44cc73300f9c817c9455e866395af0ebaadac77a`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9d3e69e197d6e0a5091fd3be948bac07f0cefefb29f336d0fc54d6ba476000`  
		Last Modified: Mon, 03 Jun 2024 19:55:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4f9f478f268b61110e05330afe918336a544febe9e4b3409188f45f46749a1`  
		Last Modified: Mon, 03 Jun 2024 20:42:07 GMT  
		Size: 101.6 MB (101643933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfc0b3d78085d0ac25acd575df315a28c8aa40735a053a73d81d9de8bdca77b`  
		Last Modified: Mon, 03 Jun 2024 20:42:05 GMT  
		Size: 9.2 KB (9208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b38813b07e8135e0bbe594e2e5a0c94e4951113b1188518e116caaa3fc07d5`  
		Last Modified: Mon, 03 Jun 2024 20:42:05 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebb1bb91207f06b3831bda347611519b9d2974c66bf3d8359dc857b48904661`  
		Last Modified: Mon, 03 Jun 2024 20:42:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb201d1ef0616d98eb65bd0d5c09cae2755b2f3dd552fdeca0796f6998315cf6`  
		Last Modified: Mon, 03 Jun 2024 20:42:06 GMT  
		Size: 5.4 KB (5425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac64303d8f5e01b31e90c4c511e672994ac0575db793711f67308bb698b26e2`  
		Last Modified: Mon, 03 Jun 2024 20:42:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:14-alpine3.19` - unknown; unknown

```console
$ docker pull postgres@sha256:aefc43cedd00a42b3627870c8e80fb9cc563f838bfb60d22fa81eca693fceee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.5 KB (991517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40dd449127361aeeb5b0c4efd759425cb4956a3f45f9f9709ad4530b00ff3552`

```dockerfile
```

-	Layers:
	-	`sha256:e35a8f0fbd6c23479b9bfb282d67d95727e3f9e15d28de8300acefd08141db92`  
		Last Modified: Mon, 03 Jun 2024 20:42:05 GMT  
		Size: 954.7 KB (954740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece51ebf7b90e1ac800a32c5310cf2bdb26001f29a3f6200cc2c455b22da07f6`  
		Last Modified: Mon, 03 Jun 2024 20:42:05 GMT  
		Size: 36.8 KB (36777 bytes)  
		MIME: application/vnd.in-toto+json
