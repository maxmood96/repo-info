## `postgres:17beta1-alpine`

```console
$ docker pull postgres@sha256:eb3c5cd513d7eae9a6a29ef643c26d17565e8e524d69e78e0b3e37832620ed5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `postgres:17beta1-alpine` - linux; amd64

```console
$ docker pull postgres@sha256:f765a95ca35c01752fc240764f2bc7c3bc2c3c687bbd8d558761e7b3019a4a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97005407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a991f2df6a0bd3424c30f9050c1456758edb16d3ca80858456216f462672a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f5d72b13907cb9054d0653aa46c9255dcb5f9fe15a65fb18a7f3b617a31ce`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df5710b9df958cb437a07e202d7c0dc5379305a4b7543178fcc7feb4815fd5b`  
		Last Modified: Mon, 03 Jun 2024 19:06:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630c0819a816bcec85b2c2f301b72f1180019bb037fc4266610f4d171f62e9aa`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 93.4 MB (93366421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75638bc4839a0e4d20e54da43e324dcdf7da1fb20f0e7c9a322f0fcb0b06efc`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 9.9 KB (9890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55d8da6ed23828ae6cd0211ac5341fbbbd139fa9412b597bd1eb36cd14e114`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cfd0fa930f458c0fa76b0dbc424968b6f652e3633b11746db1be8d69fea7d1`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1247eb592eee26860ce41230da4f88266e22eae4819ff37b8cb19066f5110c01`  
		Last Modified: Mon, 03 Jun 2024 19:06:48 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68ed9d9013b7733b1856c884d451010ff9678dde7fe0fe338ab37bcff1dd7e9`  
		Last Modified: Mon, 03 Jun 2024 19:06:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:f0e481d4aff4690d9b110f7f02c326143bb6cddec5534b21c6f1a12b71641d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 KB (615317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67db56f88bf728381ba68208bf4f1836b02c46c26f01908a5caa217e848de1c3`

```dockerfile
```

-	Layers:
	-	`sha256:c5dc96cfd93311a8cf3cdbc34f3a6a1e041237d1a346563f4f382799c6e4cf1c`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 578.4 KB (578404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0ba079d6d029d9368dbd08d74aaf30584edece8b935d24b144ca7f5ec74c0e`  
		Last Modified: Mon, 03 Jun 2024 19:06:47 GMT  
		Size: 36.9 KB (36913 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine` - linux; arm variant v6

```console
$ docker pull postgres@sha256:e19fb5f357e9c93c81daba68721f5431b5ca467864229a6d5f90a1ffc94b648d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95715561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e436fa3791b03199c21e2bcbf14f2614b6256daa05fdcf63e418a400c5c510`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c63537711e2b71098dfef581dede9863d3952e51cf921a6044c1ca139319887`  
		Last Modified: Mon, 03 Jun 2024 19:21:48 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687782b67bec9f1ff4f194d23363629e4e78d8095a9aacd4311a20f5b9473ff3`  
		Last Modified: Mon, 03 Jun 2024 19:21:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a617c3a3fdd45ceaaea8e1427cc439c1b55d79e83e34a61a9979e60591f07bc4`  
		Last Modified: Mon, 03 Jun 2024 19:21:51 GMT  
		Size: 92.3 MB (92333616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b847f73cbbb79d0cf1bcda4f0b32696ca1ab186320fab1aee3d5b3bf1d48f3`  
		Last Modified: Mon, 03 Jun 2024 19:21:48 GMT  
		Size: 9.9 KB (9891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f55d8516122ee4b5d1596a066cbb4dfc1e43606d3d98dcc8ca824b97c593be`  
		Last Modified: Mon, 03 Jun 2024 19:21:49 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784c60225eab921bf3149c1659d667d793ad26fa99d543c9240d0b040a6d7c57`  
		Last Modified: Mon, 03 Jun 2024 19:21:49 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0aff94484d5084834bf113f305daa615f0dafe6ae7af979ba7943e7542a40de`  
		Last Modified: Mon, 03 Jun 2024 19:21:50 GMT  
		Size: 5.4 KB (5420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d96fb9e533e03ed5770203f222146af87a0a5cbc2cb6ec0dde1e7c037e91b3`  
		Last Modified: Mon, 03 Jun 2024 19:21:50 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:84673b03b7077b76f832d241f885f7eb20d28a766ba5b43c5f2b3361209365c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 KB (36826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d25da71ca8032b22efa2f5b2d385ee369cc88f61d7f6688314fc5949d08ae6`

```dockerfile
```

-	Layers:
	-	`sha256:4d4fde10e008077a6dfa0b3f9bf734d49cd535c8014484cdad9ab75a37826908`  
		Last Modified: Mon, 03 Jun 2024 19:21:48 GMT  
		Size: 36.8 KB (36826 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine` - linux; arm variant v7

```console
$ docker pull postgres@sha256:451ba6b9bd22d1bed3e14d4c2fd5b3d8ce3e879d2e95cba4c765b1d90a365104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90087119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d108f23a989665cfa701051274074cb5284adc43a984520b9dafb6d2de10d11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13461a0b11d0afdd53d0436602eddc4ad89878a2ad40b64f0c4359a03b9d9dac`  
		Last Modified: Mon, 03 Jun 2024 20:38:43 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98fb215bc78e59d29bdad767e1ab4e8eea96fb261ffb0fcde16724b44ac745b`  
		Last Modified: Mon, 03 Jun 2024 20:38:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5022f85adb22a1196e004ec60251f18affa55461afc7dd19f90c508d4175158c`  
		Last Modified: Mon, 03 Jun 2024 20:38:45 GMT  
		Size: 87.0 MB (86976191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940786564eccb076de71864a4e91cdf68fa302759f6c757e642d8dc87be13036`  
		Last Modified: Mon, 03 Jun 2024 20:38:43 GMT  
		Size: 9.9 KB (9890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fd994a3695a94aefdcd6399b6b110e41a9dac46e4b2b5e785973242f7859e1`  
		Last Modified: Mon, 03 Jun 2024 20:38:44 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4815855d6970dff2858e6124a411ffdbc40599bdb89b2f8d2533281bc0070e`  
		Last Modified: Mon, 03 Jun 2024 20:38:44 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b931816648607afc02fc1d6401a25f62b98726d09f19000cb3f17ae50858bb6`  
		Last Modified: Mon, 03 Jun 2024 20:38:44 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5e99e4e64dd65fa3e3371c9f7225f1ea0314177fc51c9267596e032081d967`  
		Last Modified: Mon, 03 Jun 2024 20:38:45 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:0c89edbb021e41e3b589332d31fa71059b195c6b7f73ab9ae16f3552f89d9bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.5 KB (615469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6ad36a8810ca6f19e55e27b2486ccbc57e3a2e594d5529dfa6a25898cad4fa`

```dockerfile
```

-	Layers:
	-	`sha256:09fbb13d96f2b6464cd830aae7f0c63df9c27f71f412d5572be84f0dab5d57ae`  
		Last Modified: Mon, 03 Jun 2024 20:38:43 GMT  
		Size: 578.4 KB (578424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1975da803c414f065197dff5b1bb85c0349a4d149664b66d124ad8ed764518e3`  
		Last Modified: Mon, 03 Jun 2024 20:38:43 GMT  
		Size: 37.0 KB (37045 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine` - linux; arm64 variant v8

```console
$ docker pull postgres@sha256:12cf037f13119d897fabb1a5824924bc5462074525f72cfc883f6eb32e7fd9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96299742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f916f86bef3c02b38965049671e8099245d63661842389f5c157283c13a8a005`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627e3392ede98e4e7a885f6a504fa11567d3e4e97a7b74a25c2e8cc69f515ab1`  
		Last Modified: Tue, 04 Jun 2024 16:43:44 GMT  
		Size: 981.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe49b55b743f92c555113781fb44395adf51ee8b7d661470831d9465c0aa63bb`  
		Last Modified: Tue, 04 Jun 2024 16:43:44 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0df41f4d183ba7644ddba7d9cb414d214381846c4b65e3500a6d6b5b589f35`  
		Last Modified: Tue, 04 Jun 2024 16:43:47 GMT  
		Size: 92.2 MB (92196070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d40ce0853db0c2922004f4ce0cb1af282b066dbc55c33b07d7555c27a2a590`  
		Last Modified: Tue, 04 Jun 2024 16:43:44 GMT  
		Size: 9.9 KB (9893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6127e7502d8822ea28c24f88e77310e0b22370a92eba4da22ec994fe248326c7`  
		Last Modified: Tue, 04 Jun 2024 16:43:45 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72bcc1d949e1c216972424ff43c2fdb26c75c5d892d8a2532564523f660bb29`  
		Last Modified: Tue, 04 Jun 2024 16:43:45 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f94ddd507e40db9409d03d5aa36bcb715f42c279b5fe2e30d533cfe57c75a2`  
		Last Modified: Tue, 04 Jun 2024 16:43:45 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e5f86fec093191300e7fa62d2f3c90dcca52573c5db43f13f3b356d8376761`  
		Last Modified: Tue, 04 Jun 2024 16:43:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:87d48d0c3878d51ecb1af5b792d2c1d48770e47ccb8f74cbfa44437111cc1486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.6 KB (615625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14577161acf8b00378017aa431763ea358090f7de280c2aac025a2686cd36408`

```dockerfile
```

-	Layers:
	-	`sha256:55dd3ef4ffc8b3048ce6ce2d40a9eb501831f1e8237498aad80d8c79528a06a0`  
		Last Modified: Tue, 04 Jun 2024 16:43:44 GMT  
		Size: 578.4 KB (578436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5baa02934b221bb28b904a288f7dab258e176a203052b8658dea7f30ea3b7365`  
		Last Modified: Tue, 04 Jun 2024 16:43:44 GMT  
		Size: 37.2 KB (37189 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine` - linux; 386

```console
$ docker pull postgres@sha256:2ea12c3cc46a8ebeca5e84b58180e192602b2dc7b34b2f3b34000b75a930d911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f3e020fd3eecf4510e102cc9541a3c80baec4db1d5b1670ef003a5a244662e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce9cd8a7f447170bf4cee9d8b55f6291fa1225e2fc945afbd0bac61349d97e5`  
		Last Modified: Mon, 03 Jun 2024 19:07:24 GMT  
		Size: 979.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c427bb79c9865e3559d5b9bb4341e74cb48254537ca94b36434d2e5836168b`  
		Last Modified: Mon, 03 Jun 2024 19:06:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970cac4076d21e2a29984eca703c0f2cc71d0403b782efbd969053c40adf7bd7`  
		Last Modified: Mon, 03 Jun 2024 19:07:27 GMT  
		Size: 98.9 MB (98909736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc0210a014bc567929c69f276099990c4b056179abcc28efe2695e3e59740f7`  
		Last Modified: Mon, 03 Jun 2024 19:07:24 GMT  
		Size: 9.9 KB (9890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f725219fbe0b29fdf2a1ff2d7eb8667fbf6c1c98bfb5b67a80835a9a7b3179`  
		Last Modified: Mon, 03 Jun 2024 19:07:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea29bebbe6ee02492fb2367f4074205f610551c3ca2229a171fe13e7b5fc5531`  
		Last Modified: Mon, 03 Jun 2024 19:07:25 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877b6de0d27cf6dc0ffcc38641254d7b6c75d88c27ed098c9226ed2c9b26a967`  
		Last Modified: Mon, 03 Jun 2024 19:07:25 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b885564cefc17172ffade4430fffca351c9700d0c6d2a90bf12f49388e9161`  
		Last Modified: Mon, 03 Jun 2024 19:07:26 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:1e6d0e932aba3480c6e31a4af5f73d0e8373ef1fecfd5f8284a069549e7235fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **615.3 KB (615271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c791eb5c43f0c10adb8a518b37cfcc2182f38b53b2c15fed9e38f73dc7f6b14`

```dockerfile
```

-	Layers:
	-	`sha256:bd5ab997809169c6e46404d3ef69354c19fc407707f8dbc64acab9be2575d316`  
		Last Modified: Mon, 03 Jun 2024 19:07:24 GMT  
		Size: 578.4 KB (578389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f00ffabc7b021fe617afa6b140154150a5e8496302fbd0b09621f7896993256`  
		Last Modified: Mon, 03 Jun 2024 19:07:24 GMT  
		Size: 36.9 KB (36882 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine` - linux; ppc64le

```console
$ docker pull postgres@sha256:d2d714d8976c721a8834588e0e8af7374f58f6fe0b14425455e6d3298a7765f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101714417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca30a29f708795042c1252a78e28606e1c54d618c846a9c9ed35f8702222305`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd1eee4c10ba5c208f6bdc0ac4fc73f2cbfadc9b2c92194411c012e4b9ac8b`  
		Last Modified: Tue, 04 Jun 2024 00:37:56 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2a6fa94842fa4d229e3c1c2c0afc9b3e7cf8bac75896cd4c7fbce3b0bb68aa`  
		Last Modified: Tue, 04 Jun 2024 00:37:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdf3834a4ddd1b2de406a340baddfd6b69ee5f7bcf376bfe0df352aa2e82928`  
		Last Modified: Tue, 04 Jun 2024 00:38:00 GMT  
		Size: 98.1 MB (98127674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a93a7b9e444aecaeb2f77831c0b2e85d273e1c461b98b6b4c37781c19ebbf3a`  
		Last Modified: Tue, 04 Jun 2024 00:37:56 GMT  
		Size: 9.9 KB (9892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19314b8d383330cb44e6455a44b2dc8079ad1059dbf9e80206289890326f332b`  
		Last Modified: Tue, 04 Jun 2024 00:37:57 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a439c54a9e5c2e4d7a600485036bf850e35ba5552add1df8360c4c4d1fdf1f0`  
		Last Modified: Tue, 04 Jun 2024 00:37:57 GMT  
		Size: 169.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe728334848b562645e43b5dc580c1a1cc2dd42da7b7b074e25b2a7022ba6957`  
		Last Modified: Tue, 04 Jun 2024 00:37:58 GMT  
		Size: 5.4 KB (5426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2ad8f477244a65dd8303dc857b40f619655da5a6387e54fd1f17d9c0b9e6b4`  
		Last Modified: Tue, 04 Jun 2024 00:37:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:49830235a0a38c1755e48d8c30509940409b07dc9c55b3ff9b22887ff5d834dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **611.9 KB (611902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cf278bc1ebd139c48fb556e138ef2a028ce7e7f31c68017161bb2a31551f40`

```dockerfile
```

-	Layers:
	-	`sha256:36c82cf99919a0927574360fe242db8a66492486050ef6496a6d139288b30ccf`  
		Last Modified: Tue, 04 Jun 2024 00:37:57 GMT  
		Size: 575.0 KB (574951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c025b8b7351acf9f324ab3ca767dca85169b0b526088fdb63e9f5bb5fdf504`  
		Last Modified: Tue, 04 Jun 2024 00:37:56 GMT  
		Size: 37.0 KB (36951 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine` - linux; riscv64

```console
$ docker pull postgres@sha256:8e82ff835a2a2818a487a18447f0288f5183d8d16b417f2d2c56ea5da000f3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97182869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65597baa2335cff217c9c1801bb41fd9e7ba871c555661315e25c3b743c66652`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397835f90d5b54bcf3350893c533d7f62222ce163422e08c4292b57e32932472`  
		Last Modified: Mon, 03 Jun 2024 20:18:07 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7681dc06ba012f91e87730fc72d8d4f0a1859d02a200495489016d5d487395`  
		Last Modified: Mon, 03 Jun 2024 20:18:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e99884354034c967c3bb3fa99aabde016cc715f022ee62a85985e58e3f2f1f5`  
		Last Modified: Mon, 03 Jun 2024 20:18:20 GMT  
		Size: 93.8 MB (93797405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c72a726ea7f9b4ccac634f5c0928eaaef00af2a77e7c0afda233bbf4235a1`  
		Last Modified: Mon, 03 Jun 2024 20:18:07 GMT  
		Size: 9.9 KB (9896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff48401e8ff5982e6a63f346c72da9f6a50603f3c0dacf7dd3faa9ae5ed7b26d`  
		Last Modified: Mon, 03 Jun 2024 20:18:08 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34abb29d1d2e65b4caaea3ba832936546f05e9fe21b33965b43ee47645183c7c`  
		Last Modified: Mon, 03 Jun 2024 20:18:08 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fa5f42178ea6454cac1f01e35fa7cd90bf3f6b5fcf9bb00382d203ecca018e`  
		Last Modified: Mon, 03 Jun 2024 20:18:08 GMT  
		Size: 5.4 KB (5427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa8799b0d09da3294c145d0e6d47c811319b089ae6b3811825c8e2ac1577629`  
		Last Modified: Mon, 03 Jun 2024 20:18:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:90c25d564bfe70c1dcf307bbd1a91cd9883119e8e0dc90bada9667fd3a9a313d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.4 KB (613419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1aeb1819aa0a6d1f92df7336a22ba09a037a38d5d3f416fa02a168b06364ba`

```dockerfile
```

-	Layers:
	-	`sha256:bed5cd78821d5f6f3ff779ed20cef9c21af0760a40a1cc751ab7ee705db2f819`  
		Last Modified: Mon, 03 Jun 2024 20:18:07 GMT  
		Size: 576.5 KB (576468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25bf8c1f1955dd0506b90f2f5d842dddd58b75f07fbc65c3a14db609c507d130`  
		Last Modified: Mon, 03 Jun 2024 20:18:07 GMT  
		Size: 37.0 KB (36951 bytes)  
		MIME: application/vnd.in-toto+json

### `postgres:17beta1-alpine` - linux; s390x

```console
$ docker pull postgres@sha256:ccc454dbd8def22fda6a7e0a27c49a8b099812295e8082803055be2390d642c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (105966216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47de86cbffb0e4bcda7b561dea68d02e8bad3b66eed0237fe2fd6592484c6136`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["postgres"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 	addgroup -g 70 -S postgres; 	adduser -u 70 -S -D -G postgres -H -h /var/lib/postgresql -s /bin/sh postgres; 	mkdir -p /var/lib/postgresql; 	chown -R postgres:postgres /var/lib/postgresql # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV LANG=en_US.utf8
# Fri, 31 May 2024 13:43:40 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_MAJOR=17
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_VERSION=17beta1
# Fri, 31 May 2024 13:43:40 GMT
ENV PG_SHA256=089e8854fecd0ca1ec5cd8b29526938f9ef5e91cc331f5d6e118d13468f08f50
# Fri, 31 May 2024 13:43:40 GMT
ENV DOCKER_PG_LLVM_DEPS=llvm15-dev 		clang15
# Fri, 31 May 2024 13:43:40 GMT
RUN set -eux; 		wget -O postgresql.tar.bz2 "https://ftp.postgresql.org/pub/source/v$PG_VERSION/postgresql-$PG_VERSION.tar.bz2"; 	echo "$PG_SHA256 *postgresql.tar.bz2" | sha256sum -c -; 	mkdir -p /usr/src/postgresql; 	tar 		--extract 		--file postgresql.tar.bz2 		--directory /usr/src/postgresql 		--strip-components 1 	; 	rm postgresql.tar.bz2; 		apk add --no-cache --virtual .build-deps 		$DOCKER_PG_LLVM_DEPS 		bison 		coreutils 		dpkg-dev dpkg 		flex 		g++ 		gcc 		krb5-dev 		libc-dev 		libedit-dev 		libxml2-dev 		libxslt-dev 		linux-headers 		make 		openldap-dev 		openssl-dev 		perl-dev 		perl-ipc-run 		perl-utils 		python3-dev 		tcl-dev 		util-linux-dev 		zlib-dev 		icu-dev 		lz4-dev 		zstd-dev 	; 		cd /usr/src/postgresql; 	awk '$1 == "#define" && $2 == "DEFAULT_PGSOCKET_DIR" && $3 == "\"/tmp\"" { $3 = "\"/var/run/postgresql\""; print; next } { print }' src/include/pg_config_manual.h > src/include/pg_config_manual.h.new; 	grep '/var/run/postgresql' src/include/pg_config_manual.h.new; 	mv src/include/pg_config_manual.h.new src/include/pg_config_manual.h; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	wget -O config/config.guess 'https://git.savannah.gnu.org/cgit/config.git/plain/config.guess?id=7d3d27baf8107b630586c962c057e22149653deb'; 	wget -O config/config.sub 'https://git.savannah.gnu.org/cgit/config.git/plain/config.sub?id=7d3d27baf8107b630586c962c057e22149653deb'; 		export LLVM_CONFIG="/usr/lib/llvm15/bin/llvm-config"; 	export CLANG=clang-15; 		./configure 		--enable-option-checking=fatal 		--build="$gnuArch" 		--enable-integer-datetimes 		--enable-tap-tests 		--disable-rpath 		--with-uuid=e2fs 		--with-pgport=5432 		--with-system-tzdata=/usr/share/zoneinfo 		--prefix=/usr/local 		--with-includes=/usr/local/include 		--with-libraries=/usr/local/lib 		--with-gssapi 		--with-ldap 		--with-tcl 		--with-perl 		--with-python 		--with-openssl 		--with-libxml 		--with-libxslt 		--with-icu 		--with-llvm 		--with-lz4 		--with-zstd 	; 	make -j "$(nproc)" world-bin; 	make install-world-bin; 	make -C contrib install; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 			| grep -v -e perl -e python -e tcl 	)"; 	apk add --no-cache --virtual .postgresql-rundeps 		$runDeps 		bash 		su-exec 		tzdata 		zstd 		icu-data-full 		$([ "$(apk --print-arch)" != 'ppc64le' ] && echo 'nss_wrapper') 	; 	apk del --no-network .build-deps; 	cd /; 	rm -rf 		/usr/src/postgresql 		/usr/local/share/doc 		/usr/local/share/man 	; 		postgres --version # buildkit
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
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f17f8c990c0ab5858469098b11d092d504ecbf4970fc3447a12f12e8acbfab`  
		Last Modified: Mon, 03 Jun 2024 19:51:51 GMT  
		Size: 980.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1a12ac87f16915117c6298db53620efe1c42e9277ed1b5b851ac46ffc57bd0`  
		Last Modified: Mon, 03 Jun 2024 19:51:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ebb522a985d71934d33adf247b4d4bbc4153fd683c70d8844a89068ca6e74`  
		Last Modified: Mon, 03 Jun 2024 19:51:53 GMT  
		Size: 102.5 MB (102488976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daedbe6b4c6413523dcca9d68484ff0d2f9a5bc53189543f8b40883d9638a6c7`  
		Last Modified: Mon, 03 Jun 2024 19:51:51 GMT  
		Size: 9.9 KB (9896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffa2615c5e27f5c4ca04d1126e14fa10e88801c44b5cdc4af28aca6d6d62b3c`  
		Last Modified: Mon, 03 Jun 2024 19:51:52 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7873c41434d6b7afcc7b23b8c141dc046c6f85723dfe1425c091af1d53bea66c`  
		Last Modified: Mon, 03 Jun 2024 19:51:52 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e26fb42f67151829c96a23c72e3aed74e6d64559d97662496e0920f1acfb7ef`  
		Last Modified: Mon, 03 Jun 2024 19:51:52 GMT  
		Size: 5.4 KB (5423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b8b2cd8b2e491964f88225935766e0aec303996076305a3a45f84aa20554f3`  
		Last Modified: Mon, 03 Jun 2024 19:51:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postgres:17beta1-alpine` - unknown; unknown

```console
$ docker pull postgres@sha256:e86df9057db9da544cea63f2cb5917a410417610fab8aeeed90bfcfc9633c890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **613.4 KB (613369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c43f43fcd5f9edb69145d698073e1033795a1c271e0041ec09ee050751874c44`

```dockerfile
```

-	Layers:
	-	`sha256:3e88a35f48e59efd9e8c8e782763a3787977548b67c5ad6e7fb3ffbf4339510c`  
		Last Modified: Mon, 03 Jun 2024 19:51:51 GMT  
		Size: 576.5 KB (576450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88453570ea178d10cbd0a70515e4f20e58ce500ffbd7cdf06b5a997f9ac365b1`  
		Last Modified: Mon, 03 Jun 2024 19:51:51 GMT  
		Size: 36.9 KB (36919 bytes)  
		MIME: application/vnd.in-toto+json
