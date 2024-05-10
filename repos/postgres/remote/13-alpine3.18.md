## `postgres:13-alpine3.18`

```console
$ docker pull postgres@sha256:30b939edd80d881e9e7d4ba52fcc9923260602e96f872074781699b33836f358
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

### `postgres:13-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:c11dcfc801d2089bfa50c9df6f4a25afe5e0de9a411d76bab5b288372241da11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93330828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2f277c7b78d9ee0c8a139457631930e704725308214c2d2d5e86c97f31bef6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e6cda13bf3edc426931327d402edf47769ad7d0f37f3a0032d955e4842e3cb`  
		Last Modified: Thu, 09 May 2024 21:56:33 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1848dd6094cf1686d38fcbdef52e8bebcc21d39ad47f3a1b38864d767282936`  
		Last Modified: Thu, 09 May 2024 21:56:33 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07a6a5ab0176b2094c84fb1d8231476d6f656ae5d3520e15ea5a56415acd821`  
		Last Modified: Thu, 09 May 2024 21:56:34 GMT  
		Size: 89.9 MB (89911987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e61ff105c4da556f4da3a6600a59ac38e5a4e12514efff87791a3c5af2d02d3`  
		Last Modified: Thu, 09 May 2024 21:56:33 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c26158f907a1428c5f84bc2d11d09c1ed4336ccae76f9839af13c801cb9c0f2c`  
		Last Modified: Thu, 09 May 2024 21:56:34 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc0f4eeceea6a90456d3f7a4a2dbdb39a2d6c3a05d44be2f9b7a127945f79f7`  
		Last Modified: Thu, 09 May 2024 21:56:34 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e0c7662b64c65421fc12339f88eb861592ce6390197f25beb1a3ac01538b6`  
		Last Modified: Thu, 09 May 2024 21:56:34 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6db83171497a8d7d72dcd1c38f7188412574c2cf711f6295efb69930f1a803`  
		Last Modified: Thu, 09 May 2024 21:56:34 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:b6f8ddb30a467f14b2f627c91fdb95ba19d31e8a1f55016dd7f855a1038cea8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.0 KB (990050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0b4f062bb742a83f2bbbf74ddd9daf650cc4ea2d3d91f8ce38a5eff61f55e4`

```dockerfile
```

-	Layers:
	-	`sha256:975ca9705c5d6d9abd8b4d14b7ac8f755203b9198ad760aa93b40a6270020a94`  
		Last Modified: Thu, 09 May 2024 21:56:33 GMT  
		Size: 953.4 KB (953414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aac4e93d3e30421d7df21b9fc8baf528254fe71887d1316cb4673541eb2909a`  
		Last Modified: Thu, 09 May 2024 21:56:33 GMT  
		Size: 36.6 KB (36636 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:6b2ada5632628ab425f9cbdc8b5ff3773de6510f3ff641628df77988538a642a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91725759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41e2dc0755fb1cbf598df14753baf19ecd8f878fa458d3e5d398590a0abcddf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a108ab915fc8c9e416a781c5a7bc761154864183018326b62496c9ab46c866`  
		Last Modified: Thu, 09 May 2024 22:03:00 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67939ca05ee3b2791aa4415e0f9cd611de6318af5254b1813898bcbd5a17f6b5`  
		Last Modified: Thu, 09 May 2024 22:03:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f3f555cbea2bd5418315cebfbdb1c4ab078f311541cabbdb6015b836134079`  
		Last Modified: Thu, 09 May 2024 22:22:50 GMT  
		Size: 88.6 MB (88562401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0bebef09e02cd4c2757f3f71589e180b07930bce5c056d7940d71c297a924f`  
		Last Modified: Thu, 09 May 2024 22:22:48 GMT  
		Size: 9.0 KB (9016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859508cc9c921ef401e70d6cef598d235b2069dfcae2bdbb0de582c454665700`  
		Last Modified: Thu, 09 May 2024 22:22:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486f47570d64d1d06c7328efb84ead7cfb261243c6e986d8500de95846cbf566`  
		Last Modified: Thu, 09 May 2024 22:22:48 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665b629eee437868c38f3e4d7dfc52827abdec8ed9f891e635fe8b63e5f8de44`  
		Last Modified: Thu, 09 May 2024 22:22:49 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4717499ff619e318ec1dfd2ad5c33ba65dd54723762d5a1b5546d8e8149c311`  
		Last Modified: Thu, 09 May 2024 22:22:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:c700b6c5fdbc1d686a87b6ecf8e1d679ff90795a249d70d7ec5dca420a6e0b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70bf47af258bf5e6a247bf7b733d08c6e29f3a48a12de8867b42916403694d45`

```dockerfile
```

-	Layers:
	-	`sha256:89ccf43e3015b80280d061c39f13d14bd46fadef17faae485c475367dd132fb0`  
		Last Modified: Thu, 09 May 2024 22:22:48 GMT  
		Size: 36.4 KB (36383 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:b499b39b5e49091b4d9d5eafa2f19c7803425178821a00a4e18b68cb2699ad17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86315946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243e3407ec42731d96991f2308fa76575ddf8046426e3380e21ec975e708b54b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936f8464cbf158786c7cdc2123b4210e01ed6c1cdbc9dc688a0d21f81007defb`  
		Last Modified: Thu, 09 May 2024 22:47:34 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b00a5706ba36d0ddd0b2f4e216fce8e5a410b6b853cbe133d4896bdb15e4d8`  
		Last Modified: Thu, 09 May 2024 22:47:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb75a3cf19e74072e60b2e3308b47ef45d3c83e46d318c908effd39a43e7f97`  
		Last Modified: Fri, 10 May 2024 01:29:08 GMT  
		Size: 83.4 MB (83398256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a4dc35ee537f4616f3b23973a98da67a11f4bbf5f167d6c13ce70e587819ea`  
		Last Modified: Fri, 10 May 2024 01:29:06 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c112bdc4df47cf682ee30d609eaaab2fca6a40b4c23d2c4b7cd58fc3fa48014b`  
		Last Modified: Fri, 10 May 2024 01:29:06 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3606dd3ff4d77c9ca1eb023397c397072f8540c6b5fac25d49952920be92ed6`  
		Last Modified: Fri, 10 May 2024 01:29:06 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a3dd335b6794dc85ce5da3369e8ead82e5b824984d48f534043d807f05e822`  
		Last Modified: Fri, 10 May 2024 01:29:07 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8d90c64770dcde596fc33c5e2ef33f697f05de491fc241bde3cbcaa773b708`  
		Last Modified: Fri, 10 May 2024 01:29:07 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:f13ff60fa1831c5a0d04cef63c4ce673552cf61ceb88435875d8664c65d79552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.0 KB (990036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd33a8f2c748bff1385202b69081e80dcd1abcccb083f284b1e3568b055b728c`

```dockerfile
```

-	Layers:
	-	`sha256:aa99ea4c1dab26f1e23875fc71ff189dc8b0380e2001678ba7ace82d40059590`  
		Last Modified: Fri, 10 May 2024 01:29:06 GMT  
		Size: 953.4 KB (953434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a257261383b7561a3297cd954f5121275cedce179f68dc95403f30c65fa379db`  
		Last Modified: Fri, 10 May 2024 01:29:06 GMT  
		Size: 36.6 KB (36602 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:3477683dfeacbb2040df3b3dfbd7b72b7bd1139ca81a5d9d1adcbd03a7e68920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92197267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718eb99b899fe4267ce9aab68b3b1cc660cb2a2bcf8bdbf433c6b4078326c3ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b240be4b3e5ec1e8dcb9ed310937046e4279e0fa6616a6838631e3652dfe15c5`  
		Last Modified: Thu, 09 May 2024 22:26:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8682ae92e29385ff5d6f1929c06e62fdf846fcd1d301154ad1747043bee37f21`  
		Last Modified: Thu, 09 May 2024 22:26:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f427a627270742f5fdab2799d6c632a719fc10f361df9b370a0626a7446b5d88`  
		Last Modified: Thu, 09 May 2024 23:22:12 GMT  
		Size: 88.8 MB (88847608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564069efda4c46f229b21a6f8367786a412a4ba5f40728c5eabc7a728fea0bed`  
		Last Modified: Thu, 09 May 2024 23:22:09 GMT  
		Size: 9.0 KB (9015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4404f9edd8d9e4c43834741773a1f8b375a1f7e21e258f62bf323c0d8ba0f102`  
		Last Modified: Thu, 09 May 2024 23:22:09 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c00a8019cd119104acab7d2e3af6f854364ba861ad6091071ac3b7ba5dd9081`  
		Last Modified: Thu, 09 May 2024 23:22:09 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c45a321edf3ca12c88da960e13d1b1f6d6a992a56f1b4e8a8e83f94ca930dc`  
		Last Modified: Thu, 09 May 2024 23:22:10 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1040d444a7e7b01190cd3794feb1517eeb1cbc72807f1538fb682ebc6fa16dc2`  
		Last Modified: Thu, 09 May 2024 23:22:10 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:e601f6cd8d720bcfb1a9e816d46dab43481b70d25012132a4276a28a07fe25d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.9 KB (989896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d342b35dbbd0cb786d80de954dd05843bd283a52452e040f801285baed264c5`

```dockerfile
```

-	Layers:
	-	`sha256:6bac84d17562cd2d71149d4171d9fc750e8ad3679f59769079677315852bd645`  
		Last Modified: Thu, 09 May 2024 23:22:10 GMT  
		Size: 953.4 KB (953421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc480c1a4f852c98a343ee0ecad9d8c74357c6c915e0ea48a486009ca9582f6`  
		Last Modified: Thu, 09 May 2024 23:22:09 GMT  
		Size: 36.5 KB (36475 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:509dcdee6c8fa4994d335e4fd498cd99470658e12cd3c2380760fa0b5f7e1483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98085401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7f62ad0974eb65ab20d1f5f6ef300246a61d8d37993b0aa89e21e836177625`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1ab1dd9b61df7c34352b158c566fcf2bd5a4de21d2a2eb79d26b430763f1e7`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7e50cbdc7c01e0da3f1a672326aabb89ffe278e48e80c6653806632f4a5831`  
		Last Modified: Thu, 09 May 2024 21:56:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e523c940c22bf56c9b49a89254a33be21d3cf97d9d59b522863c5030e822b488`  
		Last Modified: Thu, 09 May 2024 21:56:50 GMT  
		Size: 94.8 MB (94830036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c3f894b203f3deeeb549bed440c10dc81b0930875006c575eaa1dc956de7cc`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47a4d935dc6574a0def569c4cd3adc73aee13998a64d8c706a66b180f437950`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e388e59bb36a4fc1165cce188bbfcba208d88e1272dfcfe4a7c46bd80b19d0`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdd3292f4b6ce5aa1ce130a00d014962367822f6114873a5249b2556360a8df`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101eb26e93f540d494252ff751d6d2e58828f261f682ad2ee30a34da4dc0633`  
		Last Modified: Thu, 09 May 2024 21:56:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:9e4bc71515bd4bd25578fdd9ba81cf1a074ad7170a7fca0c11167e451af5b6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.0 KB (990004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d15e6011151b147db0ec9930d8c665aaa2d2a34f1a1b993053ad23bbbf47f21`

```dockerfile
```

-	Layers:
	-	`sha256:2d85862a65c2921936c12fa49936056a2d71dffc4a4ba56d9ff954ed4fe76715`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 953.4 KB (953399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:505bf8345a9fcaa1453bcb9d7ee255f8787684b03b02aebd9a148ad30f0cc490`  
		Last Modified: Thu, 09 May 2024 21:56:48 GMT  
		Size: 36.6 KB (36605 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:1a8e4404d2ba9e60cbe5759648685acb4f0b072aa01464a7818a8c27ab4189a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98733133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5793ba4bac4374367e3da6125aa11de290b9b486c6988d063717750ef7ca06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77322eb0ef5fb1c0b25ef0df12557560463db0b38939424f1178620dd8876ab1`  
		Last Modified: Thu, 09 May 2024 22:25:13 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa939cb59294636bfd8b37b029911175203f0809bfbc9a9e8d81d0df524136`  
		Last Modified: Thu, 09 May 2024 22:25:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5321ca1a27c69ed486d565f3045c5d9410970c6482f9c255772e1c7cd5c73a5f`  
		Last Modified: Thu, 09 May 2024 23:29:39 GMT  
		Size: 95.4 MB (95368336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3317037ee7c114dfa274adfd4c566f410de2bc6c0869abacc866ab2e4e0ee`  
		Last Modified: Thu, 09 May 2024 23:29:36 GMT  
		Size: 9.0 KB (9021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989ced719ab449cfab8af67f7a235076c8c9295b70e71546f4cdeb187997a0a2`  
		Last Modified: Thu, 09 May 2024 23:29:36 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc284a9dcbf6ff6a07f5c19fbb76542ecad9a0a3fd99eae643191347fc9168ec`  
		Last Modified: Thu, 09 May 2024 23:29:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56865465df07aec079062b3400b03bc7dca4923de1481d7ccc73887008c11cd`  
		Last Modified: Thu, 09 May 2024 23:29:37 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae43aa3c2abf24a666ef3ae3b9951505351e1ccaeb71d7f4826d20848d7ea7d9`  
		Last Modified: Thu, 09 May 2024 23:29:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:120b2ae4ab0d1fd3bc6486ed8bbb56eeaa341ad6553ca1863cca24613e48e862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **986.5 KB (986469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00763ec6f83f83f5ae66a488a894979b87e0c74014c1e38e058c9ef65fa1b05`

```dockerfile
```

-	Layers:
	-	`sha256:62a0ae79cf811f8075a3611c28d6c7d419f949a7e66ba3551e5cd0ce71ef4975`  
		Last Modified: Thu, 09 May 2024 23:29:36 GMT  
		Size: 950.0 KB (949961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d994faeb0b0aaaa49b1371f8170d65b95e91074085fb6305ae6e3cad7a8f3971`  
		Last Modified: Thu, 09 May 2024 23:29:35 GMT  
		Size: 36.5 KB (36508 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:13-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:2fabffaba0a2bd78c5fbfafc47e0b0ba9f1f621989c19b2ca891b6471cb80be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94687171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e2ab3f0ef4f2153091e2638a605f661b85e3117be58d042e0c6be6de176a68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_MAJOR=13
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_VERSION=13.15
# Thu, 09 May 2024 18:16:46 GMT
ENV PG_SHA256=42edd415446d33b8c242be76d1ad057531b2264b2e86939339b7075c6e4ec925
# Thu, 09 May 2024 18:16:46 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:16:46 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:16:46 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:16:46 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:16:46 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:16:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:16:46 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:16:46 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:16:46 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7673a4910a6fe9d042a53154b0dae00bc60a57223cd10a184ea7a99d82bd0cc`  
		Last Modified: Thu, 09 May 2024 22:17:47 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2a19d1c8865ecd491b02ece010add44b02f480a09889be228a72bd65e790fd`  
		Last Modified: Thu, 09 May 2024 22:17:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2e5ddb834e51b5a77d306e885a2692f8ef166cbffe45c81ebe252a7f0d80b8`  
		Last Modified: Thu, 09 May 2024 22:50:14 GMT  
		Size: 91.5 MB (91453340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a1124e8134bb31ec84d9533f37dc3a036d7bec7593807f95ed364e54c87640`  
		Last Modified: Thu, 09 May 2024 22:50:07 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c742d2700a59062e527773db88aeacf77ce10c39a45bf9530889e41ca1a501`  
		Last Modified: Thu, 09 May 2024 22:50:07 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f54752c7370a5b5460189c725326602788a9559037ad36edec9316f629b00a`  
		Last Modified: Thu, 09 May 2024 22:50:07 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfb8e049cbb20bc134b8b9e33284e3631759fef56563d607e389b178fba9fad`  
		Last Modified: Thu, 09 May 2024 22:50:08 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924bbb2f30a4dc363d3dd1fef007350167562615074c5c6b95c8a44305032465`  
		Last Modified: Thu, 09 May 2024 22:50:08 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:13-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:248eb197fc5c51b0cc8c14d05383f6cce1c8383236131ec3a0b5111e5a6527b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **987.9 KB (987930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03748401031108d02d3953e29a27bf3be2bf47f8b027652bdb4b2b2e130192af`

```dockerfile
```

-	Layers:
	-	`sha256:5356f970672688591738607f4fdc759459cf8b761e256c83e21e29caec833453`  
		Last Modified: Thu, 09 May 2024 22:50:07 GMT  
		Size: 951.5 KB (951460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abbf7ec0cf0a93b4044077947ad6efb6d776c1242f520cd3d2dbfe4bbd9627c`  
		Last Modified: Thu, 09 May 2024 22:50:07 GMT  
		Size: 36.5 KB (36470 bytes)  
		MIME: application/vnd.in-toto+json
