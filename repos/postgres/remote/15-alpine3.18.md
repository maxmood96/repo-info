## `postgres:15-alpine3.18`

```console
$ docker pull postgres@sha256:aabeeb2f4c68bd2a9bc030c63a7ef86597556bdc012063c754a4526b9447100e
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

### `postgres:15-alpine3.18` - linux; amd64

```console
$ docker pull postgres@sha256:9a489d69c35e74fff4e91be918f756ea7334dec06b2f28fafe15eaf3bf3ccbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.5 MB (95479938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e93867ef624f86dd4b406d3bce570f46d50fa2a6932a73a9e94af9c105115a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75686bba78ea7c692fc8c0ac9c9704916c6aa9779ed32f400b50540f40b76722`  
		Last Modified: Thu, 09 May 2024 21:56:37 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a73a394343e27f59c1371368bebd16cf6c8c6c986527d41c25914f8183a6eb48`  
		Last Modified: Thu, 09 May 2024 21:56:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e00279ac7933ca1c5654a3bd83a53c1aa8a1e6d5b396d084dd5f1203aa23c1`  
		Last Modified: Thu, 09 May 2024 21:56:39 GMT  
		Size: 92.1 MB (92060661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c266e599af1aee0f84be53398d337c15d890e9ac9b0284fb53f0961a8f77991c`  
		Last Modified: Thu, 09 May 2024 21:56:37 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274da6810f39d4dec075d56ca40ddc7ff68e1f4c880c2d17c49a48ac99331ff3`  
		Last Modified: Thu, 09 May 2024 21:56:38 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60520291326a37e18ed9844b25de5a3da16f3f9ad7af5eb0fe7b9d0fe57b2d`  
		Last Modified: Thu, 09 May 2024 21:56:38 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7368a384be3c23de3bea90b7aafb21254c32a6aad6baea1a6c3ca0d5bb0269`  
		Last Modified: Thu, 09 May 2024 21:56:38 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e1db5f4d9ac996fe7387dba125e6df1f0bcc3e0fff3c173a7a84a5f68c8820`  
		Last Modified: Thu, 09 May 2024 21:56:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:1efa60535c6cd68a5092aaabb069a49cd67267461d0bc0519c67c3ca4b4d05f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.3 KB (993301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d423660ce0a4aa09140fd97ad85389c8f277a6b5cc52bd7e5639104d16ca75c`

```dockerfile
```

-	Layers:
	-	`sha256:65b2e9967e9969ef8fc065d3f8f5343329ab1bb7aaa28c2425bdc987870790c7`  
		Last Modified: Thu, 09 May 2024 21:56:38 GMT  
		Size: 956.1 KB (956072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a22c57b6f95d7457684b86f8c14196579ddf447a8a86600af8d9a02bbc11c5f4`  
		Last Modified: Thu, 09 May 2024 21:56:37 GMT  
		Size: 37.2 KB (37229 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; arm variant v6

```console
$ docker pull postgres@sha256:cf0e886f30cf6674119484d3506e37ed5c1d999899fdabb849ebbb52d36cb3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93851282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0febbf04fc4d1d1cf209eda420b9a21232442149d7d86593363218c085f6429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
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
	-	`sha256:ca2c4e2b64a06721fa82f98d7dbe0c40db41479c9147db44841f112b69acf88a`  
		Last Modified: Thu, 09 May 2024 22:09:34 GMT  
		Size: 90.7 MB (90687480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea2ca3aea0d0340c0bd8195674916dc39511203c3cd6684b38ca5f66c9eb972`  
		Last Modified: Thu, 09 May 2024 22:09:31 GMT  
		Size: 9.5 KB (9455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e144c73eed7814fb115859f69e439e68dd12ade3923de9b9e1a11aad7f921fc5`  
		Last Modified: Thu, 09 May 2024 22:09:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beed21301b7336b2c666e1bd9e459388e4c5f158b730f77a7e5e922e619ca231`  
		Last Modified: Thu, 09 May 2024 22:09:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ec87acee7596032f14e389787be1829370bec5895cc1c450fc4d03ffb1dedd`  
		Last Modified: Thu, 09 May 2024 22:09:32 GMT  
		Size: 5.4 KB (5421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ee8ba1cb9a451eec18aecf06716d1b1b7e4887bb34b3bbe4fc89049fc9e6d5`  
		Last Modified: Thu, 09 May 2024 22:09:32 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:79ea052c847fc9f74fdd7740dc45d8a3a0b191c95a9db4a5374d93ef62d913ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 KB (36976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9375a74b031d78037abea9b28c105256c4ecc8c143d166abec0bb032b3e67fff`

```dockerfile
```

-	Layers:
	-	`sha256:bf309decc5e589fd88ed56204fd7e4b9921b33a29b164a3d28deeb953d9b150f`  
		Last Modified: Thu, 09 May 2024 22:09:31 GMT  
		Size: 37.0 KB (36976 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; arm variant v7

```console
$ docker pull postgres@sha256:e4f9a200420a5c07a49468e7db7ac93c9ab4c6e5b9ec2f43f88f90b1151f7a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88388134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a93adbc7e2c6fdd2267f334d0f368ca74b4df91a88851365a3dcfbf731f6ad1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
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
	-	`sha256:9eb91695d451752ecabce34d5f0a1f11012d34c10d57744683bcc47b18fd56db`  
		Last Modified: Thu, 09 May 2024 23:52:00 GMT  
		Size: 85.5 MB (85470006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e87f13e3cce3e768f9765eb956e85e960cbea5360f0dee69124681d780edd646`  
		Last Modified: Thu, 09 May 2024 23:51:57 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348309a3f2d1e495b1c36dee988b24d5483ed85337443f662f663712c69723c3`  
		Last Modified: Thu, 09 May 2024 23:51:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f639ba92338bdd5e7ca04310bf6ea4b1e1cc7067a802b5bbe34e4603f470ee`  
		Last Modified: Thu, 09 May 2024 23:51:58 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f581d870eaa11f5ca35114e76ff9110030c0d60d70d0991d9c510c094b9b92c`  
		Last Modified: Thu, 09 May 2024 23:51:58 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f92a850c3a4da636902b3bd101d7cfa773ae6de79980564febbb9a8fa78547`  
		Last Modified: Thu, 09 May 2024 23:51:58 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:82fec210310369b8b8d80021bbe8c4eeac379a376c69086b46a02cf50aa57c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.3 KB (993287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b767af4e55d674b0bb3cb2e98b18eacc744dbb30e73a548c7ce0665f2b2178`

```dockerfile
```

-	Layers:
	-	`sha256:500dbe63483ec5acef4e2f9617ee7d9b679b639375e73b9fe226c1fd0ced6a19`  
		Last Modified: Thu, 09 May 2024 23:51:57 GMT  
		Size: 956.1 KB (956092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cab43d19237d8fd98e1ef619edc638251be23bc007ce66c4aacd4292a99806f`  
		Last Modified: Thu, 09 May 2024 23:51:57 GMT  
		Size: 37.2 KB (37195 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:4997cbbe03515317794d666ca0a8fcd87202a578843479369c2ed4cd9e0e2dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94317627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed66e0aab861845b1937270f1c3704c8984285abca3cc678adc23c65aad09bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
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
	-	`sha256:6f44da89ec027da1f06422ff1523d792f4dbfe5f72df7f47821a6e303ff8946e`  
		Last Modified: Thu, 09 May 2024 22:34:44 GMT  
		Size: 91.0 MB (90967539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a61ea1b31eb65bf64462df28117331d5fe70e3b8ee76f3112ef067c827a975b`  
		Last Modified: Thu, 09 May 2024 22:34:41 GMT  
		Size: 9.4 KB (9444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4696a965efad547b181b8648224b36694d21180cafbc3b1b822e04d146c9864`  
		Last Modified: Thu, 09 May 2024 22:34:41 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ea7a92607978101e1c685a0fd21edde19af40551a7d8420150343faa6092acb`  
		Last Modified: Thu, 09 May 2024 22:34:42 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961e90ed08fe2e53007b87cab65ff9ec9c7ce209a27a7d8016daf02243c98ae7`  
		Last Modified: Thu, 09 May 2024 22:34:42 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e266e3de4f3d6fbffeca768ce8fdfc636e5e1025326adffa32b698450ace522c`  
		Last Modified: Thu, 09 May 2024 22:34:42 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:aa373a91225f13ba1e9805154f3febd46301f728e1638d17af486824084ec0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.1 KB (993146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d869cfa8760cc2250ae2d60f884062370592c88e395ebe1faa87ce6d98bb994f`

```dockerfile
```

-	Layers:
	-	`sha256:69503e95563ba8ada937416999b6798533362462aca3315dc6c940dcd2602231`  
		Last Modified: Thu, 09 May 2024 22:34:42 GMT  
		Size: 956.1 KB (956079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:589e7b8d454a6004038ebf70ec60f856d0fdcc624f1956ea85b739ffcbbbe663`  
		Last Modified: Thu, 09 May 2024 22:34:41 GMT  
		Size: 37.1 KB (37067 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; 386

```console
$ docker pull postgres@sha256:147334a72b3498d7bdb60061bcf9f45367fd1c89e551decba4fd9b792e003fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100306478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3aaa99283e74e34eadb88400bcd392cc24bfc03a461b5874d6cb3195ac7f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f66ea424717655d9a6e3176bfbb4fe0f5a1e66eb3818e54efae25d389f34cc8`  
		Last Modified: Thu, 09 May 2024 21:57:22 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3260e18d0377ade67a750729399f7ee725fbb46a97404fb501436f7b453f0245`  
		Last Modified: Thu, 09 May 2024 21:56:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a49c081ca9848390a8415381ab655ec60ba9d766f7033c1ae20642b27367ab`  
		Last Modified: Thu, 09 May 2024 21:57:25 GMT  
		Size: 97.1 MB (97050680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9b5c7ccdd4f5208631a8e4c7534a9fd0caff2953c04a6c0e9e11ca83962b66`  
		Last Modified: Thu, 09 May 2024 21:57:22 GMT  
		Size: 9.4 KB (9447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f0247945d48e3cc4e91a13f248cc9f005c13b4ea5dcb99e33011122b3380d`  
		Last Modified: Thu, 09 May 2024 21:57:23 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd22b060c2319aaabafdcaf1e5e62cb6dd13a91b879488f4617ae6e4f390483`  
		Last Modified: Thu, 09 May 2024 21:57:23 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c644c53bd59f3327c857d5f2bc3935b35d734153811eff5396a4e8bb0dec63bd`  
		Last Modified: Thu, 09 May 2024 21:57:24 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019bbf827489d28471cd90cca2d02a81cbdf05518ca2a4800018dd0fb4f4c218`  
		Last Modified: Thu, 09 May 2024 21:57:24 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:627571b43d59e52bf43badb507efb44b027aac6b42230e1f4beee62b692d535d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.3 KB (993255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1321ba31c07f320b896b20edcbec2d791e5be5135665074d0a8251b56e4034b`

```dockerfile
```

-	Layers:
	-	`sha256:b41762726e29381e4d0400ab7cb9a8d2337035e04f8c3c4280d1e119f5843fe9`  
		Last Modified: Thu, 09 May 2024 21:57:22 GMT  
		Size: 956.1 KB (956057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14adfcbe98d57f6d2d4970205ebe0426677f3a1103040b439d416df552dee2bc`  
		Last Modified: Thu, 09 May 2024 21:57:22 GMT  
		Size: 37.2 KB (37198 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; ppc64le

```console
$ docker pull postgres@sha256:16d3393f8241af85596f9146799d446b35a62aa636bb828da327ba14d5a7ed76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101058679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6eec4d5818d818f08ba049420b97054d08548a2179cf22222c7a01b602f552`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
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
	-	`sha256:47a5189a2377a887c30b7aaacbd910ed89416122e7bd8387b3c24f3ee7d01bd4`  
		Last Modified: Thu, 09 May 2024 22:38:22 GMT  
		Size: 97.7 MB (97693451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d7c815c6fd23cc49200a9d9f3ccab8fc30b4d4e5487b63a963deab8a0a94d9`  
		Last Modified: Thu, 09 May 2024 22:38:19 GMT  
		Size: 9.5 KB (9453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88799d9b388109d1430e160db6d792fb921b22224f145467c9cd965c3b39aa4`  
		Last Modified: Thu, 09 May 2024 22:38:20 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ab8f4da4a724e0fc41b72af6bf2e60659e60f625c90ecc562b4d8aa9f0482`  
		Last Modified: Thu, 09 May 2024 22:38:19 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d0ff58cdb83243b13ebf009ee2a78720316f300a986f483cae71d9d6cd3dc8`  
		Last Modified: Thu, 09 May 2024 22:38:21 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91fb20b55932a8e4211662dd453ff9a807f5980698ed76d2f990311d4ba1f1ea`  
		Last Modified: Thu, 09 May 2024 22:38:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:11340aa3eb077075382877b0d35e0bf82747e64351adc36a60428326a9b0b1c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.7 KB (989720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f2bdee8a639e08795c66d7a92e5698b4e55dea1ce37184d306982201222861`

```dockerfile
```

-	Layers:
	-	`sha256:32d9b3e3b528d4c6a87631062b50e4190107552e0b59a2eaeec23117b1d2599d`  
		Last Modified: Thu, 09 May 2024 22:38:19 GMT  
		Size: 952.6 KB (952619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:152cb95eab455202085bae932cd3faf01fdbbadf8e96f955ebe1df256c744546`  
		Last Modified: Thu, 09 May 2024 22:38:19 GMT  
		Size: 37.1 KB (37101 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:15-alpine3.18` - linux; s390x

```console
$ docker pull postgres@sha256:41f1f579ab319ebd588efd6fb249958b903755b0e04bfece39d67007967dbbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96900698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c1b86b8a4a4f5d3f4181bf7ada5f3c6298e546642df9071305c37178271e98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV LANG=en_US.utf8
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_MAJOR=15
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_VERSION=15.7
# Thu, 09 May 2024 18:44:17 GMT
ENV PG_SHA256=a46fe49485ab6385e39dabbbb654f5d3049206f76cd695e224268729520998f7
# Thu, 09 May 2024 18:44:17 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 09 May 2024 18:44:17 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 09 May 2024 18:44:17 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 09 May 2024 18:44:17 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 09 May 2024 18:44:17 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 09 May 2024 18:44:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 May 2024 18:44:17 GMT
STOPSIGNAL SIGINT
# Thu, 09 May 2024 18:44:17 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 09 May 2024 18:44:17 GMT
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
	-	`sha256:132f0d2306328039e110ae56c9917fad40f939a5f33bf5e03212c0929185fe97`  
		Last Modified: Thu, 09 May 2024 22:28:06 GMT  
		Size: 93.7 MB (93666433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69c79cf4fd55c1f04e396000cf6f0ee8deccaf24b410dcd6955d283896ae4ca`  
		Last Modified: Thu, 09 May 2024 22:28:04 GMT  
		Size: 9.5 KB (9451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cb75f980e8e650a38caa9634984c8f6b57dafd6464c0b2e37266989e8f1d88`  
		Last Modified: Thu, 09 May 2024 22:28:04 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550c4205a1e7096be20467b836b0bba5f6dfb31d892a385c2f0803d91bded83f`  
		Last Modified: Thu, 09 May 2024 22:28:04 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090afb34ec210ae6d40019147762d19b1de37c0654ba3be5bb6fb6108a09e941`  
		Last Modified: Thu, 09 May 2024 22:28:05 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00c3028f3c1f13d79bb18dfcf4a8970cb8ea6158632e4731951289ed17338b9`  
		Last Modified: Thu, 09 May 2024 22:28:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:0fe1f67f883218c6d599e696965be1858505c1294794d18fa75ac3e5ea8445ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **991.2 KB (991181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89aa795056a742800fcb12ae19218b43c3003cb24d94fceebcecfbf9daf93e09`

```dockerfile
```

-	Layers:
	-	`sha256:6c7ec887371e95fac95f27119bea95fcf4a2e90052c204a644c65b8c345c65d2`  
		Last Modified: Thu, 09 May 2024 22:28:05 GMT  
		Size: 954.1 KB (954118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4e4b482c9c29d032b7a2505b8ba779f3db212832d09226281af911ae646904b`  
		Last Modified: Thu, 09 May 2024 22:28:04 GMT  
		Size: 37.1 KB (37063 bytes)  
		MIME: application/vnd.in-toto+json
