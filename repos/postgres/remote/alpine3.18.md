## `postgres:alpine3.18`

```console
$ docker pull postgres@sha256:64e18e8fb3e9c9aac89ac590c5dd8306b862478404f76cd9b5f7720d012b4c47
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

### `postgres:alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:79790a9fa3ab75f5f590766d095fdd21cf292f1abbaa834bfe2036585ed0f2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96346821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3acdf1fbc4579765d9f6cb6752d574de50e543edb4519d1421d5cb346be6c832`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Thu, 09 May 2024 18:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146012bc821fd3af9b0c2e2b3f933362d8eb556e36b527cbe6933d87a40c926a`  
		Last Modified: Thu, 09 May 2024 21:56:42 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e5e530fb80dec92397c8eba8a4571f39b61afb5a72eea1fa7f3e28b3bfa990`  
		Last Modified: Thu, 09 May 2024 21:56:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661c13c9621ca40af50f7c06875faf301d6be17d098c1f8cd06c834094a8a22`  
		Last Modified: Thu, 09 May 2024 21:56:44 GMT  
		Size: 92.9 MB (92927432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6d06d5b1de43e307f863f5c0b0bc2ad899066f756af5f679e0a24b1b706c75`  
		Last Modified: Thu, 09 May 2024 21:56:42 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86982049feafe2745a0de237ab6acb18fe3028b481ae7079648e7037efc63a45`  
		Last Modified: Thu, 09 May 2024 21:56:43 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a67f7fc28defcc1669044794916160c45ddb5863778e7de542a39c05c35b7e`  
		Last Modified: Thu, 09 May 2024 21:56:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68866bed91bf6bb952ed165f069156447c2733e03aa5ff0e70a105064895c325`  
		Last Modified: Thu, 09 May 2024 21:56:43 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f0a21a917940a4a071e6ad4dd2c1a316f098e58409fd11f16ef1c6648f9e5d`  
		Last Modified: Thu, 09 May 2024 21:56:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:1124169cced262312bec6995a90fad3a02163f08cab787764aba8886b12879e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 KB (993837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014fc5f26c2bcd0aee508136e42c9e73bf826ec651c799ab3e2dcd51445d2d33`

```dockerfile
```

-	Layers:
	-	`sha256:689df894ca5002876f2424cd8c35b1bc0442f4afbd3c8071eb543a8b7afd83f0`  
		Last Modified: Thu, 09 May 2024 21:56:42 GMT  
		Size: 956.4 KB (956382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7abdf2294126a319d3e4e6f5971cdfb15fc691896f0713c0815bec91e14cce2`  
		Last Modified: Thu, 09 May 2024 21:56:42 GMT  
		Size: 37.5 KB (37455 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:303de2a6952660082a3e535e100655055b3e5bf99fd79f1ccc5148fdcd5f4dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94668811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0293c2f189de3d01391f7984a9166bb6592ec93601ba5ba5be12c86095562637`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Thu, 09 May 2024 18:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
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
	-	`sha256:a165a6536cc1af679bb95f52cb2227939a7020e678f4c0cf3dca169544a5248b`  
		Last Modified: Thu, 09 May 2024 22:03:03 GMT  
		Size: 91.5 MB (91504908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23e63f7cbfc7c229a42a4d79ccdba7a7726c6d684406dcabb357eaca8bfc14e`  
		Last Modified: Thu, 09 May 2024 22:03:00 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b9751d06a0e7d516d945ce08a7244b1d6e0eba3d1f27649c2a2ca5e03df3b`  
		Last Modified: Thu, 09 May 2024 22:03:01 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382ac26c98dd22e40fbdfc4d07d2c917e018958e638a2bbefbbe5fa6ad0b15e0`  
		Last Modified: Thu, 09 May 2024 22:03:02 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464e6e49c67a0a63f3fb08c95b16c543633a2b323c9a3a5797d1ca032ce79db9`  
		Last Modified: Thu, 09 May 2024 22:03:02 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208adc9afca67683a77bc14ec9ae9430e9d39e0356468fd91ed23a13cad743c8`  
		Last Modified: Thu, 09 May 2024 22:03:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:1d81225563107dc9fe826be3b3890bde95891f90a3c8a951f7d290f7a8fc905d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 KB (37376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1c0427aa15fea95d512a56c6883bdc12a0d82e2f545430db45112c2f32bf2ac`

```dockerfile
```

-	Layers:
	-	`sha256:59e0d5edac90d2f8e74b58743dda7af61791178ba83221cf27747c5dff182dae`  
		Last Modified: Thu, 09 May 2024 22:03:00 GMT  
		Size: 37.4 KB (37376 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e787980a362ebc003d5295b9dc820e9c902b34add0c5c9379bd42f2b87e6f4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89182862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2deda2fdce32628bb4d6478ea702a7723b7e610115043deba40c8bbdbcf01bb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Thu, 09 May 2024 18:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
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
	-	`sha256:6b93656da3b4b07fda4cd301af163c3ce0bf32c0edbb98cc505db5902a544f8d`  
		Last Modified: Thu, 09 May 2024 22:47:37 GMT  
		Size: 86.3 MB (86264631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5342827a20b42267a23708c71675b3deee852ab2ab91669c391c52503a01b4`  
		Last Modified: Thu, 09 May 2024 22:47:34 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0785c2af02c202efbf4369dce46f83dff2718d48071aceca6971e87dde37d1`  
		Last Modified: Thu, 09 May 2024 22:47:35 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a232d2457dfe96d97dca6c75b14ffd3d701057eef9ae35616c3c7133fda19`  
		Last Modified: Thu, 09 May 2024 22:47:35 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8ab714206ef8a153a623f909998d358e1618ee3751ad9c715f9262df8302c0`  
		Last Modified: Thu, 09 May 2024 22:47:35 GMT  
		Size: 5.4 KB (5418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5440bcab4ec5e5f3b310d65f384c0ba9eed8605aca1d1d1d998f3a2cdc0f7daa`  
		Last Modified: Thu, 09 May 2024 22:47:36 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:cd71585cd0f4c95989a84a6d177e546b8ef2abafbccaf44b5af76b4890d4b747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 KB (993838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86af029170da48eb47b00823b2e81325d740efdf580cacd9f0f7cd3377be59cd`

```dockerfile
```

-	Layers:
	-	`sha256:fb73c2538f0187a46792a64b4ff6d5b3b07f56bbafa639ead634839291b8029a`  
		Last Modified: Thu, 09 May 2024 22:47:34 GMT  
		Size: 956.4 KB (956410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e866b428b0aedf7b66e2ff7f721711dd295fb468a21ebb5b998d92d2426f13a`  
		Last Modified: Thu, 09 May 2024 22:47:33 GMT  
		Size: 37.4 KB (37428 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4d5415b5e223450b64da7162c3ff8d0a95ed47fac26cd6bac1e012d6e506870e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95174456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e153fe0db72ab992c6113795190d0198c53d1498b4457b71f4eb09ac4782d5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Thu, 09 May 2024 18:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
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
	-	`sha256:9127be88c93e4edd91c9b1b7daa578783a266392105017f04e564dfa42e0576d`  
		Last Modified: Thu, 09 May 2024 22:26:28 GMT  
		Size: 91.8 MB (91824248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b6254a733d752e4370bf949178ec881576599453d26358ea3d87c56d27fc5b`  
		Last Modified: Thu, 09 May 2024 22:26:25 GMT  
		Size: 9.6 KB (9563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845f53a49c0a3aa915a497c544e43395716c8ec6c5514cc5bdf01f3787040d5e`  
		Last Modified: Thu, 09 May 2024 22:26:27 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327eed1700131001ef49b46658c40b18d3f51b042e62c55141b33fc8185557b2`  
		Last Modified: Thu, 09 May 2024 22:26:26 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef18ca11c5eca4215b0e4efee8b1ea382355a1ec6ab66d7e51ad832f19a2f745`  
		Last Modified: Thu, 09 May 2024 22:26:27 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b83de97e6a4198dcf985faca93a3e1ceaf0a6b2ebc830a1df5ef54e64ea3f3`  
		Last Modified: Thu, 09 May 2024 22:26:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:0272800203550c50fd1fae17167dc5594e614c9cdb3db6332395550fb9f9db80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.9 KB (993854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db4807182dab12ab3705317dde74feec789fd5df7c3ea6858c872408a364c3a`

```dockerfile
```

-	Layers:
	-	`sha256:eb98b6242c8f233b5bbc2de8fcdfa186aa86ab5b63b520abe1286452642fbe03`  
		Last Modified: Thu, 09 May 2024 22:26:25 GMT  
		Size: 956.4 KB (956391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d0d4ad41a3d857955dd0eef7cdc98389731b1ae34c6ca8dbff4ac16fb00de85`  
		Last Modified: Thu, 09 May 2024 22:26:25 GMT  
		Size: 37.5 KB (37463 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:8d0095406410050d6a03e24ea4d01cfeb6dfea5ae969ccd583860ea091f93c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101139753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed80f688992e271e0c932323bead17558fb2337bca578b830f49fe40027b59c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Thu, 09 May 2024 18:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63442760d47705d963ffd6c0fe952b3bd83ee09447d373288e1a81da09d9bc65`  
		Last Modified: Thu, 09 May 2024 21:57:23 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a45293e80f23c1b22445f56979280bc98c0eafd2aa57181939fc2fff806ca0a`  
		Last Modified: Thu, 09 May 2024 21:57:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34af8a1c4ebbbf04d8625625678cc144af5eec7f26f0b486c8592237ec4001d8`  
		Last Modified: Thu, 09 May 2024 21:57:25 GMT  
		Size: 97.9 MB (97883842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699650fcc387518cf2aeb03346033dac780fb6329fc9aae60a1cf0710ca7d73d`  
		Last Modified: Thu, 09 May 2024 21:57:23 GMT  
		Size: 9.6 KB (9561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19fe821a532f3bf5f9277e389cf8930e0f63d482b5b04aecc9152d2ee8cc7e5a`  
		Last Modified: Thu, 09 May 2024 21:57:24 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0bbe555c1a01a88d70343fd4084533c86070eec0ff309ef1468f78d1e4683e`  
		Last Modified: Thu, 09 May 2024 21:57:24 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261d40fc984357267be37d6403a8e7766b66e8b89be62f0ff67ecfb49bc58f61`  
		Last Modified: Thu, 09 May 2024 21:57:24 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c1d16b18e76a0470bf1576659cb1256cb37a23c717e5939fff38600da43c36`  
		Last Modified: Thu, 09 May 2024 21:57:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:f55324fbc2fb3d11ce3f81e47800ffd69cee4b853a327e50e1fc34a6e7301e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.8 KB (993781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b995db2fb01e299a6ab4c114044aa5e722c3640fc94e732480f10f763f298b8f`

```dockerfile
```

-	Layers:
	-	`sha256:dbed407815754f664a53d0d1f30b0d8dd13ae05a0e2e655adbbfd99d36c95c11`  
		Last Modified: Thu, 09 May 2024 21:57:23 GMT  
		Size: 956.4 KB (956362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7ded8228dcf9ce7520f06555532266c302ba3cd7f79a7272e452f26787f3836`  
		Last Modified: Thu, 09 May 2024 21:57:22 GMT  
		Size: 37.4 KB (37419 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:869ac5e1e9c0e00a88f916e991c84081a149fba3ac291cea8205ab31dc220196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101947703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b4865148e5226c4c842b3947ffb09e8a5c67f5c6fe5752fb56041c520820a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Thu, 09 May 2024 18:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
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
	-	`sha256:8c8272873f145c06be510d0db0f9a372476ffc64d63fe30ef9724a319c008f66`  
		Last Modified: Thu, 09 May 2024 22:25:17 GMT  
		Size: 98.6 MB (98582361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbbdcd80665fcb01a7eb43752cc949604dbce2d01b2518a56027fc79441fefd`  
		Last Modified: Thu, 09 May 2024 22:25:13 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28af2287306578b3cbe8a3fe65ae83b83e2adb682f1ad14d3845d225013034e1`  
		Last Modified: Thu, 09 May 2024 22:25:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4c143be0c113b96236d5db7e36bae9540fee32a77ec10df6c63e8516b118e2`  
		Last Modified: Thu, 09 May 2024 22:25:14 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1384431f71a7c327263f62e021299c56eed1b56c5df3459eb859de8de9696b02`  
		Last Modified: Thu, 09 May 2024 22:25:15 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990c4fc3c912eec9abe76bb5af83fc656e87c56bc2a850f5dd127b017616d1ad`  
		Last Modified: Thu, 09 May 2024 22:25:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:ad08af52cdf497466cf737c58afc34a947611448db05a04db0b85ee8cf6d8fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.3 KB (990267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372302d48e7bad81972393f7fe3b79a0bb7932c55adaaf6260bcc013710249a7`

```dockerfile
```

-	Layers:
	-	`sha256:3ee2820cea662feb075df7cac95072e3325d80723ca2d4ed0a36f304a4d507e2`  
		Last Modified: Thu, 09 May 2024 22:25:13 GMT  
		Size: 952.9 KB (952935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cab47282cc299bd467655478f705e25f5609efa84496bd577302f52ec390a15`  
		Last Modified: Thu, 09 May 2024 22:25:13 GMT  
		Size: 37.3 KB (37332 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:32e8b9ad640ce29dbdba1edda9e7d34e06bcfef2fe0a60cfac739c2f8694cac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97773410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf104cfa1f5468841acde062f81469617065db116b6ac98d392cef4945460cae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_MAJOR=16
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_VERSION=16.3
# Thu, 09 May 2024 18:58:11 GMT
ENV PG_SHA256=331963d5d3dc4caf4216a049fa40b66d6bcb8c730615859411b9518764e60585
# Thu, 09 May 2024 18:58:11 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:58:11 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:58:11 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:58:11 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:58:11 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:58:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:58:11 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:58:11 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:58:11 GMT
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
	-	`sha256:548d3b3bffdff824c252076cd9e79b8903d5c3f56b88385f2938df962367b04d`  
		Last Modified: Thu, 09 May 2024 22:17:49 GMT  
		Size: 94.5 MB (94539034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83832979c5c280f4e28efefaa8c478a9e6f99db19fc278340efdc3f86caa8d`  
		Last Modified: Thu, 09 May 2024 22:17:47 GMT  
		Size: 9.6 KB (9562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb754707283a82de8ec33ede0eb3a0194c7b8ef62e7f77847dc837778c141c`  
		Last Modified: Thu, 09 May 2024 22:17:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a084854ebb66410497f6599e24a7756e70078f801284e1601211ef7687970a`  
		Last Modified: Thu, 09 May 2024 22:17:48 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18167053e383ade84f9dcd2cc0f95d806ab7d4285f6fe545300704dd579d13e`  
		Last Modified: Thu, 09 May 2024 22:17:48 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f752f8fa5d6078b500ba96161168294b6f4015da110438af8b7c076d8b12a`  
		Last Modified: Thu, 09 May 2024 22:17:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:3dc83469b45cad57d8a74f24e38eb174d39964c5024c547c67c31f9ef63e09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.9 KB (991883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7021f67d636b7f3b2d7efa7768eb73e7af050aeabb6ec9d013a3ba10accffa1`

```dockerfile
```

-	Layers:
	-	`sha256:c1dc65e2fcb96224b53cf9e5780ffe90070b51924b24a9a3c65541281f4ff11a`  
		Last Modified: Thu, 09 May 2024 22:17:47 GMT  
		Size: 954.4 KB (954428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceab15c3a8d0e82aa440900d920ea144c4edaad4c4e4d0726a0d92d46c3bd25d`  
		Last Modified: Thu, 09 May 2024 22:17:47 GMT  
		Size: 37.5 KB (37455 bytes)  
		MIME: application/vnd.in-toto+json
