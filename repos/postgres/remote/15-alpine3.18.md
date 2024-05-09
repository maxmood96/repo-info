## `postgres:15-alpine3.18`

```console
$ docker pull postgres@sha256:268cd7e4124219d20ca3800c0bebc136ab2a80ff69e36b9d35706d4be4aa3ae3
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
$ docker pull postgres@sha256:c693fb1391d95b9b2fa8e0e8f10dd2558b8bf365ad19ef6fe6f3b1f3fd3cb352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.8 MB (86753610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8934784a7ddb78d3032da42b2523547b68e3238d02dd720a3552c1f703d958e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd951a98e9bc26ad55202a730fbf176a99a4f1dafeac246adac9b93116e6841`  
		Last Modified: Sat, 16 Mar 2024 16:26:55 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83b4bffee9860001c77fb26ccc9519a32dcc2324e1b6490008d4eee80c0ab7a`  
		Last Modified: Sat, 16 Mar 2024 16:26:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1428b6cc64ce42ccf9837d859c10ba2aa0ae5a05f5752227fa43ba2211adea`  
		Last Modified: Sat, 16 Mar 2024 16:37:35 GMT  
		Size: 83.8 MB (83835497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e358aa6b68bf8a3cef48818321767fc758e7848b8f747a3bfefc6c1de18e96a9`  
		Last Modified: Sat, 16 Mar 2024 16:37:32 GMT  
		Size: 9.4 KB (9446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2225b03cfb613fc8cb7da9354a180cf3f3f3f080c0ceaf9be8f2c7eeb372aa`  
		Last Modified: Sat, 16 Mar 2024 16:37:33 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab82d69f3df360155fecf4f073efcd8c98c34dec3e7e9873fc9a99437c3f874`  
		Last Modified: Sat, 16 Mar 2024 16:37:33 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17efbf3558286415a9c1fed21d579455fe0e57fc5094a4f1d256169ba9c2463`  
		Last Modified: Sat, 16 Mar 2024 16:37:34 GMT  
		Size: 5.4 KB (5416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8669425b48a734c365aa2282c5b5dc0714c470716fd6dec09cacb6711995dc4c`  
		Last Modified: Sat, 16 Mar 2024 16:37:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:afef2032721a0cf92d696066af0d0a73742cefd8dc74898c2bcf490f9bc12519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **993.3 KB (993279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6428a69a527b6979c150c47a43e2f97c13cdbd994afbd9224cf508b6377d21e`

```dockerfile
```

-	Layers:
	-	`sha256:2053872cf8428d52897dd487d8df443f8c0fb3c1146c56b33711862443514f83`  
		Last Modified: Sat, 16 Mar 2024 16:37:33 GMT  
		Size: 956.1 KB (956088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e2597cc52a096a14fee14b097ef79d8a53b5ffb29e8676d8980f1736558a9a1`  
		Last Modified: Sat, 16 Mar 2024 16:37:32 GMT  
		Size: 37.2 KB (37191 bytes)  
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
$ docker pull postgres@sha256:47b7b81cacb801c844d36319eb1e0c27f4cbcc0371b03db2b3352a26741531b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.1 MB (99104110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a12f4fe65e86befa4c7c98213979be0c392f1e502c6ae7b202e317ed2dbab6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV LANG=en_US.utf8
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_MAJOR=15
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_VERSION=15.6
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PG_SHA256=8455146ed9c69c93a57de954aead0302cafad035c2b242175d6aa1e17ebcb2fb
# Thu, 08 Feb 2024 19:40:08 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-thread-safety 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-gnu-ld 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world; 	make install-world; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN set -eux; 	cp -v /usr/local/share/postgresql/postgresql.conf.sample /usr/local/share/postgresql/postgresql.conf.sample.orig; 	sed -ri "s!^#?(listen_addresses)\s*=\s*\S+.*!\1 = '*'!" /usr/local/share/postgresql/postgresql.conf.sample; 	grep -F "listen_addresses = '*'" /usr/local/share/postgresql/postgresql.conf.sample # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p /var/run/postgresql && chown -R postgres:postgres /var/run/postgresql && chmod 3777 /var/run/postgresql # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENV PGDATA=/var/lib/postgresql/data
# Thu, 08 Feb 2024 19:40:08 GMT
RUN mkdir -p "$PGDATA" && chown -R postgres:postgres "$PGDATA" && chmod 1777 "$PGDATA" # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
VOLUME [/var/lib/postgresql/data]
# Thu, 08 Feb 2024 19:40:08 GMT
COPY docker-entrypoint.sh docker-ensure-initdb.sh /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
RUN ln -sT docker-ensure-initdb.sh /usr/local/bin/docker-enforce-initdb.sh # buildkit
# Thu, 08 Feb 2024 19:40:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Feb 2024 19:40:08 GMT
STOPSIGNAL SIGINT
# Thu, 08 Feb 2024 19:40:08 GMT
EXPOSE map[5432/tcp:{}]
# Thu, 08 Feb 2024 19:40:08 GMT
CMD ["postgres"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bf06424f58ac7307d52d4ae986fc96c03d14c3e8c9546673273e53c183a35a`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545ceadfd5057505b4e5d6cd51ddf57b0cb73f291f5b2ab2e392c78a73f6318c`  
		Last Modified: Sat, 16 Mar 2024 10:40:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1d2f76524906b3c954df9e447d7837bcfff477541453646e265eb2993f598a`  
		Last Modified: Sat, 16 Mar 2024 10:46:33 GMT  
		Size: 95.7 MB (95738888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d17b28f27edfc0f3bb4ce402e8b1e428daea53b23ad624ee38e26abde89e3903`  
		Last Modified: Sat, 16 Mar 2024 10:46:31 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1f05b5dcf12da8534b81f0416954b1fdffe6e66e9c828af429113d4009a7fb`  
		Last Modified: Sat, 16 Mar 2024 10:46:31 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42d8a9f0eddaeb0d1fdfac0872257600b0c277b611f4ccf9c08c05b8c2b1ab4`  
		Last Modified: Sat, 16 Mar 2024 10:46:31 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43d016b936b2e53b26ffd8e86738e64c98da04891074bcef8d31b293a322876`  
		Last Modified: Sat, 16 Mar 2024 10:46:32 GMT  
		Size: 5.4 KB (5419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ae119bafc139a52e0e459d69a332387f7425fdeceb598637d821a9d8647034`  
		Last Modified: Sat, 16 Mar 2024 10:46:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:15-alpine3.18` - unknown; unknown

```console
$ docker pull postgres@sha256:0a82814b7ae7c1be9a659a28815024a636fe2e165081dbfcfdc5782b57742dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **989.7 KB (989712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596aa58c4456e50db89fa74531cf3ad5b0ee05cf29946b5ba0b7abc298f41f8f`

```dockerfile
```

-	Layers:
	-	`sha256:6d6135639f3c8183ac0db44ac52de750d55f3987725cd111ed62edebdde2daf7`  
		Last Modified: Sat, 16 Mar 2024 10:46:31 GMT  
		Size: 952.6 KB (952615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62ff59ecc4ac7f3b6f5b1cc55ed6c8163c991b665ba09b990291b6d7329235d7`  
		Last Modified: Sat, 16 Mar 2024 10:46:30 GMT  
		Size: 37.1 KB (37097 bytes)  
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
